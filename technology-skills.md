[Home](README.md) &nbsp;|&nbsp; [Experience](experience.md) &nbsp;|&nbsp; **Technology Skills** &nbsp;|&nbsp; [Management](management.md) &nbsp;|&nbsp; [Education](education.md)

---

### ☁️ Technology Ratings

| Skill | Proficiency |
|---|---|
| Architecture | ████████████ Expert |
| Cloud | ████████████ Expert |
| Containers | ████████████ Expert |
| CI/CD | ████████████ Expert |
| Development | ████████████ Expert |
| Security | ██████████░░ Advanced |
| Agentic-AI | ██████████░░ Advanced |
| AI/ML | ███████░░░░░ Trained |
| Gen-AI | ███████░░░░░ Trained |

---

### 🏛️ Architecture & Design Patterns

- **Cloud-Native Architecture** — containerized, orchestrated, observable platforms
- **Microservices** — decomposition, service mesh, API contracts
- **Event-Driven Architecture** — Kafka, Camel, messaging-based workflows
- **Domain-Driven Design** — bounded contexts, aggregates, CQRS
- **Enterprise Design Patterns** — MVC, EIP, SOLID, IoC, AOP
- **Multi-Tenancy** — isolation strategies for SaaS platforms
- **Zero-Downtime Deployments** — rolling, blue/green, canary
- **PaaS Design** — internal developer platforms, self-service deployments


---
### 🔒 Security

MTech in Cybersecurity (REVA University, 2024) — security is a first-class concern across every layer of the stack: cluster networking, policy enforcement, service mesh, pipelines, and cloud posture.

| Area | Detail |
|---|---|
| **Cilium** | CNCF-graduated eBPF-based CNI replacing iptables; enforces L3/L4/L7 network policies using workload identity, transparent WireGuard/IPsec encryption, real-time network flow visibility via Hubble, and multi-cluster policy enforcement across cloud boundaries |
| **Kyverno** | Kubernetes-native CNCF policy engine; validates, mutates, and generates resources via admission webhook using plain YAML policies — enforces image signing (Cosign/Sigstore), resource limits, security contexts, and auto-generates NetworkPolicies; policy-as-code in GitOps workflows |
| **Istio** | CNCF service mesh with Envoy sidecar; provides automatic mTLS for zero-trust service identity, fine-grained L7 authorization policies, canary/circuit-breaking traffic management, fault injection, and automatic Prometheus/trace observability — used at Ondot Systems across the full microservices fleet |
| **DevSecOps Pipeline** | Security gates at every stage: SAST, container scan (Trivy), SBOM generation, supply chain signing *(MTech capstone)* |
| **Container Security** | Distroless/minimal base images, read-only root filesystems, no-root enforcement via Kyverno |
| **Web Security** | OWASP top-10 mitigations, WAF integration |
| **Supply Chain Security** | SBOM (Software Bill of Materials), Cosign image signing, Kyverno signature enforcement |
| **PII Compliance** | Multi-tenancy data isolation, PII detection (MS Presidio + LLM), data obfuscation *(MTech capstone, patent: 202441078002)* |
| **SSO / IAM** | SSO integration for enterprise platforms; AWS IRSA, Kubernetes RBAC, least-privilege IAM |
| **Compliance** | Achieved 100% compliance across web, container, deployment, cloud, and supply chain layers at eSentire |


---

### ☁️ Cloud 
| Service / Area | Usage |
|---|---|
| **EKS** (Elastic Kubernetes Service) | Primary Kubernetes platform; multi-cluster, multi-region deployments |
| **AKS** (Azure Kubernetes Service) | Kubernetes orchestration for payments platform (Volante) |
| **EC2** | Compute for workloads and build infrastructure |
| **S3** | Object storage, artifact storage, log archival |
| **CloudWatch** | Log ingestion, metrics, alarms; cross-system correlation with GenAI |
| **Secrets Manager / SSM** | Configuration externalization, secrets at runtime for containerized apps |
| **IAM** | Fine-grained access control, IRSA for pod-level permissions |
| **Savings Plans / Reserved Instances** | FinOps: ~15% yearly cost reduction through commitment-based pricing |
| **Cost Explorer / Budgets** | Resource attribution, cost monitoring, quarterly optimization reviews |
| **Multi-Region** | New region deployments automated via Claude-based automation agents |
| **VPC / Networking** | Secure network architecture for cloud-native workloads |
| **Azure Entra** | Managing teams and access with Azure |
| **Azure App Registrations** | Single Sign on with Azure  |
---


### 🤖 AI / ML & Generative AI

`Agentic AI` `Claude Automations` `GenAI Frameworks` `LLM Integration`  
`AI-Driven Code Generation` `AI-Driven Observability` `Arize Phoenix`

- Built plugins, agents, and skills on Claude for DevOps automation
- Cross-system log/event correlation using GenAI (Loki, CloudWatch, K8s)
- Enterprise-specific automated code generation and tech stack upgrades
- **~5–10x productivity improvements** in select engineering workflows

---

### ⚙️ Containers and Kubernetes

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

### 🔭 Observability & Site Reliability Engineering

`Grafana` `Loki` `Prometheus` `Datadog` `ELK Stack` `AWS CloudWatch` `Arize Phoenix`

- Full-stack observability: logs, metrics, distributed traces
- MTTR reduction by **~60–70%** through unified alerting and dashboards
- Incident management, automated remediation foundations
- SLA/SLO/SLI definition and adherence

---

### 💾 Messaging & Databases

**Messaging:** `Kafka` `RabbitMQ`  
**NoSQL:** `Cassandra` `MongoDB`  
**RDBMS:** PostgreSQL, MySQL, Oracle  
**Caching:** In-memory caching systems, distributed cache  
**ORM:** JPA / Hibernate

---


### 🔧 DevSecOps & CI/CD

`GitHub Actions` `Terraform` `Kubernetes` `Helm` `Argo CD` `Jenkins` `Ansible` `Docker` `Istio`  
`Security Compliance` `SBOM` `Software Supply Chain Security` `Container Security` `Web Security`

- Zero-downtime deployment strategies, rolling upgrades, blue/green
- 100% security compliance across deployment layers
- CI/CD pipeline design, standardization, and migration



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
| **Ansible** | Infrastructure provisioning, configuration management |
| **Bash / Shell** | Cloud automation, Kubernetes scripting, pipeline scripting |
| **Python** | ML model development, automation scripting |
| **Terraform** | IaC for multi-cloud provisioning |




---

### 🔗 Public Profiles & Talks

| | |
|---|---|
| GitHub | [github.com/ranajit-jana](https://github.com/ranajit-jana) |
| LinkedIn | [linkedin.com/in/ranajitjana](https://linkedin.com/in/ranajitjana) |

---

*[← Experience](experience.md) &nbsp;·&nbsp; [Management →](management.md)*
