# disaster_prediction
machine learning model deploy

Disaster Prediction

Link deploy: https://ancana-b21-cap0252.el.r.appspot.com/

Predict API: https://ancana-b21-cap0252.el.r.appspot.com/predict (POST/GET with image)


## Deployment Steps
Assuming you have configured your GCP Project, here are the steps of deploying this integration of ML to the cloud.
1.  Configure your App Engine in GCP
2.  Open Google Cloud console and activate cloud shell
3.  From the cloud shell terminal clone this repository.
    '''sh
    git clone https://github.com/yusufaudri/disaster_prediction.git
    '''
4.  Move to the working directory
    '''sh
    cd disaster_prediction
    ''' 
5.  In the cloud shell click open editor to review the required files to deploy to App Engine
    1. main.py          ==> The API for your machine learning model to run in the cloud. in this project we use Flask.
    2. requirement.txt  ==> This requirements.txt file is used for specifying what python packages are required to run the project you are looking at
    3. app.yaml         ==> You configure your App Engine app's settings in the app.yaml file The app.yaml file contains information about your app's code, such as the runtime and the latest version identifier.
6.  return to the cloud shell terminal and run this code to authorizes gcloud and other SDK tools to access Google Cloud Platform using your user account credentials, or from an account of your choosing whose credentials are already available and Sets up a new or existing configuration.
    '''sh
    gcloud init 
    '''
7.  still in Cloud Shell terminal, to deploy our ML model to App Engine run this code.
    '''sh
    gcloud app deploy 
    '''
8.  After succesful deployment, you can access the given endpoint and test the prediction using https://web.postman.co/ (POST with image)


Happy Testing!
    
    











