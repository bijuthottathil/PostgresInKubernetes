# Deploy Postgres in Kubernetes using Helm and access with PGAdmin in local machine


1. Install Helm in windows by executing "winget install Helm.Helm" from powershell prompt

 D:\Streamlit> winget install Helm.Helm    
2. Make sure that Docker for Windows is up and running  
3. Execute Minikube start  from command prompt
4. Execute Minikube dashboard  from command prompt  ![image](https://github.com/user-attachments/assets/cb5c57e2-97ea-4953-a497-c6a1856e2063)  


5. Run below command from command prompt  
  helm install my-postgresnew bitnami/postgresql  --set auth.username=admin --set auth.password=mypassword --set auth.database=mydb  --set primary.service.type=NodePort
6. kubectl get svc ![image](https://github.com/user-attachments/assets/76ac252e-4bc2-4790-988c-a37674b35665)

7.  Run  kubectl port-forward svc/my-postgresnew-postgresql 5432:5432    ![image](https://github.com/user-attachments/assets/1e57458c-d891-4135-a2d8-00ab1afda9d9)
8.  Open PGAdmin editor and connect to server 127.0.0.1 and use the credentials mentioned in step5 to login to mydb
9.  ![image](https://github.com/user-attachments/assets/1ffe027f-26c9-4206-8693-1e12251f50d4)

