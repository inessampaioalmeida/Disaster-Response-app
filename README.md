### Disaster Response Project

Summary:

This project was developed to create a system which classifies disaster messages received and which retrieves the kind of response needed to articulate with the responsible parties and give the response neeeded to the request received.

Files in this repository:

This reposity contains three folders: 

- data: contains disaster messages data and script to clean the data and store it in a database)
- model: contains a pickled model which reads the data from the database created in the previous step and returns a prediction on the type of response neeeded for a disaster message)
- app (contains script of a Web App created to run the prediction model in a web browser)

Instructions to run this project:

1. To set up database and model:

- In the root directory run the following command to set up the database:
    `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
- In the root directory run the following command to train the model and generated the trained pickled model:
    `python model/train_classifier.py data/DisasterResponse.db model/model.pkl`

2. Run the following command in the app's directory to run the web app:'python run.py`

3. Go to http://0.0.0.0:3001/ and insert a message to be classified.
