# CHICKEN DISEASE DETECTION

## Project Description
The Chicken Disease Detection project focuses on developing an AI-driven solution to detect and classify chicken diseases based on fecal images. This innovative approach aims to improve early disease detection in poultry farming, reducing economic losses and enhancing animal health management. Using advanced deep learning techniques, the system identifies and classifies fecal images into four categories: Healthy, Salmonella, Newcastle Disease, and Coccidiosis.

### **Benefits**  
- **🔍 Early Disease Detection**  
  Helps farmers identify diseases early before widespread outbreaks occur, reducing the risk of mass poultry mortality due to delayed diagnosis.  

- **⏱️ Operational Efficiency**  
  Saves time and effort compared to manual or traditional methods and does not require intensive supervision by field experts.  

- **📈 Improved Farm Productivity**  
  Quick disease identification and treatment keep poultry healthy, ensuring optimal productivity, such as egg and meat production.  

- **💰 Reduced Treatment Costs**  
  Early detection minimizes the need for expensive treatments for severe or widespread diseases.  

- **📊 Support for Farm Management Decisions**  
  Diagnosis reports can be used as data for strategic decisions, such as vaccination schedules or coop cleaning.  

- **🐔 Enhanced Animal Welfare**  
  With more precise monitoring, the health and welfare of poultry can be better ensured.  

### **Features**  
- **✅ High Accuracy:** The model is designed with a high-quality annotated dataset, ensuring high accuracy in disease detection.  
- **⚡ Fast Response:** Capable of delivering diagnostic results within seconds after an image is uploaded.  
- **📄 Informative Reports:** Provides digital reports that include **Detected disease categories** and **Recommendations for further actions**.   

