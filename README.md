#  Semiconductor Packaging: From Basics to 3D Integration

This repository documents the key technical content from a comprehensive semiconductor packaging workshop. It covers the evolution, types, integration strategies, manufacturing flows, and simulation methods used in modern chip packaging — from wire bonding to full 3D TSV-based systems.

---

##  1. The Role and Evolution of Semiconductor Packaging

Semiconductor packaging transforms fragile silicon dies from foundries (TSMC, Intel, Samsung, Micron, SK Hynix) into robust, electrically connected, and thermally managed components.

### Key Functions:
- **Protection:** Guards against moisture, corrosion, and mechanical damage.
- **Electrical Bridging:** Connects die-to-board and die-to-die signals.
- **Thermal Management:** Dissipates heat from high-power chips.
- **Mechanical Integrity:** Enables surface mount compatibility.

---

##  2. Types of Packages and Selection Criteria

###  Foundational Package Structure

| Layer                         | Description                                              |
|------------------------------|----------------------------------------------------------|
| Mold Compound                | Encapsulation against environment                        |
| Die (Chip)                   | Executes logic/memory functions                          |
| Die-to-Carrier Interconnects | Wire bonds or flip-chip bumps                            |
| Carrier (Substrate)          | Signal routing & mechanical support                      |
| Carrier-to-Board Interconnects | Solder balls, pins                                      |
| System Board (PCB)           | Integration of multiple packages                         |

###  Carrier Material Options

| Material    | Characteristics                        | Usage                      |
|------------|------------------------------------------|----------------------------|
| Leadframe  | Metal-based, cost-effective             | Discrete ICs               |
| Laminate   | Copper routing, flexible                | Consumer electronics       |
| Ceramic    | Thermally/electrically superior         | Military, aerospace        |
| Silicon    | High-precision, TSV-compatible          | 2.5D/3D integration        |
| Glass      | High-density routing                    | Emerging tech              |

###  Mounting/Package Types

| Technology       | Package Type     | Use Case                          |
|------------------|------------------|-----------------------------------|
| Through-hole     | DIP, SIP, PGA     | Legacy, large ICs                 |
| Surface Mount    | SOIC, QFP, QFN    | Analog, digital, RF               |
| Advanced         | FC-BGA, CSP, SiP  | SoCs, CPUs, chiplets              |

 **Examples**:
- **CoWoS (NVIDIA GP100)** – Chip-on-Wafer-on-Substrate for AI workloads  
- **PoP (Qualcomm, Samsung)** – Package-on-Package for compact mobile SoCs

---

##  3. Advanced Packaging and Dimensional Integration

###  Classification

- **2D**: Single die on substrate  
- **2.1D/2.3D**: Redistribution & stacked passives  
- **2.5D**: Dies on interposer (TSV-enabled)  
- **3D**: Full vertical die stacking with TSVs  

###  Interconnect Techniques

- **RDL (Redistribution Layer)**: Metal layers to re-route I/O
- **Fan-In WLP**: Bumps stay within die footprint
- **Fan-Out WLP**: Reconstituted dies with extended I/O area
- **Flip-Chip**: Die flipped onto substrate using solder bumps
- **TSV (Through-Silicon Via)**: Vertical inter-die connections for 3D stacking

---

##  4. Semiconductor Supply Chain & ATMP Process

###  Stages:
- **Design**: Fabless design (e.g., NVIDIA, AMD)  
- **Wafer Fab**: Foundries (e.g., TSMC, Intel)  
- **ATMP**: OSATs (e.g., ASE, Amkor) handle packaging & testing  
- **Board Assembly**: ICs mounted to PCBs via SMT  
- **Product Assembly**: Final systems (phones, servers, etc.)

###  ATMP Facility Layout

- **Offices**: QA, engineering  
- **Material Storage**: Die, epoxy, substrates  
- **Cleanroom**: Die attach, molding, flip-chip bonding  
- **Test Area**: Burn-in, E-test, functional test  
- **Warehouse**: Final-packaged chips  
- **Maintenance**: HVAC, safety systems

---

##  5. Manufacturing Flow: From Wafer to Package

###  Key Steps

- **Pre-Prep**: Lamination, back-grinding, dicing  
- **Die Attach**: Die bonded to substrate with epoxy  
- **Curing**: Adhesive hardening  
- **Wire Bonding**: Gold/Cu wire loop bonded  
- **Singulation**: Sawed into individual packages  
- **Molding**: Epoxy encapsulation  
- **Marking**: Laser labeling

###  Flip-Chip Flow

- Bump Formation → Die Placement → Reflow Solder → Underfill → Mold/Mark

###  WLP (Wafer-Level Packaging)

- **Fan-In**: Within die  
- **Fan-Out**: RDL beyond die boundary

---

##  6. Reliability and Testing

###  Test Flows

- **Wafer Probe**
- **Package Electrical Test**
- **Burn-In Test** (High T/V stress)
- **Final System-Level Test**

###  Burn-In Failure Curve

| Phase           | Description                                 |
|------------------|---------------------------------------------|
| Infant Mortality | Caught early via burn-in                   |
| Useful Life      | Stable performance                         |
| Wear-Out         | Aging, degradation phase                   |

---

##  7. Package Design and Simulation (ANSYS AEDT)

**Modeled Example:**
- Die: 3 × 3 × 0.2 mm  
- Substrate: 5 × 5 × 0.5 mm  
- Die Attach: 0.1 mm  
- Mold Compound: 1.2 mm Epoxy-Kevlar  
- Bond Wires: Gold (JEDEC 4-point profile)

###  Simulation Steps:
1. Define geometry of each layer  
2. Assign electrical/thermal properties  
3. Add bond wires & encapsulation  
4. Run electrical & thermal simulations  

---

## References
- Episode1(https://news.skhynix.com/semiconductor-back-end-process-episode-1-understanding-semiconductor-testing/)
- Episode2(https://news.skhynix.com/semiconductor-back-end-process-episode-2-semiconductor-packaging/)
- Episode3(https://news.skhynix.com/semiconductor-back-end-process-episode-3-understanding-the-different-types-of-semiconductor-packages/)
- Episode4(https://news.skhynix.com/semiconductor-back-end-process-episode-4-packages-part-2/)
- Episode5(https://news.skhynix.com/semiconductor-back-end-process-episode-5-package-design-and-analysis/)

## Acknowledgement
- [Kunal Ghosh](https://github.com/kunalg123)

- [Tarun Agarwal-Professor-IIT Gandhinagar](https://iitgn.ac.in/faculty/ee/fac-tarun)

- [Abhimanyu Singh](https://www.linkedin.com/in/abhimanyu-singh-633737a/)




