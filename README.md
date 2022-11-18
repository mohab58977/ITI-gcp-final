
# CICD Pipeline

## Demo

This Repo contains Infrastructure section of the CICD Pipeline project I'm gonna explain CICD stage.

Check App & pipeline section in this Repo : https://github.com/mohab58977/challenge-iti
 

## Tools & Plugins


#### Kubernetes :

#### Jenkins :

  - Create CICD pipeline to build and push the image of our app & deploy  on GKE cluster.

##  docker file

1- I will create a docker file to create an image from app (Jenkins will build and push this image to dockerhub)



## Deployment files

- I will create 2 deployment files (app.yaml & service.yaml & prodns.yaml) Jenkins will deploy these files on GKE cluster



## Jenkinsfile

1- "CI" stage in the Pipeline will ( clone the github repo & build app image & push image to dockerhub ) "Pipeline will run on Jenkins Slave Pod"


2- "CD" stage in the Pipeline will ( authenticate access to the cluster using Service account which is created with terraform in the infra section & gcloud auth command )
   I added a new credentials "secret file" in jenkins which contains Service account '.json key'


## Feedback

If you have any feedback, please reach out to me at mohab5897@gmail.com
