---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# fit_EOS
This is code that allows to fit [Birch-Murnaghan](https://en.wikipedia.org/wiki/Birch–Murnaghan_equation_of_state), [Vinet](https://en.wikipedia.org/wiki/Rose–Vinet_equation_of_state), and polynomial log-log functional forms to Pressure-Volume ($P\text{-}V$) data provided by the user. The code uses a the ```curve_fit``` from ```scipy.optimize``` in combination with ```InterpolatedUnivariateSpline``` from ```scipy.interpolate```. The code supports error bars $\delta P_i$ in the pressure $P_i$, which changes the weights in the fitting to $w_i=1/\delta P_i$.  The output provides the fitting parameters for each of the functional forms with their respective errors from the covariance matrix. Different indicators are provided to determine which fit worked better, including RMSE, standard deviation of the residuals, $R^2$, and $\chi^2$  (see below).


Download the code [here](https://github.com/fgonzcat/fit_EOS).
