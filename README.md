# WAIpred

### Introduction

WAIpred is a program that predicts middle ear pathology in newborns using raw wideband acoustic immittance (WAI) data. It makes decisions based on the following five models:

1. Feedforward Neural Network (FNN)  
2. Convolutional Neural Network (CNN)  
3. Kernel Density Estimation (KDE)  
4. Random Forest (RF)  
5. Support Vector Machine (SVM)

### Download

Download WAIpred_ENG.exe (English version) or WAIpred_CHN.exe (Chinese version) from the main branch. You will also need to download the models, temp, and train_data folders and place them in the same directory as the WAIpred executable file. If you are using Windows 7, the WAIpred executable file may encounter errors. In this case, you can try installing the contents of the "windows7" folder to resolve the issue.  

### Tutorial
WAIpred GUI:  

<img src="https://github.com/yk-Zhao/WAIpred/blob/main/introduction/GUI-2.png" width="600" height="650">

>(A) WAI file input area: upload your raw WAI data file here (with a .m extension) and select the save location for the prediction result text file (optional).  
>(B) Text results display area, including basic input information and the prediction results for each model  
>(C) Visualization of the input WAI data and contrast WAI data  
>(D) Auxiliary judgment area, including the admittance curve at 226Hz and 1000Hz  

### Input
The input raw WAI file needs to include the following data entries, you can refer to the example WAI files provided in the "examples" folder for more details.:  
* FREQ: Contains 107 stimulus frequency points ranging from 226 to 8000 Hz.
* PRESSURE: Sound pressure values covering at least the range from -350 daPa to +150 daPa, without duplicate values.
* ABSORBANCE: Contains the sound absorption rate for each frequency and pressure, as a 2D matrix.
* TYMP_Y_226Hz: Contains the acoustic admittance values at 226 Hz for different pressure values, in mmho.
* TYMP_Y_1000Hz: Contains the acoustic admittance values at 1000 Hz for different pressure values, in mmho.

### Output
The output results text display box shows the sample's basic information, the final prediction result, and the prediction results and probabilities for each model.

Below the prediction results are the absorbance heatmaps of the input sample and the contrast sample, aiding in identifying abnormalities by visualizing the similarities. Below the heatmaps are the tympanogram admittance curves at 226Hz and 1000Hz. The program automatically performs peak identification (marked with red "x") and classifies the tympanogram at 226Hz as type A (peaked), B (flat), or C (negative pressure). The peak detection results are also displayed below the 1000Hz graph.  

If there is a conflict between the model prediction results and the tympanogram curves，the program will prompt the user that the prediction for the sample may not be accurate, and further examination is needed to determine if it is abnormal.
