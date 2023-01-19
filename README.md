# sample-app-java
Deploy Java Application
1. Go to the sample java app repo root directory, Deploy the manifest by running the following command:


$ kubectl apply -f deployment/
 It will create web and mongo pods. Also 2 services for web and mongo,


2. Generate request from inside the web pod or from your terminal if you can access web service loadbalancer endpoint.


curl "0.0.0.0:8080/"

curl -H 'Content-Type: application/json' -X POST "0.0.0.0:8080/notes" -d "hello world"

curl 0.0.0.0:8080/notes/id_string

curl -H 'Content-Type: application/json' -X PUT "0.0.0.0:8080/notes/id_string" -d "another description"

curl  -X DELETE "0.0.0.0:8080/notes/id_string"

curl 0.0.0.0:8080/notes

curl -H 'Content-Type: application/json' -X PUT "0.0.0.0:8080/notes/1" -d "another description"

e.g. kubectl exec -it web-68fc4f79b5-652wq -- bash
curl "0.0.0.0:8080/"

