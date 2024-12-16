📊 MLB Wins Predictor
⚾ Overview
The MLB Wins Predictor is a machine learning project that forecasts the number of wins a Major League Baseball (MLB) team will achieve in a season based on key performance metrics. This project utilizes a Keras neural network model trained on historical team data, with a FastAPI backend serving real-time predictions via a RESTful API.

🚀 Features
Machine Learning Model: Predicts team wins using a neural network.
FastAPI Endpoint: Serves predictions via a /predict endpoint.
Scalable Deployment: Deployed on an AWS EC2 instance with Uvicorn.
Model Training Pipeline: Includes feature selection, hyperparameter tuning, and model evaluation.
📂 Project Structure
plaintext
Copy code
mlb-wins-predictor/
│
├── app.py                # FastAPI application for serving predictions
├── mlb_wins_model.h5     # Trained Keras model (HDF5 format)
├── scaler.pkl            # StandardScaler for data normalization
├── pitching_batting_combined_df.csv  # Combined dataset for model training
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies
└── tuner_results/        # Keras Tuner results for hyperparameter tuning
📈 Model Training Workflow
Data Preparation:

The dataset pitching_batting_combined_df.csv contains various performance metrics (batting and pitching).
Features are selected based on their importance to predict wins (W).
Feature Selection:

Used a Random Forest model to identify the top 10 features contributing to win predictions:
WAR, RS, SO_y, SV, ER, R_y, SH, GB, ERA, BB_y
Model Training:

Neural network with two dense layers, dropout for regularization, and ReLU activations.
Hyperparameter tuning with Keras Tuner to optimize model architecture.
Model Evaluation:

Evaluated on a test set using Mean Absolute Error (MAE) and Mean Squared Error (MSE).
🛠️ Tech Stack
Python (3.10)
TensorFlow / Keras
Scikit-Learn
FastAPI
Uvicorn
Joblib
AWS EC2 (Deployment)
⚙️ Setup Instructions
1. Clone the Repository
bash
Copy code
git clone https://github.com/yourusername/mlb-wins-predictor.git
cd mlb-wins-predictor
2. Create a Virtual Environment
bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install Dependencies
bash
Copy code
pip install -r requirements.txt
4. Ensure Model and Scaler Files Are Present
Place the following files in the root directory:

mlb_wins_model.h5: Trained Keras model.
scaler.pkl: StandardScaler for input data normalization.
5. Run the FastAPI App
bash
Copy code
uvicorn app:app --host 0.0.0.0 --port 8000
The API should now be running at http://0.0.0.0:8000.

🔮 Usage
Endpoint: /predict
Method: POST

Content-Type: application/json

Request Format:

json
Copy code
{
  "data": [[45, 850, 1300, 45, 520, 650, 30, 1400, 3.50, 450]]
}
Example Response:

json
Copy code
{
  "predictions": [90.5]
}
Using curl:
bash
Copy code
curl -X 'POST' \
  'http://your_server_ip:8000/predict' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "data": [[45, 850, 1300, 45, 520, 650, 30, 1400, 3.50, 450]]
  }'
📊 Example Data
Typical input values for the model based on MLB team stats:

Feature	Description	Example Value
WAR	Wins Above Replacement	45
RS	Runs Scored	850
SO	Strikeouts by pitchers	1300
SV	Saves	45
ER	Earned Runs	520
R	Runs allowed by pitchers	650
SH	Sacrifice Hits	30
GB	Ground Balls	1400
ERA	Earned Run Average	3.50
BB	Walks allowed by pitchers	450
✅ Testing the API
Go to Docs: Open the Swagger UI to test the API via a user-friendly interface:

plaintext
Copy code
http://your_server_ip:8000/docs
Interactive API Documentation: Use the Swagger interface to send POST requests and view responses.

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

👨‍💻 Author
Your Name
LinkedIn: Your LinkedIn Profile
GitHub: Your GitHub Profile
🌟 Acknowledgments
TensorFlow and Keras for model building.
FastAPI for creating the API.
AWS EC2 for deployment.
Scikit-Learn for data preprocessing and feature selection.
