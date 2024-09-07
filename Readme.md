1. Before deploying an application to kubernetes cluster, make sure ConfigMap and Screts exist in the cluster.
2. To create the above two files, run:

- kubectl apply -f mongo-config.yaml
- kubectl apply -f mongo-secret.yaml
- kubectl apply -f mongo.yaml
- kubectl apply -f webapp.yaml

3. After running the above commands, you can basic operations with the following commands.

- kubectl get all
- kubectl get configmap - shows the configs running
- kubectl get secret - shows you the secret running
- kubectl get node
- kubectl get pod
- kubectl get svc

4. To see more details about a particular service, run the command

- kubectl describe service webapp-service

5. To see more details about the pods, run the command

- kubectl describe pod _podname_

6. To see the logs of a particluar pod, run the command

- kubectl get pod, then
- kubectl logs webapp-deployment-9fccd564d-nqwjf
  To stream the logs, add -f at the end
- kubectl logs webapp-deployment-9fccd564d-nqwjf -f

7. To see the node running, issue the command

- kubectl get node

8. Get the services running

- kubectl get svc

9. To get more additional details about the node or service, or pod

- kubectl get node -o wide
- kubectl get svc -o wide
- kubectl get pod -o wide
