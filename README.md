# Oprand

JavaScript library that provides generic primitive `OP` and a set of functions
to semi-overload arithmetic operators.

## Background

JavaScript as many other programming languages have it's own representation of
[arithmetic](https://en.wikipedia.org/wiki/Arithmetic) and it's operations:
addition, subtraction, multiplication, division, etc.

Those operations denoted by commonly agreed symbols, like: `+` for addition,
`-` for subtraction, `*` or `✕` for multiplication, `/` or `÷` for division,
and so forth, and applied to a pair[^1] of operands, on a left from the sign and
on a right from it.

Depending on a applied operation, those operands might called differently, as
they played different roles.

JavaScript implements arithmetic traits from it's beginning[^2].

As in many other programming languages, in JavaScript arithmetic operations can
be applied only to a particular set of values, — widely known as numbers. Values
of other types required to be converted first to a number, to be able to perform
arithmetic operations with 'em. Though, in some cases JavaScript hiddenly make
such type conversion by itself while evaluation math expression, or at least try
to do it correctly.

[^1]: Some operations are non binary, but unary.

[^2]: First edition of [ECMA-262](https://www.ecma-international.org/wp-content/uploads/ECMA-262_1st_edition_june_1997.pdf) (1997) suggests most of the arithmetic operations.

- what limitations arithmetic have?
- what this library aimed for?


