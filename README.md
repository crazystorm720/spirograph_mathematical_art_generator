# Spirograph - Mathematical Art Generator

A minimal implementation of spirograph patterns across three computational paradigms: C, Assembly, and WebAssembly.

![Spirograph Example](examples/output.png)

## Overview

This project demonstrates the same mathematical concept implemented in three different ways:

- **C**: Reference implementation for clarity
- **Assembly**: x86-64 bare metal performance  
- **WebAssembly**: Portable web module

All implementations generate the same mathematical patterns using parametric equations.

## Mathematics

The core spirograph equations:

```
x(t) = R·cos(t) + r·cos(k·t)
y(t) = R·sin(t) - r·sin(k·t)
```

Where:
- R = fixed circle radius
- r = moving circle radius
- k = frequency ratio
- t ∈ [0, 2π]

## Project Structure

```
spirograph/
├── c/                 # C implementation
├── asm/               # x86-64 Assembly
├── wasm/              # WebAssembly module
├── examples/          # Sample outputs
└── README.md
```

## Quick Start

```bash
# Build all implementations
make

# Run C version
./c/spirograph

# Run Assembly version
./asm/spirograph

# Serve WebAssembly version
cd wasm && python3 -m http.server
```

## Implementations

### C
Reference implementation focusing on mathematical clarity and portability.

### Assembly  
x86-64 implementation demonstrating low-level optimization and direct hardware control.

### WebAssembly
Portable module for web deployment, showcasing modern computational patterns.

## Build Requirements

- C: gcc/clang with math library
- Assembly: nasm, ld
- WebAssembly: wat2wasm

## Output

All implementations output (x,y) coordinate pairs to stdout, which can be visualized with tools like gnuplot or custom renderers.

## License

MIT License - see LICENSE file for details.
