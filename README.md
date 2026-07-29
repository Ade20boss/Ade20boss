# Adeoluwa Daniel Ademoye

Systems programmer working in C, from the layer beneath the frameworks — virtual machines, memory allocators, a neural-network engine built from scratch. Third-year physiotherapy student at the University of Lagos; everything here is self-taught, built because I wanted to know how the machine actually works, not because anyone assigned it.

📍 Lagos, Nigeria

### What I build

From-scratch, dependency-free C. I care about how memory is laid out, how bytes move on the wire, and how the machine executes them — so I build the engine rather than import one. Every project below carries a technical README that documents the design decisions and their tradeoffs, not just how to run it.

### Projects

**[Ghost VM](https://github.com/Ade20boss/ghost-vm)** — A stack-based bytecode virtual machine with its own binary network protocol. A five-kind typed object system, FNV-1a packet integrity, zero-copy parsing off a flexible-array-member wire format, and a strict manual-ownership memory model. Two independent layers — transport and execution — sharing nothing but a wire-format contract. Full design record in the README.

**[Kestrel](https://github.com/Ade20boss/kestrel)** — A single-header neural-network engine in C. Zero third-party dependencies, arena-backed memory, and zero heap allocation in the forward and training loops. Trains via finite-difference gradient descent today; backpropagation and a SIMD (AVX2 / NEON) backend are the mapped roadmap. The README is an honest design doc — including what isn't built yet.

**[fsplit](https://github.com/Ade20boss/fsplit)** — A dependency-free file splitter and assembler in C. Chunked 4 KB binary I/O, so it never loads the whole file into memory and handles multi-gigabyte inputs; byte-perfect reassembly; and fault-tolerant deferred cleanup that preserves the parts if a merge fails midway.

### Currently

- Building backpropagation into Kestrel, then taking it to MNIST.
- Working through CS fundamentals and the mathematics behind ML.
- Grinding data structures and algorithms in C.

### Tools

C, Python · GCC/Clang, GDB, Valgrind, Make, Git · Linux

### Contact

[LinkedIn](https://www.linkedin.com/in/daniel-ademoye-a05a56305)
