## Ranajit Jana — Detailed Technologies

[Home](README.md) &nbsp;|&nbsp; [Experience](experience.md) &nbsp;|&nbsp; [Skills](skills.md) &nbsp;|&nbsp; **Detailed Technologies** &nbsp;|&nbsp; [Education](education.md)

---

### 🔒 Security & Compliance

> MTech in Cybersecurity (REVA University, 2024) — security is a first-class concern across every layer of the stack: cluster networking, policy enforcement, service mesh, pipelines, and cloud posture.

---

#### Cilium — eBPF-based Kubernetes Networking & Security

Cilium is a CNCF-graduated CNI (Container Network Interface) plugin that replaces traditional iptables-based networking with **Linux eBPF**, pushing policy enforcement directly into the kernel for higher performance and deeper visibility.

| Capability | Detail |
|---|---|
| **eBPF Networking** | Kernel-level packet processing; eliminates iptables overhead for large-scale clusters |
| **Network Policy Enforcement** | L3/L4/L7 policies using Kubernetes labels and identities, not just IP addresses |
| **Identity-Based Security** | Pod-to-pod communication governed by workload identity, not ephemeral IPs |
| **Transparent Encryption** | WireGuard or IPsec-based node-to-node encryption with zero application changes |
| **Hubble Observability** | Real-time network flow visibility, DNS query tracking, HTTP/gRPC tracing across services |
| **Cluster Mesh** | Multi-cluster service discovery and policy enforcement across cloud boundaries |

Cilium's identity-based model makes it a strong fit for zero-trust architectures where network segmentation must survive dynamic pod scheduling.

---

#### Kyverno — Kubernetes-Native Policy Engine

Kyverno is a CNCF policy engine that validates, mutates, and generates Kubernetes resources using **policies written as Kubernetes YAML** — no Rego or OPA required. It runs as an admission webhook, enforcing rules before resources are admitted to the cluster.

| Capability | Detail |
|---|---|
| **Validation Policies** | Reject non-compliant resources: enforce resource limits, required labels, approved registries |
| **Mutation Policies** | Auto-inject sidecars, add default labels/annotations, patch missing security contexts |
| **Generation Policies** | Auto-create NetworkPolicies, ConfigMaps, or RBAC roles when a namespace is created |
| **Image Signature Verification** | Enforce Sigstore/Cosign-signed images — blocks unsigned or tampered images at admission |
| **Policy Reports** | Audit mode generates CRD-based reports for compliance dashboards without blocking workloads |
| **GitOps Integration** | Policies stored as YAML in Git; enforced via CI/CD before cluster apply |

Kyverno enables **policy-as-code** in GitOps workflows — security rules live alongside application manifests and are reviewed, versioned, and audited the same way as code.

---

#### Istio — Service Mesh

Istio is a CNCF service mesh that adds a transparent proxy layer (Envoy sidecar) to every pod, providing security, traffic control, and observability **without application code changes**.

| Capability | Detail |
|---|---|
| **Mutual TLS (mTLS)** | Automatic certificate issuance and rotation; encrypts all service-to-service traffic; enforces zero-trust identity |
| **Authorization Policies** | Fine-grained L7 access control: allow/deny based on service identity, HTTP method, path, headers |
| **Traffic Management** | Canary releases, A/B testing, weighted routing, retries, timeouts, circuit breaking at the mesh level |
| **Fault Injection** | Inject delays and errors into traffic for resilience testing without touching application code |
| **Observability** | Automatic generation of metrics (Prometheus), distributed traces (Jaeger/Tempo), and access logs for every service call |
| **Ingress / Egress Control** | Gateway-based north-south traffic management with TLS termination and routing rules |

Used at Ondot Systems for the microservices and containerization strategy — Istio provided the security and observability layer across the entire service fleet without requiring individual services to implement them.

---

#### Additional Security Practices

