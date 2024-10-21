
# **One-Class SVM: Anomaly Detection with Diabetic Patients Dataset**

## **Overview**
This project demonstrates the use of **One-Class SVM** to detect anomalies by identifying diabetic patients from a dataset. One-Class SVM is a powerful tool for **anomaly detection** or **outlier detection**, where the goal is to learn the characteristics of a dominant class and flag unusual data points.

## **Project Structure**
**svm_mono_classe.py**:  
The main script that:
- Loads the diabetes dataset.
- Separates the data into diabetic and non-diabetic patients.
- Trains the One-Class SVM using **linear** and **RBF kernels**.
- Evaluates the model with **accuracy** and **AUC (Area Under the Curve)** metrics.

## **How to Run the Code**

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/one-class-svm.git
   cd one-class-svm
   ```

2. **Install Dependencies:**  
   Make sure you have Python and the required libraries installed. You can install dependencies using:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Script:**  
   Execute the `svm_mono_classe.py` script:
   ```bash
   python svm_mono_classe.py
   ```

## **How the Code Works**

1. **Data Loading and Preprocessing:**  
   - The dataset is split into two parts: **diabetic patients** and **non-diabetic patients**.
   - Labels are prepared, with non-diabetic patients relabeled as `-1` (anomalies).

2. **Training the One-Class SVM:**  
   - The model is trained **only on diabetic patients** using:
     - **Linear kernel:** Works well with linearly separable data.
     - **RBF kernel:** Captures non-linear patterns for complex data.

3. **Making Predictions:**  
   - The trained model predicts whether a new patient is diabetic or non-diabetic.

4. **Model Evaluation:**  
   - **Accuracy:** Measures the percentage of correct predictions.
   - **AUC (Area Under the Curve):** Evaluates the model's ability to distinguish between diabetic and non-diabetic patients.

## **Results**

- **Accuracy:** The script outputs the percentage of correct predictions.
- **AUC:** Shows the model's performance in distinguishing true positives from false positives.

## **Why Use One-Class SVM?**

One-Class SVM is ideal when:
- **Training data is imbalanced** (more normal cases than anomalies).
- **We want to detect anomalies or outliers** (e.g., fraudulent transactions, network intrusions).
- **We have examples from only one class** (as in this project with diabetic patients).

## **Technologies Used**
- **Python**
- **scikit-learn** for One-Class SVM and metrics
- **NumPy** and **pandas** for data handling

## **Contribute**
Feel free to open issues or submit pull requests to improve the code or documentation.

## **License**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## **Author**
Developed by **Your Name**.

---

Happy coding! 🚀
