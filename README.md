# Discussion and conclusion

**1.** All textual features were manually examined: Potential text patterns indicative of malicious files were analyzed for correlations(**2.1**)

**2.** Correlation

    2.1 Between textual features and labels: ['f_2_no_signature', 'f_9_no_signature', 'f_59_True', 'f_59_False']

    2.2 Between float features and labels: ['f_7', 'f_71']

    2.3 Between Outliers features and labels (More than 2 stds): ['f_68', 'f_70', 'f_74', 'f_83', 'f_87']

Only 2 out of the 8 correlations are considered important in the final model.

**3.** No clusters are visualized  in 2D.

**4.** Model results

    4.1 F1 score: Train set - 91% | Test set - 89%.

    4.2 Accuracy: Train set - 92% | Test set - 89%. (Better than baseline random selection - 56%)

# Furure impovment:

**1.** Filling NaN values is done using the __mode__.

    1.1 Some most frequnt values, are small percentage of dataset. E.g: 
        f_0: 28.93%
        f_1: 36.87%
        f_4: 21.11%
        f_8: 5.26%

    1.2 Another possibility would be fill them with PCA
   
**2.** Textual features:

    2.1 Rather than treating these features as a close set, we can feed them into a deep learning model to obtain their embeddings.

    2.2 We can then apply a dimensionality reduction technique to these embeddings to identify outliers.
