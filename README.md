# first-app

Create google cloud account.

Write the python docker requirement and yaml files

enable container registry in gcp

create an vm instance under compute engine
    select any service account, which costs less
    change boot disk to ubuntu
    allow full access to cloud api
    allow http and https

open ssh of that created instance
    install docker on the ubuntu (https://docs.docker.com/engine/install/ubuntu/)

steps
    clone the repo onto ubuntu
        git clone https://github.com/sarvasuddi-balaganesh/first-app.git
    go to repo
        cd first-app
    build and push the container using cloudbuild.yaml file
        gcloud builds submit --config cloudbuild.yaml . # . -> docker file
    you can see the pushed image in gcp under container resources
    run the docker file
        docker run gcr.io/hands-on-kube/first_app/first-app
    after successful run, use the gcp vm instance externalip without https
        <external-ip>/iris  
    

ref : https://www.youtube.com/watch?v=v36R-lwzUSI&list=PLOtrf6rnS2fmnCZc4uElGzClfxDXOi3BS&index=3&ab_channel=DataLounge