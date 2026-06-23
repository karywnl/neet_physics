# Units and measurement

!!! intuition "The gist"
    Every measurement in physics is two things stuck together: a **number** and a **unit** (for example $5\ \text{m}$). The whole world of physics is built from just **seven base quantities**. Every other quantity (speed, force, energy) is made by combining them, and the recipe for that combination is called its **dimensions**.

## Why it exists

Suppose you tell a friend "the table is 5 long". Five what? Five centimetres? Five metres? Five steps of your foot? The number alone means nothing. A measurement only makes sense when you say **how many** and **of what standard size**. That standard size is the **unit**, and the count is the **number**.

$$
\text{measurement} = \text{number} \times \text{unit}
$$

So $5\ \text{m}$ means "5 times the standard length we call one metre". This is why physics insists you always carry the unit. A bare number is an unfinished sentence.

There is a second problem. There are hundreds of physical quantities: length, time, speed, area, force, pressure, energy, and on and on. We do not want a fresh, unrelated standard for each one. Luckily we do not need one. A small set of quantities is enough, and everything else is built from them. The chosen few are called **base quantities**; the rest are **derived quantities**.

## Picture it

Think of base quantities as a few "ingredients", and every other quantity as a "dish" you cook by combining them.

```text
        SEVEN BASE QUANTITIES (the ingredients)
   length   mass   time   current   temp   amount   luminous
    [L]     [M]    [T]     [A]      [K]    [mol]     [cd]
                          |
                          |  combine them
                          v
        DERIVED QUANTITIES (the dishes)
   area   = length x length          -> [L^2]
   speed  = length / time            -> [L T^-1]
   force  = mass x length / time^2   -> [M L T^-2]
```

You never invent a new ingredient for "speed". You just say speed is length divided by time. **In one line: seven base quantities are mixed in different proportions to make every other quantity in physics.**

## How it works

### The seven base quantities and their SI units

The world has agreed on one set of units, the **SI system** (Système International, French for "International System"). It fixes one unit for each of the seven base quantities.

| Base quantity | SI unit | Symbol |
| --- | --- | --- |
| Length | metre | $\text{m}$ |
| Mass | kilogram | $\text{kg}$ |
| Time | second | $\text{s}$ |
| Electric current | ampere | $\text{A}$ |
| Thermodynamic temperature | kelvin | $\text{K}$ |
| Amount of substance | mole | $\text{mol}$ |
| Luminous intensity | candela | $\text{cd}$ |

For NEET, learn these seven by heart. Most of mechanics (this whole first part of the course) uses only the first three: $\text{m}$, $\text{kg}$, and $\text{s}$.

!!! note "You do not memorise the formal definitions"
    The official definition of the metre involves the speed of light, and the kilogram involves the Planck constant. The NCERT text says plainly these exact definitions "need not be remembered or asked in a test". Know the names and symbols, not the constants behind them.

### Derived units

A **derived unit** is just the base units multiplied or divided, following the formula for that quantity.

- Speed is distance over time, so its unit is $\text{m/s}$ (written $\text{m s}^{-1}$).
- Area is length times length, so its unit is $\text{m}^2$.
- Force is mass times acceleration, so its unit is $\text{kg}\cdot\text{m/s}^2$, which we give the special name **newton** ($\text{N}$).

### Significant figures: how many digits you are allowed to trust

Every measuring instrument has a limit. A ruler marked in millimetres cannot tell you a length to the nearest micrometre. So a measured value carries only so many trustworthy digits. These trustworthy digits, the ones known reliably plus the first uncertain one, are the **significant figures**.

If a pendulum's time period is measured as $1.62\ \text{s}$, the $1$ and $6$ are certain and the $2$ is the estimated last digit. That is **three significant figures**.

The rules for counting them:

- **All non-zero digits are significant.** $42.5$ has three.
- **Zeros between non-zero digits are significant.** $2.308$ has four.
- **Leading zeros (before the first non-zero digit) are not significant.** $0.0052$ has two ($5$ and $2$); the zeros only place the decimal point.
- **Trailing zeros in a number with a decimal point are significant.** $4.700$ has four; the zeros were written on purpose to show precision.
- **Trailing zeros in a whole number with no decimal point are not significant.** $123\ \text{m} = 12300\ \text{cm}$ still has three.

