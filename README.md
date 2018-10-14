# 1DCNN
### Summary

CNN, Convolutional Neural Network, is famous for image recognition, but could be a good modeling framework for time series data with multiple variables.  Convolutional operation applied to 1d data sets and graphical interpretation of the logic will be explained. Classification of different types of bearing faults using raw accelerometer data is performed and compared with different approaches. The experiments implies

### Datasets and Inputs

 The data is available from [CaseWestern Reserve University Bearing Data Center](http://csegroups.case.edu/bearingdatacenter/pages/download-data-file). The data is sampled from 3 accelerometers (Drive End, Fan End and Base) on an industrial equipment at 12k hz.  However Normal data is missing on Base, so only Drive End and Fan End will be used. For training of auto-encoder, the Normal data will be used with some shifts to create large number of training data. To evaluate the fault classification capability, 30 data files from 10 types of faults and 3 types of Motor Load(HP) will be used as described in paper [1].  The 10 types of faults are Normal, Ball(0.007, 0.014, 0.021-inch faults), Inner Race (same 3 types as above), and Outer Race (same 3 types as above). One sample for the model is the form of 2,048x 2 (Drive End and Fan End) array. There are 19,800 test samples and 750 test samples. The 10 types of faults are completely balanced across training and test dataset. Test samples does not have any shift (overlap).

## Prerequisites

- Create ./data and ./data/download before running functions in data_prep.ipynb


### Reference

[1] Wei Zhang,Gaoliang Peng, Chuanhao Li, Yuanhang Chen and Zhujin Zhang, “[A New Deep Learning Model forFault Diagnosis with Good Anti-Noise and Domain Adaption Ability on RawVibration Signals](http://www.mdpi.com/1424-8220/17/2/425)”, MDPI Sensors, 2017.