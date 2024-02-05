
## Human Activity Recognition
# Done in colaboration with [Aaryan](https://github.com/Aaryan-18).
Human Activity Recognition (HAR) refers to the capability of machines to identify various activities performed by the users. The knowledge acquired from these recognition systems is integrated into many applications where the associated device uses it to identify actions or gestures and performs predefined tasks in response.

## Dataset
For this project we used a publically available dataset called [UCI-HAR](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8567275). The dataset is available to download [here](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones). The Dataset contains data for 30 participants . Each participant performed six activities while wearing a Samsung Galaxy S II smartphone on their waist (The video of the participants taking data is also available [here](http://www.youtube.com/watch?v=XOEN9W05_4A)). The smartphone's accelerometer and gyroscope captured 3-axial linear acceleration and 3-axial angular velocity. Read all the `readme` and `info` files for more information.


## Tasks performed

1. Plotted the waveform for data from each activity class. Spotted Visual differences between the activities. 

2. Evaluated wether we need a machine learning model to differentiate between static activities (laying, sitting, standing) and dynamic activities(walking, walking_downstairs, walking_upstairs)? Looked at the linear acceleration $(acc_x^2+acc_y^2+acc_z^2)$ for each activity.

3. Trained Decision Tree using trainset and reported Accuracy and confusion matrix using testset.

4. Train Decision Tree with varrying depths (2-8) using trainset and report accuracy and confusion matrix using Test set. Accessed if the accuracy changes when the depth is increased? Plotted the accuracies and reason why such a result has been obtained.

5. Used PCA (Principal Component Analysis) on Total Acceleration $(acc_x^2+acc_y^2+acc_z^2)$ to compress the acceleration timeseries into two features and plotted a scatter plot to visualize different class of activities. Next, used [TSFEL](https://tsfel.readthedocs.io/en/latest/) ([a featurizer library](https://github.com/fraunhoferportugal/tsfel)) to create features and then performed PCA to obtain two features. Plotted a scatter plot to visualize different class of activities.

6. Used the features obtained from TSFEL and trained a Decision Tree. Reported the accuracy and confusion matrix using test set. Noticed that featurization works better than raw data. Trained Decision Tree with varrying depths (2-8) and compared the accuracies obtained in point 4 with the accuracies obtained using featured trainset. Plotted the accuracies obtained in point 4 against the accuracies obtained in this.

7. Answered if there any participants/ activitivies where the Model performace is bad? If Yes, Why?

# Deployment! (ON SELF COLLECTED DATA using `Physics Toolbox Suite`)
Utilized app `Physics Toolbox Suite` from our smartphone to collect our data in .csv/.txt format. Ensured at least 15 seconds of data is collected, trimming edges to obtain 10 seconds of relevant data. Collected 3-5 samples per activity class and reported accuracy using both featurized and raw data. You have to train on UCI dataset (You can use the entire dataset if you want) and tested it on the data that we collected and reported the accuracy and confusion matrix. Tested the model's performance on the collected data.
