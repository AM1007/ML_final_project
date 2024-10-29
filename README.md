# ML_final_project

The dataset for research and model training contains 10,000 entries. There are a total of 230 features, of which the first 190 are numerical, and the remainder are categorical. Your task is binary classification, with the target variable labeled as y.

You will need the following files, which can be found on the competition page as well as in the repository:

final_proj_data.csv - the training dataset
final_proj_test.csv - the validation dataset
final_proj_sample_submission.csv - a sample file for submitting predictions in the correct format

### Useful Tips for Participating in the Competition

1. Carefully analyze the dataset.

2. Identify feature types and check for missing values.

3. Consider whether to impute missing data and assess if features with missing values are worth using.

4. Count the number of unique categories for categorical features and select an optimal encoding method.

5. Evaluate the class distribution in the dataset and decide if balancing is necessary, and if so, how best to approach it.

6. Depending on the chosen prediction algorithm, assess whether feature normalization is required.

7. Conduct experiments with dimensionality reduction and compare the accuracy of predictions.

8. When needed, test different algorithms/ensembles of models and tune their hyperparameters.

9. For objective prediction assessment, try building an ML pipeline and performing cross-validation. If you decide to balance classes using the imblearn package, note that the Pipeline object allows you to integrate the class balancing step directly into the ML pipeline.

10. Before generating predictions for the validation set, retrain (or fine-tune) your final model on all available data (both training and test datasets).

11. Prepare a .csv file in which, for each client identifier in the validation set (column index), you indicate the predicted value of the target variable y.

12. The file should include headers and follow this format:

```python
index,y
0,0
1,0
2,1
3,0
4,0
5,0
...
```

After submitting the file with predictions and calculating the competition metric, consider ways to improve your results and continue experimenting to boost the metric.
