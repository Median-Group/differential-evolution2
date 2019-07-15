This is a hastily modified version of
[martinus'](https://github.com/martinus)
[differential-evolution-rs](https://docs.rs/differential-evolution/0.2.2/differential_evolution/)
library. 

I needed an optimization library that could be compiled to WebAssembly for
use in a [demo](http://mediangroup.org/insights2) I was working on, and
most of them required functionality that wasn't easily available in WASM
(e.g., [`rusty_machine`](https://crates.io/crates/rusty-machine/) depends
on an old version of [`rand`](https://crates.io/crates/rand) that doesn't
work in WASM,
[OptimizationEngine](https://crates.io/crates/optimization_engine) is
targeted at realtime systems and needs access to system time, etc).

The original version of this library also depended on a version of `rand`
that doesn't work in WASM, but fortunately the library was simple enough
that updating the API wasn't too difficult.
