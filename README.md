# Fluent

Fluent is a localization system designed to unleash the expressive power of
the natural language.

This repository contains the specification, the reference implementation of the
parser and the documentation for Fluent.

## Fluent Syntax (FTL)

FTL is the syntax for describing translation resources in Project Fluent.  FTL
stands for *Fluent Translation List*. Read the [Fluent Syntax Guide][] to get
started learning Fluent.

The `syntax/` directory contains the reference implementation of the syntax as
a _LL(infinity)_ parser.

The `spec/` directory contains the formal EBNF grammar, autogenerated from the
reference implementation.

## Development

While working on the reference parser, use the following commands to test and
validate your work:

    npm test                   # Test the parser against JSON AST fixtures.
    npm run lint               # Lint the parser code.

    npm run generate:ebnf      # Generate the EBNF from syntax/grammar.js.
    npm run generate:fixtures  # Generate test fixtures (FTL → JSON AST).

    npm run build:guide        # Build the HTML version of the Guide.

    npm run bench              # Run the performance benchmark on large FTL.

## Other Implementations

This repository contains the reference implementation of the parser. Other implementations exist which should be preferred for use in production and in tooling.

  - The JavaScript implementation at [`fluent.js`](https://github.com/projectfluent/fluent.js), including the [React bindings](https://github.com/projectfluent/fluent.js/tree/master/fluent-react).
  - The Python implementation at [`python-fluent`](https://github.com/projectfluent/python-fluent).
  - The Rust implementation at [`fluent-rs`](https://github.com/projectfluent/fluent-rs).

We also know about the following community-driven implementations:

  - [`Fluent.Net`](https://github.com/blushingpenguin/Fluent.Net) by [@blushingpenguin](https://github.com/blushingpenguin). See [#93](https://github.com/projectfluent/fluent/issues/93) for more info.
  - A Java/Kotlin implementation has been requested in [#158](https://github.com/projectfluent/fluent/issues/158).
  - [`elm-fluent`](https://github.com/elm-fluent/elm-fluent) by [@spookylukey](https://github.com/spookylukey/)
  - A Lua implementation effort is underway at [`fluent-lua`](https://github.com/alerque/fluent-lua) by [@alerque](https://github.com/alerque).
  - A D implementation effort is underway at [`fluentd`](https://github.com/SirNickolas/fluentd) by [@SirNickolas](https://github.com/SirNickolas).

## Learn More and Discuss

Find out more about Project Fluent at [projectfluent.org][] and discuss the future of Fluent at [Mozilla Discourse][].

[Fluent Syntax Guide]: http://projectfluent.org/fluent/guide
[projectfluent.org]: http://projectfluent.org
[Mozilla Discourse]: https://discourse.mozilla.org/c/fluent
