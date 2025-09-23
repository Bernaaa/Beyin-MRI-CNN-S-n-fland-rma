# Beyin-MRI-CNN-Sınıflandırma
Eğitim/doğrulama değerlendirmesi ve raporlama ile beyin MRG sınıflandırması için CNN modeli.

## Projenin Amacı
Bu proje, beyin MR görüntülerini sınıflandırmak için CNN (Convolutional Neural Network) kullanmaktadır. Amaç, pituitary, notumor, meningioma ve glioma türlerini ayırt edebilen bir model geliştirmektir.

## Veri Seti
- **Kaynak:** [Kaggle Brain MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
- **Train:** 5712 görüntü (4 sınıf)
- **Validation:** 1311 görüntü (4 sınıf)
- **Sınıflar:** pituitary, notumor, meningioma, glioma

## Kullanılan Yöntemler
- CNN mimarisi:
  - Conv2D + MaxPooling katmanları
  - Dense ve Dropout katmanları
  - ReLU ve Softmax aktivasyonları
- Veri çoğaltma (augmentation)
- ModelCheckpoint ve ReduceLROnPlateau callback’leri

## Elde Edilen Sonuçlar
- Eğitim grafikleri: `reports/training_history.png`
- Model: `models/final_model.h5`
- En iyi performans:
  - Epoch: 12
  - Validation Loss: 0.4136
  - Validation Accuracy: 0.8391
  - 
*Kaggle Linki: https://www.kaggle.com/code/geneticat/brain-tumor-cnn-classification-bootcamp/edit

## Kullanım
```bash
git clone <REPO_URL>
cd BrainMRI-CNN-Classification
# Notebook aç ve çalıştır: notebooks/brain_mri_cnn.ipynb
