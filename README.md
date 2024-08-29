# Discussion and conclusion

**1.** All textual features are manually looked at - Probabale text that may indicate an malicious file were checked for correlation(**2.1**)

**2.** Correlation

    2.1 Between textual features and labels: ['f_2_no_signature', 'f_9_no_signature', 'f_59_True', 'f_59_False']

    2.2 Between float features and labels: ['f_7', 'f_71']

    2.3 Between Outliers features and labels (More than 2 stds): ['f_68', 'f_70', 'f_74', 'f_83', 'f_87']

Only 2 correlations out of 8 are shown in the final model to be important

**3.** No clusters are vizulaied in 2D.

**4.** Model results

    4.1 F1 score: Train set - 91% | Test set - 89%.

    4.2 Accuracy: Train set - 92% | Test set - 89%. (Better than baseline random selection - 56%)

# Furure impovment:

**1.** Filling NaN values are done with the __Mode__:

    1.1 Some most frequnt values, are small percentage of dataset. E.g: 
        f_0: 28.93%
        f_1: 36.87%
        f_4: 21.11%
        f_8: 5.26%

    1.2 Another possibility would be fill them with PCA
   
**2.** Textual features:

    2.1 Instead of looking at them as close set, we can pass them into DL model to get their embeddings.
   
    2.2 A dimension reduction technique can be implied on those embeddings to find outliers