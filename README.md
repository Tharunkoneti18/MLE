



# Face Recognition via Eigenfaces (PCA + SVM)

This repository contains a Google Colab-based implementation of a facial recognition system. By leveraging **Principal Component Analysis (PCA)** for dimensionality reduction and **Support Vector Machines (SVM)** for classification, the project demonstrates how high-dimensional image data can be compressed into "Eigenfaces" without losing critical identity information.

## 🚀 Project Overview
The "Eigenface" method treats face recognition as a 2D numerical optimization problem. We reduce 2,914-dimensional images (62x47 pixels) into a compact 150-dimensional feature set, allowing for efficient and accurate identity classification.

### Key Features:
* **Dataset:** Uses the *Labeled Faces in the Wild (LFW)* dataset via Scikit-Learn.
* **Dimensionality Reduction:** Implementation of Eigendecomposition to extract principal components.
* **Visualization:** Detailed plots of the "Mean Face," the top 20 Eigenfaces, and reconstruction quality.
* **Machine Learning:** An SVM classifier optimized to recognize individuals based on projected features.

---

## 📂 Repository Structure
* **mle.ipynb`**: The primary Jupyter Notebook containing all code, visualizations, and analysis.
 List of Python dependencies (Scikit-Learn, NumPy, Matplotlib, Seaborn).
* (Optional) Directory containing exported plots of the Eigenfaces and reconstruction comparisons.

---

## 🛠️ The Pipeline
The project follows a standard Computer Vision pipeline:

1.  **Data Acquisition:** Fetching and filtering the LFW dataset for individuals with a minimum of 70 images.
2.  **Preprocessing:** Flattening 2D images into 1D vectors and performing **Mean Subtraction** to center the data.
3.  **Decomposition:**
    * Computing eigenvectors and eigenvalues.
    * Visualizing the **Eigenfaces** (the principal components that capture the most variance).
4.  **Projection:** Mapping the original training and testing data into the 150-dimensional PCA subspace.
5.  **Classification:** Training a C-Support Vector Classifier with an RBF kernel on the reduced data.
6.  **Reconstruction:** Testing the "lossy" nature of PCA by rebuilding faces from a limited number of components.

---

## 📊 Results & Visualization
The notebook provides insights into:
* **Explained Variance:** A plot showing how much information is retained as we increase the number of components.
* **Reconstruction Quality:** A side-by-side comparison showing how a face looks when reconstructed from 10, 50, 100, and 150 components.
* **Model Accuracy:** A classification report and confusion matrix detailing the precision and recall for each identity.

---

## 💻 How to Run
1.  Open the `.ipynb` file in **Google Colab**.
2.  Ensure your runtime is set to Python 3.
3.  Run the cells sequentially. The dataset will be downloaded automatically via `sklearn.datasets`.

---

## 📚 Dependencies
* `numpy`
* `matplotlib`
* `scikit-learn`
* `seaborn`

---

> **Note:** This project is for educational purposes, demonstrating the power of Linear Algebra in modern Machine Learning applications.
