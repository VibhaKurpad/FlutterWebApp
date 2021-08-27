## Integrated Developer Workflow solution

This repo consists of all the code and artifacts required to make a flutter web application with the help of an end-to-end delivery pipeline.

### Aim

To create an integrated developer workflow solution with the help of Cloud Build and Google Kubernetes Engine.

Clone the repository onto your local system to get started

### About the App

It is a chat and RSVP app that lets you register and login, RSVP to an event and send messages.

For more information and detailed steps to create the app [click here](https://firebase.google.com/codelabs/firebase-get-to-know-flutter?hl=en&continue=https%3A%2F%2Fcodelabs.developers.google.com%2F#0)

### Directory structure

- **Dockerfile**: Used to create the image which will run the web application. Port 8080 is exposed
- **cloudbuild.yaml**: Used by the cloud build trigger to register the pipeline and create the release
- **clouddeploy.yaml**: Used to define the targets and sequence of the delivery pipeline
- **policy.yaml**: Creates the policy that is used by Binary Authorization
- **skaffold.yaml**: Helps to automate the deployments
- **kubernetes/deployment.yaml**: Deployment file for Kubernetes cluster
- **lib/main.dart**: Main source code for the flutter web app

To secure the deployment pipeline [refer to this link](https://codelabs.developers.google.com/codelabs/cloud-binauthz-intro/#0)
