# kustomize-nginx

# Pre-Requisites:
    - EKS-Cluster
# Clone the code from Github
    https://github.com/Naresh240/kustomize-nginx.git
    cd kustomize-nginx/base
# Create Base Resources
    kubectl apply -k base
    
    Eg for python-stackdemo application:
    
 ![image](https://user-images.githubusercontent.com/54719289/116147777-07dcf500-a6d8-11eb-862a-ce2b32a84416.png)
 ![image](https://user-images.githubusercontent.com/54719289/116147838-1a572e80-a6d8-11eb-81cd-2eb34b527c6f.png)

# Check pods
    kubectl get pods -n dev
  ![image](https://user-images.githubusercontent.com/58024415/101765267-16e75000-3b07-11eb-9cc0-2eac1207f941.png)
# Increasing Replicas from 1 to 2
    kubectl apply -k .
# Now check number pods (Here I am paching replica count)
    kubectl get pods -n dev
  ![image](https://user-images.githubusercontent.com/58024415/101765481-5e6ddc00-3b07-11eb-9059-b83820b4fe4c.png)
# Clean-UP
    kubectl delete -k .
