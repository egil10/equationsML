# equationsML

Learning machine learning and neural networks by approximating classic mathematical functions.

The aim of this repository is to build small, understandable experiments: start with simple sampled data, fit models to known functions, compare interpolation and extrapolation behavior, and inspect where neural networks succeed or struggle.

<hr>

## Function Roadmap

1. **Runge function**

$$
f(x)=\frac{1}{1+25x^2}
$$

Useful for studying interpolation difficulty, oscillations, and how models behave near interval edges.

2. **Sine wave**

$$
f(x)=\sin(x)
$$

A smooth periodic baseline for learning repeated structure.

3. **Cosine mixture**

$$
f(x)=0.6\cos(x)+0.4\cos(3x)
$$

A slightly richer periodic target with multiple frequencies.

4. **Gaussian bump**

$$
f(x)=e^{-x^2}
$$

A localized smooth function for learning peaks and decay.

5. **Absolute value**

$$
f(x)=|x|
$$

A simple non-smooth function with a sharp corner at zero.

6. **ReLU**

$$
f(x)=\max(0,x)
$$

A piecewise linear target connected directly to common neural network activations.

7. **Sigmoid**

$$
f(x)=\frac{1}{1+e^{-x}}
$$

A smooth saturating curve for studying bounded outputs.

8. **Hyperbolic tangent**

$$
f(x)=\tanh(x)
$$

A centered saturating function often used in neural network examples.

9. **Damped oscillation**

$$
f(x)=e^{-0.2x}\sin(3x)
$$

A target that combines frequency, changing amplitude, and extrapolation challenges.

10. **Two-dimensional saddle**

$$
f(x,y)=x^2-y^2
$$

A first step beyond one-dimensional regression into surfaces.

<hr>

## Repository Structure

```text
code/
  data/       Small generated datasets and notes.
  notebooks/  Exploratory notebooks.
  scripts/    Reusable experiment scripts.
  plots/      Generated figures and model diagnostics.
```

<hr>

## Working Goal

Each function should eventually have a small experiment that:

- samples training and test points,
- trains at least one baseline model and one neural network,
- plots predictions against the true function,
- records what worked, what failed, and why.
