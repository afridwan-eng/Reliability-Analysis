# Reliability Analysis: Distribution Fitting for Time to Failure (TTF)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?logo=scipy&logoColor=white)](https://scipy.org/)

## 📌 Ringkasan

Proyek ini melakukan **analisis keandalan (reliability analysis)** dengan **fitting distribusi statistik** pada data **Time to Failure (TTF)**. Tujuannya adalah menentukan distribusi probabilitas terbaik yang merepresentasikan pola kegagalan suatu sistem, kemudian menghitung:

- **MTTF (Mean Time to Failure)**
- **Reliability (keandalan) pada waktu tertentu**
- **Waktu penggantian optimal** berdasarkan threshold reliabilitas (khusus Weibull)

## 🧠 Distribusi yang Dianalisis

| Distribusi | Karakteristik | Penggunaan Umum |
|------------|---------------|------------------|
| **Weibull** | Fleksibel (shape parameter β menentukan fase kegagalan) | Paling umum dalam reliability engineering |
| **Exponential** | Constant failure rate (β=1) | Untuk sistem dengan kegagalan acak |
| **Normal** | Simetris, wear-out failure | Komponen mekanik dengan masa pakai terbatas |
| **Log-Normal** | Right-skewed | Waktu perbaikan (MTTR) atau kegagalan korosi |

## 📊 Metode Evaluasi

### Goodness-of-Fit Tests
- **AIC (Akaike Information Criterion)** – Semakin rendah, semakin baik
- **BIC (Bayesian Information Criterion)** – Semakin rendah, semakin baik  
- **KS Statistic (Kolmogorov-Smirnov)** – Mengukur jarak maksimum antara CDF empiris dan teoritis
