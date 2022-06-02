# C4.5

C4.5 Algorithm uses Entropy and Information Gain Ratio measures to analyse categorical and numerical data. The function returns: 1) The decision tree rules. 2) The total number of rules. You can try it in [Colab](https://colab.research.google.com/drive/1upOPNWJbMEW5BOUIuy2Ubna3vOpV4NYs?usp=sharing).

* Xdata = Dataset Attributes

* ydata = Dataset Target

* cat_missing = "none", "missing", "most", "remove" or "probability". If "none" is selected then nothing will be done if there are missing categorical values. If "missing" is selected then the missing categorical values will be replaced by a new category called Unkown. If "most" is selected then the categorical missing values will be replaced by the most popular category of the attribute. If "remove" is selected then the observation with missing categorical values will be deleted from the dataset. If "probability" is selected then the categorical missing values will be randomly replaced by a category based on the category distribution of the attribute.

* num_missing = "none", "mean", "median", "remove" or "probability". If "none" is selected then nothing will be done if there are missing numerical values. If "mean" is selected then the missing numerical values will be replaced by the attribute mean. If "median" is selected then the numerical missing values will be replaced by the attribute median. If "most" is selected then the numerical  missing values will be replaced by the most popular value of the attribute. If "remove" is selected then the observation with missing numerical values will be deleted from the dataset. If "probability" is selected then the numerical missing values will be randomly replaced by a value based on the numerical distribution of the attribute.

* pre_pruning = "none",  "chi_2", "impur" or "min". If "none" is selected then no pruning is performed. If "chi_2" is selected then a pre-pruning method based on a Chi Squared test is performed, if the table is in the 2x2 format and has less than 10,000 examples then a Fisher Exact test is performed instead. If "impur" is selected then a pre-pruning method is performed, pruning child nodes that do not improve the impurity from its father node. if "min" is selected then a node must have a minimum quantity of data examples to avoid pruning.

* chi_lim = 0.1. Chi Squared limit (p-value) to prune a node. Only relevant if pre_pruning = "chi_2".

* min_lim = 5. Minimum quantity of data examples that a node should have to avoid pruning. Values lower than this limit makes a node to be pruned. Only relevant if pre_pruning = "min".

* Finnaly a prediction function - prediction_dt_c45( ) - is also included.

# Acknowledgement 
This section is dedicated to all the people that helped to improve or correct the code. Thank you very much!

* Patrick Eiselt (26.FEBRUARY.2019) - Germany
* Xiuzhu Zhao (26.APRIL.2021) - China
