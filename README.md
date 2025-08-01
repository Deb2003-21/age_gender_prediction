# Age and Gender Prediction Model

This project implements an age and gender prediction system using a Convolutional Neural Network (CNN). The model is served using a Flask web server and can be accessed from a website to display predictions in real time.

## Features

- **CNN-Based Prediction**: Utilizes a deep learning model to predict both age and gender from input images.
- **Regression for Gender, Classification for Age**:  
  - **Gender Prediction** is performed as a regression task.
  - **Age Prediction** is performed as a classification task.
- **Flask API**: The trained model is wrapped with a Flask server, providing REST API endpoints for inference.
- **Web Integration**: A front-end website communicates with the Flask server, allowing users to upload images and view prediction results instantly.

## How It Works

1. **Model Training**:  
   - A CNN is trained on a labeled dataset containing images with age and gender annotations.
   - The model is designed to:
     - Predict gender as a regression output.
     - Predict age as a classification output.

2. **Flask Server**:  
   - The trained model is loaded into a Flask application.
   - The server exposes endpoints (e.g., `/predict`) to accept image uploads and return predictions as JSON.

3. **Website Frontend**:  
   - Users can upload images through the website interface.
   - The frontend sends the image to the Flask server and displays the predicted age and gender on the page.
     

## Result
<img width="874" height="874" alt="Screenshot 2025-08-01 124019" src="https://github.com/user-attachments/assets/7c0f1bd8-2862-4a78-8837-359d36ebe1ea" />



### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/age-gender-prediction.git
cd age-gender-prediction
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Run the Flask Server

```bash
python app.py
```

### 4. Launch the Website

- Open the `index.html` file in your browser, or serve it using a simple HTTP server if needed.
- Upload an image and view the prediction results.

## Project Structure

```
age-gender-prediction/
├── model/                # Trained CNN model files
├── static/               # Static files for the website (CSS, JS)
├── app.py                # Flask server script
└── README.md
```

## Example

1. Upload an image via the website.
2. The image is sent to the Flask server.
3. The server returns:
    ```json
    {
      "age": 27,
      "gender": "Male"
    }
    ```
4. Results are displayed on the site.

## Dependencies

- Python 3.x
- Flask
- TensorFlow / Keras or PyTorch (depending on your implementation)
- OpenCV, NumPy, and other standard libraries

## Acknowledgements

- Pre-trained models and datasets for age and gender prediction
- Flask documentation
- Front-end libraries (if any)

---

Feel free to customize this README for your specific implementation and add further instructions as needed!