## Contributor
| Full Name | Affiliation | Email | LinkedIn | Role |
| --- | --- | --- | --- | --- |
| Akhras Athiyah | Startup Campus, AI Track | akhrasathiyah@gmail.com | [link](https://www.linkedin.com/in/akhrasathiyah/) | Team Lead |
| Alfrizky Elnesta | Startup Campus, AI Track | elnesta32@student.uns.ac.id | [link](https://www.linkedin.com/in/alfrizkye/) | Team Member |
| Eko Ginanjar Basuki Rahmat | Startup Campus, AI Track | ekoginanjar4@gmail.com | [link](https://www.linkedin.com/in/ekoginanjar/) |Team Member |
| Gladis Hafifah | Startup Campus, AI Track | ghmaliq24@gmail.com | [link](https://www.linkedin.com/in/gladishafifah/) | Team Member |
| Melviana Mayandra Putri Budi Setyo | Startup Campus, AI Track | melvianamayandraputri@gmail.com | [link](https://www.linkedin.com/in/melvianampbs) | Team Member |
| Muhamad Fariz Sabilah Putra Fajar | Startup Campus, AI Track | putrafajar198@gmail.com | [link](https://www.linkedin.com/in/putrafjrr/) | Team Member |
| Muhammad Zhulal | Startup Campus, AI Track | 2010103065.zhulal@gmail.com | [link](https://www.linkedin.com/in/muhammad-z-07869b109/) | Team Member |
| Aries Fitriawan | Startup Campus, AI Track | aries.fitriawan@ioh.co.id | [link](https://linkedin.com/in/ariesfitriawan) | Supervisor |

## Setup
### Prerequisite Packages (Dependencies)
- Torch == 2.5.1
- Torchvision == 0.20.1
- Numpy == 1.26.4
- PIL == 11.0.0
- Pandas == 2.2.2
- Matplotlib == 3.8.0
- Tqdm == 4.66.6
- OpenAI == 1.54.4

### Environment
| | |
| --- | --- |
| CPU | 13th Gen Intel(R) Core(TM) i5-13450HX (16 CPUs), ~2.4GHz |
| GPU | NVIDIA GeForce RTX 4050 Laptop GPU |
| ROM | 512 GB SSD |
| RAM | 16 GB |
| OS | Windows 11 |

## Dataset  
The "Chicken Disease Image Classification" dataset is designed to support research and development of computer vision-based models for identifying and classifying various types of chicken droppings. This dataset consists of 8,067 annotated images labeled to reflect different health conditions of chickens. The images include variations in shape, texture, and color of chicken droppings, aiming to enhance the model's generalization capability.  

The dataset is divided into three main groups: 6,453 samples for training, 806 for validation, and 808 for testing. Each image is classified into one of four categories: **Healthy**, **Salmonella**, **Newcastle Disease**, and **Coccidiosis**.  

This dataset is systematically and comprehensively designed to support the development of artificial intelligence-based models applicable in various fields, such as image-based poultry disease detection systems.  
- Link: [Chicken Disease Datasets](https://www.kaggle.com/datasets/allandclive/chicken-disease-1)

## Results
### Model Performance
In this section, we present the results from the final project experiments, covering various aspects of the model's evaluation through metrics, ablation study, and training/validation curves. These results are summarized in the tables below and supported by visual illustrations to provide deeper insights.

#### 1. Metrics
Here are some explorations we have conducted to evaluate and compare the performance of various models.

| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall | test_acc |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DenseNet121 | 50 |  0.00001 | 32 | Adam | 0.0854 | 98% | 97% | 95.92% |
| DenseNet121 | 50 |  0.00001 | 64 | Adam | 0.0839 | 97% | 96% | 96.78% |
| DenseNet121 | 80 |  0.00001 | 16 | Adam | 0.1039 | 97% | 96% | 96.41% |
| DenseNet121 | 80 |  0.00001 | 32 | Adam | 0.0905 | 97% | 96% | 96.16% |
| DenseNet121 | 80 |  0.00001 | 64 | Adam | 0.0839 | 97% | 96% | 96.21% |
| Resnet50 | 50 |  0.00001 | 32 | Adam | 0.1334 | 96% | 97% | 97.03% |
| Resnet50 | 50 |  0.00001 | 64 | Adam | 0.1297 | 97% | 96% | 96.41% | 
| VGG16 | 50 |  0.00001 | 32 | Adam | 0.1362 | 96% | 95% | 95.79% |
| VGG16 | 50 |  0.00001 | 64 | Adam | 0.1539 | 97% | 97% | 96.29% |
| VGG16 | 50 |  0.00001 | 32 | Adamax | 0.0857 | 95% | 95% | 95.92% |
| VGG16 | 50 |  0.00001 | 64 | Adamax | 0.1444 | 96% | 96% | 96.53% |


From the explorations conducted, we selected the best model based on optimal performance, which is:
| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall | test_acc |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DenseNet121 | 50 |  0.00001 | 64 | Adam | 0.0839 | 97% | 96% | 96.78% |

The main reason we chose this model is its stable performance without indications of overfitting, unlike other models that were tested. This shows that DenseNet121 with this hyperparameter configuration is able to achieve good generalization on the test data.

#### 2. Ablation Study
In this study, we perform a simple ablation to evaluate the effect of the **output layer** size on model performance. The DenseNet model was used with the following modifications:
- **Default Output Layer**: The original **DenseNet121** model, pretrained on ImageNet, has an output layer of size 1000 (corresponding to the 1000 classes of ImageNet).
- **Modification**: The output layer was modified to match the number of output classes in the target dataset, which is 4 classes.
- **Effect**: The model's output layer now has 4 units instead of 1000, corresponding to the 4 target classes.

This line replaces the original output layer with one that has `num_classes` outputs (in this case, 4).
```python
self.model.classifier = torch.nn.Linear(self.model.classifier.in_features, num_classes)  
```

| model | output_layer | top1_acc |
| --- | --- | --- |
| DenseNet121 Default | 1000 | - |
| DenseNet121 Modified | 4 | 96.78% | 

#### 3. Training/Validation Curve
The graph shows that both **train loss** and **validation loss** consistently decrease with similar trends and no significant differences, while accuracy
![Training/Validation Curve](https://github.com/user-attachments/assets/c452e8a6-75eb-4440-a5cb-3b165a8989ae)

#### 4. Confusion Matrix
![image](https://github.com/user-attachments/assets/ccf78c6c-95d8-42f8-b9e8-4db70962100e)

The confusion matrix shows the model's performance in classifying poultry diseases based on their droppings, with results reflecting the accuracy level for each class. In the Healthy class, the model correctly classified 240 samples, with 12 samples misclassified. In the Salmonella class, there were 254 correct samples and 6 incorrect samples, while in the Coccidiosis class, the model recorded 224 correct samples and 7 incorrect samples. Finally, for the Newcastle Disease class, the model showed 62 correct samples and 3 incorrect samples.

To further improve the model's accuracy, data augmentation techniques such as horizontal flip, resize, and rotation were applied to enrich the variation of the training data and enhance the model's generalization capability. Based on the confusion matrix analysis, most classes have achieved accuracy above 95%, indicating that the model has excellent ability to identify and differentiate disease categories with minimal errors.
 
### Testing
The model was tested using the testing dataset to evaluate its classification performance. From this evaluation, the model achieved an accuracy of **96.78%**. Below are some visual results of the classifications on the testing data. Each image is accompanied by the ground truth label and the model's prediction.
![Testing](https://github.com/user-attachments/assets/71fabcca-ea02-484e-a50c-cc774f879c6d)

### Deployment (Optional)
#### Overview
This project consists of a **Next.js frontend** deployed on **Vercel** and a **Flask backend** deployed on **Google Cloud**. The frontend and backend work together to deliver a seamless user experience, with Next.js handling the client-side interface and Flask providing API logic and data processing on the server.

#### Frontend Deployment (Next.js on Vercel)
The frontend is built using **Next.js**, a React framework for building modern web applications. Next.js supports both **server-side rendering (SSR)** and **static site generation (SSG)**, providing fast and optimized pages for the user.

- **Deployment Platform**: Vercel

#### Backend Deployment (Flask on Google Cloud)
The backend is built using **Flask**, a lightweight Python web framework. It provides RESTful API endpoints that the frontend communicates with.

- **Deployment Platform**: Google Cloud

#### Deployment Link
https://chicken-disease-detection.vercel.app/


## Supporting Documents
### Presentation Deck
- Link: [Chicken Disease Detector](https://drive.google.com/file/d/1yZEcFpZJCbYOwqQZ5subHIwzRLq7vTdY/view?usp=sharing)

### Business Model Canvas
![BMC Chicken Disease🐔](https://github.com/user-attachments/assets/4fffd21e-0c6c-44b2-938e-1cc0ac2251c0)


### Short Video
Provide a link to your short video, that should includes the project background and how it works.
- Link: https://youtu.be/SoLLlzMYBnU

## References
Provide all links that support this final project, i.e., papers, GitHub repositories, websites, etc.
- Link: https://...
- Link: https://...
- Link: https://...

## Additional Comments
Provide your team's additional comments or final remarks for this project. For example,
1. ...
2. ...
3. ...

## How to Cite
If you find this project useful, we'd grateful if you cite this repository:
```
@article{
...
}
```

## License
For academic and non-commercial use only.

## Acknowledgement
This project entitled <b>"CHICKEN DISEASE DETECTION"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
