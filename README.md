# purescript-howto

How to solve common programming tasks in PureScript. Submit content or topic ideas please!

## Motivation

This project was motivated by andrewc, who suggested a curated PureScript cookbook, which would have tutorials for solving tasks in PureScript which are more complicated "hello world". The cookbooks I've seen aren't terribly useful, as they are little more than a collection of code snippets and prescribe a library rather than analyzing the problem. This repo aims to be useful to the audience that would use a PureScript cookbook, but to be a better reference than a cookbook by being a teacher rather than a snippet repository or library prescriber.

## Scope

To help decide which topics fit into the content and structure of this repo, use the following guidelines:

- The tasks in this repo should be common tasks which have well-accepted solutions.
- The alternatives in this repo should be generic concepts.

The scope guidelines are open for updates. We don't want to exclude otherwise useful content. :thumbsup:

## Style

Rather than spending hours analyzing the problem on your own and crafting the right functions, datatypes, & typeclasses to solve a relatively common programming task, it's easier to just use a shared solution. Before a person can confidently accept a shared solution, they need to know that it is indeed a well-considered and well-designed solution. The content in this repo should communicate this.

Style guidelines:

- Explain the problem and constraints.
- Use code samples using one or more libraries to illustrate the solution in PureScript
- Avoid teaching a specific library or API
- Avoid assuming the reader understands relatively unrelated concepts
- AVoid deeply explaining unrelated concepts

## Patterns

Initial ideas of documentation patterns follow.

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
