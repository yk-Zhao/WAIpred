# WAIpred

### Introduction

WAIpred is a program that predicts middle ear pathology in newborns using raw wideband acoustic immittance(WAI) data. It makes decisions based on the following five models:

1. Feedforward Neural Network(FNN)  
2. Convolutional Neural Network(CNN)  
3. Kernel Density Estimation(KDE)  
4. Random Forest(RF)  
5. Support Vector Machine(SVM)

### Download

Download WAIpred_ENG.exe (English version) or WAIpred_CHN.exe (Chinese version) from the main branch. You will also need to download the models, temp, and train_data folders and place them in the same directory as the WAIpred executable file. If you are using Windows 7, the WAIpred executable file may encounter errors. In this case, you can try installing the contents of the "windows7" folder to resolve the issue.  

### Tutorial
WAIpred GUI:  
![](https://github.com/yk-Zhao/WAIpred/tree/main/introduction/GUI.png)  
(A) WAI file input area：upload your raw WAI data file here (with a .m extension) and select the save location for the prediction result text file (optional).  
(B) Text results display area, including basic input information and the prediction results for each model  
(C) Visualization of the input WAI data and contrast WAI data  
(D) Auxiliary judgment area, including the admittance curve at 226Hz and 1000Hz  
