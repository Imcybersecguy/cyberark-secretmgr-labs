🔐 CyberArk Secrets Management Labs

Conjur Cloud • CyberArk Secrets Manager • Secrets Hub

Overview

This repository contains hands-on, security-focused labs and reference implementations for CyberArk Secrets Manager, CyberArk Conjur Cloud, and Secrets Hub.
The goal is to demonstrate secure, cloud-native secrets management patterns using identity-based authentication, zero-trust principles, and DevSecOps best practices across modern infrastructure.

These labs focus on how secrets should be designed, protected, and consumed in production environments, not just how to make them work.

Why This Repository Exists

Most secrets management failures are not tooling issues—they are design and security failures:

Hardcoded credentials in CI/CD

Over-permissioned access

Poor rotation and audit visibility

Secret sprawl across cloud services

This repository addresses those problems by showcasing secure-by-design implementations using CyberArk technologies.

Scope & Technologies

This repository covers:

CyberArk Conjur Cloud

CyberArk Secrets Manager

CyberArk Secrets Hub

Cloud-native authentication (IAM, JWT, Kubernetes)

CI/CD integrations (GitHub Actions, Jenkins, Azure DevOps)

Multi-cloud environments (AWS, Azure, GCP)

Kubernetes workloads

Secret rotation, audit, and governance

Architecture Overview

High-level architecture patterns demonstrated in this repository:

Identity-based authentication (no static credentials)

Centralized secrets governance

Runtime secret injection

Least-privilege access controls

High availability and resiliency

End-to-end auditability

📌 Architecture diagrams for each lab are available in the /architecture directory.

Labs Breakdown
🔹 Lab 01 – IAM Authentication (AWS / Azure)

Objective:
Demonstrate secure, identity-based authentication using cloud IAM instead of static credentials.

Key Security Concepts:

AWS IAM roles / Azure Managed Identity

SigV4 request signing

Trust boundary enforcement

Least privilege policy design

Security Focus:

Eliminates long-lived secrets

Prevents credential leakage

Enforces workload identity

🔹 Lab 02 – JWT Authentication for CI/CD

Objective:
Secure CI/CD pipelines using short-lived JWT tokens issued by trusted CI/CD providers.

Key Security Concepts:

JWT claims validation (iss, aud, sub)

Trust relationships between CI/CD and Conjur Cloud

Token expiry and replay protection

Security Focus:

No secrets stored in pipelines

Fine-grained workload identity

Reduced blast radius

🔹 Lab 03 – Kubernetes Secret Injection

Objective:
Demonstrate secure secret delivery to Kubernetes workloads at runtime.

Key Security Concepts:

Kubernetes authenticator

Sidecar / init container patterns

Runtime secret injection

Security Focus:

Avoids Kubernetes Secrets storage

Prevents plaintext secrets at rest

Supports dynamic rotation

🔹 Lab 04 – CyberArk Secrets Hub

Objective:
Show how CyberArk Secrets Hub synchronizes secrets into cloud-native secret stores.

Key Security Concepts:

Centralized source of truth

Controlled secret propagation

Rotation visibility and audit

Security Focus:

Prevents secret sprawl

Maintains governance while enabling cloud-native services

Trade-offs vs direct Conjur access

Security Design Principles

All labs follow these principles:

Zero Trust: No implicit trust between systems

Identity First: Authentication via workload identity, not credentials

Least Privilege: Minimal access required to retrieve secrets

Auditability: Every secret access is traceable

Resilience: HA and failure-aware design

No Hardcoded Secrets: Ever

Threat Model (High-Level)
Threat	Mitigation
Credential leakage	IAM/JWT authentication
Pipeline compromise	Short-lived tokens
Secret sprawl	Centralized governance
Over-permission	Policy-based access
Insider risk	Audit logging & RBAC
Failure Scenarios Covered

Each lab documents and demonstrates:

Authentication failures

Token expiration

Misconfigured policies

Identity mismatch

Network or Edge failures

Understanding what breaks and why is critical for secure production deployments.

Compliance & Audit Considerations

The implementations support:

Centralized audit logging

Access traceability

Evidence collection for compliance frameworks (ISO, SOC2, PCI-DSS).
