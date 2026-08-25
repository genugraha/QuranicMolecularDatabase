# Qur'anic-Based Natural Compound Database

**A 3D-optimized, open-access molecular database of natural products explicitly mentioned in the Qur'an, curated for High-Throughput Virtual Screening (HTVS) and Computer-Aided Drug Discovery (CADD).**

![Open Access](https://img.shields.io/badge/Open%20Access-Yes-success)
![Format](https://img.shields.io/badge/Format-SDF%20%7C%20SMI%20-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## Overview
This repository contains a comprehensively curated, 3D-optimized molecular database of secondary metabolites derived from **32 botanical species explicitly mentioned in the Qur'an** (e.g., *Zingiber officinale*, *Nigella sativa*, *Olea europaea*, *Punica granatum*). It is designed to bridge historical-cultural knowledge with modern computational oncology and pharmacology by providing ready-to-use, energy-minimized ligand conformations for High-Throughput Virtual Screening (HTVS) and molecular docking campaigns.

## Dataset Curation Pipeline
The library was generated from an initial pool of 2,308 secondary metabolites and processed through a rigorous chemoinformatic pipeline:

1. **Compound Retrieval & Structural Curation:** Data extracted from the LOTUS database, followed by the elimination of broken/invalid structures, resulting in **2,301 valid bioactive compounds**.
2. **3D Conformational Optimization:** 3D structural generation and energy minimization executed within the **YASARA Structure** environment (YASARA2 force field, AMBER 14) to achieve thermodynamically stable conformations at physiological pH 7.4.
3. **Comprehensive ADMET Profiling:** Pharmacokinetic and toxicity predictions were evaluated using the **ADMETlab 3.0** machine-learning platform to ensure candidates possess favorable predicted safety profiles suitable for food therapeutic approaches.

## Repository Structure
The entire database is consolidated into a single archive: **`Natural Compound Quranic Database.rar`** (~10 MB). 

To facilitate ethnobotanical-specific research, the data inside the archive is systematically organized into **32 distinct folders** based on the botanical taxonomy (e.g., `Acacia_tortilis`, `Zingiber_officinale`). 

Inside each plant's specific directory, you will find:
*   `[Plant Name].sdf`: The aggregated 3D-energy minimized structural coordinates of all valid metabolites found in that specific plant.
*   `Screening [Plant Name].smi`: The 1D SMILES strings used for initial screening and property prediction.
*   `3D Optimization/`: A dedicated sub-folder containing the raw output logs and specific minimized coordinate geometries from the YASARA optimization cycle.

## How to Use
1. Download the **`Natural Compound Quranic Database.rar`** archive from the repository.
2. Extract the archive to your local directory. You will see 32 folders corresponding to each Qur'anic plant.
3. Navigate to your plant of interest.
4. The `.sdf` files can be directly imported into major molecular modeling and docking software (e.g., AutoDock Vina, AutoDock 4.2 LGA, YASARA, Discovery Studio, Schrödinger) for immediate virtual screening.

## Citation
If you utilize this database in your research, please cite our repository as follows:

> **Nugraha, G., Khanifah, F., Arifin, M.Z., Vaulina, E., & Delsy, Y. (2026).** *Qur'anic-Based Natural Compound Database for Virtual Screening in Computer-Aided Drug Discovery* [Dataset]. GitHub Repository. Available at: https://github.com/genugraha/QuranicMolecularDatabase

*(Note: A peer-reviewed methodological article detailing the construction of this database is currently under review).*

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
