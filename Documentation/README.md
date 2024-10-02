# Done By

Asma'a Anees Alariqi / 202170289 / asmaalariqi68@gmail.com 

# Overview

This project is a simple web application that detects whether an uploaded image is real or a deepfake using a Convolutional Neural Network (CNN). The model is integrated into a Flask web application, allowing users to upload images through a web interface and get predictions about whether the image is classified as "Real" or "Fake."
Deepfakes are synthetic media in which a person’s likeness is replaced with someone else’s. This project aims to create a system that can accurately identify deepfake images, enhancing awareness and trust in digital media.


# Project Structure

├── Data/                                 # Directory where datasets images are saved

├── DeepFake.ipynb                        # Flask application file

├── model/deepfake_detector.h5            # Pre-trained deepfake detection model

├── Documentation/README.md               # Project documentation

├── templates/                            # HTML template folder 

├──Test/                                  # Directory where images used for test

├──uploads/                               # Directory where uploaded images are saved

└── requirements.txt                      # Required Python packages



* uploads/: Directory where uploaded images are saved.

* DeepFake.ipynb : The main file that contains the code and the Flask application and routes.

* deepfake_model.h5: Pre-trained deepfake detection model.

* README.md: Documentation for the project.

* requirements.txt: List of Python dependencies for the project.



# Requirements

## Main libraries used:

* matplotlib (for plot and show the image)

* sklearn (for machine learning tasks like classification, regression, clustering, and dimensionality reduction)

* Flask (for building the web application)

* OpenCV/PIL (for image processing)

* TensorFlow/Keras (for loading and using the deepfake detection model)

* NumPy (for numerical operations)

## Datasets
https://universe.roboflow.com/deepfake-q1kew/deepfake-detection-h3was/dataset/1


# How to Run

1. Clone the repository and navigate to the project directory.

git clone https://github.com/Asmmmmma/Deepfake-Image-Detection-Using-Deep-Learning-A-CNN-Based-Flask-Web-Application

cd deepfake-detector

---
2. Activate Virtual env

virtualenv venv

python3 -m venv venv

source venv/bin/activate

---
3. Install the required dependencies:

pip install -r requirements.txt

---
4. Run the Flask app:

python DeepFake.ipynb

---
5. Access the web interface: Open your browser and go to:

http://127.0.0.1:5000

---
6. Upload an Image:

Upload an image for deepfake detection.

After uploading, the model will predict if the image is real or fake and display the result on the page.




# Code Explanation

1. Image Processing:

* Uploaded images are resized to 128x128 pixels for model compatibility.

* The image is normalized (pixel values scaled to [0, 1]).

* The image is reshaped to match the input shape of the CNN model (1, 128, 128, 3).



---
2. Deepfake Prediction:

* The pre-trained model is used to predict the image category.

* If the prediction is less than 0.5, the image is classified as Real, otherwise, it is classified as Fake.


---
3. Web Interface:

* The project uses Flask to create a simple web interface where users can upload images.

* Upon submission, the image is processed and the result (Real or Fake) is displayed.


---
4. Flask Routes:

* /: The home page where users can upload an image.

* /upload: Handles the image upload and calls the prediction function.




# Future Improvements

* Add support for video files: Extend the functionality to allow users to upload videos for deepfake detection.

* Improve model accuracy: Retrain the model with a larger dataset to improve detection performance.

* Implement email alerts: Notify users through email if a deepfake image is detected.
