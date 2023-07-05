# Breast Cancer Segmentation (Malignant, Benign, Normal):
Breast cancer is one of the most common causes of death among women worldwide. Early detection helps reduce the number of premature deaths. Data reviews medical images of breast cancer using ultrasound. The breast ultrasound dataset is categorized into three categories: normal, benign, and malignant images.
- In the study, I am working on creating a convolutional neural network capable of identifying tumor areas within medical images (which were taken with ultrasound).
- Through the following study, I am working on producing a highly efficient Segmentation model with the ability to generalize and identify the cancer area, regardless of the type or area of cancer.
- The methodology used in the study depended on many factors. Initially, all medical images were used, whether (malignant cancer, benign cancer, or images that did not contain any cancer).
- The U-NET structure was used in addition to making the neural network predict the types of cancer that it selects. I believe that making the neural network carry out additional tasks helps increase the accuracy of the model and its ability to generalize the results it reaches.
- The proposed structure of the neural network tries to build a system capable of understanding the following sentence: "What type of cancer does the patient suffer from? Is it malignant cancer? Or is it benign cancer? Or is there no cancer?" After answering the first question, we move on to the second question, where is the cancerous tumor located In medical images?
- The previous sentence helps the neural network to accurately determine the area of ​​the cancerous tumor after knowing the type of cancer.
- But to facilitate the discovery of the cancer region in the medical images, the MSE loss function was used to determine the two types of cancer, which makes the loss function derivable and continuous at any moment, which facilitates the training process, and makes the neural network able to find the link between the cancer tumor area and its shape with the two types of cancer tumor.
- As we mentioned, a stable training must be found between recognizing the two types of cancerous tumors, and identifying the cancerous tumor area in the medical image (as we mentioned, this helps in the ability to know the shape and characteristics of the cancerous tumor easier and faster).
- On the other hand, in order not to make the neural network focus only on the dark area in the medical images, DATA_AUGMENTATION was used to make each medical image (as it is, lighter by adding lighting, darker by using contrast).
# Dataset Used:
## Dataset Link: 
https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset
## Samples of Dataset:
![__results___15_0](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/f411d764-20b8-4aee-b16d-40bd5872d67a)

# Neural network architecture proposal:
A convolutional neural network structure was proposed according to the U-NET model, with the neural structure doing an additional task including recognizing the type of cancerous tumor.
# Results and metrics:
| # | Metrics |
| :---:   | :---: |
| Evaluation on Training and Validation Data |  ![image](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/22f06daf-d616-479d-baf2-789f538a55a5) ![image](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/f4f65453-a658-4b33-9b45-6cbc7120e615)|
| Classification Report, Accuracy Score, Precision Score, Recall Score, F1 Score, specificity, dice Score, sensitivity |  ![image](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/3ac7d756-0563-43eb-9557-4987383cd202) ![image](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/eaca1f0b-161d-4ec1-93f1-97d6efd6afca)|

## Visual review of the results:
| # Samples of Validation Data (compare the predicted masks with the true masks)    |
| :---: |
| ![__results___41_0](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/9f35141d-2359-4cf9-8491-a50cdb64af55)|
|  ![__results___39_0](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/7ac45d11-a2d6-4516-8c8a-c06caef0c135)|
| ![__results___40_0](https://github.com/kaledhoshme123/Breast-cancer-segmentation-malignant-benign-normal-/assets/108609519/911d8b8f-f81a-42ed-9a42-1a63b1e4668a)|
