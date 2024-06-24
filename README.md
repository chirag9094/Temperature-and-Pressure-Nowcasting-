# Temperature-and-Pressure-Nowcasting

## Overview
This particular project aims to introduce a modified neural network of the RainNet model designed specifically for nowcasting temperature and pressure. Drawing from the foundational architecture of RainNet, strategic adjustments were made to accommodate the distinct requirements of temperature and pressure prediction. These modifications include alterations in the number of layers, kernel initializers, activation functions, and other architectural elements to optimize the model for the intended task. With a finalized architecture consisting of approximately 4.7 million parameters, the model excels in capturing crucial features and intricacies within atmospheric data. Extensive experimentation and validation demonstrate the model's high accuracy in predicting temperature and pressure values, establishing its efficacy as a valuable tool for nowcasting applications in meteorology and related fields.

## Dataset Used
The data used for this project was obtained from the open-access website "https://cds.climate.copernicus.eu/cdsapp#!/search?type=dataset&text=iq%20data," providing ERA5 data spanning from 2013 to 2021, total of 78,888 images with a one-hour time gap between successive images. All 78,888 images were utilized for training, while 23,000 randomly selected images were used for validation

## Training 
The nowcasting project was structured into two distinct sections: training and operational. In the training phase, a model was developed and trained over 20 epochs, with the primary metric being loss. The model weights were saved into a file named "model_weights.h5" only if the loss in a particular epoch was lower than that of all previous epochs. Subsequently, in the operational phase, the trained model weights were utilized along with the most recent 20 images to nowcast the subsequent images. This approach ensures that the model is trained effectively and deployed efficiently for accurate nowcasting of temperature and pressure values.

## Output
Nowcasted Temperature after 5 minutes
<img src="output/temp.png">
Nowcasted Pressure after 5 minutes
<img src="output/pressure.png">
