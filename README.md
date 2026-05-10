# Dissertation_ExplainableAI
# Research so far
* [Intro from documentation](./https://shap.readthedocs.io/en/latest/overviews.html)
* [SHAP Interpretations Depend on Background Data](./https://mindfulmodeler.substack.com/p/shap-interpretations-depend-on-background)
*

jupyter nbconvert --to script *.ipynb --stdout | grep "^# ##"
📄 cardio_train_data_preprocessing.ipynb
  ↳ Data description
  ↳ Gender based Histograms to see more imbalance
  ↳ Different Feature combinations
📁 config
  📄 dataset_split_sizes.json
📄 cvd_fairness_analysis.ipynb
  ↳ CVD Fairness Analysis — XGBoost Baseline
  ↳ 1. Imports
  ↳ 2. Load Model & Test Data
  ↳ 3. Fairness Metrics (EOD & Disparate Impact)
  ↳ 4. Define Prediction Groups
  ↳ 5. Feature Summary: FN vs TP (Women & Men)
  ↳ 6. SHAP Setup & Group-Level Analysis (Women)
  ↳ 7. Most Common Negative SHAP Driver in FN Women
  ↳ 8. Mean SHAP Bar Chart: FN Women
  ↳ 9. SHAP Dependence: Systolic BP (Women & Men)
  ↳ 10. KDE Distributions: FN vs TP (Women & Men)
  ↳ 11. KDE: TN vs FN — Age & Systolic BP (Women & Men)
  ↳ 12. Violin Plots: TN vs FN Women
  ↳ 13. Categorical Feature Distributions: TN vs FN Women
  ↳ 14. TN Women — Clinical Risk Zone Analysis
  ↳ 15. SHAP Waterfall: FN Woman vs Nearest Matched Male
  ↳ 16. SHAP Counterfactual: Gender Swap
📁 data
  📁 preprocessing_notebooks
    📄 01_data_preprocessing.ipynb
      ↳ Data Preprocessing
      ↳ Dataset Description
      ↳ 1. Imports and Paths
      ↳ 2. Load Raw Data and Recode Gender
      ↳ 3. Age Conversion and BMI
      ↳ 4. Identify Implausible Values
      ↳ 5. Apply Filters
      ↳ 6. Validate Cleaning Preserved Key Distributions
      ↳ 7. Save Cleaned Dataset
      ↳ 7. Distribution Table — Before and After Cleaning
    📄 02_eda.ipynb
      ↳ Exploratory Data Analysis
      ↳ 1. Imports and Paths
      ↳ 2. Feature Distributions by Sex
      ↳ 3. Sex-Stratified Categorical Feature Rates
      ↳ 4. CVD Rate by Sex
      ↳ 5. Feature Correlation Matrix
      ↳ 6. Systolic BP Distribution by Sex
      ↳ 7. Feature Correlation with CVD Outcome
      ↳ 8. Smoking, Sex, and CVD
  📁 processed
    📄 cardio_baseline_clean.csv
  📁 raw
    📄 cardio_train.csv
  📁 test_train_val_sets
    📄 cardio_baseline_test.csv
    📄 cardio_baseline_train.csv
    📄 cardio_baseline_val.csv
    📄 cardio_fe_test.csv
    📄 cardio_fe_train.csv
    📄 cardio_fe_val.csv
    📄 cardio_fe_{split}.csv
📄 feature_correlations.ipynb
📁 Framigham_stuff
  📄 data_preprocessing.ipynb
    ↳ Outliers
    ↳ Class weights
    ↳ training model
    ↳ Grid search approach omg
  📄 FalseNegative_Evaluation.ipynb
    ↳ Raw values : FN vs TP women
  📄 Framigham_model_metrics.ipynb
  📄 framingham.csv
📄 generate_str.ipynb
📁 models
  📁 baseline_models
    📄 cardio_xgb_baseline_model.pkl
  📄 models.ipynb
    ↳ Dataset Split Overview
    ↳ Train models
    ↳ Using monotonic clipping on ap_hi
  📁 models_cleaned_notebooks
    📄 baseline_model.ipynb
      ↳ 1. Data Splitting
      ↳ 2. Split Validation Table
      ↳ 3. Prepare Features and Labels
    📄 model_evaluation.ipynb
    📄 model_refinement.ipynb
  📁 refined_models
    📄 cardio_xgb_constrained.pkl
    📄 cardio_xgb_fe.pkl
    📄 cardio_xgb_monotone.pkl
    📄 cardio_xgb_tuned.pkl
    📄 cardio_xgb_weighted.pkl
📁 outputs
  📁 eda
    📄 correlation_heatmap.png
    📄 cvd_rate_by_sex.png
    📄 distributions_by_sex.png
    📄 feature_target_correlation.png
    📄 kde_ap_hi_by_sex.png
    📄 scatter_ap_hi_ap_lo.png
    📄 split_validation_table.png
  📁 fairness
    📄 fairness_metrics_summary.csv
  📁 models
    📄 calibration_by_sex.png
    📄 shap_global_model_comparison.png
    📄 split_validation_table.png
  📁 preprocessing
    📄 distribution_table.png
    📄 validation_loss_curve.png
  📁 shap
    📄 clinical_benchmarking_summary.csv
    📄 fn_rate_by_bp_bin_female.csv
    📄 pdp_age_years_sex_stratified.png
    📄 pdp_ap_hi_sex_stratified.png
    📄 shap_base_value.npy
    📄 shap_bin_summary_age_years.csv
    📄 shap_bin_summary_ap_hi.csv
    📄 shap_counterfactual_gender_swap.png
    📄 shap_dependence_age_years_sex_stratified.png
    📄 shap_dependence_ap_hi_fn_vs_tp.png
    📄 shap_dependence_ap_hi_interaction.png
    📄 shap_dependence_ap_hi_sex_stratified.png
    📄 shap_dependence_ap_lo_sex_stratified.png
    📄 shap_dependence_cholesterol_sex_stratified.png
    📄 shap_dependence_gluc_sex_stratified.png
    📄 shap_dependence_weight_sex_stratified.png
    📄 shap_fn_vs_tp_women_comparison.csv
    📄 shap_mean_bar_fn_women.png
    📄 shap_summary_bar_full.png
    📄 shap_summary_bar_sex_stratified.png
    📄 shap_summary_dot_full.png
    📄 shap_summary_dot_sex_stratified.png
    📄 shap_underresponse_flag_table.csv
    📄 shap_values_baseline_female.npy
    📄 shap_values_baseline_full.npy
    📄 shap_values_baseline_male.npy
    📄 shap_waterfall_fn_woman_vs_matched_male.png
📄 README.md
📄 Resources.md
📁 SHAP_fairness_notebooks
  📄 fairness_evaluation.ipynb
    ↳ Fairness Evaluation
    ↳ 1. Imports
    ↳ 2. Paths and Constants
    ↳ 3. Sanity Checks
    ↳ 4. Sex Masks and Subgroup Splits
    ↳ 5. Helper: get_rates
    ↳ 6. Formal Fairness Metrics
  📄 shap_01_global_validation.ipynb
    ↳ SHAP Global Validation & Feature Importance
    ↳ 1. Imports
    ↳ 2. Paths & Constants
    ↳ 3. Notebook Sanity Checks
    ↳ 4. Build Sex Masks & Subgroup Splits
    ↳ 5. SHAP Explainer Setup & Additivity Validation
    ↳ 6. Sex-Stratified SHAP Computation
    ↳ 7. Global Summary Plots — Full Test Set
    ↳ 8. Sex-Stratified Summary Plots
    ↳ 9. SHAP Dependence Plots — 6 Features, Sex-Stratified
    ↳ 10. `ap_hi` Interaction-Coloured Dependence
    ↳ 11. Partial Dependence Plots — `ap_hi` and `age_years`
    ↳ 12. SHAP Response to Systolic BP by Bin — Female Patients
    ↳ 13. SHAP Response by BP and Age Bin — Female vs Male
    ↳ 14. NB1 Output Summary
  📄 shap_02_local_subgroup_benchmarking.ipynb
    ↳ SHAP Local Explanations & Clinical Benchmarking
    ↳ 1. Imports
    ↳ 2. Paths and Constants
    ↳ 3. Sanity Checks
    ↳ 4. Build Prediction Groups
    ↳ 5. SHAP Comparison: FN vs TP Women
    ↳ 6. Mean SHAP Bar Chart — FN Women
    ↳ 7. Most Common Negative SHAP Driver — FN Women
    ↳ 8. SHAP Dependence: ap_hi — TP vs FN Women and Men
    ↳ 9. SHAP Waterfall — FN Woman vs Nearest Matched Male
    ↳ 10. Counterfactual — Gender Swap
    ↳ 11. Clinical Benchmarking Summary
    ↳ 12. NB2 Output Summary
📄 Shap_implementation.ipynb
  ↳ Sex-Stratified SHAP now
  ↳ The ap_hi dependence plot
📁 SHAP_intro
  📄 intro_Shap.ipynb
    ↳ Dataset : California Housing
    ↳ Model Coefficients
    ↳ Partial dependence plots
📄 visualisation.ipynb