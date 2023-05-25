
## SVM Multiclass Classification. 
 
### Lecture note 
[SVM_pdf](SVM_SS.pdf) or [SVM_pptx](SVM_SS.pptx).  

### Coding Exercise
SVM does not support multiclass classification natively. Two commonly used approaches that extend SVM for multiclass classification are One-vs-One and One-vs-Rest. In this exercise, we would like you to apply multiclass classification using SVM to classify number 0-10 from MNIST dataset. 
 
Specifically, we would like you to explore the following: 

1. **[5 scores]** You may randomly select 6000 samples for training and 1000 sample for testing. Ensure that you have chosen the samples evenly from each class. Then, show us the distribution of labels in the selected training and testing samples.

2. **[10 scores]** Let's assume that we choose the RBF kernel for SVM. You may separate your training set for tuning and validation. Please show the following results:   
*   a. Show the accuracy (or loss ) curves across of the validation set across different kernels and model parameters. 
*   b. Pick the best set of parameters and verify the final performance on the testing dataset.  

3. **[25 scores]** To see the differences between One-vs-one and One-vs-the rest. Let’s observe the positive and negative supports.  
*   a. For one-vs-one classification, what is the number of binary classifiers and how is it related to the number of classes? 
    - Observe the positive and negative supports of the first separation, the last separation, and any where in the middle.
*   b. For one-vs-rest classification, same question for the binary classifiers and number of classes. 
    - Also, observe the positive and negative supports of the first separation,  the last separation, and any where inbetween.
    
*   c. Can you tell the differences between the observation in (3.a) and (3.b)? 
    - For each observation, you may plot the mean shapes of the positive and negative supports & the histogram of the labels associated with the positive and negative supports.

---

## Prerequisite 

Please make sure you have install anaconda and jupyternote book. 

```
conda env create -f environments.yml
```

```
conda activate mysvm
```

---

### Note about scoring 

To get the full score, you should be able to provide the following plots with resonable results and **with good explaination**:

1. SVM_1_MNIST_label_distribution.png  **[5 scores]**  
2. SVM_2_ModelSelection.png **[5 scores]** +  your answers **[5 scores]**
3. Two sets for one_vs_one plots **[10 scores]**  and one_vs_rest_0/8/x plots **[10 scores]** and your answers **[5 scores]**. The examples of the plot files are as follows: 

  - SVM_3_mean_positive_support_one_vs_one_0.png
  - SVM_3_mean_positive_support_one_vs_one_8.png
  - SVM_3_mean_positive_support_one_vs_one_x.png
  - SVM_3_mean_negative_support_one_vs_one_0.png
  - SVM_3_mean_negative_support_one_vs_one_8.png
  - SVM_3_mean_negative_support_one_vs_one_x.png

  - SVM_3_MNIST_neg_pos_distribution_one_vs_one_0.png
  - SVM_3_MNIST_neg_pos_distribution_one_vs_one_8.png
  - SVM_3_MNIST_neg_pos_distribution_one_vs_one_x.png

  - SVM_3_positive_support_one_vs_one_0.png
  - SVM_3_positive_support_one_vs_one_8.png
  - SVM_3_positive_support_one_vs_one_x.png

  - SVM_3_negative_support_one_vs_one_0.png
  - SVM_3_negative_support_one_vs_one_8.png
  - SVM_3_negative_support_one_vs_one_x.png
