# k8s-simple-demo

This example assumes you have a kubernetes cluster running and kubectl configured

To deploy the example:
  1. Deploy the pods with: kubectl apply -f deployment.yaml
  2. Create the loadblancer with: kubectl apply -f service.yaml
  3. Get the load balancer IP with: kubectl get service
    Wait for the external IP to be available.
  4. View the external IP in a browsers

To update the app:
  1. Edit deployment.yaml and change the container from v1 to v2
  2. Run: kubectl apply -f deployment.yaml
  3. Watch the pods update with: kubectl get pods -w
  4. When the update is done, press ctrl+c to cancel watching the pods
