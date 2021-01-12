# Snapshot report for `test/prefer-number-properties.js`

The actual snapshot is saved in `prefer-number-properties.js.snap`.

Generated by [AVA](https://avajs.dev).

## Invalid #1
      1 | const foo = {[NaN]: 1}

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = {[Number.NaN]: 1}␊
    ␊
    Error 1/1:␊
    > 1 | const foo = {[NaN]: 1}␊
        |               ^^^ Prefer `Number.NaN` over `NaN`.␊
    `

## Invalid #2
      1 | const foo = {[NaN]() {}}

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = {[Number.NaN]() {}}␊
    ␊
    Error 1/1:␊
    > 1 | const foo = {[NaN]() {}}␊
        |               ^^^ Prefer `Number.NaN` over `NaN`.␊
    `

## Invalid #3
      1 | foo[NaN] = 1;

> Snapshot 1

    `␊
    Output:␊
      1 | foo[Number.NaN] = 1;␊
    ␊
    Error 1/1:␊
    > 1 | foo[NaN] = 1;␊
        |     ^^^ Prefer `Number.NaN` over `NaN`.␊
    `

## Invalid #4
      1 | class A {[NaN](){}}

> Snapshot 1

    `␊
    Output:␊
      1 | class A {[Number.NaN](){}}␊
    ␊
    Error 1/1:␊
    > 1 | class A {[NaN](){}}␊
        |           ^^^ Prefer `Number.NaN` over `NaN`.␊
    `

## Invalid #5
      1 | foo = {[NaN]: 1}

> Snapshot 1

    `␊
    Output:␊
      1 | foo = {[Number.NaN]: 1}␊
    ␊
    Error 1/1:␊
    > 1 | foo = {[NaN]: 1}␊
        |         ^^^ Prefer `Number.NaN` over `NaN`.␊
    `

## Invalid #6
      1 | const foo = Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = Number.POSITIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = Infinity;␊
        |             ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #7
      1 | if (Number.isNaN(Infinity)) {}

> Snapshot 1

    `␊
    Output:␊
      1 | if (Number.isNaN(Number.POSITIVE_INFINITY)) {}␊
    ␊
    Error 1/1:␊
    > 1 | if (Number.isNaN(Infinity)) {}␊
        |                  ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #8
      1 | if (Object.is(foo, Infinity)) {}

> Snapshot 1

    `␊
    Output:␊
      1 | if (Object.is(foo, Number.POSITIVE_INFINITY)) {}␊
    ␊
    Error 1/1:␊
    > 1 | if (Object.is(foo, Infinity)) {}␊
        |                    ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #9
      1 | const foo = bar[Infinity];

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = bar[Number.POSITIVE_INFINITY];␊
    ␊
    Error 1/1:␊
    > 1 | const foo = bar[Infinity];␊
        |                 ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #10
      1 | const foo = {Infinity};

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = {Infinity: Number.POSITIVE_INFINITY};␊
    ␊
    Error 1/1:␊
    > 1 | const foo = {Infinity};␊
        |              ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #11
      1 | const foo = {Infinity: Infinity};

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = {Infinity: Number.POSITIVE_INFINITY};␊
    ␊
    Error 1/1:␊
    > 1 | const foo = {Infinity: Infinity};␊
        |                        ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #12
      1 | const foo = {[Infinity]: -Infinity};

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = {[Number.POSITIVE_INFINITY]: Number.NEGATIVE_INFINITY};␊
    ␊
    Error 1/2:␊
    > 1 | const foo = {[Infinity]: -Infinity};␊
        |               ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    Error 2/2:␊
    > 1 | const foo = {[Infinity]: -Infinity};␊
        |                          ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #13
      1 | const foo = {[-Infinity]: Infinity};

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = {[Number.NEGATIVE_INFINITY]: Number.POSITIVE_INFINITY};␊
    ␊
    Error 1/2:␊
    > 1 | const foo = {[-Infinity]: Infinity};␊
        |               ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    Error 2/2:␊
    > 1 | const foo = {[-Infinity]: Infinity};␊
        |                           ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #14
      1 | const foo = {Infinity: -Infinity};

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = {Infinity: Number.NEGATIVE_INFINITY};␊
    ␊
    Error 1/1:␊
    > 1 | const foo = {Infinity: -Infinity};␊
        |                        ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #15
      1 | const {foo = Infinity} = {};

> Snapshot 1

    `␊
    Output:␊
      1 | const {foo = Number.POSITIVE_INFINITY} = {};␊
    ␊
    Error 1/1:␊
    > 1 | const {foo = Infinity} = {};␊
        |              ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #16
      1 | const {foo = -Infinity} = {};

> Snapshot 1

    `␊
    Output:␊
      1 | const {foo = Number.NEGATIVE_INFINITY} = {};␊
    ␊
    Error 1/1:␊
    > 1 | const {foo = -Infinity} = {};␊
        |              ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #17
      1 | const foo = Infinity.toString();

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = Number.POSITIVE_INFINITY.toString();␊
    ␊
    Error 1/1:␊
    > 1 | const foo = Infinity.toString();␊
        |             ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #18
      1 | const foo = -Infinity.toString();

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = -Number.POSITIVE_INFINITY.toString();␊
    ␊
    Error 1/1:␊
    > 1 | const foo = -Infinity.toString();␊
        |              ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #19
      1 | const foo = (-Infinity).toString();

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = (Number.NEGATIVE_INFINITY).toString();␊
    ␊
    Error 1/1:␊
    > 1 | const foo = (-Infinity).toString();␊
        |              ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #20
      1 | const foo = +Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = +Number.POSITIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = +Infinity;␊
        |              ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #21
      1 | const foo = ++Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = ++Number.POSITIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = ++Infinity;␊
        |               ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #22
      1 | const foo = +-Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = +Number.NEGATIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = +-Infinity;␊
        |              ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #23
      1 | const foo = -Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = Number.NEGATIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = -Infinity;␊
        |             ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #24
      1 | const foo = --Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = --Number.POSITIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = --Infinity;␊
        |               ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #25
      1 | const foo = -(-Infinity);

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = -(Number.NEGATIVE_INFINITY);␊
    ␊
    Error 1/1:␊
    > 1 | const foo = -(-Infinity);␊
        |               ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #26
      1 | const foo = -(--Infinity);

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = -(--Number.POSITIVE_INFINITY);␊
    ␊
    Error 1/1:␊
    > 1 | const foo = -(--Infinity);␊
        |                 ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #27
      1 | const foo = 1 - Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = 1 - Number.POSITIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = 1 - Infinity;␊
        |                 ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #28
      1 | const foo = 1 - -Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const foo = 1 - Number.NEGATIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const foo = 1 - -Infinity;␊
        |                 ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `

## Invalid #29
      1 | const isPositiveZero = value => value === 0 && 1 / value === Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const isPositiveZero = value => value === 0 && 1 / value === Number.POSITIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const isPositiveZero = value => value === 0 && 1 / value === Infinity;␊
        |                                                              ^^^^^^^^ Prefer `Number.POSITIVE_INFINITY` over `Infinity`.␊
    `

## Invalid #30
      1 | const isNegativeZero = value => value === 0 && 1 / value === -Infinity;

> Snapshot 1

    `␊
    Output:␊
      1 | const isNegativeZero = value => value === 0 && 1 / value === Number.NEGATIVE_INFINITY;␊
    ␊
    Error 1/1:␊
    > 1 | const isNegativeZero = value => value === 0 && 1 / value === -Infinity;␊
        |                                                              ^^^^^^^^^ Prefer `Number.NEGATIVE_INFINITY` over `-Infinity`.␊
    `