# Disaster Response Pipeline Project

### Project Description:

In this project, I built a data transformation - machine learning pipeline that is capable to curate the class of the messages. The pipeline is eventually built into a flask application. The project include a web app where an emergency worker can input a new message and get classification results in several categories. The landing page of the webapp also includes 4 visualizations of the training dataset built with plotly.

### Dependencies
* Python 3.5+
* Machine Learning Libraries: NumPy, SciPy, Pandas, Sciki-Learn
* Natural Language Process Libraries: NLTK
* SQLlite Database Libraqries: SQLalchemy
* Model Loading and Saving Library: Pickle
* Web App and Data Visualization: Flask, Plotly


### Model
You can build your own model using `train_classifier.py`, but if you want to use the pre-trained model you can download it [here](https://drive.google.com/file/d/1ngLraihD2DlodsrLRuz6wLofkWCGaWc5/view?usp=sharing).

### File Descriptions:
The project contains the following files,

* ETL Pipeline Preparation.ipynb: Notebook experiment for the ETL pipelines
* ML Pipeline Preparation.ipynb: Notebook experiment for the machine learning pipelines
* data/process_data.py: The ETL pipeline used to process data in preparation for model building.
* models/train_classifier.py: The Machine Learning pipeline used to fit, tune, evaluate, and export the model to a Python pickle (pickle is not uploaded to the repo due to size constraints on github).
* app/templates/~.html: HTML pages for the web app.
* run.py: Start the Python server for the web app and prepare visualizations.


Example message to classify: "Help, Fire!"

### Local Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        ```
        python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
        ````
    - To run ML pipeline that trains classifier and saves
        ```
        python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
        ```

2. Run the following command in the app's directory to run your web app.
    ```
    python run.py
    ```

3. Go to the local host: http://0.0.0.0:3001/


![Webapp Screenshot](https://github.com/lokissue/Data-Analysis-Project-Portfolio/blob/master/Project%204%20-%20Disaster%20Response%20Pipeline/app/webapp%20screenshot.png?raw=true)
