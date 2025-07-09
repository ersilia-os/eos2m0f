# Staphylococcus aureus activity prediction

Staphylococcus aureus activity prediction based on phenotypic ChEMBL data. Each column corresponds to a specific bioactivity dataset derived from ChEMBL, encompassing multiple assays and binarization cut-offs. The global consensus score summarizes the probability of being active. Model developed by Ersilia.

This model was incorporated on 2025-06-13.

## Information
### Identifiers
- **Ersilia Identifier:** `eos2m0f`
- **Slug:** `chembl-saureus`

### Domain
- **Task:** `Annotation`
- **Subtask:** `Activity prediction`
- **Biomedical Area:** `Antimicrobial resistance`
- **Target Organism:** `Staphylococcus aureus`
- **Tags:** `Antimicrobial activity`, `ChEMBL`, `ESKAPE`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `51`
- **Output Consistency:** `Fixed`
- **Interpretation:** The higher the probabilities and the global consensus scores, the more likely this compound is active against Staphylococcus aureus

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| 0_consensus_score | float | high | Consensus score among datasets |
| 1_assay_chembl4296184_inhibition_percentage_activity_percentile_10_organism_1 | float | high | Predicted probability of being active according to task 1_assay_chembl4296184_inhibition_percentage_activity_percentile_10_organism_1 |
| 1_assay_chembl4296184_inhibition_percentage_activity_percentile_1_organism_1 | float | high | Predicted probability of being active according to task 1_assay_chembl4296184_inhibition_percentage_activity_percentile_1_organism_1 |
| 1_assay_chembl4296184_inhibition_percentage_activity_percentile_25_organism_1 | float | high | Predicted probability of being active according to task 1_assay_chembl4296184_inhibition_percentage_activity_percentile_25_organism_1 |
| 1_assay_chembl4296184_inhibition_percentage_activity_percentile_5_organism_1 | float | high | Predicted probability of being active according to task 1_assay_chembl4296184_inhibition_percentage_activity_percentile_5_organism_1 |
| 1_assay_chembl4296184_mic_pchembl_percentile_25_organism_1 | float | high | Predicted probability of being active according to task 1_assay_chembl4296184_mic_pchembl_percentile_25_organism_1 |
| 1_assay_chembl4296184_mic_pchembl_value_6_organism_1 | float | high | Predicted probability of being active according to task 1_assay_chembl4296184_mic_pchembl_value_6_organism_1 |
| 1_assay_chembl4296184_mic_pchembl_value_7_organism_1 | float | high | Predicted probability of being active according to task 1_assay_chembl4296184_mic_pchembl_value_7_organism_1 |
| 1_assay_chembl4296192_inhibition_percentage_activity_percentile_25_organism_3 | float | high | Predicted probability of being active according to task 1_assay_chembl4296192_inhibition_percentage_activity_percentile_25_organism_3 |
| 2_target_chembl352_activity__percentage_activity_75_organism_2 | float | high | Predicted probability of being active according to task 2_target_chembl352_activity__percentage_activity_75_organism_2 |

_10 of 51 columns are shown_
### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos2m0f](https://hub.docker.com/r/ersiliaos/eos2m0f)
- **Docker Architecture:** `AMD64`, `ARM64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos2m0f.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos2m0f.zip)

### Resource Consumption
- **Model Size (Mb):** `867`
- **Environment Size (Mb):** `730`
- **Image Size (Mb):** `3245.43`

**Computational Performance (seconds):**
- 10 inputs: `37.2`
- 100 inputs: `27.54`
- 10000 inputs: `591.56`

### References
- **Source Code**: [None](None)
- **Publication**: [None](None)
- **Publication Type:** `Other`
- **Publication Year:** `2025`
- **Ersilia Contributor:** [arnaucoma24](https://github.com/arnaucoma24)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [GPL-3.0-only](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos2m0f
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos2m0f
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
