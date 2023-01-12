## Major tasks performed in this demo:
 1. Install the Required Operators using Kustomize
 2. Fork a template repository that will be used by Openshift GitOps (ArgoCD) to automate and manage Service Mesh Control Plane
 3. Install and Launch ArgoCD instance "app of apps" pattern to manage a Demo Cluster using GitHub and Kustomize
 4. Provision Bookinfo sample application to be managed by ArgoCD
 5. Perform a Service Mesh Control Plane version upgrade

## GitHub Repositories Structure

 1. RHC-STP-OSSM/GitOps-OSSM: 
 - Operator Subscriptions for: Kiali, Distributed Tracing (Jaeger), Elasticsearch, and OSSM
 - OSSM provisioning: contains base and overlays for defining Service Mesh Control Plane.  The overlay is used for upgrading the control plane.

 2. RHC-STP-OSSM/cluster-gitops:
 - Template repository that can be forked to provision a specific instance of ArgoCD to manage Service Mesh projects
 - Provision additional Service Mesh Control Plane capabilities: adding/removing Service Mesh Member Roll namespaces

 3. RHC-STP-OSSM/gitops-app-bookinfo:
 - Service Mesh CRDs: VirtualService, Gateway, DestinationRule, etc.
 - Simulate bookinfo deployment environments: qa, test, prod, etc.

