# platform-components
Defines and configures the core platform services running inside the cluster, managed declaratively via ArgoCD. 

Contains ArgoCD Application manifests and environment-specific Helm values for baseline services including ArgoCD (self-managed post-bootstrap), Harbor, Vault, cert-manager, ingress-nginx, and the observability stack (Prometheus, Grafana).

Responsible for: 
- GitOps management of platform services
- Environment-specific configuration per service
- ArgoCD App of Apps bootstrap manifest.

Does not manage:
- Application workloads (see platform-deploy)
- Reusable application Helm charts (see platform-charts)
- Infrastructure provisioning (see platform-infra).