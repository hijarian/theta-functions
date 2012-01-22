theta-functions
===============

Implementation of theta-functions using trigonometric series.

They're the special functions of two variables. Described very well at [Wikipedia article](http://en.wikipedia.org/wiki/Theta_function).

Library exports four theta-functions and a small helper to calculate their second parameter.

Theta functions are functions of Complex variables, FYI.

Interface summary
=================

    thetaN n q u

where N is a number from 1 to 4, `n` is a quantization factor, `q` is a theta-functions special parameter, and `u` is an actual argument of function.

Parameter `q` should be calculated with the helper function `qpar`, which accepts real numbers as argument:

    qpar tau

qpar itself returns Complex value. This helper is used to draw the library closer to the definition of theta-functions provided in the books.

Constraints
===========

Never call theta1..4 with `u` > pi. Theta-functions are raising very rapidly (maybe it's because of trigonometric series representing them), so with large values of argument they overflow badly and return incorrect results.