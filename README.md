the process:


Déploiement:

  1- for emna-redis-leader-deployment.yaml:
  
    - creationg the folder with the help of "https://kubernetes.io/docs/tutorials/stateless-application/guestbook/"
    
  2- for emna-node-redis.yaml:
  
    - copying the previous file and chanching the spec with "imagePullSecrets name regcred"
    
    - changing the path


Service:

  1- creating the service file  emna-service-redis.yaml
  
  2- creating the service file  emna-service-node-redis.yaml
  
  3- running the commands: 
  
    kubectl apply -f emna-service-redis.yaml
    
    kubectl apply -f emna-service-node-redis.yaml
    
  4- gething the path
  
  5- running the command: 
  
    kubectl apply -f emna-redis-leader-deployment.yaml
    
    kubectl apply -f emna-node-redis.yaml
    

  4- running the command line : 
  
    kubectl get pods
    
    kubectl logs emna-node-redis-759754bf7-mbhcn
    
    kubectl logs emna-redis-leader-5fb59b74cc-r5qph
    
  5- ready to accept connections
