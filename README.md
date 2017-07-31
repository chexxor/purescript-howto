# purescript-howto

How to do common programming tasks in PureScript. Submit content please!

## Motivation

This project was motivated by andrewc, who suggested a curated Purescript cookbook, which has examples of things that come after "hello world".

## Patterns

### Tasks

Content examples:

- Compiling PureScript (e.g. make, pulp, psc-package, purify, nix)
- PureScript dependency management (e.g. psc-package, purify, nix)
- Using PureScript from JavaScript
- Wrapping a JavaScript library

Needs a template.

### Alternatives

One part of learning a language is idioms. One way to learn a language's idioms is by seeing alternative, or just kinda similar, ways of writing a thing. [Github issue discussion](https://github.com/purescript/documentation/issues/85)/

Content examples:

- people first learn `logShow`, then discover `traceAny`.
- people first learn "do-notation", then discover that using `>>=`, `<$>`, and maybe `>=>` is better in some situations.
- people first learn records, then discover ADTs and lens are better in some situations.
- people first learn `ContT`, then discover `Aff` is more appropriate, or vice-versa.
- people first learn `Either MultipleErrors a`, then discover clever use of `ExceptT` is a bit better.
- people first use simple recursion, then discover `MonadRec` or fix-point concepts are helpful.

These Alternatives might need to be organized, perhaps by problem category.

- Debugging
- Parsing
- Error-handling
- Data structures

Needs a template.

### Other useful how-to docs

Open to creating other kinds of how-to docs here, given a motivating example.