!!! tip "Scientific notation removes all the confusion"
    Write the value as $a \times 10^b$ where $a$ is between 1 and 10. Then every digit in $a$ is significant, full stop. $4700\ \text{mm}$ is ambiguous, but $4.700 \times 10^3\ \text{mm}$ clearly has four significant figures. This is the safe way to report any measurement.

### Arithmetic with significant figures

Your answer cannot be more precise than the least precise number you started with. Two rules:

=== "Multiply or divide"

    The result keeps as many **significant figures** as the input with the **fewest** significant figures.

    A mass of $4.237\ \text{g}$ (4 figures) in a volume of $2.51\ \text{cm}^3$ (3 figures):

    $$
    \rho = \frac{4.237\ \text{g}}{2.51\ \text{cm}^3} = 1.688\ldots \approx 1.69\ \text{g cm}^{-3}
    $$

    The volume had only 3 figures, so the answer gets 3 figures.

=== "Add or subtract"

    The result keeps as many **decimal places** as the input with the **fewest** decimal places.

    $$
    436.32\ \text{g} + 227.2\ \text{g} + 0.301\ \text{g} = 663.821\ \text{g} \approx 663.8\ \text{g}
    $$

    The value $227.2\ \text{g}$ has only one decimal place, so the answer is rounded to one decimal place.

!!! warning "Do not mix the two rules"
    For multiply/divide you count **significant figures**. For add/subtract you count **decimal places**. Using the wrong rule is one of the most common NEET errors.

??? question "Quick check: significant figures"
    How many significant figures are in (a) $0.0070\ \text{m}$, (b) $6.320\ \text{J}$, and (c) $0.2370\ \text{g cm}^{-3}$?

    **Answer:** (a) **two**: the leading zeros do not count, only $7$ and the trailing $0$ after the decimal. (b) **four**: $6$, $3$, $2$, and the trailing $0$ (it follows a decimal point). (c) **four**: $2$, $3$, $7$, and the trailing $0$; the leading zero before the decimal never counts.

### Errors in measurement: how wrong is your number?

No measurement is ever exact. The gap between your measured value and the true value is the **error**. Errors are not mistakes; they are unavoidable, and physics is honest about them by always reporting *how much* a result could be off.

If you measure the same thing several times you usually get slightly different readings $a_1, a_2, \ldots, a_n$. The best single estimate of the true value is their average, the **arithmetic mean**:

$$
a_{\text{mean}} = \frac{a_1 + a_2 + \cdots + a_n}{n}
$$

Each reading differs from this mean by some amount. The size of that gap (ignoring its sign) is the **absolute error** of that reading, $|\Delta a_i| = |a_{\text{mean}} - a_i|$. Averaging those gaps gives the **mean absolute error**:

$$
\Delta a_{\text{mean}} = \frac{|\Delta a_1| + |\Delta a_2| + \cdots + |\Delta a_n|}{n}
$$

You then report the result as $a = a_{\text{mean}} \pm \Delta a_{\text{mean}}$. This says "the true value lies somewhere in this band".

Two more ways to state the same error, often more useful:

- **Relative error** $= \dfrac{\Delta a_{\text{mean}}}{a_{\text{mean}}}$ (a pure fraction, no units).
- **Percentage error** $= \dfrac{\Delta a_{\text{mean}}}{a_{\text{mean}}} \times 100\%$.

A mass of $1.02\ \text{g}$ known to $\pm 0.01\ \text{g}$ has a percentage error of $\frac{0.01}{1.02}\times 100\% \approx 1\%$, while $9.89\ \text{g}$ known to the same $\pm 0.01\ \text{g}$ has only $\frac{0.01}{9.89}\times 100\% \approx 0.1\%$. **The same absolute error is "worse" on a smaller measurement.**

### Combining errors (this is the NEET favourite)

Most quantities you want are *calculated* from measured ones (density from mass and volume, area from two lengths). Each measured value carries its own error, and those errors spread into the result. The rules for the **maximum** possible error are:

