# geo_gse133997_tbi_mirna

# geo-gse133997-tbi-mirna
Time-dependent changes of rmTBI microglial exosome miRNA analysis + miRNet targets (3d, 14d)

## Dataset
- GEO Series: **GSE133997**
- Platform: **GPL21265** 
- Contrast: **exosome_rmTBI_3d vs exosome_control**
- Sample size: control **n=3**, rmTBI_3d **n=3**
- Mus musculus
- Exosomal miRNA

### Samples used in this repo
**Control (exosome_control)**
- GSM3932557 — exosome_control_rep1
- GSM3932558 — exosome_control_rep2
- GSM3932559 — exosome_control_rep3

**rmTBI 3d (exosome_rmTBI_3d)**
- GSM3932560 — exosome_rmTBI_3d_rep1
- GSM3932561 — exosome_rmTBI_3d_rep2
- GSM3932562 — exosome_rmTBI_3d_rep3

**rmTBI 14d (exosome_rmTBI_14d)**
- GSM3932563 — exosome_rmTBI_14d_rep1
- GSM3932564 — exosome_rmTBI_14d_rep2
- GSM3932565 — exosome_rmTBI_14d_rep3

## Methods overview
### Differential expression (R / limma)
- R + **limma**
- Preprocessing/normalization: `[background correction + normalizeBetweenArrays]`
- Thresholds used for exporting up/down miRNA lists:
  - **adj.P.Val < 0.05**
  - **|logFC| ≥ 1**

### Target genes (miRNet)
- Input: up-/down-regulated miRNA lists exported from limma
- Databases: **TarBase v8.0**, **miRTarBase v8.0**
- miRNet exports (targets tables) are saved under: `mirnet/exports/`

---
