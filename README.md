This project demonstrates how to package, deploy, upgrade, and rollback a simple Flask web application using Helm in a Kubernetes cluster.

Step 1: Clone the repository -> Git clone https://github.com/AvinashKumar-Nagarro/k8s_advanced.git

Step 2: Change folder -> cd k8s_advanced

Step 3: Create a namespace -> kubectl create namespace dev

Step 4: Install the application using Helm -> helm install flask-app ./flask-app --namespace dev

Step 5: To access the application locally, forward the port -> kubectl port-forward --namespace dev svc/flask-app 5000:80

Step 6: To update the application, update values.yaml file and run command -> helm upgrade flask-app ./flask-app --namespace dev

Step 7: To get the list of revisions -> helm history flask-app --namespace dev

Step 8: To rollback to a specific revision -> helm rollback flask-app <revision_no.> --namespace dev
