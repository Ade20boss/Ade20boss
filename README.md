# Adeoluwa Daniel Ademoye

**Systems Engineer | Computing Researcher | Runtime & ML Infrastructure**

📍 Lagos, Nigeria · [LinkedIn](https://www.linkedin.com/in/adeoluwa-ademoye-a05a56305)

I'm interested in what happens between the code we write and the machine that executes it: how instructions are interpreted, how memory is organized, how computational workloads interact with hardware, and why different implementations of the same computation can behave so differently.

My work focuses on systems programming, runtime architecture, numerical computing, compiler and virtual-machine design, and performance engineering.

Much of my computer science education has been self-directed. I learn by studying the underlying ideas, implementing them, questioning architectural decisions, and testing my understanding against actual system behavior.

## Selected Projects

### [Kestrel](https://github.com/Ade20boss/kestrel)
**C · Numerical Computing · Automatic Differentiation · Heterogeneous Execution · In Progress**

Kestrel is a neural-network library and hardware-aware computational runtime written in C. Its long-term objective is to make machine-learning computation more efficient across different hardware configurations, including consumer computing systems.

At its core, Kestrel brings together numerical computation, automatic differentiation, tensor infrastructure, memory management, and heterogeneous execution.

**Numerical and neural-network infrastructure**

The project began with neural-network implementations built from first principles, including regression, binary classification, and multilayer XOR networks.

Its numerical foundation encompasses multidimensional tensors, shape and stride metadata, typed numerical storage, aligned memory arenas, and tensor operations.

The automatic differentiation architecture uses computational graphs and reverse-mode differentiation to propagate and accumulate gradients. Numerical differentiation provides an independent reference for verifying analytical gradients.

**Hardware-aware execution architecture**

One of Kestrel's central engineering problems is understanding the relationship between a computational workload and the hardware available to execute it.

Its runtime architecture separates physical computing resources, execution devices, memory resources, and backend capabilities. A hardware-topology discovery system collects source-attributed observations, identity evidence, resource relationships, and locators, with reconciliation responsible for constructing a coherent representation of the machine.

This infrastructure forms the foundation for execution planning that considers computational requirements, hardware capabilities, memory placement, and backend availability.

**Heterogeneous computing and performance**

Kestrel's execution architecture encompasses scalar CPU computation, SIMD-accelerated numerical kernels, and GPU execution through CUDA, with hardware discovery and execution abstractions designed to support broader heterogeneous environments.

The performance work includes memory-locality optimization, cache-aware matrix multiplication, vectorized kernels, device-memory management, and controlled comparisons against established numerical libraries such as cuBLAS.

The larger research direction is to investigate how knowledge of a workload, the hardware, and the intervening software stack can inform more efficient execution decisions.

---

### [Ghost VM](https://github.com/Ade20boss/Ghost_VM)
**C · Virtual Machines · Compilers · Network Protocols · Runtime Systems · In Progress**

Ghost VM is a stack-based bytecode virtual machine exploring language implementation, instruction execution, memory representation, and the safe execution of bytecode received through a network protocol.

Unlike a standalone interpreter that executes only locally generated instructions, Ghost VM's architecture treats executable bytecode as potentially untrusted input.

**Bytecode execution and language implementation**

The virtual machine is built around a custom instruction set, a stack-based execution model, and runtime object representations supporting numerical values, strings, collections, and vector operations.

Its language architecture extends into a single-pass source compiler using lexical analysis and Pratt parsing, with bytecode generation for expressions, variables, control flow, functions, and local and global state.

The execution model includes call frames, operand-stack management, instruction-pointer control, and support for branching and function calls.

**Networked bytecode transport and validation**

Ghost VM includes a custom binary packet format supporting serialized instruction batches, packet metadata, and integrity checks.

The protocol architecture encompasses explicit byte ordering, versioned packet headers, bounded decoding, and TCP-based communication between clients and execution servers.

A central design principle is that bytecode must be validated before execution. This includes checking instruction operands, buffer boundaries, and control-flow targets to ensure that jumps cannot escape the bytecode region or land in the middle of encoded instructions.

Coverage-guided fuzzing, sanitizers, and malformed-input testing form part of the protocol and interpreter validation strategy.

**Memory management and interpreter optimization**

The runtime design explores NaN-boxed value representations, reducing unnecessary heap allocation, precise mark-and-sweep garbage collection, string interning, and efficient management of stack and heap objects.

On the execution side, Ghost VM investigates computed-goto instruction dispatch, constant folding, peephole optimization, and bytecode superinstructions.

An important part of this work is measuring the contribution of individual optimizations rather than assuming that a lower instruction count or a more compact representation necessarily produces better runtime performance.

Ghost VM is ultimately an exploration of the complete path from source-language constructs to compiled bytecode, validated transport, runtime execution, and performance optimization.

---

### [fsplit](https://github.com/Ade20boss/fsplit)
**C · Systems Programming · File I/O**

A dependency-free command-line utility for splitting large files into smaller binary chunks and assembling them back into the original file.

The implementation uses 4 KB buffered binary I/O, supports byte-perfect reassembly, and preserves source chunks if reconstruction fails.

The project explores low-level file handling, streaming data processing, error recovery, and reliable command-line utility design.

## Other Engineering Directions

My broader engineering interests also include build systems, distributed execution infrastructure, and mathematically grounded computational research.

**Raptor — Build Systems**

A C-based declarative build system designed around dependency graphs, content-based change detection, action hashing, incremental compilation, parallel scheduling, and content-addressed build caching.

Its central problem is determining which build actions actually need to execute, using dependency information and content hashes rather than relying exclusively on file modification times.

**Talon — Container Runtimes & Orchestration**

A container orchestration architecture in Go combining a distributed manager-worker control plane with an independent Linux container runtime.

The design covers OCI-compatible container execution, Linux namespaces, cgroups v2, filesystem isolation, container networking, scheduling, and Raft-based control-plane replication.

**EQUILIBRIUM — Computational Research**

A reproducible market-microstructure research environment combining a deterministic limit-order-book exchange in C with mathematical modeling and numerical experimentation in Python.

Its research scope includes execution optimization, statistical estimation, uncertainty quantification, portfolio allocation, sequential decision-making, and evaluating learned policies against analytical and numerical baselines.

The emphasis is on reproducible experiments, explicit mathematical assumptions, and results that can be independently checked.

## Engineering & Research

**Chief Technology Officer — Canopy**

Architect and implement backend services and subscription infrastructure using Python, FastAPI, PostgreSQL, and Supabase.

My responsibilities span API and service design, transactional database workflows, authentication and authorization, payment verification, subscription lifecycle management, and operational reliability.

**Head of Computing Research — Texyn Systems**

Lead investigations into computational performance and the interaction between workloads, hardware, and execution strategies.

My interests include compiler behavior, memory hierarchy, numerical performance, reproducible benchmarking, and workload-specific optimization.

**Open Source Contributor — Tracer OpenSRE**

Contributed to an AI-assisted incident investigation system, including a merged P0 security fix addressing the exposure of sensitive infrastructure identifiers in LLM prompts.

The change introduced masking at upstream processing boundaries and prompt construction to prevent raw identifiers from reaching the language model.

## Current Technical Focus

I'm concentrating my technical development around two complementary activities:

- **Kestrel:** Building computational infrastructure, with an emphasis on correctness, memory systems, hardware topology, and eventually hardware-aware execution.
- **Computer Systems:** Studying *Computer Systems: A Programmer's Perspective (CSAPP)* to strengthen my understanding of machine-level execution, memory hierarchy, linking, processes, and the hardware–software interface.

I also explore compiler construction and programming-language implementation out of curiosity.

## Tools & Technologies

**Languages:** C · Python · SQL

**Systems & Development:** Linux · GCC/Clang · GDB · Valgrind · Make · Git

**Backend:** FastAPI · PostgreSQL · Supabase

**Areas of Interest:** Computer Architecture · Runtime Systems · Numerical Computing · Compilers · Performance Engineering · Heterogeneous Computing

## Writing & Technical Explanations

I enjoy explaining difficult concepts by working through their underlying mechanisms and implementing them.

Through **Daniel Builds**, I share explanations, programming experiments, and explorations of computer science and machine learning.

🎥 [Daniel Builds — YouTube](https://www.youtube.com/@danielbuildsdev)

---

I'm interested in connecting with engineers and researchers working on systems programming, computer architecture, compilers, runtimes, and computational infrastructure.

**[Connect on LinkedIn](https://www.linkedin.com/in/adeoluwa-ademoye-a05a56305)**
