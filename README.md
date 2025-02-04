## MNIST Handwritten Digit Classifier Project  

This project builds and deploys a machine learning model to recognize handwritten digits using the MNIST dataset.

### Tools:
- Python 3.x
- FastAPI
- NumPy
- Scikit-learn
- PIL (Pillow)
- Uvicorn 
  
### Model Training  

- The dataset (`mnist_784`) is loaded using `fetch_openml`.  
- The data is split into training and test sets.  
- A `RandomForestClassifier` is trained on the dataset and evaluated on the test set.  
- The trained model is saved as `mnist_model.pkl` using `pickle`.  

### FastAPI Backend for Image Prediction  

- A **FastAPI** server is set up to handle image uploads.  
- The uploaded image is preprocessed:  
  - Converted to grayscale  
  - Resized  
  - Reshaped  
- The trained model predicts the digit from the processed image.  
- The API returns the predicted digit as JSON.  

### Frontend Interface  

- A simple **HTML** page allows users to upload an image of a handwritten digit.  
- The frontend sends the image to the **FastAPI** backend for prediction.  
- The predicted digit is displayed to the user.  
