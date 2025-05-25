# 🔊 Spam Detection using Machine Learning

This project implements a machine learning-powered spam detection system that classifies text messages as **Spam** or **Ham (Not Spam)**. Built using FastAPI, it includes training, prediction, and deployment pipelines suitable for real-world use cases.

---

## 📈 Problem Statement

Spam messages—whether emails, SMS, or online comments—can be a nuisance and a security threat. This project builds a system that can automatically detect whether a given message is spam (unwanted) or ham (legitimate).

---

## 🔧 Solution

The solution leverages natural language processing (NLP) and machine learning algorithms. It uses vectorization and classification techniques to build a predictive model trained on labeled message datasets.

---

## 🧪 Tech Stack

* **Backend**: Python, FastAPI
* **ML Algorithms**: Naive Bayes (MultinomialNB, GaussianNB), Support Vector Machine (SVC)
* **DevOps & Deployment**: Docker, GitHub Actions
* **Database**: MongoDB Atlas
* **Cloud Infrastructure**:

  * AWS S3
  * AWS EC2
  * AWS ECR

---

## 📑 Project Structure

```
├── app.py                  # FastAPI application entry point
├── src/                    # Core ML pipeline and components
├── templates/              # HTML templates for UI
├── static/                 # Static files (CSS/JS)
├── requirements.txt        # Required Python packages
├── Dockerfile              # Container configuration
├── .gitignore
├── README.md
```

---

## 🚀 Getting Started

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/spam-detection-app.git
cd spam-detection-app
```

### Step 2: Create a Conda Environment

```bash
conda create --prefix venv python=3.7 -y
conda activate venv/
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Run the Application

```bash
python app.py
```

Visit: `http://localhost:5000/`

### Step 5: Train the Model

```bash
GET http://localhost:5000/train
```

### Step 6: Make Predictions

```bash
POST http://localhost:5000/predict
```

---

## 📅 Run with Docker

### Build the Docker Image

```bash
docker build --build-arg AWS_ACCESS_KEY_ID=<your_key> \
             --build-arg AWS_SECRET_ACCESS_KEY=<your_secret> \
             --build-arg AWS_DEFAULT_REGION=<region> \
             --build-arg MONGODB_URL=<mongo_url> .
```

### Run the Docker Container

```bash
docker run -d -p 5000:5000 <image_name>
```

---

## 🔢 Machine Learning Models Used

* [Multinomial Naive Bayes](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html)
* [Gaussian Naive Bayes](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html)
* [Support Vector Classifier (SVC)](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)

> GridSearchCV is used for hyperparameter tuning.

---

## 📂 Project Highlights

* Modular ML pipeline: data ingestion, transformation, model training, evaluation
* Integrated FastAPI server for real-time prediction
* Dockerized app for deployment
* Environment variables for secure deployment (MongoDB, AWS, etc.)

---

## 📊 Conclusion

This project is a scalable, modular, and production-ready spam detection system. It’s suitable for deployment in SMS gateways, email servers, or content moderation platforms.

---


