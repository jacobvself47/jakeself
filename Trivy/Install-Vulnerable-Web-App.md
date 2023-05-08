# Install Vulnerable Web App
Resources: https://github.com/AnaisUrlichs/trivy-demo/tree/main/manifests
* Step 1: Add Deployment and Service yaml files to working directory.
    - In terminal: 
        - `<mkdir demo-manifests>`
        - `<cat < deployment.yaml>`
        - `<cat < service.yaml>`
    - Copy in deployment and service yaml from the link above into the newly created files
* Step 2: Create new name space
    - `<kubectl create ns app>`
* Step 3: Deploy yaml manifests
    - `<kubectl apply -f Github/jakeself/demo-manifests/deployment.yaml -n app>`
        - Response: "deployment.apps/react-application created"
    - `<kubectl apply -f Github/jakeself/demo-manifests/service.yaml -n app>`
        - Response: "service/react-application created"
* Step 4: Use K9s to view new application
    - `<:pods>`
        - Two new pods created in the "app" namespace
    - `<:services>`
        - `<shift + f>`
        - set Local Port to 8080
        - Navigate to "OK" to confirm
* Step 5: View Application on LocalHost
    - In browser type 'http://localhost:8080/'
    - Application should be running