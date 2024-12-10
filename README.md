**This is a stub for raising interest in the preliminary implementation of Buddelchip within the Chips JU A-IQ Ready project. More information will be available later, after corresponding scientific publications.**
 
 ---

**BuddelChip** is a SystemC/TLM2.0 framework to model different RISC-V systems. There are several RISC-V platform implementations of the same Instruction Set Architecture **(ISA)** but targeting different systems. 

The name **BuddelChip** is a play on words based on the art of crafting miniature ships inside glass bottles – commonly known as Buddelships. Building upon previous experiences in designing SoCRocket (Schuster, 2014), a SoC design framework for aerospace applications also used by the European Space Agency (ESA), BuddelChip adds several unique technical and quality-of-life features.

For convenience and as a starting point for new users, several popular open-source RISC-V cores are already included in the framework, such as the HiFive by Sifive and the ESP32-C2 by Espressif. Furthermore, integration with several FPGA platforms is also available, such as the very popular ChipYard by UC Berkley and Pulp by ETH Zürich. At the same time, any RISC-V core adhering to the RISC-V instruction set architecture (ISA) can be substituted. 

Beyond just the core, BuddelChip also models the most important peripherals such as general purpose input/output (GPIO) and the serial peripheral interface (SPI) bus, which are especially important for the simulation of micro controllers (MCUs). For running an OS on the simulated core, BuddelChip also supports the forwarding of systems calls through specially designed APIs.

Mayor usability improvements are achieved through the BuddelChip build system. It utilizes CMake for the environment configuration, Conan to handle external dependencies and Make as the actual build manager. BuddelChip is containerized to ensure compatibility with all operating systems. Different preconfigured containers are available including different tools for different purposes, for example the full RISC-V tool chain or even the Chipyard build environment. This is not to be confused with the architecture of the simulated system. The SystemC architecture contains all the models that in unison constitute the system and complements them by utilizing the equivalent hardware and analysis tools to refine the model until the behaviour is functionally and timing-wise equivalent. The Twinspace Load Profile Description Language (LPDL) additionally offers an interface to measure the load on the simulated hardware.

Most likely the biggest novelty achieved by BuddelChip is the addition of a Python API that enables accessing the inner workings of the simulation. This mainly alludes to directly querying parameters or hooking into callbacks. As these callbacks play a central role in SystemC, hooking into one effectively enables logging of arbitrary communications.
