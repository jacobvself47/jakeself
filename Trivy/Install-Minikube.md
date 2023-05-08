# Install minikube
Refernces: https://minikube.sigs.k8s.io/docs/start/
* Step 1:
    - `<brew install minikube>`
* Step 2:
    - `<minikube start>`
* Step 3:
    - Received error warning "Unable to pick a default driver."
* Step 4:
    - Download and install Docker
    - Link: https://docs.docker.com/desktop/install/mac-install/
* Step 5:
    - To run Docker, the following command is needed
    - `<softwareupdate --install-rosetta>`
* Step 6:
    - Set up Docker following the in-app instructions
* Step 7:
    - Run the `<minikube start>` command again
* Step 8:
    - Install kubectl
    - `<brew install kubectl>`
* Step 9 (Optional):
    - Set kubectl as an alias
    - `<alias kubectl="minikube kubectl --">`
* Step 10:
    - Validate minikube is running
    - `<kubectl get services>`
    - Result:

        | Name       | Type      | Cluster-IP | External-IP | Ports(s) | Age   |
        | ---------- | --------- | ---------- | ----------- | -------- | ----- |
        | kubernetes | ClusterIP | `*.*.*.*`  | none        | 443/TCP  | 5m25s |