# Truffle Tools Changelog

This changelog summarizes major changes between Truffle Tools versions.

## Version 21.3.0
* Reimplemented CPUSampler to use the Truffle language safepoints thus deprecating several API functions.
* Support for hash interoperability in Insight - no need to use `Truffle::Interop.hash_keys_as_members` anymore

## Version 21.1.0

* Use `--heap.dump=/path/to/file/to/generate.hprof` to enable [Heap Dumping via Insight](docs/Insight-Manual.md#Heap-Dumping)
* [Insight object API](https://www.graalvm.org/tools/javadoc/org/graalvm/tools/insight/Insight.html) provides access to `charIndex`, `charLength` and `charEndIndex`

## Version 21.0.0

* `--insight` option is no longer considered experimental
* Use `ctx.iterateFrames` to [access whole stack and its variables](docs/Insight-Manual.md#Accessing-whole-Stack)
* Embedders can [inject additional objects](docs/Insight-Embedding.md#Extending-Functionality-of-Insight-Scripts) into Insight scripts

## Version 20.3.0

* [GraalVM Insight](docs/Insight.md) Maven artifact is now `org.graalvm.tools:insight:20.3.0`
* [GraalVM Insight](docs/Insight-Manual.md#intercepting--altering-execution) can intercept execution and modify return values

## Version 20.2.0

* [GraalVM Insight](docs/Insight-Manual.md#modifying-local-variables) can modify values of local variables
* Write [GraalVM Insight](docs/Insight-Manual.md#python) scripts in Python

## Version 20.1.0

* [GraalVM Insight](docs/Insight-Manual.md#hack-into-the-c-code) can access local variables in C, C++ and other LLVM languages
* [GraalVM Insight](docs/Insight.md) is the new name for the former *T*-*Trace* technology

## Version 20.0.0
* Access to source location (see `line`, `column`, etc.) and `sourceFilter` selector in [Insight agent object API](https://www.graalvm.org/tools/javadoc/org/graalvm/tools/insight/Insight.html#VERSION)
* Embedding [Insight](docs/Insight-Embedding.md) into own application is now easily done via [Graal SDK](https://www.graalvm.org/tools/javadoc/org/graalvm/tools/insight/Insight.html#ID)
* Apply [Insight scripts](docs/Insight-Manual.md) C/C++/Julia & co. code - e.g. *hack into C with JavaScript*!
* Better error handling - e.g. propagation of errors from [Insight scripts](docs/Insight-Manual.md) to application code
* Hack your [Insight scripts in R](docs/Insight-Manual.md)!

## Version 19.3.0
* Introducing [GraalVM Insight](docs/Insight.md) - a  multipurpose, flexible tool for instrumenting and monitoring applications at full speed.
* Added a CLI code coverage tool for truffle languages. Enabled with `--coverage`. See `--help:tools` for more details.