| Area | Detail |
|---|---|
| **DevSecOps Pipeline** | Security gates at every stage: SAST, container scan (Trivy), SBOM generation, supply chain signing *(MTech capstone)* |
| **Container Security** | Distroless/minimal base images, read-only root filesystems, no-root enforcement via Kyverno |
| **Web Security** | OWASP top-10 mitigations, WAF integration |
| **Supply Chain Security** | SBOM (Software Bill of Materials), Cosign image signing, Kyverno signature enforcement |
| **PII Compliance** | Multi-tenancy data isolation, PII detection (MS Presidio + LLM), data obfuscation *(MTech capstone, patent: 202441078002)* |
| **SSO / IAM** | SSO integration for enterprise platforms; AWS IRSA, Kubernetes RBAC, least-privilege IAM |
| **Compliance** | Achieved 100% compliance across web, container, deployment, cloud, and supply chain layers at eSentire |

---

### ☁️ AWS — Amazon Web Services

| Service / Area | Usage |
|---|---|
| **EKS** (Elastic Kubernetes Service) | Primary Kubernetes platform; multi-cluster, multi-region deployments |
| **EC2** | Compute for workloads and build infrastructure |
| **S3** | Object storage, artifact storage, log archival |
| **CloudWatch** | Log ingestion, metrics, alarms; cross-system correlation with GenAI |
| **Secrets Manager / SSM** | Configuration externalization, secrets at runtime for containerized apps |
| **IAM** | Fine-grained access control, IRSA for pod-level permissions |
| **Savings Plans / Reserved Instances** | FinOps: ~15% yearly cost reduction through commitment-based pricing |
| **Cost Explorer / Budgets** | Resource attribution, cost monitoring, quarterly optimization reviews |
| **Multi-Region** | New region deployments automated via Claude-based automation agents |
| **VPC / Networking** | Secure network architecture for cloud-native workloads |

---

### ☁️ Azure — Microsoft Azure

| Service / Area | Usage |
|---|---|
| **AKS** (Azure Kubernetes Service) | Kubernetes orchestration for payments platform (Volante) |
| **Azure DevOps / Pipelines** | CI/CD integration for build and release |
| **Azure Messaging** | Event-driven architecture with Kafka/RabbitMQ on Azure |
| **Azure Blob / Storage** | Artifact and data storage |
| **Multi-Cloud Portability** | Architected cloud-agnostic Kubernetes platform to eliminate vendor lock-in |

---

### 🏗️ Terraform

| Area | Detail |
|---|---|
| **Infrastructure as Code** | Declarative provisioning of AWS and Azure resources |
| **Multi-Cloud Modules** | Reusable modules for compute, networking, storage across cloud providers |
| **Remote State** | S3 + DynamoDB backend for team-based, locking-safe state management |
| **Terraform + GitHub Actions** | Fully automated infra provisioning in CI/CD pipelines |
| **New Region Deployments** | Automated region rollouts using Terraform + Claude-based agents |

---

### ⚙️ Kubernetes

| Area | Detail |
|---|---|
| **Certification** | **CNCF Certified Kubernetes Administrator (CKA) — 2020** |
| **Helm Charts** | Authored and standardized Helm charts for application onboarding; ~80% template reuse |
| **Argo CD** | GitOps-based continuous delivery; declarative app sync and rollback |
| **Istio** | Service mesh: mTLS, traffic management, observability, circuit breaking — see Security section above |
| **Multi-Cluster** | Multi-region, multi-environment cluster strategy with isolated branch deployments |
| **Kubernetes Security** | Pod Security Standards, RBAC, network policies, image scanning |
| **Zero-Downtime Deployments** | Rolling updates, blue/green, canary release strategies |
| **Auto-scaling** | HPA/VPA for workload-responsive scaling |

---

### 🔁 CI/CD — GitHub Actions & Pipelines

| Tool | Usage |
|---|---|
| **GitHub Actions** | Primary CI/CD platform; migrated all pipelines from Jenkins — **60% reduction in execution time** |
| **Jenkins** | Legacy pipelines (decommissioned and replaced with GitHub Actions) |
| **GitLab CI** | Used in Wipro PaaS platform |
| **SonarQube** | Static code analysis, quality gates in pipelines |
| **Nexus** | Artifact repository management |
| **Trivy / Container Scanning** | Image vulnerability scanning in release pipelines |
| **SBOM** | Software Bill of Materials generation for supply chain compliance |

---

### 🤖 Agentic AI & Generative AI

