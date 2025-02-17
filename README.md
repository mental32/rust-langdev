# Langdev libraries for Rust

- [Lexers](#lexers)
- [Parsers](#parsers)
- [Codegen](#codegen)
- [String interning](#string-interning)
- [Just-in-time compilation](#just-in-time-compilation)
- [Error reporting](#error-reporting)
- [Language server protocol](#language-server-protocol)
- [Testing](#testing)
- [Incremental compilation](#incremental-compilation)
- [Floats/Ints/Bools](#floatsintsbools)
- [Binary & object file parsing, generating and processing](#binary--object-file-parsing-generating-and-processing)
- [Solvers](#solvers)
- [CLI](#cli)
- [Repl](#repl)
- [String handling](#string-handling)
- [Syntax trees](#syntax-trees)
- [Pretty printing](#pretty-printing)
- [Variable binding](#variable-binding)
- [Caching](#caching)
- [WASM](#wasm)
- [Logging](#logging)
- [Storage](#storage)
  - [Disjoint-sets](#disjoint-sets)

## Lexers

- [`logos`](https://crates.io/crates/logos) Logos has two goals: To make it easy to create a Lexer, so you can focus on more complex problems and to make the generated Lexer faster than anything you'd write by hand
- [`lrlex`](https://crates.io/crates/lrlex) A replacement for [`lex`](http://dinosaur.compilertools.net/lex/index.html)/[`flex`](https://westes.github.io/flex/manual/) that generates Rust code
    
## Parsers

- [`parze`](https://crates.io/crates/parze) Parze is a clean, efficient parser combinator written in Rust
- [`lalrpop`](https://crates.io/crates/lalrpop) A convenient LR(1) parser generator
- [`nom`](https://crates.io/crates/nom) A byte-oriented, zero-copy, parser combinators library
- [`combine`](https://crates.io/crates/combine) Fast parser combinators on arbitrary streams with zero-copy support.
- [`pom`](https://crates.io/crates/pom) PEG parser combinators using operator overloading without macros.
- [`peg`](https://crates.io/crates/peg) A simple Parsing Expression Grammar (PEG) parser generator.
- [`glue`](https://crates.io/crates/glue) Glue is a parser combinator framework for parsing text based formats, it is easy to use and relatively fast too
- [`pratt`](https://crates.io/crates/pratt) A general purpose pratt parser for Rust
- [`pest`](https://crates.io/crates/pest) A general purpose parser written in Rust with a focus on accessibility, correctness, and performance using parsing expression grammars (PEG)
- [`lrpar`](https://crates.io/crates/lrpar) A Yacc-compatible parser.
    
## Codegen

- [`cranelift`](https://crates.io/crates/cranelift) Cranelift is a low-level retargetable code generator
- [`llvm-sys`](https://crates.io/crates/llvm-sys) Bindings to LLVM's C API
- [`llama`](https://crates.io/crates/llama) Friendly LLVM bindings
- [`inkwell`](https://crates.io/crates/inkwell) Inkwell aims to help you pen your own programming languages by safely wrapping llvm-sys
- [`llvm-ir`](https://crates.io/crates/llvm-ir) LLVM IR in natural Rust data structures
- [`llvmenv`](https://crates.io/crates/llvmenv) Manage multiple LLVM/Clang builds
- [`walrus`](https://crates.io/crates/walrus) A library for performing WebAssembly transformations
- [`cilk`](https://github.com/maekawatoshiki/cilk) Toy Compiler Infrastructure influenced by LLVM written in Rust.
    
## String interning

- [`lasso`](https://crates.io/crates/lasso) A multithreaded and single threaded string interner with a minimal memory footprint and arena allocation
- [`string-interner`](https://crates.io/crates/string-interner) A data structure to cache strings efficiently
- [`simple-interner`](https://crates.io/crates/simple-interner) A simple append-only interner
- [`string_cache`](https://crates.io/crates/string_cache) A string interning library for Rust, developed as part of the Servo project
    
## Just-in-time Compilation

- [`masm-rs`](https://github.com/playxe/masm-rs) A JSC/SpiderMonkey like macro assembler
- [`jit`](https://crates.io/crates/jit) (LibJIT) Just-In-Time Compilation in Rust using LibJIT bindings
- [`lightning-sys`](https://crates.io/crates/lightning-sys) GNU lightning bindings for rust
- [`gccjit`](https://crates.io/crates/gccjit) Higher-level Rust bindings for libgccjit
- [`cranelift`](https://crates.io/crates/cranelift) Cranelift is a low-level retargetable code generator
- [`dynasm`](https://crates.io/crates/dynasm) A Dynamic assembler written in Rust for Rust
    
## Error reporting

- [`codespan-reporting`](https://crates.io/crates/codespan-reporting) Beautiful diagnostic reporting for text-based programming languages
- [`codespan`](https://crates.io/crates/codespan) Data structures for tracking locations in source code
- [`text-size`](https://crates.io/crates/text_size) A library that provides newtype wrappers for `u32` and `(u32, u32)` for use as text offsets
    
## Language server protocol

- [`lsp-types`](https://crates.io/crates/lsp-types) Types for interaction with a language server, using VSCode's Language Server Protocol
- [`tower-lsp`](https://crates.io/crates/tower-lsp) Language Server Protocol implementation based on Tower
- [`codespan-lsp`](https://crates.io/crates/codespan-lsp) Conversions between codespan types and Language Server Protocol types
- [`lsp-server`](https://crates.io/crates/lsp-server) A generic LSP server scaffold
    
## Testing

- [`goldentests`](https://crates.io/crates/goldentests) A golden file testing library where tests can be configured within the same test file
- [`lang_tester`](https://crates.io/crates/lang_tester) Concise language testing framework for compilers and VMs (Linux only)
- [`compiletest_rs`](https://crates.io/crates/compiletest_rs) The compiletest utility from the Rust compiler as a standalone testing harness
- [`insta`](https://crates.io/crates/insta) A snapshot testing library for Rust
- [`k9`](https://crates.io/crates/k9) Snapshot testing and better assertions
    
## Unicode

- [`unicode-xid`](https://crates.io/crates/unicode-xid) Determine if a char is a valid identifier for a parser and/or lexer according to [Unicode Standard Annex #31](https://www.unicode.org/reports/tr31/) rules.
- [`unicode-normalisation`](https://crates.io/crates/unicode-normalization) Unicode character composition and decomposition utilities as described in [Unicode Standard Annex #15](http://www.unicode.org/reports/tr15/)
- [`unicode-segmentation`](https://crates.io/crates/unicode-segmentation) Iterators which split strings on Grapheme Cluster or Word boundaries, according to the [Unicode Standard Annex #29](http://www.unicode.org/reports/tr29/) rules
- [`unicode-width`](https://crates.io/crates/unicode-width) Determine displayed width of char and str types according to [Unicode Standard Annex #11](http://www.unicode.org/reports/tr11/) rules
- [`lexical-sort`](https://crates.io/crates/lexical-sort) Lexicographical sorting of unicode strings
    
## Incremental compilation

- [`salsa`](https://crates.io/crates/salsa) A generic framework for on-demand, incrementalized computation
    
## Floats/Ints/Bools

- [`lexical`](https://crates.io/crates/lexical) Lexical, to- and from-string conversion routines (Fast lexical conversion routines for both `std` and `no_std` environments)
- [`lexical-core`](https://crates.io/crates/lexical-core) Lexical, to- and from-string conversion routines (Low-level, lexical conversion routines for use in a `no_std` context)
- [`lexical_bool`](https://crates.io/crates/lexical_bool) A bool-like type that can be parsed from a string
- [`ryu`](https://crates.io/crates/ryu) A Rust implementation of the PLDI'18 paper [Ryū: fast float-to-string conversion](https://dl.acm.org/doi/10.1145/3192366.3192369) by Ulf Adams
- [`hexponent`](https://crates.io/crates/hexponent) C11 compliant hex float parsing
- [`ordered-float`](https://crates.io/crates/ordered-float) Total ordering on floats
- [`half`](https://crates.io/crates/half) A half-precision floating point `f16` type for Rust implementing the IEEE 754-2008 standard
- [`f128`](https://crates.io/crates/f128) Bindings to the gcc quadmath library
- [`approx`](https://crates.io/crates/approx) Approximate floating point equality comparisons and assertions
    
## Binary & object file parsing, generating and processing

- [`goblin`](https://crates.io/crates/goblin) An impish, cross-platform, ELF, Mach-o, and PE binary parsing and loading crate
- [`gimli`](https://crates.io/crates/gimli) A library for reading and writing the DWARF debugging format.
- [`faerie`](https://crates.io/crates/faerie) ELF and Mach-o native binary object file emitter
- [`object`](https://crates.io/crates/object) A unified interface for reading and writing object file formats.
- [`elf`](https://crates.io/crates/elf) A pure-rust library for parsing ELF files
- [`elfkit`](https://crates.io/crates/elfkit) An elf parser and manipulation library in pure rust 
    
## Symbolic Execution

- [`haybale`](https://crates.io/crates/haybale) Symbolic execution of LLVM IR
    
## Solvers

- [`rsmt2`](https://crates.io/crates/rsmt2) Wrapper for SMT-LIB 2 compliant SMT solvers.
- [`z3`](https://crates.io/crates/z3) A high-level rust bindings for the Z3 SMT solver from Microsoft Research
- [`z3-sys`](https://crates.io/crates/z3-sys) Low-level bindings for the Z3 SMT solver from Microsoft Research
- [`z3_ref`](https://crates.io/crates/z3_ref) A high level interface to the Z3 SMT solver
- [`z3d`](https://crates.io/crates/z3d) Z3 DSL interface for Rust
- [`boolector`](https://crates.io/crates/boolector) Safe high-level bindings for the Boolector SMT solver
- [`boolector-sys`](https://crates.io/crates/boolector-sys) Low-level bindings for the Boolector SMT solver

## CLI

- [`structopt`](https://crates.io/crates/structopt) Parse command line arguments by defining a struct
- [`clap`](https://crates.io/crates/clap) A simple to use, efficient, and full-featured Command Line Argument Parser 
- [`pico-args`](https://crates.io/crates/pico-args) An ultra simple CLI arguments parser
- [`argh`](https://crates.io/crates/argh) A derive-based argument parser optimized for code size
    
## Repl

- [`rustyline`](https://crates.io/crates/rustyline) Rustyline, a readline implementation based on Antirez's Linenoise
- [`repl-rs`](https://crates.io/crates/repl-rs) Library to generate a REPL for your application
- [`termwiz`](https://crates.io/crates/termwiz) Terminal Wizardry for Unix and Windows

## String handling

- [`beef`](https://crates.io/crates/beef) Faster, more compact implementation of [`Cow`](https://doc.rust-lang.org/alloc/borrow/enum.Cow.html).
- [`smol_str`](https://crates.io/crates/smol_str) Small-string optimized string type with O(1) clone
- [`smallstring`](https://crates.io/crates/smallstring) 'Small string' optimization: store small strings on the stack using smallvec
- [`heck`](https://crates.io/crates/heck) Heck is a case conversion library that exists to provide case conversion between common cases like CamelCase and snake_case. It is intended to be unicode aware, internally consistent, and reasonably well performing

## Syntax trees

- [`rowan`](https://crates.io/crates/rowan) Generic lossless syntax trees

## Pretty printing

- [`pretty`](https://crates.io/crates/pretty) Wadler-style pretty-printing combinators in Rust

## Variable binding

- [`moniker`](https://crates.io/crates/moniker) An automagical variable binding library for tracking variables in scopes

## Caching

- [`cached`](https://crates.io/crates/cached) Caching structures and simplified function memoization

## WASM

- [`wain`](https://crates.io/crates/wain) WebAssembly interpreter written in Safe Rust with zero dependencies
- [`wasmer`](https://crates.io/crates/wasmer) The high-level public API of the Wasmer WebAssembly runtime
- [`wasmtime`](https://crates.io/crates/wasmtime) High-level API to expose the Wasmtime runtime
- [`wasmtime-jit`](https://crates.io/crates/wasmtime-jit) JIT-style execution for WebAsssembly code in Cranelift
- [`wasmlite-parser`](https://crates.io/crates/wasmlite-parser) This crate parses WebAssembly modules and can generate LLVM IR based the data extracted from a module
- [`parity-wasm-cp`](https://crates.io/crates/parity-wasm-cp) WebAssembly binary format serialization/deserialization/interpreter
- [`substrate-wasm-builder`](https://crates.io/crates/substrate-wasm-builder) A utility for building WASM binaries
- [`walrus`](https://crates.io/crates/walrus) A library for performing WebAssembly transformations 

## Logging

- [`tracing`](https://crates.io/crates/tracing) Application-level tracing for Rust
  - [`tracing-timing`](https://crates.io/crates/tracing-timing) Inter-event timing metrics on top of `tracing`
  - [`tracing-coz`](https://crates.io/crates/tracing-coz) Rust-tracing support for the [coz](https://github.com/plasma-umass/coz/#installation) Causal Profiler
  - [`tracing-flame`](https://crates.io/crates/tracing-flame) A tracing `Layer` for generating a folded stack trace for generating flamegraphs and flamecharts with inferno
  - [`test-env-log`](https://crates.io/crates/test-env-log) A crate that takes care of automatically initializing logging and/or tracing for Rust tests.
  - [`tracing-unwrap`](https://crates.io/crates/tracing-unwrap) This crate provides `.unwrap_or_log()` and `.expect_or_log()` methods on `Result` and `Option` types that log failed unwraps to a `tracing::Subscriber`
- [`log`](https://crates.io/crates/log) A Rust library providing a lightweight logging facade
- [`slog`](https://crates.io/crates/slog) An ecosystem of reusable components for structured, extensible, composable and contextual logging for Rust

## Storage

- [`indexmap`](https://crates.io/crates/indexmap) A hash table with consistent order and fast iteration
- [`vecmap`](https://crates.io/crates/vecmap) Vec-based Map and Set data structures

### Disjoint-sets

- [`union-find`](https://crates.io/crates/union-find) Struct and methods for union-find operation
- [`ena`](https://crates.io/crates/ena) An implementation of union-find in Rust; extracted from (and used by) rustc
