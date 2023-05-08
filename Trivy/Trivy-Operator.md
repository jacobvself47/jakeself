# Install Helm
Helm is a tool that automates the creation, packaging, configuration, and deployment of Kubernetes applications by combining your configuration files into a single reusable package.

Resources: https://aquasecurity.github.io/trivy-operator/v0.13.2/getting-started/installation/helm/

* Step 1: Install Helm
    - `<brew install helm>`
* Step 2: Add Trivy Helm Repos
    - `<helm repo add aqua https://aquasecurity.github.io/helm-charts/>`
        - Response: "aqua" has been added to your repositories
    - `<helm repo update>`
        - Response: Update Complete. Happy Helming!
* Step 3: Deploy the trivy-operator
    ```
    helm install trivy-operator aqua/trivy-operator \
  --namespace trivy-system \
  --create-namespace \
  --set="trivy.ignoreUnfixed=true" \
  --version 0.13.2
    ```