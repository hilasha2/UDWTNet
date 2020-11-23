# Cell segmentation and tracking challenge (HeLa Cells, DIC microscopy)

This code was written as part of a final project of a deep learning course taught by Raja Giryes and Barak Hadad at Tel Aviv University.

The code implements U-Net for cell segmentation.
The project is based on the cell segmentation and tracking challenge:

https://celltrackingchallenge.net 

Data used was time-lapse microscopic images of HeLa Cells.

We combined U-Net and a watershed transform network (DWTNet) based on Urtasun's and Bai's work:

https://github.com/min2209/dwt 

We called the combined network: UDWTNet.

In order to run the code, run the following code blocks by order - 

## PART A:

	1. Install Pytorch 1.6.0
	2. Install imgaug. 
		Installtion of libraries for image augmentations.
		You would be prompted to approve the installations.
		Type 'y' when asked. 
	3. Import libraries.
	4. Mount Google Drive.
		For saving and loading models.
		You would be prompted to approve drive access, please do.
	5. Set GPU device.
	6. Set path to Data base / save Path. 
		If you don't have access to our drive, 
		please upload the DIC-C2DH-HeLa dataset from 
		celltrackigchallenge.net 
		into your drive and change the saving paths accordingly. 
	7. Load database / class CustomDataset.
	8. Define show_dataset
	9. Optional: View original dataset.
	10. Define Class for Data Augmentation
	11. Optional: View augmentated dataset

## PART B: 

	Defining the network models. 
	
	For U-Net only:
	1. UNet model. 
		Defining the model. 
	2. Optional: Debug class UNet.
		for checking layers dimensions. 

	For U-Net + DWTNet:
	Training U-Net first, then training DWTNet based on U-Net. 
	1. UNet Model.  
	2. Optional: Debug class UNet.
	3. DWTNet Model. 
	4. Optional: Debug DWTNet Model

	For UDWTNet:
	A combined model of U-Net and DWTNet.
	1. UNet Model.  
	2. Optional: Debug class UNet.
	3. DWTNet Model. 
	4. Optional: Debug DWTNet Model.
	5. UDWTNet Model
	6. Optional: Debug UDWTNet model.

## PART C: 
	Supporting functions used for training and testing.
	
	1. Define Load Model.
		For loading saved model (files ending with '.pt').
	2. Define plotModelResult
	3. Dice Loss. 
		The models run with cross entropy loss, 
		but if you want to explore, try using dice loss as well. 
		Change accordingly in the train options. 
	4. IoU. Defining the accuracy measurement. 
	5. Post Processing of Estimated Label. 
		Still needs a little bit of touch up.
	6. Optional: Debug Post Processing. 
	7. Optional: Define Gradients Graph.
		For gradients' behaviour checkup. 

## PART D: 

	Training and testing.

	For U-Net only:
	1. Train UNet.
	2. Test U-Net.

	For U-Net + DWTNet:
	1. Train UNet.
	2. Train DWTNet.
	3. Test DWTNet.

	For UDWTNet:
	1. Train UDWTNet. 
	2. Test UDWTNet. 
