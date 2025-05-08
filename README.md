
# 🌾 Crop Recommendation API

A lightweight, machine learning–powered REST API that predicts the most suitable crop to cultivate based on soil and environmental parameters. Built with Flask and deployed on Vercel, this API is ideal for integration into agricultural decision-making tools, mobile apps, or dashboards.

## 🚀 Live Demo

👉 [api-crop.vercel.app](https://api-crop.vercel.app)

## 📦 Features

* Predicts optimal crops using a hybrid machine learning model.
* Accepts key soil and climate inputs: nitrogen (N), phosphorus (P), potassium (K), temperature, humidity, pH, and rainfall.
* Returns a recommended crop label.
* Deployed as a serverless API on Vercel for fast and scalable access.

## 🧪 API Usage

### Endpoint

```

POST /predict
```



### Request Payload (JSON)

```json
{
  "N": 90,
  "P": 42,
  "K": 43,
  "temperature": 22.5,
  "humidity": 80,
  "ph": 6.5,
  "rainfall": 200
}
```



### Response

```json
{
  "prediction": "rice"
}
```



## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/priyanshufox/api-crop.git
cd api-crop
```



### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```



### 3. Install Dependencies

```bash
pip install -r requirements.txt
```



### 4. Run the API Locally

```bash
python app.py
```



The API will be available at `http://localhost:5000/predict`.

## 🧠 Model Artifacts

The repository includes the following pre-trained model files:

* `crop_recommendation_hybrid.pkl` – the core prediction model
* `label_encoder.pkl` – encodes crop labels
* `scaler.pkl` – standardizes input features([GitHub][1], [GitHub][2])

These files are loaded automatically when the API starts.

## 📁 Project Structure

```

api-crop/
├── app.py
├── requirements.txt
├── crop_recommendation_hybrid.pkl
├── label_encoder.pkl
├── scaler.pkl
└── README.md
```



## 📤 Deployment

This API is deployed on Vercel using its Python serverless runtime. To deploy your own version:([GitHub][3])

1. Install the Vercel CLI:

   ```bash
   npm install -g vercel
   ```



2. Deploy the project:

   ```bash
   vercel
   ```



Ensure that all model files are included in your deployment.

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

For more projects by Priyanshu Rathore, visit [github.com/priyanshufox](https://github.com/priyanshufox).([GitHub][4])

---

[1]: https://github.com/priyanshufox/cropPredictionAPI/blob/main/crop_recommendation_hybrid.pkl?utm_source=chatgpt.com "cropPredictionAPI/crop_recommendation_hybrid.pkl at main - GitHub"
[2]: https://github.com/priyanshufox/api-crop?utm_source=chatgpt.com "GitHub - priyanshufox/api-crop"
[3]: https://github.com/priyanshufox/crop-api?utm_source=chatgpt.com "GitHub - priyanshufox/crop-api"
[4]: https://github.com/priyanshufox?utm_source=chatgpt.com "priyanshufox (Priyanshu Rathore) - GitHub"
