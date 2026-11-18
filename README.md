# SMART-D_longitudinal Analysis
Set of scripts to analyze the SMART-D longitudinal resting-state functional connectivity data

smart_rsfc_analysis.Rmd: This script analyzes resting-state functional connectivity (rsFC) data from the SMART-D clinical trial to examine neural changes following eight weeks of antidepressant treatment with sertraline or bupropion. The analyses investigate longitudinal changes in connectivity between anterior cingulate cortex (ACC) subdivisions, hippocampal formation, and cortical regions, as well as associations with treatment response, remission, and dimensional changes in depressive symptoms.

Code includes:
- Combining, merging, and cleaning neuroimaging, clinical, and demographic datasets
- Descriptive statistics and participant characteristics
- Longitudinal rsFC analyses using linear mixed-effects models
- Treatment response and remission interaction analyses
- Associations between connectivity changes and percentage improvement in MADRS scores
- Post hoc comparisons using estimated marginal means
- Multiple comparison correction using false discovery rate (FDR)
- Sensitivity analyses adjusting for antidepressant medication and biomarker-based treatment assignment
- Fisher's exact and binomial tests examining the direction of connectivity changes
- Generation of manuscript figures, statistical summaries, and supplementary tables
