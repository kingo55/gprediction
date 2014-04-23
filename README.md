gprediction
===========

A simple and effective Google Prediction API client for R.

1. Getting started
First you'll need a copy of devtools to install the package. Follow the steps below to get it setup:

```r
install.packages("devtools")
require("devtools")
```

Now you can install the package:
```r
install_github("jdeboer","gprediction")
require("gprediction")
```

2. Connecting to the Google Prediction API service

-Login to Google Cloud Console and hit the "Create Project" button: https://console.developers.google.com/project
-Give it a name and ID and create the project.
-Once the project has been created you'll be taken to a Welcome screen where you can manage the project.
-Under "APIs & Auth > APIs", enable "Cloud Storage" and "Prediction API"
-Next "APIs & Auth > Credentials", create a client ID for OAuth as an installed application.
-Make a note of the client secret - this will be the api_secret you use to connect R to Google's servers

```r
model_id <- "model_name" # You can call the model anything you like, and reuse it down the track
project <- "12345678910111213" # This is the project number of the project you configured in the Google API Console
api_secret <- "XXXXXXXXXXXXXXXX" # This is your API secret - guard this with your life
oauth <- GetAuthToken(appname= model_id, key= project, secret = api_secret) # This function handles authentication
```

You can now list all of your models stored under your account:
```r
GpList(project, oauth)
```

3. Training a model

For the training data, you'll need a CSV file without headers in a format as follows:

To be written


4. Getting predictions

To be written


5. Other commands
This package is very flexible and allows you to complete most tasks directly from within the R console. Here are a few more which weren't outlined above.

To be written
