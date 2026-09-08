<p align="left">
 <img width="200" src="../master/docs/assets/istio/k8s_istio.png">
</p>

# Istio multi-cluster on minikube

Step-by-step notes for running an [Istio](https://istio.io/) service mesh spanning **two Kubernetes clusters** on a single laptop.

Multi-cluster Istio is normally something you only meet in a real cloud environment. These notes reproduce the same topology locally, so the moving parts — ingress gateways, cross-cluster service discovery, shared trust — can be inspected and deliberately broken without touching any infrastructure.

**[Read the notes →](https://wookiej.github.io/istio-multiclusters-minikube/)**

## What is covered

- Two minikube clusters (`cluster-1`, `cluster-2`) on the VirtualBox driver
- The **replicated control planes** topology: an independent Istio control plane in each cluster, joined through ingress gateways
- Cross-cluster service discovery, with a worked example of traffic crossing the boundary

## Running the notes locally

```bash
brew install mkdocs
mkdocs serve
```

## Versions

Written against **Istio 1.5.4** and verified on macOS. Istio's multi-cluster setup changed substantially in later releases — expect the commands to differ on current versions.
