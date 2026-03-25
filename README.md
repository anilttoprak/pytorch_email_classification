# Linear Classification with PyTorch

E-posta verisi kullanarak ikili sınıflandırma (binary classification) problemi. Aktivasyon fonksiyonu olmayan lineer modelin e-posta sınıflandırmasındaki performansı incelenmektedir.

## Problem

Konu biçimselliği (`subject_formality_score`) ve gönderici ilişki skoru (`sender_relationship_score`) özelliklerine bakarak e-postanın tipini tahmin etmek. (0: normal, 1: spam)

## Veri Seti

- 1000 örnek, 2 özellik, 1 hedef sütun
- %80 eğitim / %20 test olarak bölündü

## Model Mimarisi

Giriş (2) → Linear(2→5) → Linear(5→1) → Çıkış



Aktivasyon fonksiyonu olmadığı için model düz bir karar sınırı öğrenir. Veri lineer ayrılabilir olduğundan ~%95 doğruluğa ulaşır.

## Sonuçlar

| Epoch | Train Accuracy | Test Accuracy |
|-------|---------------|---------------|
| 0     | ~%50          | ~%52          |
| 50    | ~%71          | ~%77          |
| 95    | ~%95          | ~%95          |

## Kullanılan Teknolojiler

- Python
- PyTorch
- Scikit-learn
- Matplotlib / Seaborn / NumPy

## Çalıştırma

```bash
pip install torch pandas scikit-learn matplotlib seaborn numpy
jupyter notebook pytorch_linear.ipynb
