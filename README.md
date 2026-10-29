# energies-4693739-data
Data and code for the paper "Delayed Load Frequency Regulation via a Load-Disturbance-Integrated Integral Sliding Manifold" submitted to Energies.

This repository contains the Simulink models, MATLAB scripts, and datasets required to reproduce the simulation results presented in our paper submitted to ***Energies***.

##  Repository Structure

- **`1area/`**: Single-area power system simulations.
  - `Hinfsys.m`: MATLAB script for parameter initialization, preliminary calculations (including the PP scenario), and loading data into the Simulink model.
  - `HinfLFCnonlinear_controlled_sys.slx`: Simulink model containing the proposed controller scenarios and a comparative scenario (Hinf with parallel LDFF). The standalone Hinf case can be derived from this model.
- **`2area/`**: Two-area interconnected power system simulations.
  - `Hinf_2_SMC_f.m`: MATLAB script for parameter initialization and preliminary calculations.
  - `Sys.slx`: Simulink model representing the proposed controller integrated into the two-area system, including comparison scenarios matching the manuscript description.
  - `metrics summary.xlsx`: Excel file containing the manually recorded performance metrics for the two-area system simulations.
- **`Minimal dataset.zip`**: Compressed archive containing the **raw frequency deviation data (in `.csv` format)** exported directly from the Simulink simulations for both areas. This serves as the minimal raw dataset for evaluation.

##  Requirements
- **MATLAB** (Recommended version: R2024b or newer)
- **Simulink**

##  How to Run

**Important:** You must run the `.m` script to initialize the workspace parameters **BEFORE** opening or running the `.slx` model.

### For Single-Area System (1area)
1. Open MATLAB and navigate to the `1area` folder.
2. Run the script `Hinfsys.m`. This will calculate and load all necessary parameters (such as the PP scenario) into the MATLAB workspace.
3. Open the Simulink model `HinfLFCnonlinear_controlled_sys.slx`.
4. Run the simulation. 

### For Two-Area System (2area)
1. Open MATLAB and navigate to the `2area` folder.
2. Run the script `Hinf_2_SMC_f.m` to initialize parameters.
3. Open the Simulink model `Sys.slx`.
4. Run the simulation.

## 🎛️ Simulation Scenarios & Controls

The Simulink models are configured to simulate various conditions, including:
- **Step Changes:** SLD (Step Load Disturbance) and RSLD (Random Step Load Disturbance).
- **Cyber Attacks:** The controller input can be selected to simulate EA (Energy Attack), RA (Random Attack), and LA (Latency Attack) scenarios.

*(The specific configurations for these scenarios can be adjusted directly within the Simulink blocks.)*

##  License
- The **code** (`.m`, `.slx`) is released under the **MIT License**.
- The **data** (`metrics summary.xlsx`, `Minimal dataset.zip` / `.csv`) is released under the **CC0 1.0 Universal (Public Domain)** license.

## 📧 Contact
If you have any questions or encounter issues running the files, please contact:
- **[Tang Yicheng]**
- Email: [1229720076@qq.com]