=== "Sum or difference"

    For $Z = A + B$ or $Z = A - B$, the **absolute errors add**:

    $$
    \Delta Z = \Delta A + \Delta B
    $$

    Even for a difference, the errors still **add**, they never cancel. This is why subtracting two close numbers is risky: the answer is small but the error is not, so the percentage error blows up.

=== "Product or quotient"

    For $Z = AB$ or $Z = \dfrac{A}{B}$, the **relative errors add**:

    $$
    \frac{\Delta Z}{Z} = \frac{\Delta A}{A} + \frac{\Delta B}{B}
    $$

=== "Powers"

    For $Z = \dfrac{A^p\, B^q}{C^r}$, multiply each relative error by its power:

    $$
    \frac{\Delta Z}{Z} = p\frac{\Delta A}{A} + q\frac{\Delta B}{B} + r\frac{\Delta C}{C}
    $$

    A power counts more than once, so the quantity raised to the highest power is the one to measure most carefully.

Here is the NCERT worked example. A thin sheet has length $l = 16.2 \pm 0.1\ \text{cm}$ and breadth $b = 10.1 \pm 0.1\ \text{cm}$. The area is a product, so relative errors add:

$$
\frac{\Delta l}{l} = \frac{0.1}{16.2} \approx 0.6\%, \qquad \frac{\Delta b}{b} = \frac{0.1}{10.1} \approx 1.0\%
$$
$$
\frac{\Delta A}{A} = 0.6\% + 1.0\% = 1.6\%
$$

The area is $l \times b = 163.62\ \text{cm}^2$, and $1.6\%$ of that is about $2.6\ \text{cm}^2$. Rounding sensibly, the area is reported as $164 \pm 3\ \text{cm}^2$.

??? question "Quick check: percentage error (real NEET style)"
    A physical quantity is given by $P = \dfrac{a^3 b^2}{c\,\sqrt{d}}$. The percentage errors in $a$, $b$, $c$, and $d$ are $1\%$, $2\%$, $3\%$, and $4\%$. What is the maximum percentage error in $P$?

    **Answer:** Multiply each percentage error by its power ($\sqrt{d}$ means the power of $d$ is $\tfrac{1}{2}$):

    $$
    \frac{\Delta P}{P} = 3(1\%) + 2(2\%) + 1(3\%) + \tfrac{1}{2}(4\%) = 3 + 4 + 3 + 2 = \mathbf{12\%}
    $$

    Every power adds, even the one in the denominator and the square root. The answer is $12\%$.

### Dimensions: the "recipe" of a quantity

The **dimensions** of a quantity tell you which base quantities it is built from, and to what power. We write them in square brackets using the base symbols: $[\text{L}]$ for length, $[\text{M}]$ for mass, $[\text{T}]$ for time.

For example, volume is length cubed:

$$
[\text{volume}] = [\text{L}] \times [\text{L}] \times [\text{L}] = [\text{L}^3]
$$

And force is mass times acceleration, where acceleration is length per time squared:

$$
[\text{force}] = [\text{M}] \times \frac{[\text{L}]}{[\text{T}]^2} = [\text{M L T}^{-2}]
$$

This expression, $[\text{M L T}^{-2}]$, is the **dimensional formula** of force. It says: force has 1 power of mass, 1 power of length, and $-2$ powers of time. Notice the magnitude is gone. Initial velocity, final velocity, and average speed all share the same dimensions $[\text{L T}^{-1}]$, because dimensions describe the *type* of quantity, not its value.

| Quantity | Dimensional formula |
| --- | --- |
| Area | $[\text{L}^2]$ |
| Speed, velocity | $[\text{L T}^{-1}]$ |
| Acceleration | $[\text{L T}^{-2}]$ |
| Force | $[\text{M L T}^{-2}]$ |
| Energy, work | $[\text{M L}^2 \text{T}^{-2}]$ |
| Density | $[\text{M L}^{-3}]$ |

## Why it's true

!!! tip "New here? You can skip to the quick reference."
    Below is *why* dimensional analysis works, and the two things it lets you do. It is one of the most useful tricks in all of physics, so it is worth understanding, not just memorising.

