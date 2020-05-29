# helm-implementation
Helm is a package manager for Kubernetes scripts. 
The core function of the module is to create Helm chart for deploying docker containers in Kubernetes cluster. 


# Prerequisites
  1. kubectl client - latest version
  2. helm - v3.2.0
  3. Image to be deployed available in Docker Hub

# Installing
 Clone the git repository in a local directory using git clone<repository_name> command.

# Useful commands
 Update the below mentioned details of the docker image in the values.yaml.</br>
    1 repository </br>
    2 imagePullPolicy </br>
    3 tag </br>
 Then 
 <B> helm lint helm </B> to examine charts for an issues.
 For deploying the helm, use <B> helm upgrade -i helm helm </B>
  
 Check the installed helm using using <B> helm ls </B> and the service,deployment and pod(s) detail using <B> kubectl get all</B>
 
 Test The application using <B> kubectl --namespace default port-forward <pod_name> 8080:80 </B>
  
  # Other Useful Commands
  
  <B> helm delete helm </B>  - deletes the helm deployment </br>
  <B> helm package helm </B>  - packages the chart into .tgz file </br>
  <B> helm status helm </B>  - shows the installation status </br>
  <B> helm upgrade -i helm helm --set service.port=8080 </B>  - To override one of the variables(in this case service.port) insted of default installation mentioned </br>
  
  
