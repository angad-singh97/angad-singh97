# Angad Singh | Systems Engineer

**Building at the Hardware-Software Boundary.**
Currently pursuing an MSCS at Stony Brook University, specializing in **High-Performance Networking**, **Kernel Bypass**, and **Computer Architecture**.

---

### 🔧 Core Engineering Focus
* **Systems Programming:** `C`, `C++20`, `RISC-V Assembly`, `SystemVerilog`
* **Networking:** `DPDK` (Poll Mode Drivers), `Kernel Bypass`, `TCP/IP Internals`, `Zero-Copy DMA`
* **Architecture:** `Cache Coherency (MESI)`, `Pipelining`, `Weak Memory Models`, `Branch Prediction`

---

### 🚀 Featured Research & Projects

#### [SBUnix — Coming Soon](https://compas.cs.stonybrook.edu/cse506-v3)
* **The Scope:** Full Unix-like OS from scratch — kernel, file system (TARFS), virtual memory, preemptive scheduling, COW fork(), and user-mode processes (ring 3).
* **The Stack:** Shell (SBUsh), init, syscalls (fork, execve, pipe, etc.), and libc (sblibc). Built in C and assembly.

#### [User-Space Networking on RISC-V (DPDK + F-Stack)](https://github.com/angad-singh97/riscv-network-stack)
* **The Challenge:** Bypassing the Linux Kernel on experimental RISC-V FPGA hardware to minimize packet processing latency.
* **The Engineering:**
    * Engineered a custom **Poll Mode Driver (PMD)** for a proprietary NIC.
    * Solved a hardware race condition caused by RISC-V's **Weak Memory Model** by injecting assembly `FENCE` instructions.
    * Implemented **Zero-Copy DMA** via Hugepages and `vfio-platform`.

#### [5-Stage Pipelined RISC-V Core](https://github.com/angad-singh97/riscv-core-verilog)
* **The Architecture:** RV64IM ISA implementation with a 5-stage pipeline (Fetch, Decode, Execute, Memory, Writeback).
* **The Optimization:** Implemented a **Data Forwarding Unit** to resolve RAW hazards without stalling and a **2-bit Dynamic Branch Predictor** to minimize control penalties.

#### [LuigiDB - Geo-Distributed Transaction Protocol](https://github.com/angad-singh97/luigi-db)
* Timestamp-ordered execution with a 2-WRTT commit bound; 30–60× higher throughput than OCC in multi-shard geo setups.
* Built on Mako (OSDI'25); TPC-C benchmarks on cloud infrastructure with simulated network latency.

#### [Raft Consensus in C++](https://github.com/angad-singh97/dslabs-cpp-angad-singh97)
* **The Scope:** Raft consensus protocol for a replicated state machine in a distributed systems framework (MIT 6.824–style lab).
* **The Engineering:** Implemented leader election with randomized timeouts, log replication via AppendEntries, and RPC handlers for RequestVote/AppendEntries. Thread-safe state machine with mutexes and atomic terms; all 8 correctness tests passing.

#### [Paxos-Based Distributed Transaction System](https://github.com/angad-singh97/paxos)
* **The Scope:** Fault-tolerant distributed bank using a modified Multi-Paxos protocol over gRPC across five replica servers. When a server lacks balance for a transaction, it runs a full consensus round to reconcile state, then applies the agreed transaction block.
* **The Engineering:** Implemented the full Paxos pipeline: extended Prepare/Promise with ballot codes for follower lag, proposer lag, and concurrent clashes; async consensus via `CompletableFuture` and gRPC deadlines; catch-up mechanism for lagging nodes; and a background transaction worker with retry logic. Designed Protobuf schemas for consensus and catch-up RPCs. Built in Java with Spring Boot and gRPC.
---

### 💼 Professional Experience
* **Veolia North America:** Building scalable cloud observability infrastructure (AWS/Java).
* **Volante Technologies:** Ex-Senior Software Engineer. Architected low-latency payment engines and led migration to Java 17.

---

[LinkedIn](https://www.linkedin.com/in/angad-sde-nyc) | [Email](mailto:angadsdenyc@gmail.com)
