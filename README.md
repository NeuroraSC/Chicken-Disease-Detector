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
- pandas==2.1.0
- openai==0.28.0
- google-cloud-aiplatform==1.34.0
- google-cloud-bigquery==3.12.0
- ...
- ...

### Environment
| | |
| --- | --- |
| CPU | 13th Gen Intel(R) Core(TM) i5-13450HX (16 CPUs), ~2.4GHz |
| GPU | NVIDIA GeForce RTX 4050 Laptop GPU |
| ROM | 512 GB SSD |
| RAM | 16 GB |
| OS | Windows 11 |

## Dataset
Dataset "Kotoran ayam" dirancang untuk  menggunakan teknik computer vision. Dataset ini terdiri dari gambar-gambar yang telah dianotasi dengan label yang merepresentasikan berbagai jenis kotoran ayam. Yaitu berisi kumpulan foto kotoran ayam yang berjumlah 8.067 data, dengan pembagian sebanyak 6453 data train, 806 data validation, dan 808 data test yang terbagi menjadi 4 kategori yaitu Healthy, Salmonella, Newcastle Disease, and Coccidiosis.
- Link: [Chicken Disease Datasets](https://www.kaggle.com/datasets/allandclive/chicken-disease-1)

## Results
### Model Performance
In this section, we present the results from the final project experiments, covering various aspects of the model's evaluation through metrics, ablation study, and training/validation curves. These results are summarized in the tables below and supported by visual illustrations to provide deeper insights.

#### 1. Metrics

| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall | test_acc |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DenseNet121 | 50 |  0.00001 | 32 | Adam | 0.0854 | 98% | 97% | 95.92% |
| DenseNet121 | 50 |  0.00001 | 64 | Adam | 0.0839 | 97% | 96% | 96.78% |
| Resnet50 | 50 |  0.00001 | 32 | Adam | 0.1334 | 96% | 97% | 97.03% |
| Resnet50 | 50 |  0.00001 | 64 | Adam | 0.1297 | 97% | 96% | 96.41% | 
| VGG16 | 50 |  0.00001 | 32 | Adam | 0.0857 | 95% | 95% | 95.92% |
| VGG16 | 50 |  0.00001 | 64 | Adam | 0.1524 | 97% | 97% | 96.29% | 

#### 2. Ablation Study
Any improvements or modifications of your base model, should be summarized in this table. Feel free to adjust the columns in the table below.

| model | layer_A | layer_B | layer_C | ... | top1_acc | top5_acc |
| --- | --- | --- | --- | --- | --- | --- |
| vit_b_16 | Conv(3x3, 64) x2 | Conv(3x3, 512) x3 | Conv(1x1, 2048) x3 | ... | 77.43% | 80.08% |
| vit_b_16 | Conv(3x3, 32) x3 | Conv(3x3, 128) x3 | Conv(1x1, 1028) x2 | ... | 72.11% | 76.84% |
| ... | ... | ... | ... | ... | ... | ... |

#### 3. Training/Validation Curve
Insert an image regarding your training and evaluation performances (especially their losses). The aim is to assess whether your model is fit, overfit, or underfit.
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
Provide a screenshot of your Business Model Canvas (BMC). Give some explanations, if necessary.

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
This project entitled <b>"YOUR PROJECT TITLE HERE"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
