# 🌙 Lunar Dust

> A Lua implementation in Rust, aimed to faithfully recreate the behavior of the original C code.

---

## What is Lunar Dust?

**Lunar Dust** is a from-scratch implementation of the [Lua](https://www.lua.org/) programming language, written in Rust.

It **is not** meant to be a production runtime, this is a study project, with the goal of **behavior fidelity to the reference implementation** (Lua 5.5.0), not novelty.

---

## Status

Don't expect quick updates nor a very high level code, not that I would not try.

- [ ] Front-End + Basic
	- [ ] Lexer
	- [ ] Parser
	- [ ] Lua value
	- [ ] Lua table 
    - [ ] Lexical scoping
- [ ] Code generator
    - [ ] Symbol resolution
    - [ ] Register allocation
    - [ ] Constant folding & optimizations
    - [ ] Emission of bytecode
- [ ] Virtual machine
	- [ ] Stack & Call Frames
    - [ ] Register-based dispatch loop
    - [ ] Call frames & stack
    - [ ] Metamethods & Metatables
    - [ ] Error handling (pcall/xpcall)
    - [ ] Coroutines
- [ ] Garbage collector
    - [ ] Mark & sweep
    - [ ] Incremental collection
    - [ ] Generational mode
    - [ ] Finalizers (\__gc)
    - [ ] Weak tables
- [ ] Standard library
	- [ ] Basic library
	- [ ] String
	- [ ] Table
	- [ ] Math
	- [ ] IO
	- [ ] OS
	- [ ] UTF-8
	- [ ] Debug
- [ ] C API & Embedding
- [ ] Tooling & Testing
	- [ ] Write a REPL
	- [ ] Implement Bytecode serialization
	- [ ] Pass the official Lua test suite

*(Subject to change/updates)*

---

## Building

```bash
git clone https://github.com/<you>/lunar-dust.git
cd lunar-dust
cargo build --release
```

Run a script:

```bash
cargo run --release -- path/to/script.lua
```

Run the test suite:

```bash
cargo test
```

---

## Why "Lunar Dust"?

Between the options to name it, one was "Lunar Rust", what I thought was strange, then changed to "Lunar Dust", which I liked, liked so much that I chose it. 
(some ideas I discarded: "Lua.rs", "Luast", "Rua", ...)

---

## References

- [Lua 5.5 source code](https://www.lua.org/ftp/)
- [*The Implementation of Lua 5.0*](https://www.lua.org/doc/jucs05.pdf) — Ierusalimschy et al.
- [*Lua 5.5 Reference Manual*](https://www.lua.org/manual/5.5/)

---

## License

MIT — same spirit as Lua's. See [License](license) or [Lua license page](https://www.lua.org/license.html).

It would be weird to relicense a language you're reimplementing.
