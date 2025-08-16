# 📄 MLPayGrade – Project Report - 🔴 **Advanced Track**

Welcome to your personal project report!  
Use this file to answer the key reflection questions for each phase of the project. This report is designed to help you think like a data scientist, guide AI tools more effectively, and prepare for real-world job interviews.

---

## ✅ Week 1: Setup & Exploratory Data Analysis (EDA)

> Answer the EDA questions provided in the project materials here. Focus on data quality, trends, anomalies, and relationships.

### 🔑 Question 1: What roles or experience levels yield the highest average salary?

### 🔑 Question 2: Does remote work correlate with higher or lower salaries?

### 🔑 Question 3: Are there differences in salary based on company size or location?

### 🔑 Question 4: How consistent are salaries across similar job titles?

---

## ✅ Week 2: Feature Engineering & Data Preprocessing

#### 🔑 Question 1:
**Which categorical features are high-cardinality, and how will you encode them for use with embedding layers?**  

💡 **Hint:**  
Use `.nunique()` and `.value_counts()` to inspect cardinality.  
Use `LabelEncoder` or map categories to integer IDs.  
Think about issues like rare categories, overfitting, and embedding size selection.

✏️ *Your answer here...*

---

#### 🔑 Question 2:
**What numerical features in the dataset needed to be scaled before being input into a neural network, and what scaling method did you choose?**  

💡 **Hint:**  
Use `df.describe()` and histograms to evaluate spread and skew.  
Neural networks are sensitive to feature scale.  
Choose between `StandardScaler`, `MinMaxScaler`, or log-transform based on the data.

✏️ *Your answer here...*

---

#### 🔑 Question 3:
**Did you create any new features based on domain knowledge or data relationships? If yes, what are they and why might they help the model predict salary more accurately?**  

💡 **Hint:**  
Try combining features like `job_title + experience_level`, or flags like `is_remote = remote_ratio == 100`.  
Think like a recruiter: What drives salary changes?

✏️ *Your answer here...*

---

#### 🔑 Question 4:
**Which features, if any, did you choose to drop or simplify before modeling, and what was your justification?**  

💡 **Hint:**  
Drop features that are redundant, uninformative, or leak the target.  
Check for near-constant values or high missingness.  
Use `df.isna()`, `df.nunique()`, and correlation checks.

✏️ *Your answer here...*

---

#### 🔑 Question 5:
**After preprocessing, what does your final input schema look like (i.e., how many numerical features and how many categorical features)? Are there any imbalance or sparsity issues to be aware of?**  

💡 **Hint:**  
Print input shapes and schema after preprocessing.  
Use value counts and histograms to detect class imbalance or feature sparsity.  
This helps you reason about model convergence or need for regularization.

✏️ *Your answer here...*


---

### ✅ Week 3: Model Development & Experimentation

---

### 🔑 Question 1:
**What does your neural network architecture look like (input dimensions, hidden layers, activation functions, output layer), and why did you choose this structure?**  
🎯 *Purpose: Tests architectural understanding and reasoning behind model design.*

💡 **Hint:**  
Describe your FFNN: number of layers, units per layer, ReLU activations, batch normalization, dropout rates, etc.  
Explain why this architecture fits the tabular regression task (salary prediction).  
Include code and rationale for each component.

✏️ *Your answer here...*

---

### 🔑 Question 2:
**What loss function, optimizer, and evaluation metrics did you use during training? How did these choices influence your model’s learning behavior?**  
🎯 *Purpose: Tests knowledge of training dynamics and evaluation strategy.*

💡 **Hint:**  
Use MSE or MAE as loss (for regression), Adam or SGD as optimizer.  
Track RMSE, MAE, R².  
Reflect on how your metric trends evolved over epochs — was the model improving or plateauing?

✏️ *Your answer here...*

---

### 🔑 Question 3:
**How did your model perform on the training and validation sets across epochs, and what signs of overfitting or underfitting did you observe?**  
🎯 *Purpose: Tests ability to diagnose model behavior using learning curves.*

💡 **Hint:**  
Plot loss and metrics over time.  
Overfitting → validation error increases while training error decreases.  
Underfitting → both remain high.  
Include screenshots or plots and interpretation.

✏️ *Your answer here...*

---

### 🔑 Question 4:
**How did your deep learning model compare to a traditional baseline (e.g., Linear Regression or XGBoost), and what might explain the difference in performance?**  
🎯 *Purpose: Encourages comparative evaluation and model introspection.*

💡 **Hint:**  
Train a traditional model and compare RMSE, MAE, R².  
If the FFNN underperforms, discuss whether you need more tuning, more data, or regularization.  
If it outperforms, explain what complex patterns it likely captured.

✏️ *Your answer here...*

---

### 🔑 Question 5:
**What did you log with MLflow (e.g., architecture parameters, metrics, model versions), and how did tracking help guide your experimentation?**  
🎯 *Purpose: Tests reproducibility and experiment management awareness.*

