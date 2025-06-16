#  Support Vector Machine (SVM) Optimization Assignment

This project performs hyperparameter optimization for Support Vector Machine (SVM) classifiers using a random search strategy. The goal is to evaluate performance across 10 different data splits and identify the best hyperparameters for each.

---

## 📊 Dataset Used

- **Digits dataset** from `sklearn.datasets`
- Classification task with **10 classes (digits 0–9)**

---

## 🔧 Optimization Strategy

For each of the 10 random train-test splits:
- 100 random combinations of the following SVM parameters were tested:
  - **Kernel**: `linear`, `poly`, `rbf`, `sigmoid`
  - **C**: Logarithmically spaced between 0.1 and 100
  - **Gamma**: `scale`, `auto`
- Best configuration selected based on highest test accuracy.

---

## ✅ Final Results

| Sample # | Best Accuracy | Best SVM Parameters |
|----------|----------------|---------------------|
| S1       | 0.987037       | Kernel=rbf, C=1.0, Gamma=auto |
| S2       | 0.97963        | Kernel=linear, C=0.21544346900318834, Gamma=scale |
| S3       | 0.988889       | Kernel=poly, C=21.54434690031882, Gamma=scale |
| S4       | 0.992593       | Kernel=poly, C=21.54434690031882, Gamma=scale |
| S5       | 0.985185       | Kernel=poly, C=10.0, Gamma=scale |
| S6       | 0.985185       | Kernel=poly, C=21.54434690031882, Gamma=scale |
| S7       | 0.988889       | Kernel=rbf, C=2.1544346900318834, Gamma=scale |
| S8       | 0.987037       | Kernel=poly, C=100.0, Gamma=scale |
| S9       | 0.985185       | Kernel=poly, C=100.0, Gamma=auto |
| S10      | 0.988889       | Kernel=poly, C=46.41588833612777, Gamma=scale |

🎯 **Best Performing Sample**: `S4` with **Accuracy = 0.992593**

---

## 📈 Convergence Plot – Sample S4

Below is the fitness convergence plot over 100 iterations for Sample S4:

![SVM Convergence for S4]![Screenshot 2025-04-19 172200](https://github.com/user-attachments/assets/262b8081-db05-4bdc-8a23-e0ab12999c92)


---

## 🛠️ Tools & Libraries

- Python 3.x
- `scikit-learn`
- `numpy`, `pandas`
- `matplotlib`
- `tqdm`
- `tabulate`

---
