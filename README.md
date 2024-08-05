# Classification-of-Normal-vs-Oral-Squamous-Cell-Carcinoma-OSCC-Cells 
## (This project was part of my Introduction to Machine Learning Course at Khalifa University)

# Introduction

In today's modern world, medical advancements are critical for early disease detection and treatment. Oral squamous cell carcinoma (OSCC), the seventh most common oral malignancy, annually affecting over 500,000 people, is a significant concern. OSCC is responsible for over 90% of oral cancer cases and has a high global mortality rate. 


One of the primary challenges in the battle against OSCC is the timely and accurate diagnosis of this condition. Traditional diagnostic methods may be time-consuming and subject to human error. Here, the opportunity lies in automating the analysis of oral biopsy images, which could significantly assist histopathologists in potentially more precise OSCC diagnosis.

Our project's primary goal is to develop a deep-learning model that can analyze oral biopsy images with a high degree of accuracy, enabling the early detection of OSCC. By providing a tool that can support healthcare professionals in making faster and more reliable diagnoses, we aim to improve patient outcomes and contribute to the reduction of OSCC-related mortality rates.

# Data

![image](https://github.com/user-attachments/assets/125fee53-5869-4bea-b8f7-ff66b423ddc3)


# Procedure
1) Data was split into training, testing, and validation before augmenting the data. 130 images in total were put for each testing and validation (30 from each of the 100x and 400x normal cells, and 35 from each of the 100x and 400x cancerous cells).

2) Augmentation was then applied to the normal cells in the training set to increase the dataset and keep it balanced with cancerous cells (804 images for each)

  ![image](https://github.com/user-attachments/assets/bf568a32-5520-4a8b-a90f-aaebc023dc30)



3) Data was resized to 224 by 224 and normalized on the fly for the training, validation, and testing.

4) VGG16 model was loaded with pre-trained weights, excluded top layer.

   ![image](https://github.com/user-attachments/assets/2e0166fb-de6f-43fa-b089-8d40bb33ae27)
   

5) Convolutional Layers were frozen.
   
   ![image](https://github.com/user-attachments/assets/449a9df2-9a18-48b8-a6fb-eabda43a72e2)



6) Our own model was added on top of the frozen layers (for fine-tuning).

![image](https://github.com/user-attachments/assets/d9aba431-dfc6-418c-80f2-592deaf9728a)

7) Train, validate, and test (weights for least validation loss were used).   

![image](https://github.com/user-attachments/assets/8a17b5b0-2f47-4be0-8b93-584077e9026a)

![image](https://github.com/user-attachments/assets/52dd4e1c-6244-42f0-8351-f4d84f64495f)

# Results

![image](https://github.com/user-attachments/assets/a34281c9-c41f-4fc5-adbf-5fde90eb82cb)

![image](https://github.com/user-attachments/assets/568454f5-2f21-4572-8d5d-6592305c0f38)

![image](https://github.com/user-attachments/assets/7384ea7a-66e9-4dd0-9626-598f4316b7d9)












