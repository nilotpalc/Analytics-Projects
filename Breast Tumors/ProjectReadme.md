
### Challenge 18: Explaining Cancer Predictions

******Level:****** Hard<br>******Description:****** You work as a researcher creating models to identify whether a breast tumor is benign or malign, based on anonymized patient data. Besides obtaining a classifier that works very well for both benign and malign cases, you must be able to explain how different feature values impact your results. Experiment with  [LIME](https://www.knime.com/blog/XAI-LIME-stroke-prediction)  and visualization techniques to explain your predictions and make your research more transparent. Hint: Learn more about this problem's data attributes  [here](https://archive.ics.uci.edu/dataset/15/breast+cancer+wisconsin+original).<br>******Author:****** [Keerthan Shetty](https://hub.knime.com/k10shetty1)<br>******Dataset:****** [Breast Tumor Data in the KNIME Community Hub](https://hub.knime.com/alinebessa/spaces/Just%20KNIME%20It!%20Season%203%20-%20Datasets/Challenge%2018%20-%20Dataset~JMWDCxY4oCz_eK_o/)<br><br>******Solution Summary:****** To tackle this problem, we start by lightly preprocessing the data and then building a random forest classifier to predict whether a tumour is benign ('B') or malign ('M'). We then sample two instances categorized with very high confidence (one originally labeled as benign and the other as malign) and use LIME to see how the different instance features account for their predictions. At the end of our solution, we create visualizations to better interpret the impact of the features.

**[See our Solution in KNIME Community Hub](https://hub.knime.com/knime/spaces/Just%20KNIME%20It!/Challenge%2018%20-%20Explaining%20Cancer%20Predictions~hp5ZeDuqH1UKBSPQ/current-state)**

[**Check out this blog**](https://www.knime.com/blog/XAI-LIME-stroke-prediction)

> Written with [StackEdit](https://stackedit.io/).
