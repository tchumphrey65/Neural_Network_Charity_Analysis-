# Neural_Network_Charity_Analysis

## Background

From Alphabet Soup’s business team, our team has been provided a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. The dataset contains of columns that store metadata about each organization taht applied for fuunding. Our project is to use machine learning and neural networks to analyze the data and features included to create a binary classifier capable of predicting if an applicant will be successful in obtaining funding from Alphabet Soup.

## Project Deliverable 1: Preprocessing Data for a Neural Network Model
### The following preprocessing are to be completed on this dataset:
1. The EIN and NAME columns have been dropped.
2. The columns with more than 10 unique values have been grouped together.
3. The categorical variables have been encoded using one-hot encoding.
4. The preprocessed data is split into features and target arrays.
5. The preprocessed data is split into training and testing datasets.
6. The numerical values have been standardized using the StandardScaler() module.

### Results Deliverable 1

1. The EIN and NAME columns have been dropped.

![image](https://user-images.githubusercontent.com/91839403/160283734-ceff23c2-245f-4cc2-b557-45557c453078.png)

2. The columns with more than 10 unique values have been grouped together.
Application Type and Classification were the two columns containing more than 10 unique values.  These have been grouped and reduced.

![image](https://user-images.githubusercontent.com/91839403/160283820-8797060f-b5d5-4361-9e67-18c60b0251b8.png)

![image](https://user-images.githubusercontent.com/91839403/160283856-c442dd80-3dce-42b2-a305-be8690d7a454.png)

3. The categorical variables have been encoded using one-hot encoding.

![image](https://user-images.githubusercontent.com/91839403/160283926-350f1bcd-5c55-4a2e-9f5e-b5ba0af78bd4.png)

![image](https://user-images.githubusercontent.com/91839403/160283970-3b05c97d-1af6-4b3a-bbb1-01ea8edabea5.png)

4. The preprocessed data is split into features and target arrays.

![image](https://user-images.githubusercontent.com/91839403/160283984-4aa3e349-1eeb-4e90-9f69-40cbe074fd34.png)

5. The preprocessed data is split into training and testing datasets.

![image](https://user-images.githubusercontent.com/91839403/160284001-dc90c237-da86-4936-8ccf-d0ceab278b6e.png)

6. The numerical values have been standardized using the StandardScaler() module.

![image](https://user-images.githubusercontent.com/91839403/160284026-64bc9804-c6e1-4e7a-9b79-5ee9fbc91bc2.png)

## Project Deliverable 2: Compile, Train, and Evaluate the Model
### The neural network model using Tensorflow Keras contains working code that performs the following:
1. The number of layers, the number of neurons per layer, and activation function are defined.
2. An output layer with an activation function is created.
3. There is an output for the structure of the model.
4. There is an output of the model’s loss and accuracy.
5. The model's weights are saved every 5 epochs.
6. The results are saved to an HDF5 file.

### Results Deloiverable 2
1. The number of layers, the number of neurons per layer, and activation function are defined.
2. An output layer with an activation function is created.

![image](https://user-images.githubusercontent.com/91839403/160292013-fd3221ed-6d39-43a3-ac8a-9cbc6fd0b088.png)

3. There is an output for the structure of the model.

![image](https://user-images.githubusercontent.com/91839403/160292042-96f8cba6-1f48-425a-95d5-f041691be511.png)

4. There is an output of the model’s loss and accuracy.

![image](https://user-images.githubusercontent.com/91839403/160292062-78e37e02-fbde-4af0-bbf7-311413654b47.png)

5. The model's weights are saved every 5 epochs.

![image](https://user-images.githubusercontent.com/91839403/160292202-6092ad90-57ff-45ec-b903-4633cdedf2b1.png)

6. The results are saved to an HDF5 file.
(Stored in Git Hub repository under checkpoints folder)

Deliverable 

![image](https://user-images.githubusercontent.com/91839403/160292243-dc301575-ad0e-4efc-ad6b-b9f6db6b49a8.png)


## Project Deliverable 3: Optimize the Model
Despite multiple attempts I was never able to get the model to perform at 75% accuracy.

### Atttempt 1 

Model Structure

![image](https://user-images.githubusercontent.com/91839403/160292432-3bf084b1-ed80-4fe7-b5b5-bf61dd8b7c2b.png)

Input Layers First -relu Second -relu Output -sigmoid
Hidden Nodes Layer 1 - 8
Hidden Nodes Layer 2 - 5

Result
Loss = .54 Accuracy = 73.9%

### Attempt 2

Model Structure

![image](https://user-images.githubusercontent.com/91839403/160292523-4e0e74e3-e320-456d-82d9-74c2990988f4.png)

Input Layers First -relu Second -sigmoid Output -tanh
Hidden Nodes Layer 1 - 25
Hidden Nodes Layer 2 - 8

Result
Loss = .54 Accuracy = 73.7%

### Attempt 3
Rebuilt initial data file and dropped "SPECIAL CONSIDERATIONS" Column 

Model Structure

![image](https://user-images.githubusercontent.com/91839403/160292652-93a30960-4777-4324-983e-130d084357cf.png)


Input Layers First -relu Second -relu Output -relu
Hidden Nodes Layer 1 - 80
Hidden Nodes Layer 2 - 20

Result
Loss = .57 Accuracy = 40.4%

This ended up significantly worse, so we can impact the accuracy, I do not know how to shift it to an accuracy greater than 75%

