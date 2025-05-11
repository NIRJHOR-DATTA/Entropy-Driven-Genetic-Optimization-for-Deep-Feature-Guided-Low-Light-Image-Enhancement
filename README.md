# Entropy-Driven-Genetic-Optimization-for-Deep-Feature-Guided-Low-Light-Image-Enhancement

This repository contains the original implementation of **"Entropy-Driven Genetic Optimization for Deep Feature Guided Low-Light Image Enhancement"**.

---

## 📚 Overview

Our research consists of two major phases:

1. **Unpaired Image Enhancement:**  
   We evaluate how our proposed approach performs on unpaired low-light image datasets.

2. **Generalization with Ground Truth Data:**  
   In this phase, we test how well the **CIDNet** generalizes to other datasets where **ground truth is available**, using the previously trained weights.

---

## 💡 Image Enhancement on Unpaired Datasets

You can test our image enhancement method on various datasets using the provided notebooks:

- **LIME and DICE Datasets**  
  👉 Run [`LIME-DICE.ipynb`](LIME-DICE.ipynb)

- **MEF Dataset**  
  👉 Run [`MEF.ipynb`](MEF.ipynb)

- **NPE Dataset**  
  👉 Run [`NPE.ipynb`](NPE.ipynb)

- **VV Dataset**  
  👉 Run [`VV.ipynb`](VV.ipynb)

---

## 📊 Quality Assessment Metrics

To evaluate the performance of our enhanced images using **BRISQUE** and **NIQE** scores:

👉 Run [`brisque_nique.ipynb`](brisque_nique.ipynb)

---

## 🧪 Citation

If you use this work in your research, please consider citing our paper (citation to be added).

---

## 📎 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