| Technology | Detail |
|---|---|
| **Claude Automations** | Built plugins, agents, and skills on Claude for DevOps automation |
| **Agentic AI Frameworks** | End-to-end automation of tech stack upgrades, region deployments, templated code generation |
| **GenAI for Observability** | Cross-system log/event correlation: Grafana Loki + Kubernetes + CloudWatch + Arize Phoenix |
| **Arize Phoenix** | ML observability and LLM tracing for AI-driven workloads |
| **MS Presidio** | PII detection and sensitivity scoring using LLMs and rule engines *(MTech capstone)* |
| **Code Generation** | Enterprise-specific automated code generation reducing development time ~10x |
| **Scikit-learn / TensorFlow** | ML model development (Python) |

---

### 🔭 Observability Stack

| Tool | Role |
|---|---|
| **Grafana** | Unified dashboards for metrics, logs, and traces |
| **Loki** | Log aggregation at scale; Kubernetes-native log collection |
| **Prometheus** | Metrics scraping, alerting rules, recording rules |
| **Alertmanager** | Alert routing, deduplication, on-call integration |
| **Tempo / Jaeger** | Distributed tracing for microservices |
| **ELK Stack** | Elasticsearch + Logstash + Kibana for log analytics (Wipro PaaS, Ondot) |
| **Fluentd** | Containerized log forwarding agent on Kubernetes |
| **Datadog** | APM, infrastructure monitoring, SLA dashboards (Ondot) |
| **AWS CloudWatch** | Cloud-native log ingestion and alerting for AWS workloads |
| **Arize Phoenix** | LLM / ML model observability |

---

### ☕ Java & Application Stack

| Technology | Detail |
|---|---|
| **Java / J2EE** | 20+ years; evolved from EJB/WebLogic to Spring Boot microservices |
| **Spring Boot** | Core framework for REST APIs, microservices, event-driven apps |
| **Spring Cloud (Netflix OSS)** | Service discovery (Eureka), circuit breaker (Hystrix), API gateway (Zuul) |
| **Apache Camel** | Integration framework for event-driven payments workflows (Volante) |
| **JPA / Hibernate** | ORM for RDBMS access |
| **REST APIs / API Gateways** | Design, implementation, and standardization |
| **Cryptography** | Encryption, key management in enterprise applications |

---

### 💾 Messaging & Databases

| Category | Technologies |
|---|---|
| **Messaging / Streaming** | Kafka, RabbitMQ |
| **NoSQL** | Cassandra, MongoDB |
| **RDBMS** | PostgreSQL, MySQL, Oracle, PL/SQL |
| **Caching** | In-memory caching, distributed cache layers |
| **Data Processing** | File processing pipelines, JSON/XML parsing, scaffolding frameworks |

---

### 🛠️ Automation & Scripting

| Tool | Usage |
|---|---|
| **Ansible** | Infrastructure provisioning, configuration management (Wipro PaaS, Ondot) |
| **Bash / Shell** | Cloud automation, Kubernetes scripting, pipeline scripting |
| **Python** | ML model development, automation scripting |
| **Terraform** | IaC for multi-cloud provisioning |

---

### 🏅 Certifications & Training

| Certification | Year |
|---|---|
| **CNCF Certified Kubernetes Administrator (CKA)** | 2020 |
| **Hands-on ML and Generative AI** | Recent |
| **Sun Certified Web Component Developer (SCWCD)** | 2005 |
| **Sun Certified Java Programmer (SCJP)** | 2000 |

---

### 📂 Domain Experience

`Cybersecurity` `Payments & Fintech` `Banking` `Supply Chain` `Manufacturing` `CRM` `Advertisement / Media` `e-Commerce`

---

### 🔗 Public Profiles & Talks

| | |
|---|---|
| GitHub | [github.com/ranajit-jana](https://github.com/ranajit-jana) |
| LinkedIn | [linkedin.com/in/ranajitjana](https://linkedin.com/in/ranajitjana) |
| BrightTalk Talk | [brighttalk.com/webcast/16135/307311](https://www.brighttalk.com/webcast/16135/307311) |

---

*[← Skills](skills.md) &nbsp;·&nbsp; [Education →](education.md)*
