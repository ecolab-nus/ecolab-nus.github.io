---
layout: post
title: Morpher Tutorial
---

## Organizers

[Zhaoying Li](https://zhaoying-li.github.io), [Tulika Mitra](https://www.comp.nus.edu.sg/~tulika/)

![_config.yml]({{ site.baseurl }}/images/morpher.png)



## Introduction
Coarse-Grained Reconfigurable Architecture (CGRA) provides a promising pathway to scale the performance and energy efficiency of computing systems by accelerating the compute-intensive loop kernels. However, there exists no end-to-end open-source toolchain for CGRA, supporting architectural design space exploration, compilation, simulation, and FPGA emulation for real-world applications.  This hands-on tutorial presents Morpher, an open-source end-to-end compilation and simulation framework for CGRA, featuring state-of-the-art mappers, assisting in design space exploration, and enabling application-level testing of CGRA.
Morpher can take a real-world application with a compute-intensive kernel and a user-provided CGRA architecture as input, compile the kernel using different mapping methods, and automatically validate the compiled binaries through cycle-accurate simulation using test data extracted from the application.
Morpher can handle real-world application kernels without being limited to simple toy kernels through its feature-rich compiler.
Morpher architecture description language allows users to easily specify a variety of architectural features such as complex interconnects, multi-hop routing, and memory organizations.

![_config.yml]({{ site.baseurl }}/images/morpher_framework.png)

# Schedule
1. Introduction (30min)<br>
    a. The era of domain-specific ASIC Accelerators. <br>
    b. Software-defined hardware. <br>
    c. Morpher: an end-to-end CGRA toolchain.
1. CGRA Architecture (40min)<br>
    a. The diversity of CGRA architecture, including network,  configurability, memory access, and heterogeneity. <br>
    b. Modular CGRA Architecture: Processing Elements, Function Unit, and Datapath.  <br>
    c. An example to write your own CGRA specification: neighbor-to-neighbor network, and one-cycle multiple-hops network.
1. Application and Compilation Flow (30min)<br>
    a. Data-flow Graph Generation: how to annotate the target loop, and generate the corresponding operations for each instruction. <br>
    b. Hands-on Exercise: An example for microspeech application.
1. CGRA Mapper (30min)<br>
    a. Modulo Routing Resource Graph: time-extended resource graph of the hardware, and modulo scheduling. <br>
    b. Mapping of a DFG. We introduce three mappers: PathFinder, Simulated Annealing, and LISA (from HPCA 2022).
1. Simulator, FPGA Emulator, and SOC design (30min)<br>
    a. Binary Generation: the configuration bits for hardware <br>
    b. Cycle-accurate C++ simulator: data trace generation. <br>
    c. Data Transfer and FPGA Emulation: SPI data transfer and SOC emulation with FPGA.
