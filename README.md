# CHICKEN DISEASE DETECTION

## Project Description
The Chicken Disease Detection project focuses on developing an AI-driven solution to detect and classify chicken diseases based on fecal images. This innovative approach aims to improve early disease detection in poultry farming, reducing economic losses and enhancing animal health management. Using advanced deep learning techniques, the system identifies and classifies fecal images into four categories: Healthy, Salmonella, Newcastle Disease, and Coccidiosis.

### **Manfaat**  
- **🔍 Pendeteksian Dini Penyakit**  
  Membantu peternak untuk mengidentifikasi penyakit lebih awal sebelum terjadi penyebaran yang luas dan mengurangi risiko kematian massal unggas akibat keterlambatan diagnosis.  
- **⏱️ Efisiensi Operasional**  
  Menghemat waktu dan tenaga dibandingkan metode manual atau tradisional, serta tidak memerlukan pengawasan intensif oleh tenaga ahli di lapangan.  

- **📈 Peningkatan Produktivitas Peternakan**  
  Dengan identifikasi dan perawatan penyakit yang cepat, unggas dapat tetap sehat, sehingga produktivitas seperti produksi telur dan daging tetap optimal.  

- **💰 Pengurangan Biaya Pengobatan**  
  Deteksi dini mengurangi kebutuhan akan pengobatan yang mahal akibat penyakit yang sudah parah atau menyebar.  

- **📊 Dukungan untuk Keputusan Manajemen Peternakan**  
  Laporan diagnosis dapat digunakan sebagai data untuk membuat keputusan strategis, seperti jadwal vaksinasi atau pembersihan kandang.  

- **🐔 Peningkatan Kesejahteraan Hewan**  
  Dengan pemantauan yang lebih cermat, kesehatan dan kesejahteraan unggas dapat lebih terjamin.  

### **Feature**  
- **✅ Akurasi Tinggi:** Model dirancang dengan dataset teranotasi berkualitas tinggi, memastikan akurasi tinggi dalam deteksi penyakit.  
- **⚡ Respons Cepat:** Mampu memberikan hasil diagnosis hanya dalam hitungan detik setelah gambar dimasukkan.  
- **📄 Laporan Informatif:** Menyediakan laporan digital yang mencakup: **Kategori penyakit terdeteksi** dan **Rekomendasi tindakan lebih lanjut**  

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
| Nicholas Dominic | Startup Campus, AI Track | nic.dominic@icloud.com | [link](https://linkedin.com/in/nicholas-dominic) | Supervisor |

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
Dataset "Kotoran Ayam" dirancang untuk mendukung penelitian dan pengembangan model berbasis teknik computer vision dalam mengidentifikasi dan mengklasifikasikan berbagai jenis kotoran ayam. Dataset ini terdiri dari 8.067 gambar yang telah dianotasi dengan label yang mencerminkan berbagai kondisi kesehatan ayam. Gambar-gambar tersebut mencakup variasi bentuk, tekstur, dan warna kotoran ayam, yang bertujuan untuk meningkatkan kemampuan generalisasi model.  

Dataset ini dibagi menjadi tiga kelompok utama: 6.453 data untuk pelatihan (training), 806 data untuk validasi (validation), dan 808 data untuk pengujian (testing). Setiap gambar diklasifikasikan ke dalam salah satu dari empat kategori, yaitu Healthy (sehat), Salmonella, Newcastle Disease, dan Coccidiosis.  

Dataset ini dirancang secara sistematis dan komprehensif untuk mendukung pengembangan model berbasis artificial intelligence yang dapat diaplikasikan dalam berbagai bidang, seperti sistem deteksi penyakit unggas berbasis citra.
- Link: [Chicken Disease Datasets](https://www.kaggle.com/datasets/allandclive/chicken-disease-1)

## Results
### Model Performance
In this section, we present the results from the final project experiments, covering various aspects of the model's evaluation through metrics, ablation study, and training/validation curves. These results are summarized in the tables below and supported by visual illustrations to provide deeper insights.

#### 1. Metrics
We chose the DenseNet121 model with the following hyperparameter configuration for the project:
- Epochs: 50
- Learning Rate: 0.00001
- Batch Size: 64
- Optimizer: Adam
  
This configuration was selected because it achieved the lowest validation loss (0.0839) and provided balanced performance with validation precision (97%), validation recall (96%), and test accuracy (96.78%), compared to other models and configurations tested. 

| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall | test_acc |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DenseNet121 | 50 |  0.00001 | 32 | Adam | 0.0854 | 98% | 97% | 95.92% |
| DenseNet121 | 50 |  0.00001 | 64 | Adam | 0.0839 | 97% | 96% | 96.78% |
| Resnet50 | 50 |  0.00001 | 32 | Adam | 0.1334 | 96% | 97% | 97.03% |
| Resnet50 | 50 |  0.00001 | 64 | Adam | 0.1297 | 97% | 96% | 96.41% | 
| VGG16 | 50 |  0.00001 | 32 | Adam | 0.0857 | 95% | 95% | 95.92% |
| VGG16 | 50 |  0.00001 | 64 | Adam | 0.1524 | 97% | 97% | 96.29% | 

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
The graph shows that both **train loss** and **validation loss** consistently decrease with similar trends and no significant differences, while accuracy steadily increases to over 95%. This indicates that the model generalizes well without signs of overfitting.
![Screenshot 2024-11-25 105451](https://github.com/user-attachments/assets/e9243ba5-39c7-4921-9011-a6101426b6e3)
 
### Testing
The model was tested using the testing dataset to evaluate its classification performance. From this evaluation, the model achieved an accuracy of **95.92%**. Below are some visual results of the classifications on the testing data. Each image is accompanied by the ground truth label and the model's prediction.
![testing](https://github.com/user-attachments/assets/5c14a6bc-853e-4f89-ab3b-9ddab8e17d6f)

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
- Link: https://...

### Business Model Canvas
![Business Model Canva_Neurora](https://github.com/user-attachments/assets/a084f14c-ff3c-4508-8390-dee175d9b6c6)


### Short Video
Provide a link to your short video, that should includes the project background and how it works.
- Link: https://...

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
This project entitled <b>"HICKEN DISEASE DETECTION"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
