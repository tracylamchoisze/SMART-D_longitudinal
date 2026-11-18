# SMART-D_longitudinal Analysis
A set of scripts used to extract and analyze longitudinal resting-state functional connectivity (rsFC) data from the SMART-D clinical trial. 

These scripts examine neural changes following eight weeks of antidepressant treatment with sertraline or bupropion, focusing on connectivity between anterior cingulate cortex (ACC) subdivisions, hippocampal formation, and cortical regions, and their associations with clinical improvement.

### Seed Extraction Scripts (MATLAB/CONN)

These scripts extract seed-to-region functional connectivity measurements from preprocessed resting-state fMRI data using the CONN toolbox in MATLAB. Analyses focus on predefined seed regions based on the Human Connectome Project (HCP) multimodal parcellation.

Code includes:

- Defining ACC seed regions, including the subgenual ACC (sgACC; BA25), pregenual ACC (pgACC; a24 and p32), and dorsal ACC (dACC; p24 and a32pr)
- Defining hippocampal formation regions, including the presubiculum (PreS), entorhinal cortex (EC), perirhinal/ectorhinal cortex (PeEC), and hippocampus
- Extracting seed-to-region functional connectivity measurements across 360 cortical parcels defined by the HCP multimodal parcellation
- Averaging connectivity values across hippocampal formation subregions to derive composite connectivity measures
- Organizing participant-level connectivity measurements across baseline and post-treatment sessions for subsequent statistical analyses

### ACC_rsfc_SMART_final.Rmd (R)

This script analyzes longitudinal rsFC data from the SMART-D clinical trial to characterize treatment-related connectivity changes and investigate associations with antidepressant response, remission, and dimensional improvements in depressive symptoms. Statistical analyses primarily use linear mixed-effects models with participant-specific random intercepts, adjusting for age, sex, and mean framewise displacement.

Code includes:

- Combining, merging, and cleaning neuroimaging, clinical, and demographic datasets
- Descriptive statistics and participant characteristics
- Longitudinal rsFC analyses using linear mixed-effects models
- Treatment response and remission interaction analyses
- Associations between connectivity changes and percentage improvement in Montgomery–Åsberg Depression Rating Scale (MADRS) scores
- Post hoc comparisons using estimated marginal means
- Multiple-comparison correction using the false discovery rate (FDR) procedure, separately by seed and hemisphere
- Sensitivity analyses adjusting for antidepressant medication received and biomarker-based treatment assignment
- Fisher's exact and binomial tests examining the direction of connectivity changes
- Generation of manuscript figures, statistical summaries, and supplementary tables