💡 **Hint:**  
Track model depth, units, dropout rate, learning rate, validation scores.  
Show how MLflow helped you compare runs, spot trends, or pick the best model.  
Include run screenshots or output tables.

✏️ *Your answer here...*

---

## ✅ Week 4: Model Selection & Hyperparameter Tuning

### 🔑 Question 1:

**Which neural network architecture and hyperparameters did you experiment with, and how did you decide what to tune?**
🎯 *Purpose: Tests understanding of architectural design and tuning for tabular deep learning.*

💡 **Hint:**
Tuning ideas include: number of layers, neurons per layer, dropout rate, batch size, learning rate.
Justify choices based on previous results and known model behaviors.

✏️ *Your answer here...*

---

### 🔑 Question 2:

**What tuning strategy did you follow (manual, scheduler-based, Optuna, etc.) and how did it help refine your model?**
🎯 *Purpose: Evaluates ability to apply efficient search strategies for optimization.*

💡 **Hint:**
Manual tuning = more control but slower.
Optuna/RandomSearch = broader coverage.
Schedulers = dynamic adjustment during training.
Explain tradeoffs and justify your approach.

✏️ *Your answer here...*

---

### 🔑 Question 3:

**How did you monitor and evaluate the effect of tuning on model performance? Which metrics did you track and how did they change?**
🎯 *Purpose: Tests analytical thinking and metric interpretation skills.*

💡 **Hint:**
Track F1, MAE, RMSE, or R² across validation.
Use MLflow to visualize trends.
Mention learning curves, performance on different splits, and early stopping if used.

✏️ *Your answer here...*

---

### 🔑 Question 4:

**What did MLflow reveal about your tuning experiments, and how did it help in selecting your final model configuration?**
🎯 *Purpose: Encourages tool-based reflection on the model development process.*

💡 **Hint:**
Discuss MLflow runs, comparison plots, parameter filtering.
Explain how it saved time or revealed overlooked patterns.

✏️ *Your answer here...*

---

### 🔑 Question 5:

**What is your final model setup (architecture + hyperparameters), and why do you believe it’s the most generalizable?**
🎯 *Purpose: Tests ability to justify final model selection with evidence and insight.*

💡 **Hint:**
Include a summary of hyperparameters, loss function, optimizer.
Explain why this configuration balances performance and simplicity.
Support decision with validation performance and interpretability where possible.

✏️ *Your answer here...*

---


## ✅ Week 5: Model Deployment

### 🔑 Question 1:
**How did you architect the Streamlit app to support both model inference and explainability (e.g., SHAP visualizations)? What design decisions did you make to balance usability and technical depth?**
🎯 *Purpose: Tests ability to design advanced user interfaces for ML apps.*

💡 **Hint:**
Describe how you structured the app (e.g., tabs, sidebar, input forms, output panels).
Explain how you integrated model predictions and SHAP explanations.
Discuss tradeoffs between simplicity and providing detailed insights for advanced users.

✏️ *Your answer here...*

---

### 🔑 Question 2:
**Detail the steps you took to deploy your deep learning model and Streamlit app. What technical challenges did you face (e.g., model serialization, dependency management, cloud limits), and how did you resolve them?**
🎯 *Purpose: Evaluates practical deployment skills and troubleshooting with deep learning models.*

💡 **Hint:**
List steps for saving/loading the model, preparing requirements, and deploying to Streamlit Cloud or Hugging Face Spaces.
Mention issues with model size, inference speed, or library versions.
Explain how you debugged or optimized deployment.

✏️ *Your answer here...*

---

### 🔑 Question 3:
**How did you ensure your deployed app is robust, secure, and scalable for public use?**
🎯 *Purpose: Tests awareness of production-readiness, security, and reliability.*

💡 **Hint:**
Discuss input validation, error handling, and resource management.
Mention protecting sensitive data, limiting model exposure, and handling unexpected or malicious inputs.
Explain any monitoring or update strategies you implemented.

✏️ *Your answer here...*

---

### 🔑 Question 4:
**How would you communicate the app’s predictions and SHAP-based explanations to a non-technical stakeholder?**
🎯 *Purpose: Evaluates ability to bridge technical and non-technical audiences, especially with explainability tools.*

💡 **Hint:**
Describe how you’d explain what the prediction means and how SHAP values show feature impact.
Use analogies or simple visuals.
Address uncertainty and limitations in both prediction and explanation.

✏️ *Your answer here...*

---

### 🔑 Question 5:
**If you were to extend your deployed app, what advanced features or improvements would you add, and how would they benefit users or stakeholders?**
🎯 *Purpose: Tests product thinking and ability to iterate on advanced ML solutions.*

💡 **Hint:**
Suggest features like batch predictions, downloadable reports, user authentication, or real-time monitoring.
Discuss adding more interpretability tools, support for new data, or integration with business systems.
Explain the value these enhancements would provide.

✏️ *Your answer

## ✨ Final Reflections

> What did you learn from this project? What would you do differently next time? What did AI tools help you with the most?

✏️ *Your final thoughts here...*

---
