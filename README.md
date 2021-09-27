# Spring Boot Application & React Front-end

Spring Boot Application is present under stakater-backend and Front-end / React application is present under stakater-Frontend folder.

## Pre install

Please ensure you have install the following packages

- Java >=8
- Maven
- Docker
- Minikube
- Helm
- Kubectl

## Running with Docker & Minikube

```
minikube start
```

or verify minikube status if you are already running it

```
minikube status
```

Once minikube is up and running, you can use the following command that will deploy the application using docker and helm chart

Open New terminal and run the following commands to run backend

```
cd Sample-Backend
./run-with-minikube.sh
```

Open New terminal and run the following commands for run frontend

```
cd Sample-Frontend
./run-with-minikube.sh
```

To uninstall run the following command 

```
helm uninstall stakater-backend
helm uninstall stakater-frontend
```

OR run ```.uninstall.sh``` in each folder (Sample-Backend & Sample-Frontend)

## Improvements:

Since, I was using linux with mini-kube service names were conflicting with my local network so, I did a port forward in backend.
This can be resolve with nginx and running backend behind proxy or depolying it to kubernates cluster instead of minikube.

Aggregate all helm charts in main repository so that main repository can be used to deploy the backend and frontend.
