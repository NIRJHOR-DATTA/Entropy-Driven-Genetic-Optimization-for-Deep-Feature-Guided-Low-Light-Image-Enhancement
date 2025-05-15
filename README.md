# Entropy-Driven-Genetic-Optimization-for-Deep-Feature-Guided-Low-Light-Image-Enhancement

This repository contains the official implementation of  
**"Entropy-Driven Genetic Optimization for Deep Feature Guided Low-Light Image Enhancement"**.

---

## 📚 Overview

Our research consists of two major phases:

1. **Unpaired Image Enhancement:**  
   We evaluate how our proposed approach performs on **unpaired low-light image datasets**.

2. **Generalization with Ground Truth Data:**  
   We test how well the **CIDNet** generalizes to other datasets where **ground truth is available**, using the previously trained weights.

---

## 💡 Image Enhancement on Unpaired Datasets

Run the following notebooks to apply image enhancement on respective datasets:

- **DICM Dataset**  
  👉 Run [DICM.ipynb`]
- **DICM Dataset without local search**  
  👉 Run [`DCIM nsga2-no local search.ipynb`]
- **DICM Dataset with NSGA-II only**  
  👉 Run [`DCIM-nsga2 only updated.ipynb`]
- **DICM Dataset without adaptive mutation**  
  👉 Run [`DCIM-no adaptive mutation.ipynb`]
- **LIME Dataset**  
  👉 Run [`LIME.ipynb`]
- **LIME Dataset without local search**  
  👉 Run [`LIME-no local search.ipynb`]
- **LIME Dataset with NSGA-II only**  
  👉 Run [`LIME-nsga2 only.ipynb`]
- **LIME Dataset without adaptive mutation**  
  👉 Run [`LIME-no adaptive mutation.ipynb`]
- **MEF Dataset**  
  👉 Run [`MEF Enhancement-updated.ipynb`]
- **MEF Dataset without local search**  
  👉 Run [`MEF-no local search-updated.ipynb`]
- **MEF Dataset with NSGA-II only**  
  👉 Run [`MEF-NSGA2 ONLY UPDATED.ipynb`]
- **MEF Dataset without adaptive mutation**  
  👉 Run [`MEF-no adaptive mutation-updated.ipynb`]
- **NPE Dataset**  
  👉 Run [`NPE Enhancement.ipynb`]
- **NPE Dataset without local search**  
  👉 Run [`NPE-no local search-updated.ipynb`]
- **NPE Dataset with NSGA-II only**  
  👉 Run [`NPE-NSGA2 ONLY-updated.ipynb`]
- **NPE Dataset without adaptive mutation**  
  👉 Run [`NPE-no adaptive mutation-updated.ipynb`]
- **VV Dataset**  
  👉 Run [`VV_enhancement.ipynb`]
- **VV Dataset without local search**  
  👉 Run [`VV-no local search.ipynb`]
- **VV Dataset with NSGA-II only**  
  👉 Run [`VV-NSGA2 ONLY.ipynb`]
- **VV Dataset without adaptive mutation**  
  👉 Run [`VV-no adaptive mutation.ipynb`]

---

## 📊 Quality Assessment (BRISQUE & NIQE Scores)

To evaluate the quality of enhanced images using **BRISQUE** and **NIQE**:

👉 For DICE, Run [`brisque,niqe-DICM.ipynb`]
👉 For LIME, Run [`brisque,niqe-LIME.ipynb`]
👉 For MEF, Run [`brisque,niqe-MEF.ipynb`]
👉 For NPE, Run [`brisque,niqe-NPE.ipynb`]
👉 For VV, Run [`brisque,niqe-VV.ipynb`]

---
## 💡 Part II – Generalization on MIT-5K Subset

We randomly selected **100 raw images** (and their 5 retouched versions a–e) from the MIT-5K dataset. For each retouch version, run all three methods:

| Version | Our Approach                                  | CIDNet (LoLV1)                                        | CIDNet (Generalization)                                 |
|---------|-----------------------------------------------|-------------------------------------------------------|---------------------------------------------------------|
| a       | `mit5k subset a.ipynb`                        | `mit5k_lolv1_CIDNet-part a.ipynb`                     | `mit5k_generalization_CIDNet-part a.ipynb`              |
| b       | `mit5k subset b.ipynb`                        | `mit5k_lolv1_CIDNet-part b.ipynb`                     | `mit5k_generalization_CIDNet-part b.ipynb`              |
| c       | `mit5k subset c.ipynb`                        | `mit5k_lolv1_CIDNet-part c.ipynb`                     | `mit5k_generalization_CIDNet-part c.ipynb`              |
| d       | `mit5k subset d.ipynb`                        | `mit5k_lolv1_CIDNet-part d.ipynb`                     | `mit5k_generalization_CIDNet-part d.ipynb`              |
| e       | `mit5k subset e.ipynb`                        | `mit5k_lolv1_CIDNet-part e.ipynb`                     | `mit5k_generalization_CIDNet-part e.ipynb`              |

To compute **PSNR**, **SSIM**, and **Entropy** for each method/version, run:

| Version | Final Notebook(s)                                                          |
|---------|----------------------------------------------------------------------------|
| a       | `mit5k-part-a-final-version.ipynb`                                         |
| b       | `mit5k-part-b-final-version.ipynb`                                         |
| c       | `mit5k-part-c.ipynb` and `mit5k-part-c-generalize.ipynb`                   |
| d       | `mit5k-part-d.ipynb` and `mit5k-part-d-generalize.ipynb`                   |
| e       | `mit5k-part-e.ipynb` and `mit5k-part-e-generalize.ipynb`                   |

---

## 📈 Quantitative Evaluation

### 1. BRISQUE & NIQE on Unpaired Datasets

| Method         | DICM (B/N)    | LIME (B/N)    | MEF (B/N)     | NPE (B/N)     | VV (B/N)      |
| -------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| KinD       | 48.72 / 5.15  | 39.91 / 5.03  | 49.94 / 5.47  | 36.85 / 4.98  | 50.56 / 4.30  |
| ZeroDCE     | 27.56 / 4.58  | 20.44 / 5.82  | 17.32 / 4.93  | 20.72 / 4.53  | 34.66 / 4.81  |
| RUAS      | 38.75 / 5.21  | 27.59 / 4.26  | 23.68 / 3.83  | 47.85 / 5.53  | 38.37 / 4.29  |
| LLFlow    | 26.36 / 4.06  | 27.06 / 4.59  | 30.27 / 4.70  | 28.86 / 4.67  | 31.67 / 4.04  |
| SNR-Aware  | 37.35 / 4.71  | 39.22 / 5.74  | 31.28 / 4.18  | 26.65 / 4.32  | 78.72 / 9.87  |
| PairLIE     | 33.31 / 4.03  | 25.23 / 4.58  | 27.53 / 4.06  | 28.27 / 4.18  | 39.13 / 3.57  |
| CIDNet     | 21.47 / 3.79  | **16.25 / 4.13**  | **13.77 / 3.56**  | **18.92** / 3.74  | 30.63 / 3.21  |
| **Ours**       | **17.99 / 3.57** | 21.76 / 4.43 | 25.19 / 4.14 | 23.10 / **3.58** | **25.91 / 2.92** |

> **B** = BRISQUE, **N** = NIQE. Lowest values in each column are **bold**.

---

### 2. PSNR, SSIM & Entropy on MIT-5K Subsets

| Version | Method                | PSNR    | SSIM    | Entropy |
| ------- | --------------------- | ------- | ------- | ------- |
| a       | CIDNet-LoLV1          | 9.7833  | 0.4502  | 7.0637  |
|         | CIDNet-Generalization | 14.3492 | 0.5179  | 7.3831  |
|         | **Ours**              | **15.8024** | **0.5413** | **7.6369** |
| b       | CIDNet-LoLV1          | 8.8100  | 0.4483  | 6.9222  |
|         | CIDNet-Generalization | 13.7503 | 0.5237  | 7.2718  |
|         | **Ours**              | **15.9918** | **0.5627** | **7.6397** |
| c       | CIDNet-LoLV1          | 9.7833  | 0.4502  | 7.0637  |
|         | CIDNet-Generalization | 8.8172  | 0.4372  | 6.9389  |
|         | **Ours**              | **15.0147** | **0.5353** | **7.6791** |
| d       | CIDNet-LoLV1          | 8.2457  | 0.4502  | 7.0637  |
|         | CIDNet-Generalization | 14.0834 | 0.4364  | 6.6912  |
|         | **Ours**              | **15.5798** | **0.5516** | **7.6060** |
| e       | CIDNet-LoLV1          | 8.1494  | 0.4251  | 6.7677  |
|         | CIDNet-Generalization | 13.3932 | 0.5057  | 7.3300  |
|         | **Ours**              | **14.7874** | **0.5283** | **7.6903** |

-----
## 🧪 Citation

If you use this work in your research, please consider citing our paper (citation to be added here once published).

---

## 📎 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
