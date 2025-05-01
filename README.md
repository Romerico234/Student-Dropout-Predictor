# Student-Dropout-Predictor
## Plan for SVM Classification Model – Student Dropout Dataset
### Repository Structure:
-  Folder that contains unprocessed and processed data
-  Notebook for data preprocessing
-  Notebook for picking hyperparameters
-  Notebook for model training and evaluation
  
### 1. Data Preprocessing
- Remove non-ordinal features
- Apply 5-fold cross-validation to a linear SVM with arranged folds--use statiscal analysis to determine important features
- Convert labels to binary classification 
- Scale features so they are on the same range 

### 2. Model Construction
- Implement SVMs using Batch Gradient Descent with an 80/20 train-test split
- Select a kernel function (polynomial, rdf)
- Experiment with logistic regression as a baseline classifier
- Incorporate slack variables (handles any non-linearly separable data)

### 3. Model Evaluation
- Use R² score to measure the proportion of variance explained
- Explore additional evaluation metrics
- Check for overfitting by comparing train/test performance and analyzing learning curves.

### 4. Model Improvements
- Further splitting the training set into training/validation and apply grid search on hyperparameters --> Tune kernel parameters 
- Incorporate regularization (L1 or L2) 
- Adjust the slack variable
  
### 5. Final Comparison and Analysis
- Summarize final performance, challenges, and key takeaways
- Re-evaluate unused features to test their impact on model performance
- Compare with built-in SVM implementations for benchmarking
- Optionally implement the dual form of SVM using Lagrangian optimization for further insight

### Data Set: https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success
