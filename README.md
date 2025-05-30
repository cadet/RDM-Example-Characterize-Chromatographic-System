# Characterization of Chromatographic Systems in CADET

This repository contains example simulations demonstrating the workflow for characterizing chromatographic systems using **CADET-Process** and **CADET-RDM**. The steps required to model a chromatographic system are outlined, including how to fit the model to experimental data. The characterization of the system periphery, such as tubing and valves, is not yet included in this example. The following objectives are examined: 

* Fit Column Transport Parameters - ` column_transport_parameters.py` <br>
A system with a non-binding, non-pore-penetrating tracer is simulated using the **Lumped Rate Model With Pores** unit operation model to optimize the parameters: **Bed porosity** and **Axial Dispersion**  

* Fit Pore Transport Parameters - `pore_transport.py` <br>
A system with a non-binding, pore-penetrating tracer is simulated using the **Lumped Rate Model with Pores** unit operation model to optimize the parameters: **Particle porosity** and **Film diffusion** 

* Fit Binding Model Parameters - `binding_model_parameters.py` <br>
A system with a pore-penetrating tracer is simulated using the **Lumped Rate Model with Pores** unit operation model to estimate **Steric Mass Action (SMA)** binding parameters based on multiple **gradient elution** chromatograms. 


---

## Authors

* Johannes Schmölder
* Katharina Paul
* Ronald Jäpel
* Hannah Lanzrath

---

## Running the Example Simulation

1. Clone this repository.
2. Set up the environment using the `environment.yml` file.
3. Run the simulation:

   ```bash
   python main.py
   ```

The results will be stored in the `src` folder inside the `output` directory.

> **Note**: Running `cadet-rdm` requires [**Git LFS**](https://git-lfs.com/), which needs to be installed separately.
>
> * **Ubuntu/Debian**:
>
>   ```bash
>   sudo apt-get install git-lfs
>   git lfs install
>   ```
>
> * **macOS** (with Homebrew):
>
>   ```bash
>   brew install git-lfs
>   git lfs install
>   ```
>
> * **Windows**:
>   Download and install from [https://git-lfs.com](https://git-lfs.com)

---

## Output Repository

The output data for this case study can be found here:<br>
[Link to Output Repository](https://github.com/cadet/RDM-Example-Characterize-Chromatographic-System-Output)
