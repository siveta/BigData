# Big Data Task 2

The goal of this project is to run a Python script on Docker Container.


The Dockerfile sets up a container environment with all necessary dependencies to run the model.py script. It includes instructions to copy the script and dependencies into the container, install the required packages, and execute the script.

## Project Description:

**model.py**:
- Uses Scikit-learn to load the Iris dataset.
- Splits the dataset into training and test sets using an 80-20 split.
- Trains a Random Forest classifier on the training data.
- Makes predictions on the test set and calculates the accuracy of the model.
- Saves the trained model to a file named iris_model.pkl using joblib.

**Dockerfile**:
- Sets up a lightweight Python environment.
- Installs dependencies from requirements.txt.
- Runs the model.py script upon container startup.

**requirements.txt**:
- Lists the Python packages required to run the script (pandas, scikit-learn, and joblib).


This setup allows the machine learning model to be easily built, tested, and deployed in a consistent and reproducible environment using Docker.


## Docker:
Build the Docker image:

    docker build -t iris-classification .
    
Run the Docker container:

    docker run iris-classification

List Docker images:

    docker images

Log in to Docker Hub:
    
    docker login
    
Tag the Docker image for Docker Hub:

    docker tag iris-classification siveta/iris-classification

Push the Docker image to Docker Hub:

    docker push siveta/iris-classification
    
Pull the Docker image:

    docker pull siveta/iris-classification

    

The repository in DockerHub : https://hub.docker.com/repository/docker/siveta/iris-classification/general

Docker image tag : siveta/iris-classification
