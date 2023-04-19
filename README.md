# SVM_Parameter_Optimisation
-Cherish Mahajan (102003647) 

This assignment focusses on the following points :
1. Download a multi-class dataset from UCI library.
2. Dataset size must have rows between 5k and 30k.
3. Divide the dataset into 70-30 for training and testing with 10 different samples.
4. Optimise the SVM for every sample with 1000 iterations and report the best parameters.
5. Plot the convergence graph for the sample ehose accuracy is maximum.
#

#DATASET
The data has been normalized using the Z- Normalisation method and divide into 2 datasets : a training set containing 10429 samples and a test set containing the 10437 samples.

Attribute Information:

**F1: intercolumnar distance**<br>
**F2: upper margin**<br>
**F3: lower margin**<br>
**F4: exploitation**<br>
**F5: row number**<br>
**F6: modular ratio**<br>
**F7: interlinear spacing**<br>
**F8: weight**<br>
**F9: peak number**<br>
**F10: modular ratio/ interlinear spacing**<br>
**Class: A, B, C, D, E, F, G, H, I, W, X, Y**<br>

#
#Methodology

The dataset is split into training and testing set for 10 times and the following SVC classifier hyperparameter are selected for best accuracy:

**Kernel** -  Different kernel functions to model non-linear relationships between the input variables and the output variableSelected from RBF, Polynomial, Linear and Sigmoid<br>
**C** (Regularisation parameter) - It is used to set the tolerance of the model to allow the misclassification of data points in order to achieve lower generalization error. Higher the value of C, lesser is the tolerance and what is trained is a maximum-margin classifier. Smaller the value of C, larger is the tolerance of misclassificationRandom integer values from 1 to 6<br>
**Gamma** (Kernel coefficient) - The gamma parameter defines how far the influence of a single training example reaches, with low values meaning ‘far’ and high values meaning ‘close’. The lower values of gamma result in models with lower accuracy and the same as the higher values of gamma. It is the intermediate values of gamma which gives a model with good decision boundaries.Random integer values from -1 to 6. If the value is less than 1, then gamma is randomly set as auto or scale. It is used only by rbf, poly and sigmoid kernel.<br>
**Degree** - Random integer from 1 to 7. It is only used by poly kernel and represent the degree of polynomial kernel function.<br>

#
# OBSERVATIONS

|Sample| Kernel   |   c | gamma   |   degree |   Accuracy |
|-----:|:---------|----:|:--------|---------:|-----------:|
0      | rbf      |6    |auto     | 5        |0.725791
1      |rbf       |2    | 4       |4         |0.708853
2      |rbf       |4    | 1       |6         |0.770214
3      |rbf       |5    | 1       |1         |0.771492
4      |rbf       |3    |scale    |4         |0.709492
5      |rbf       |3    | 3       |5         |0.706296
6      |rbf       |1    | 4       |7         |0.639182
7      |rbf       |4    |scale    |1         |0.736977
8      |rbf       |5    | 2       |6         |0.735059
9      |rbf       |4    |2        |3         |0.744966


#
# GRAPH

#
# RESULT

**Kernel: RBF**<br>
**C:5**<br>
**Gamma:1**<br>
**Degree:1** <br>
**Accuracy:0.771492**<br>
