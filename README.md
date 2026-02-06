# Insurance Premium Category Predictor

An end-to-end **Machine Learning project** that predicts **insurance premium categories** based on user details using a trained model, served via **FastAPI backend**, and accessed through an interactive **Streamlit frontend**.

This project demonstrates a complete ML pipeline—from raw data, preprocessing, model training, and deployment ready UI—for real-world usage and portfolio showcases.

---

## 🚀 Project Overview

Insurance companies use various factors such as age, lifestyle, income, and occupation to determine how much premium to charge.  
This application predicts the **premium category** (e.g., Low / Medium / High) for an individual based on their details.

✔️ Machine Learning model trained on insurance data  
✔️ FastAPI backend for inference  
✔️ Streamlit app for user inputs and visual results  

---

## 📌 Features

- Interactive UI built with **Streamlit**
- REST API using **FastAPI** for real-time predictions
- Model saved as pickle (`model.pkl`)
- Simple to test locally and extend for deployment
- Effective feature engineering for better model performance :contentReference[oaicite:0]{index=0}

---

## 📂 Repository Structure

```

insurance_premium_detector/
│
├── app.py                # FastAPI backend inference code
├── frontend.py           # Streamlit frontend app
├── model.pkl             # Trained machine learning model
├── insurance.csv         # Dataset used for training & exploration
├── insurance_Model.ipynb # Notebook with EDA + model building
└── README.md             # Project documentation

````

---

## 🧠 How It Works

1. **User Input** – Frontend gathers user details like age, weight, height, income, smoker status, city, occupation.
2. **Preprocessing** – Backend transforms these inputs into engineered features required by the model.
3. **Prediction** – FastAPI POST request returns the predicted premium category.
4. **Display** – Streamlit app shows results interactively.

---

## 💻 Installation & Setup

1. **Clone the repo**

```bash
git clone https://github.com/PriyanshuN19/insurance_premium_detector.git
cd insurance_premium_detector
````

2. **Run the FastAPI server**

```bash
uvicorn app:app --reload --port 8000
```

3. **Run the Streamlit app**

```bash
streamlit run frontend.py
```

4. **Open your browser**

* FastAPI UI: `http://127.0.0.1:8000/docs`
* Streamlit UI: follows printed link

---

## 🧪 API Reference

### **POST /predict**

Request body example:

```json
{
  "age": 30,
  "weight": 65,
  "height": 1.7,
  "income_lpa": 10.0,
  "smoker": false,
  "city": "Mumbai",
  "occupation": "private_job"
}
```

Response example:

```json
{
  "predicted_category": "Medium"
}
```

---

## 🛠️ Tech Stack

| Component      | Technology          |
| -------------- | ------------------- |
| Backend API    | FastAPI             |
| Frontend UI    | Streamlit           |
| Model Training | Scikit-Learn        |
| Deployment     | Local / Cloud Ready |
| Language       | Python              |

---

## 📈 Results & Evaluation

This project uses feature engineering such as:

* BMI from weight and height
* Age groups
* Lifestyle risk factors
* One-hot encoded category features

to better capture the underlying patterns in the insurance dataset, improving model reliability. ([Medium][1])

---

## 📌 Future Improvements

✔ Add confidence scores & class probabilities
✔ Dockerize the app for deployment
✔ Integrate CI/CD workflows
✔ Host on cloud platforms like Heroku / AWS

---

## 👨‍💻 Author

**Priyanshu Nailwal**
Data Science & Machine Learning Enthusiast

---

## 📄 License

This project is open-source — feel free to use and extend!

```

---

If you want, I can also generate **a banner image, badges (e.g., CI, Python version, FastAPI/Streamlit)**, and **live demo links** to make the README look even more professional 🚀.
::contentReference[oaicite:2]{index=2}
```

[1]: https://medium.com/%40amansharmaaa9313/building-an-insurance-premium-category-predictor-with-machine-learning-fastapi-and-streamlit-1c3334f330e8?utm_source=chatgpt.com "Building an Insurance Premium Category Predictor with ..."
