# Traefik-experiment
Use Traefik 2.0+ as ingress controller in Kubernetes, and display the Traefik dashboard.
Still work in progress. 

Steps to deploy:
* Go to GKE, create a cluster (e.g. 2 g1-small nodes with HTTP load balancing). 
* Connect to the Kubernetes cluster from local terminal. `kubectl apply -f k8s`. This will create an external load balancer with an ephemeral IP. 
* Go to the VPC network -> External IP Addresses, change that ephemeral IP to a static IP. 
* Put that static IP to the DNS record associated with the domain. Wait till the DNS record propagates. 
