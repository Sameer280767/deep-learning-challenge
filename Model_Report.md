# Overview of the analysis:

## Purpose of the analysis

 - The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures

  - I have used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup

   - The analysis then attempts to incresae the accuracy of the model built by using different scenarios

# Results:

## Data Preprocessing

- Target variable: 'IS_SUCCESSFUL' column from application_df

- Feature variables: all other columns from application_df --> these were defined by dropping the 'IS_SUCCESSFUL' column from the original dataframe

 - Variables removed: 'EIN' and 'NAME' columns were dropped/removed, because they were neither targets nor features for the dataset


## Compiling, Training, and Evaluating the Model*

### Base scenario: Accuracy - 73.2%
 - I used 8 hidden_nodes_layer1 and 5 hidden_nodes_layer2
 - No. of neurons were selected to try and avoid underfitting or overfitting
 - 2 hidden layers were selected as a starting point
 - Activation functions of ReLU and sigmoid were used. ReLU was used for hidden layers and sigmoid was used for output layer
 - ReLU (Rectified Linear Unit) is a popular choice for hidden layers due to its simplicity and effectiveness in preventing vanishing gradients
 - Sigmoid is useful for output layers when dealing with binary or bounded outputs

Target model performance: I was unable to achieve 75% model accuracy target

## Steps taken to increase model performance

### Scenario 1: Accuracy - 72.7%
- 'EIN', 'NAME', 'STATUS', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT' columns were removed
- I used 8 hidden_nodes_layer1 and 5 hidden_nodes_layer2
- 2 hidden layers were selected as a starting point
- Activation functions of ReLU and sigmoid were used. ReLU was used for hidden layers and sigmoid was used for output layer

### Scenario 2: Accuracy - 72.4%
- 'EIN', 'NAME', 'STATUS', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT' columns were removed
- I used 10 hidden_nodes_layer1 and 10 hidden_nodes_layer2
- 2 hidden layers were selected as a starting point
- Activation functions of ReLU and sigmoid were used. ReLU was used for hidden layers and sigmoid was used for output layer

### Scenario 3: Accuracy - 72.5%
- 'EIN', 'NAME', 'STATUS', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT' columns were removed
- I used 20 hidden_nodes_layer1 and 20 hidden_nodes_layer2
- 2 hidden layers were selected as a starting point
- Activation functions of tanH was used for 1st hidden layer
- Activation function of sigmoid was used for 2nd hidden layer
- Activation function of ReLU was used for output layer

## Overall results

### Scenario results
- Base scenario accuracy result was 73.2%
- Scenario 1 accuracy result was 72.7%
- Scenario 2 accuracy result was 72.4%
- Scenario 3 accuracy result was 72.5%

### Recommendations for higher prediction accuracy
- Data Quality and Quantity: Ensure that dataset is clean, well-preprocessed, and representative of the problem we are trying to solve
- Model Complexity: Experiment with different architectures, including varying the number of layers, neurons per layer, and activation functions
- Regularization: Regularization techniques like dropout, L2 regularization, and early stopping can help prevent overfitting by imposing constraints on the model's parameters
- Feature Engineering: Try different transformations or combinations of features to provide more meaningful input to the model
- Cross-Validation: Use techniques like cross-validation to assess model's performance on unseen data more accurately

