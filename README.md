Implement RandomForestClassifier (advanced bagging) with hyperparameter tuning on same Iris CSV dataset
🏗️ Pipeline Architecture
CSV → pandas → LabelEncoder(y) → Pipeline → Prediction
                           ↓
              ├─ standard_scaler (StandardScaler)
              └─ RF (RandomForestClassifier)
🌳 Model Architecture
100 Decision Trees × Bagging + Feature Subsampling
Each tree: max_depth=5, ~31 nodes max
Total parameters learned: ~15,000 splits
OOB Score estimate: ~0.955 (internal validation)
**🔬 Key Technical Achievements
Pipeline Integration: standard_scaler → RF prevents data leakage

Production Naming: RF__max_depth prefix convention mastered

Visualization Complete:

Feature importance bar chart (day2_importance.png)

Single tree visualization (day2_tree_viz.png)

Model Persistence: iris_rf_pipeline_v2.pkl (joblib saved)**
