# Week 2 - Halfday 3

## Missions & Activities:

### Activity 1 – ~30 minutes
- **Peer Review and Validation of Data Analysis (Halfday 2)**: Work in pairs to review and compare your code and results. Exchange the outcome of the previous activity and discuss your approach. Write together 1-2 slides with a list of the key-differences concerning:
    - The result you had
    - The method you used to get to that results
- **Consolidation by the Professor**: After peer review, the professor will provide further clarification and consolidation of the concepts.

### Activity 2
- **Problem**: Discover and implement Decision Trees.
- **Hints**: [Write a Decision Tree Classifier from Scratch](https://www.youtube.com/watch?v=LDRbO9a6XPU).
- **Tools**: scikit-learn, [classification_report — scikit-learn 1.5.1 documentation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)
- **New/Consolidation of ML Glossary**: K-NN, Decision Tree, Gini impurity, Information gain, Grid search (model tuning/selection), k-fold cross-validation, Learning curve, Confusion matrix, Accuracy, Precision, F1 score, Sensitivity (a.k.a. recall), Specificity

## Expected Outcomes:
- **Slides**: Prepare 3-5 slides to present Gini impurity and information gain for decision trees. Provide an example (e.g., toy dataset, not necessarly the Titanic dataset, and show how to use Gini impurity and information gain to evaluate the qualit of a "split").
- **Notebook**: Continue your previous Jupyter notebook to integrate the tasks and explanations outlined below. Provide direct answers to **all** the questions listed below (Section [Questions](#questions)).

## Tasks – Classification (Decision Tree)
0. Copy & Paste your notebook (the .ipynb file) from the previous part in this folder.
    In the terminal, `cd` to the project folder and run the following instructions:

     ```bash
        pip install poetry
        poetry install
    ```
1. **Implement a quick&dirty K-NN classifier**
   - use the [K-NN](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html) implementation on scikit-learn: 
   - try different values of `K`using [grid search](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
2. **Learn the Basics of Decision Tree (DT) Classification**:
   - Compute Gini impurity by hand on a small dataset for a classification problem (show what you did in your sildes).
   - Compute information gain by hand on a small dataset for a classification problem (show what you did in your sildes).
3. **Implement DT Classification Using scikit-learn on the Titanic Dataset**:
   - Understand the hyperparameters needed for a [DT Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html#sklearn.tree.DecisionTreeClassifier)
   - Find the best hyperparameters for DT using *grid search* and/or *random search* along with k-fold cross-validation.

4. **Evaluate the Performance on a Test Set**:
   - Analyze the Confusion matrix, accuracy, precision, and F1-score.
   - Print the learning curve.

## Questions:
- **[In the Slides]** Present a step-by-step approach to implementing a Decision Tree (DT):
    - How is Gini impurity used? What does it represent?
    - How is information gain used? What does it represent?
    - Are there alternatives to these metrics? (e.g., entropy)
    - Check the file "Question Decision Tree". You will have a similar question in the evaluation at the end of the week ;-)
- **[In the Jupyter notebook]**
    - What are the hyperparameters of a Decision Tree? What do they represent?
    - How can you use k-fold cross-validation to select the best hyperparameters?
    - What is the difference between grid search and random search? Advantages and disadvantages?
    - How can the learning curve help you understand if your model is overfitting or underfitting the data? What are possible solutions when using a decision tree? **Hint**: which hyperparameter(s) should you change to increase/decrease the probability to get overfitting? 
    - What is a confusion matrix for a 2-class problem? How does it differ for a multiclass problem?