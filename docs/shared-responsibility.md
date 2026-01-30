# Shared Responsibility Model

## Team responsibilities (we own)

- Application code and tests
- CI/CD pipelines and security gates
- Container image hardening
- Kubernetes manifests and policies
- Monitoring, alerts, and runbooks

## Platform responsibilities (provider)

- Cloud infrastructure availability
- Managed Kubernetes control plane (if used)
- Network and storage durability (provider-managed)

## Shared

- Identity and access management
- Secrets handling
- Incident response coordination