Dimensional analysis rests on a single, almost obvious idea, the **principle of homogeneity**:

> You can only add or compare quantities of the **same kind**.

You cannot add a length to a time, just as you cannot add 3 apples to 2 hours and get a meaningful "5". This means **every term in a correct physics equation must have the same dimensions**. That one rule gives us two powerful tools.

### Tool 1: checking whether an equation can be right

Take the kinematics equation for distance (you will meet it properly in the next chapter):

$$
x = x_0 + v_0 t + \tfrac{1}{2}a t^2
$$

For this to be valid, every term must reduce to a length, $[\text{L}]$. Let us check each one, replacing each symbol with its dimensions:

$$
[x] = [\text{L}]
$$
$$
[x_0] = [\text{L}]
$$
$$
[v_0\, t] = [\text{L T}^{-1}][\text{T}] = [\text{L}]
$$
$$
\left[\tfrac{1}{2}a t^2\right] = [\text{L T}^{-2}][\text{T}^2] = [\text{L}]
$$

The $\tfrac{1}{2}$ is a pure number with no dimensions, so it is ignored. Every term came out as $[\text{L}]$, so the equation is **dimensionally consistent**. Each step here is the heart of the method: swap symbols for dimensions, simplify the powers, and see if the terms match.

!!! danger "Consistency is necessary, but not sufficient"
    If an equation **fails** this test, it is definitely **wrong**. But if it **passes**, it is *not proven right*. Dimensional analysis is blind to pure numbers: it cannot tell $\tfrac{1}{2}mv^2$ from $\tfrac{3}{16}mv^2$, because the $\tfrac{1}{2}$ and $\tfrac{3}{16}$ have no dimensions. It only catches the wrong *kind* of quantity, not a wrong *number*.

### Tool 2: guessing a formula from scratch

Because the dimensions must balance, you can sometimes work out the *form* of a formula before you know the physics. The classic example is the time period $T$ of a simple pendulum.

Guess that $T$ depends on the length $l$, the mass of the bob $m$, and the acceleration due to gravity $g$, each raised to some unknown power:

$$
T = k\, l^x\, g^y\, m^z
$$

Here $k$ is a dimensionless constant (a pure number). Now write the dimensions of both sides. The dimensions of $g$ are $[\text{L T}^{-2}]$:

$$
[\text{T}] = [\text{L}]^x\,[\text{L T}^{-2}]^y\,[\text{M}]^z = [\text{L}^{x+y}\, \text{T}^{-2y}\, \text{M}^z]
$$

Now match the power of each base quantity on the left and right:

- Power of $\text{M}$: left has $0$, right has $z$, so $z = 0$. (The mass does not matter!)
- Power of $\text{T}$: left has $1$, right has $-2y$, so $-2y = 1$, giving $y = -\tfrac{1}{2}$.
- Power of $\text{L}$: left has $0$, right has $x + y$, so $x = -y = \tfrac{1}{2}$.

Putting the powers back in:

$$
T = k\, l^{1/2}\, g^{-1/2} = k\sqrt{\frac{l}{g}}
$$

We derived the shape of the formula without solving any forces. The method cannot find the pure number $k$ (it turns out experiment and theory give $k = 2\pi$), but it found everything else, including the surprising fact that a pendulum's swing does not depend on the mass of the bob.

### Why relative errors add for a product

The rule $\frac{\Delta Z}{Z} = \frac{\Delta A}{A} + \frac{\Delta B}{B}$ is not a formula to swallow; it falls right out of multiplying. Take $Z = AB$. The true values could be as large as $A + \Delta A$ and $B + \Delta B$, so the largest $Z$ is:

$$
Z + \Delta Z = (A + \Delta A)(B + \Delta B) = AB + A\,\Delta B + B\,\Delta A + \Delta A\,\Delta B
$$

Now divide every term by $Z = AB$:

$$
\frac{Z + \Delta Z}{Z} = 1 + \frac{\Delta B}{B} + \frac{\Delta A}{A} + \frac{\Delta A}{A}\cdot\frac{\Delta B}{B}
$$

