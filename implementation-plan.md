# Student-Dropout-Predictor

## Plan for SVM Classification Model – Student Dropout Dataset

### Repository Structure
- A folder containing the raw and processed data  
- A notebook for data cleaning and preparation
- A notebook for the linear SVM  
- A notebook for the kernel-based SVM  
- A notebook for the kernel-based SVM using scikit (for comparison with our own model)  

---

## 1. Data Preprocessing  
- Remove any non-ordinal (nominal) features  
- Convert the target variable into binary labels, either dropout vs. non-dropout or graduates vs non-graduates (depends on class proportions)
- Scale all features so they fall within the same range  

## 2. Linear SVM
- Split the dataset into 80% training and 20% testing
- Train a linear SVM trained with stochastic gradient descent and include a slack variable to allow for some misclassifications  
- Run five-fold cross-validation on the training data to evaluate performance and stability  
- Use statistical analysis to evaluate model performance

## 3. Kernel-based SVM  
- Train a non-linear SVM model using either a polynomial or RBF kernel  
- Perform grid search with a validation set to tune kernel parameters 
- Perform L1 or L2 regularization 
- Use log-loss to evaluate model performance (and optionally metrics like accuracy, precision, recall, F1 score, and confusion matrix )

## 4. Final Comparison and Analysis  
- Summarize the final results, model behaviors, and challenges encountered  
- Revisit any features that were previously excluded to see if they add value  
- Compare your models against scikit-learn’s built-in SVM for benchmarking and reference  

---

### Dataset  
UCI “Predict Students’ Dropout and Academic Success”  
https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success
