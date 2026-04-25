# 📚 Book Recommendation System with Federated Learning Simulation

## 🚀 Overview

This project implements a **Book Recommendation System** using collaborative filtering techniques, enhanced with a **Federated Learning simulation** to demonstrate privacy-preserving model training. The system processes user-book interaction data, builds a recommendation model, and provides an interactive interface using Streamlit.

The project was developed in a Jupyter/Colab environment and includes end-to-end steps: data preprocessing, model building, evaluation, and deployment.

---

## 🧠 Key Features

* 📊 Data preprocessing and cleaning pipeline
* 📖 User-item matrix creation for collaborative filtering
* 🤖 Recommendation model using **Non-negative Matrix Factorization (NMF)**
* 🔐 Simulated **Federated Learning** across multiple clients
* 📈 Model evaluation using RMSE
* 🌐 Interactive web app using **Streamlit**
* 🚀 Public deployment using **ngrok**

---

## 🏗️ Project Architecture

```
Data Input (Excel Dataset)
        ↓
Data Cleaning & Preprocessing
        ↓
User-Item Matrix Construction
        ↓
Model Training (NMF)
        ↓
Federated Learning Simulation
        ↓
Evaluation (RMSE)
        ↓
Streamlit Web Application
        ↓
Deployment via ngrok
```

---

## 📂 Dataset

The system uses a dataset containing:

* `user_id` – Unique identifier for users
* `book_id` – Unique identifier for books
* `rating` – User rating (1–5 scale)
* `timestamp` – Interaction timestamp
* `genre` – Book genre
* `author` – Book author

### Data Preprocessing Steps:

* Removed missing values in critical columns
* Filled missing `genre` and `author` with `"Unknown"`
* Normalized ratings to a 0–1 scale
* Removed duplicate user-book interactions
* Ensured valid rating range (1–5)

---

## ⚙️ Technologies Used

* **Python**
* **Pandas, NumPy** – Data manipulation
* **Scikit-learn** – Machine learning (NMF, similarity, evaluation)
* **Matplotlib** – Visualization
* **Streamlit** – Web app interface
* **pyngrok** – Public deployment
* **Google Colab** – Development environment

---

## 🤖 Recommendation Approach

### 1. Collaborative Filtering

* Constructed a **user-item interaction matrix**
* Missing values filled with zeros
* Captures user preferences implicitly

### 2. Matrix Factorization (NMF)

* Decomposes user-item matrix into latent features
* Learns hidden patterns between users and books
* Enables personalized recommendations

### 3. Similarity Computation

* Used **cosine similarity** to find similar users/items

---

## 🔐 Federated Learning Simulation

To simulate decentralized learning:

* Users are split into multiple **clients**
* Each client trains a local model on its subset of data
* Model updates are aggregated to form a global model

This approach demonstrates:

* Data privacy preservation
* Distributed learning capability
* Scalability across multiple nodes

---

## 📈 Model Evaluation

The model performance is evaluated using:

* **Root Mean Squared Error (RMSE)**
* Train-test split validation

This ensures the recommendation quality is quantitatively assessed.

---

## 🌐 Streamlit Web Application

The project includes a Streamlit app that allows users to:

* View recommendations dynamically
* Interact with the model
* Explore results visually

### Run the App

```bash
streamlit run app.py
```

---

## 🚀 Deployment (ngrok)

To expose the app publicly:

```bash
ngrok.connect(8501)
```

This generates a public URL to access the Streamlit interface remotely.

---

## 📦 Installation

Install all dependencies using:

```bash
pip install streamlit pandas numpy scikit-learn matplotlib pyngrok
```

---

## ▶️ How to Run

1. Upload the dataset (`.xlsx`) file
2. Run the notebook step-by-step in Colab or Jupyter
3. Generate the `app.py` file
4. Start the Streamlit server
5. Use ngrok to create a public link

---

## ⚠️ Notes

* The dataset file must be present in the working directory
* Large datasets may increase computation time
* ngrok requires an authentication token for public URLs

---

## 📌 Future Improvements

* Replace simulation with real federated learning frameworks (e.g., TensorFlow Federated)
* Add deep learning-based recommendation models
* Improve UI/UX of the Streamlit app
* Deploy on cloud platforms (AWS/GCP/Azure)
* Incorporate real-time user feedback

---

## 👨‍💻 Conclusion

This project demonstrates how recommendation systems can be combined with federated learning principles to build scalable and privacy-aware solutions. It bridges practical machine learning implementation with modern distributed learning concepts.

---
