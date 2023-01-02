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
such type conversion[^3] by itself while evaluation math expression, or at least try
to do it correctly.

## The issue

In some cases, when we engineering something complex, we might want to end up
with a code that have greater level of expressiveness, and describe arithmetic
operation not only on numbers but [geometry shapes](https://en.wikipedia.org/wiki/Geometric_algebra), [vectors](https://en.wikipedia.org/wiki/Vector_calculus), [matrices](https://en.wikipedia.org/wiki/Matrix_(mathematics)) or just to calculate an
amounts presented in a different currencies.

```typescript
Circle({ x: 0, y: 0, r: 5 }) + Rectangle({ x: 2, y: 1, w: 7, h: 2 })

Vec(2, -5) + Vec(2, 1)

USD(1_000) - EUR(500) + BTC(0.000001)

Matrix([1, 9, -13], [20, 5, -6]) * Matrix([3, -2, 8])
```

And JavaScript gives us a hand on that. Each object can define `valueOf` method
which will be invoked before arithmetic operation, but here is a catch,
the result of invocation should be a number.


[^1]: Some operations are non binary, but unary.

[^2]: First edition of [ECMA-262](https://www.ecma-international.org/wp-content/uploads/ECMA-262_1st_edition_june_1997.pdf) (1997) suggests most of the arithmetic operations.

[^3]: [JavaScript type conversion](https://developer.mozilla.org/en-US/docs/Glossary/Type_Conversion)

- what limitations arithmetic have?
- what this library aimed for?


