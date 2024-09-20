# K8_Nginx_Ansible

### Ansible Playbook with following modules:

1. **Helm Information**:
   * `community.kubernetes.helm_info` checks if Nginx Ingress is installed by querying Helm.
2. **Helm Installation**:
   * `community.kubernetes.helm` is used to install Nginx Ingress if it’s not already installed.
   It directly references the Helm repository and installs the chart.
3. **Kubernetes Deployment and Ingress**:
   * `community.kubernetes.k8s` is used to apply Kubernetes manifests from your YAML files (`deployment.yaml` and `ingress.yaml`).
   
   Make sure you have the `community.kubernetes` Ansible collection installed, which provides these modules.
   We can install it using the following command: `ansible-galaxy collection install community.kubernetes`

   This approach avoids using shell commands and leverages Ansible’s native modules for better error handling and integration.



