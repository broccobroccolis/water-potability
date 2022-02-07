# Water Potability

In this project, we aim to compare the performance of small data and big data solutions in predicting if the water is safe for human consumption by analyzing the pattern of water bodies quality metrics of potable and non-potable water. Our target variable will be ‘Potability’, 
which indicates the safety of the water to be consumed by human means, by taking in the other variables in the dataset as the attributes. 

In this project, two solutions will be implemented, with small data and big data respectively. 

The pipelines will be compared in terms of their performance in handling the water potability problem.
<br>
For the small data solution, the data used is the Water Quality dataset which can be accessed from https://www.kaggle.com/adityakadiwal/water-potability. It consists of 3276 rows and 10 columns. 
For the big data solution, the data used is generated from the small data we discussed above, by duplicating it 512 times. It consists of 1677312 rows and 10 columns. The dataset used for this solution is not technically considered as actual big data because of technical limitations, however, we tried adjusting it to be as equivalent as big data as possible in terms of the volume of the data. We tried increasing the data size as much as possible within the range of our computation capability.
<br><br>
Anyway, for both algorithms, the big data solution performs better than the small data solution as it has a slightly higher model accuracy. Precision and F1 scores of the algorithms are generally better in the big data pipeline. This might be because having more data points makes it easier for models to discover the underlying pattern of the data. However, recall of algorithms using small data is higher than that using big data. 
<br>
In our case, precision is more important than recall, because getting a False Positive (unsafe water identified as safe water) is very dangerous and costly, and a False Negative (safe water identified as unsafe water) is not as much. The detailed comparison can be found at Appendix 10.27. 
<br><br>
However, in real life big data situations, there might be a huge difference in models’ performance. The current big data we have now is clean and contains very little noise. But the data quality for big data is uncertain in real life scenarios. Hence, extensive data preprocessing steps are needed to be done in actual big data scenarios to ensure the data quality.
Although the same models are used in both solutions, in terms of time needed to complete the run, the big data pipeline must be implemented when the dataset is huge, to save time and to increase efficiency. 
