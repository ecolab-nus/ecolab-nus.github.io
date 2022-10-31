---
layout: post
title: Morpher Tutorial
---
![_config.yml]({{ site.baseurl }}/images/morpher.png)


## [Code Repo: https://github.com/ecolab-nus/morpher](https://github.com/ecolab-nus/morpher)

## Organizers

[Zhaoying Li](https://zhaoying-li.github.io), [Tulika Mitra](https://www.comp.nus.edu.sg/~tulika/) <br>
from _National University of Singapore_


## Introduction
Coarse-Grained Reconfigurable Architecture (CGRA) provides a promising pathway to scale the performance and energy efficiency of computing systems by accelerating the compute-intensive loop kernels. However, there exists no end-to-end open-source toolchain for CGRA, supporting architectural design space exploration, compilation, simulation, and FPGA emulation for real-world applications.  <br>
This hands-on tutorial presents Morpher, an open-source end-to-end compilation and simulation framework for CGRA, featuring state-of-the-art mappers, assisting in design space exploration, and enabling application-level testing of CGRA.  <br>
Morpher can take a real-world application with a compute-intensive kernel and a user-provided CGRA architecture as input, compile the kernel using different mapping methods, and automatically validate the compiled binaries through cycle-accurate simulation using test data extracted from the application.
Morpher can handle real-world application kernels without being limited to simple toy kernels through its feature-rich compiler. 
Morpher architecture description language allows users to easily specify a variety of architectural features such as complex interconnects, multi-hop routing, and memory organizations.

 <br> <br> <br>
<img src="https://ecolab-nus.github.io/images/morpher_framework.png" alt="drawing" width="700"/> \
<p style="text-align: center;">Fig.1 Morpher Framework</p>

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
    
    
# Related publications

[WOSET] [Morpher: An Open-Source Integrated Compilation and Simulation Framework for CGRA](https://www.comp.nus.edu.sg/~tulika/WOSET_MORPHER_2022.pdf)
        
[DAC] [PANORAMA: Divide-and-Conquer Approach for Mapping Complex Loop Kernels on CGRA](https://www.comp.nus.edu.sg/~tulika/DAC22.pdf)\
Dhananjaya Wijerathne, Zhaoying Li, Thilini Kaushalya Bandara, Tulika Mitra\
59th ACM/IEEE Design Automation Conference, 2022 __Publicity Paper__\
[Artifact Link](https://github.com/ecolab-nus/panorama)

[HPCA] [LISA: Graph Neural Network based Portable Mapping on Spatial Accelerators](https://www.comp.nus.edu.sg/~tulika/HPCA_LISA_2022.pdf)\
Zhaoying Li, Dan Wu, Dhananjaya Wijerathne, Tulika Mitra\
28th IEEE International Symposium on High-Performance Computer Architecture, 2022\
[Artifact Link](https://github.com/ecolab-nus/lisa) __Distinguished Artifact Award__

[ASPLOS] [REVAMP: A Systematic Framework for Heterogeneous CGRA Realization](https://www.comp.nus.edu.sg/~tulika/asplos22.pdf)\
Thilini Kaushalya Bandara, Dhananjaya Wijerathne, Tulika Mitra, Li-Shiuan Peh\
27th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, 2022\
[Artifact Link](https://zenodo.org/record/5848404#.YgyrPTFByUk)

[TCAD] [HiMap: Fast and Scalable High-Quality Mapping on CGRA via Hierarchical Abstraction](https://www.comp.nus.edu.sg/~tulika/HiMap-TCAD.pdf)\
Dhananjaya Wijerathne, Zhaoying Li, Anuj Pathania, Tulika Mitra, Lothar Thiele\
IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems, 41(10) 2022

[TCAD] [ChordMap: Automated Mapping of Streaming Applications onto CGRA](https://ieeexplore.ieee.org/document/9351547)\
Zhaoying Li, Dhananjaya Wijerathne, Xianzhang Chen, Anuj Pathania, Tulika Mitra\
IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems, 41(2) 2022

[Book Chapter] [Coarse-Grained Reconfigurable Array (CGRA)](https://www.comp.nus.edu.sg/~tulika/CGRA-Survey.pdf)\
Zhaoying Li, Dhananjaya Wĳerathne, Tulika Mitra\
Book chapter in “Handbook of Computer Architecture”, Springer (Invited)

[DATE] [HiMap: Fast and Scalable High-Quality Mapping on CGRA via Hierarchical Abstraction](https://www.comp.nus.edu.sg/~tulika/HiMap_DATE_2021.pdf)\
Dhananjaya Wijerathne, Zhaoying Li, Anuj Pathania, Tulika Mitra, Lothar Thiele\
Design Automation and Test in Europe 2021

[TECS] [CASCADE: High Throughput Data Streaming via Decoupled Access/Execute CGRA](https://www.comp.nus.edu.sg/~tulika/TECS-CASCADE19.pdf)\
Dhananjaya Wijerathne, Zhaoying Li, Manupa Karunaratne, Anuj Pathania, Tulika Mitra\
ACM Transactions on Embedded Computing Systems\
Special Issue on ACM/IEEE International Conference on Compilers, Architecture, and Synthesis for Embedded Systems 2019

[ICCAD] [4D-CGRA : Introducing the branch dimension to spatio-temporal application mapping of CGRAs](https://www.comp.nus.edu.sg/~tulika/4D-CGRA-ICCAD19.pdf)\
Manupa Karunaratne, Dhananjaya Wijerathne, Tulika Mitra, Li-Shiuan Peh\
38th ACM/IEEE International Conference on Computer Aided Design, November 2019

[A-SSCC] [HyCUBE: a 0.9V 26.4 MOPS/mW, 290 pJ/cycle, Power Efficient Accelerator for IoT Applications](https://www.comp.nus.edu.sg/~tulika/Hycube_for_ASSCC_2019.pdf)\
Bo Wang, Manupa Karunarathne, Aditi Kulkarni, Tulika Mitra, Li-Shiuan Peh\
IEEE Asian Solid-State Circuits Conference, November 2019

[DAC] [DNestMap : Mapping Deeply-Nested Loops on Ultra-Low Power CGRAs](https://www.comp.nus.edu.sg/~tulika/DAC18-CGRA.pdf)\
Manupa Karunaratne, Cheng Tan, Aditi Kulkarni, Tulika Mitra, Li-Shiuan Peh\
55th ACM/IEEE Design Automation Conference, June 2018

[DAC] [HyCUBE : A CGRA with Reconfigurable Single-cycle Multi-hop Interconnect](https://www.comp.nus.edu.sg/~tulika/DAC17.pdf)\
Manupa Karunaratne, Aditi Kulkarni, Tulika Mitra, Li-Shiuan Peh\
54th ACM/IEEE Design Automation Conference, June 2017

[ACM-TRETS] [Graph Minor Approach for Application Mapping on CGRAs](https://www.comp.nus.edu.sg/~tulika/TRETS14.pdf)\
Liang Chen, Tulika Mitra\
ACM Transactions on Reconfigurable Technology and Systems 2014

[FPT] Graph Minor Approach for Application Mapping on CGRAs [Much expanded journal version](https://www.comp.nus.edu.sg/~tulika/TRETS14.pdf)\
Liang Chen, Tulika Mitra\
International Conference on Field Programmable Technology, December 2012\
__Best Paper Award__