The last term is a tiny fraction times another tiny fraction (for example $0.006 \times 0.01$), so small we drop it. Subtracting the $1$ from both sides leaves exactly:

$$
\frac{\Delta Z}{Z} = \frac{\Delta A}{A} + \frac{\Delta B}{B}
$$

The power rule is the same idea applied $p$ times: $A^p$ means $A$ multiplied by itself $p$ times, so its relative error appears $p$ times over.

## Gotchas

!!! warning "Arguments of sin, log, and exp must be dimensionless"
    You can write $\sin\theta$ only if $\theta$ is a pure number (an angle in radians is a ratio of two lengths, so it is dimensionless). $\sin(5\ \text{m})$ is meaningless. The same goes for $\log$, $e^x$, and any such function.

!!! warning "A change of units never changes the number of significant figures"
    $4.700\ \text{m}$, $470.0\ \text{cm}$, and $4.700\times 10^3\ \text{mm}$ all have four significant figures. Switching units cannot make a measurement more or less precise.

!!! danger "Exact numbers have unlimited significant figures"
    A counting number or a pure factor like the $2$ in $C = 2\pi r$, or $\pi$ itself, is exact. It never limits the significant figures of your answer. Only *measured* values do.

!!! warning "Errors add even when quantities are subtracted"
    For both $A + B$ and $A - B$ the absolute errors **add**. A common trap is to think the errors cancel in a difference. They do not. Subtracting two nearly equal measured values gives a small result with a large percentage error.

!!! danger "Use percentage error for products, absolute error for sums"
    To combine errors in a product, quotient, or power, work with **relative or percentage** errors (they add). To combine errors in a sum or difference, work with **absolute** errors (they add). Mixing these up is the single most common error-analysis slip in NEET.

## Quick reference

| Idea | What to remember |
| --- | --- |
| Measurement | $\text{number} \times \text{unit}$; never drop the unit |
| Seven base units | m, kg, s, A, K, mol, cd |
| Sig figs (multiply/divide) | answer keeps the *fewest significant figures* of the inputs |
| Sig figs (add/subtract) | answer keeps the *fewest decimal places* of the inputs |
| Percentage error | $\dfrac{\Delta a}{a}\times 100\%$ |
| Error in $A \pm B$ | $\Delta Z = \Delta A + \Delta B$ (absolute errors add) |
| Error in $AB$ or $A/B$ | $\dfrac{\Delta Z}{Z} = \dfrac{\Delta A}{A} + \dfrac{\Delta B}{B}$ (relative errors add) |
| Error in $A^p B^q / C^r$ | $\dfrac{\Delta Z}{Z} = p\dfrac{\Delta A}{A} + q\dfrac{\Delta B}{B} + r\dfrac{\Delta C}{C}$ |
| Dimensions of force | $[\text{M L T}^{-2}]$ |
| Dimensions of energy | $[\text{M L}^2 \text{T}^{-2}]$ |
| Homogeneity | every term in an equation has the same dimensions |
| Dimensional check | fails $\Rightarrow$ wrong; passes $\Rightarrow$ maybe right |

## Where this connects

!!! connect "Units and dimensions sit underneath every other chapter"
    - The dimensional check used here is on the equation from [**motion in a straight line**](../kinematics/motion-straight-line.md), $x = x_0 + v_0 t + \tfrac{1}{2}at^2$. You will derive that equation properly there.
    - The dimensions of **force** $[\text{M L T}^{-2}]$ come from $F = ma$ in [**laws of motion**](../dynamics/laws-of-motion.md), and the unit is named the newton there.
    - The dimensions of **energy** $[\text{M L}^2\text{T}^{-2}]$ are checked again in [**work, energy and power**](../dynamics/work-energy-power.md), where the joule is defined.
    - The pendulum formula $T = 2\pi\sqrt{l/g}$ you half-derived here uses $g$, the acceleration due to gravity, explained in [**gravitation**](../gravitation/gravitation.md).

!!! intuition "If you remember one thing"
    A measurement is a number times a unit, everything is built from seven base quantities, and any honest physics equation must have matching dimensions on both sides. When in doubt about a formula, check the dimensions first.
