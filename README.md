# SVM Text Classification API

This project implements a text classification system using Support Vector Machines (SVM) in Python. The system is built with FastAPI for serving predictions via an API. It includes model training, prediction, and API routes for interacting with the trained model.

## Project Structure

text_classification/ 
├── app/ │  
├── main.py # FastAPI app │   
├── routes.py # API routes   
├── model/ │   
├── train.py # Model training │   
├── predict.py # Prediction logic   
├── requirements.txt # Dependencies   
└── README.md #

## Features

- **Text Classification**: Classifies text data using a Support Vector Machine (SVM) model. The model can be trained on any dataset with a 'text' and 'label' column.
- **FastAPI Endpoint**: Exposes a simple and efficient REST API to interact with the model. It provides endpoints to classify input text and get prediction results.
- **Model Training**: The `train.py` script trains the model on a given dataset, saving the trained model for later use in prediction.
- **Prediction Results**: For each prediction, the API provides both the predicted class label and the probabilities for all possible labels.

## Requirements

To run the project, you need to install the following dependencies:

- Python 3.6 or higher
- `fastapi` – A modern web framework for building APIs with Python 3.6+.
- `uvicorn` – An ASGI server to serve the FastAPI application.
- `joblib` – Used for saving and loading the trained machine learning model.
- `scikit-learn` – A library that provides the SVM model and other machine learning utilities.
- `pandas` – A powerful data manipulation library for handling datasets.

You can install all required dependencies by running:

```bash
# Install dependencies
pip install -r requirements.txt

# Train the model
python model/train.py

# Start the FastAPI app
uvicorn app.main:app --reload
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- **scikit-learn**: A powerful machine learning library that provides the SVM classifier used in this project.
- **FastAPI**: A modern web framework that enables building high-performance APIs with Python 3.6+.
- **pandas**: A versatile data manipulation library used for handling and processing datasets in this project.
- **joblib**: A Python library used to save and load the trained machine learning model efficiently.
- **Uvicorn**: A fast ASGI server used to run the FastAPI application.
