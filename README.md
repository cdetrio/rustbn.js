# rustbn.js

[![Greenkeeper badge](https://badges.greenkeeper.io/ethereumjs/rustbn.js.svg)](https://greenkeeper.io/)

Rust to Javascript compile of the [Parity fork](https://github.com/paritytech/bn) of the [Zcash bn
pairing cryptography library](https://github.com/zcash/bn), implementing an efficient bilinear pairing on the Barreto-Naehrig (BN) curve. 

## Installation

TODO

## Usage

TODO

## Developer

### Compilation

Compilation process is based on [this tutorial](http://asquera.de/blog/2017-04-10/the-path-to-rust-on-the-web/) using [Emscripten](http://kripken.github.io/emscripten-site/) to compile the original Rust sources to [asm.js](http://asmjs.org/) ([Wikipedia](https://en.wikipedia.org/wiki/Asm.js)). This might be extended in the future to also include a ``WASM`` compiled version to choose from.

For basic setup follow the "Installing the Tools" section of the tutorial (make sure to use the ``incoming`` branch of ``emsdk``).

For ``asm.js`` compilation ``asmjs-unknown-emscripten`` target has to be added with ``rustup``:

```
rustup target add asmjs-unknown-emscripten
```

Compilation steps can be found in the ``makefile`` in the main directory and executed with:

```
make asmjs
```


### WASM (Experimental)

WASM files can be compiled with ``make wasm`` to the ``exp``. This is just intended for experimentation
working in browser only (not with Node.js) and not ready for production use!

Start a server with ``python -m SimpleHTTPServer`` and browse to http://localhost:8000/. You might have
to modify the ``exp/index.html`` file to get things to work.

## Additional Resources

- Another [compilation tutorial](https://medium.com/@ianjsikes/get-started-with-rust-webassembly-and-webpack-58d28e219635) using ``Webpack``
- [Talk](https://rreverser.com/rust-javascript-interop/) on ``Emscripten`` and ``Rust``
- [Compiling Rust to your Browser](https://www.hellorust.com/emscripten/)



 