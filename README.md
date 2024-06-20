# Duplicate_Question_Checker


Here’s a step-by-step guide for users to run the Quora duplicate question detection application:

### Step-by-Step Guide

#### 1. Clone the Repository
First, clone the GitHub repository to your local machine.
Unzip the App.zip file (I have to zip it because the file size was to large).

```sh
git https://github.com/OmarBaig05/Duplicate_QuestionCheker_OnQuoraDataset.git
cd App
```
##### You can see the working process in the Initial Work folder or if you want to run the application open the 'App' folder.
#### 2. Create a Virtual Environment
It's a good practice to create a virtual environment to manage dependencies.

```sh
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

#### 3. Install Dependencies
Install the required Python packages listed in `requirements.txt`.

```sh
pip install -r requirements.txt
```

#### 4. Download NLTK Data
```sh
python -c "import nltk; nltk.download('stopwords')"
```

#### 5. Ensure Pre-trained Models are Available
Make sure the pre-trained models (`rf_model_trained` and `word2vec_model`) are available in the repository if you want to retrain the model then run the TrainCode.py file, uncomment the commented code and comment the those codes that includes the statement pickle.load().

#### 6. Run the Flask Application
Start the Flask application by running `app.py`.

```sh
python app.py
```

The application should now be running locally on `http://127.0.0.1:5000/`. See the terminal to see the local host url.

#### 7. Access the Application
Open a web browser and go to local host url(`http://127.0.0.1:5000/`) to access the application.

### Example Directory Structure
Here's an example of what your directory structure looks like:

```
App/
│
├── app.py
├── utils.py
├── TrainingCode.py
├── requirements.txt
├── rf_model_trained  # Pre-trained RandomForest model file
├── word2vec_model  # Pre-trained Word2Vec model file
└── templates/
    └── index.html  # HTML template for the Flask application
```

### Additional Documentation
#### `app.py`
This file contains the Flask application which handles HTTP requests, loads pre-trained models, processes input data, and returns predictions.

#### `utils.py`
This file includes utility functions for text preprocessing, feature extraction, and data vectorization.

#### `TrainingCode.py`
This file demonstrates how the RandomForest model was trained and evaluated using the provided dataset. It includes steps for preprocessing, training, and evaluation.

#### `requirements.txt`
This file lists all the Python dependencies required to run the application.

### Final Notes
- Ensure that the pre-trained models are included in the repository.
- Use python version lower than 3.12, most likely 3.11.8
- There is a possibility that you might encounter an error relateed to C++ environment. To resolve this, download visual studio and download the desktop application module.

By following these steps, you should be able to successfully run the Quora duplicate question detection application locally.
=======