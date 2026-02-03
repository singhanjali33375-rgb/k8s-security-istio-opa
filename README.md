# k8s-security-istio-opa
This project demonstrates how to secure a Kubernetes (v1.26) cluster using Istio for service mesh security and Open Policy Agent (OPA) for policy-based security enforcement. It implements mTLS, authorization policies, and admission control to ensure a Zero Trust Kubernetes environment.
📘 README.md (FULL & FINAL VERSION)
🔐 Kubernetes Security using Istio & Open Policy Agent (OPA)
📌 Project Overview
This project demonstrates how to secure a Kubernetes cluster (v1.26) using Istio Service Mesh and Open Policy Agent (OPA Gatekeeper).
The goal is to implement Zero Trust Security by:
Securing service-to-service communication using mTLS
Controlling traffic with Istio Authorization Policies
Enforcing security rules at admission time using OPA Gatekeeper
🏗️ Architecture
Kubernetes v1.26
Istio (Service Mesh)
Envoy Sidecar Proxies
OPA Gatekeeper (Admission Controller)

Client → Istio Ingress Gateway → Secure Services (mTLS)
                                      ↓
                              OPA Policy Validation
🛠️ Tools & Technologies
Kubernetes 1.26
Istio (Service Mesh)
Envoy Sidecar Proxies
OPA Gatekeeper (Admission Controller)

Client → Istio Ingress Gateway → Secure Services (mTLS)
                                      ↓
                              OPA Policy Validation
🛠️ Tools & Technologies
Kubernetes 1.26
Docker
Istio
Open Policy Agent (OPA)
Helm
YAML
kubectl
Linux
🚀 Features Implemented
Mutual TLS (mTLS) between services
Service-level authorization
Admission control using OPA
Blocking insecure Kubernetes deployments
Zero Trust Kubernetes security model
📂 Repository Structure
k8s-security-istio-opa/
│
├── README.md
├── kubernetes/
│   ├── namespace.yaml
│   ├── deployment.yaml
│   └── service.yaml
│
├── istio/
│   ├── peerauthentication.yaml
│   └── authorization-policy.yaml
│
├── opa/
│   ├── constraint-template.yaml
│   └── constraint.yaml
│
├── scripts/
│   ├── install-istio.sh
│   └── install-opa.sh
│
└── docs/
    ├── setup-guide.md
    └── security-policies.md
    ⚙️ Setup Instructions
    kubectl apply -f kubernetes/
sh scripts/install-istio.sh
sh scripts/install-opa.sh
kubectl apply -f istio/
kubectl apply -f opa/
🔒 Security Policies Enforced
Privileged containers are blocked
latest image tags are not allowed
Resource limits are mandatory
Unauthorized traffic is denied
✅ Outcome
Secure Kubernetes cluster
DevSecOps best practices
Interview-ready real-world project
🎯 Interview Tip (ONE LINE)
“We used Istio for network-level security and OPA for admission control, implementing a Zero Trust Kubernetes environment.”
