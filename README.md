# Extract-precise-location-of-gimme-maelstrom-TF-motifs
The precise location of TF motifs is missing in gimme maelstrom TFBS outputs. This nextflow pipeline outputs the precise location of TF motifs.


### What files do I need? Follow this directory structure

├── beds \
│   ├── Ss1_12_dense.bed_Act_Enh_12StatesModel.bed \
│   ├── Ss2_12_dense.bed_Act_Enh_12StatesModel.bed \
│   ├── Ss3_12_dense.bed_Act_Enh_12StatesModel.bed \
│   ├── Ss4_12_dense.bed_Act_Enh_12StatesModel.bed \
│   └── Ss5_12_dense.bed_Act_Enh_12StatesModel.bed \
├── extract_motif_loc.nf \
├── gimmeScan_extract_motifs.R \
├── maelstrom_extract_motifs.R \
├── motif.nr.count.txt \
├── nonredundant.motifs.pfm

### How to run the pipeline

```ruby
nextflow run extract_motif_loc.nf 
```
Shouldn't take long to finish and you should see screen output of run summary as follows:
```ruby
N E X T F L O W  ~  version 22.10.6
Launching `extract_motif_loc.nf` [fabulous_brown] DSL2 - revision: 584add0944

======================================

.---..---.  .               .                
  |  |      |              _|_   o           
  |  |---   | .-.  .-. .-.  |    .  .-. .--. 
  |  |      |(   )(   (   ) |    | (   )|  | 
  '  '      `-`-'  `-' ` -'`-`-'-' `-`-' '  `-

======================================
[6e/f8eaa0] process > GIMME_SCAN (4)            [100%] 5 of 5 ✔
[88/c24f28] process > EXTRACT_GIMME (5)         [100%] 5 of 5 ✔
[2c/fea30a] process > EXTRACT_NR_MOTIFS         [100%] 1 of 1 ✔
[ff/8c03e6] process > INTERSECT (Ss3)           [100%] 5 of 5 ✔
[43/dfc688] process > MERGE (MZF1_intersected)  [100%] 182 of 182 ✔
```


