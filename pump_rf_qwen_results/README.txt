Qwen2.5-1.5B QLoRA + Random Forest feature audit

Base model: /kaggle/input/models/qwen-lm/qwen2.5/transformers/1.5b/1
Input CSV: /kaggle/input/datasets/nguyncngo/sensor-log/sensor_log.csv
Rows: 354
Scenario episodes used for group splitting: 45
Qwen selected features: ['soil_moisture_%', 'water_level_%', 'rain_level_%']
Qwen split sizes: train=226, validation=56, test=72

Files:
- rf_groupcv_ablation.csv
- rf_grouped_feature_importance.csv
- rf_groupcv_oof_predictions.csv
- rf_groupcv_fold_metrics.csv
- source_rule_ablation.csv
- sensor_target_correlations.csv
- qwen_rf_group_test_predictions.csv
- qwen_rf_group_test_metrics.json
- qwen_boundary_tests.csv
- rf_pump_final.joblib
- qwen_pump_lora/ (QLoRA adapter and tokenizer)

Important: the dataset is synthetic and source-rule agreement should be audited.
For physical pump actuation, use a deterministic controller and hardware safety
interlocks as the final authority. Qwen predictions are diagnostic/experimental.
