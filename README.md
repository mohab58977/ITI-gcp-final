
# CICD Pipeline

![image](https://drive.google.com/uc?export=view&id=1qQR7wPd1ZI1MnPZbarEP8g6wJEgf2-mH)
## Demo

This Repo contains Pipeline section of the CICD Pipeline project I'm gonna explain CICD stages (fetch the code changes from github & build and push image to dockerhub & deploy hello world node.js app on GKE cluster & send notifications to slack channel).

Check infrastructure section in this Repo : https://github.com/mohab58977/challenge-iti
 

## Tools & Plugins


#### Kubernetes :

#### Jenkins :


  - Create CICD pipeline to build and push the image of our app & deploy  on GKE cluster.




##  docker file

1- I will create a docker file to create an image from app (Jenkins will build and push this image to dockerhub)



## Deployment files

- I will create 2 deployment files (app.yaml & service.yaml & prodns.yaml) Jenkins will deploy these files on GKE cluster

![image](https://drive.google.com/uc?export=view&id=1EvRWeop1S9Sv0S7yPU0UM-B9t9va0H0Y)

![image](https://drive.google.com/uc?export=view&id=1dkauO-iPWkvDX39EraN_lSiti9swX9Kz)

![image](https://drive.google.com/uc?export=view&id=1lYZzIQgIJDpWG20skXmkZEeZDCtcO6FT)


## Jenkinsfile

1- "CI" stage in the Pipeline will ( clone the github repo & build helloWorldapp image & push image to dockerhub ) "Pipeline will run on Jenkins Slave Pod"

![image](https://drive.google.com/uc?export=view&id=1AuAiGGQoVYy-YoCtOOphQoJ-FgRpz65k)

2- "CD" stage in the Pipeline will ( authenticate access to the cluster using Service account which is created with terraform in the infra section & gcloud auth command )
   I added a new credentials "secret file" in jenkins which contains Service account '.json key'

![image](https://drive.google.com/uc?export=view&id=18cp-nRc0sey3fRR_YJF4VIwQbtkCHFbf)




## Feedback

If you have any feedback, please reach out to me at ahmed.ali.elbaz.mohamed@gmail.com
