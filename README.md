# 🔐 CyberArk Secrets Management Labs
CyberArk Secrets Manager • Secrets Hub • Cloud & CI/CD Security

## Overview
This repository contains hands-on, security-focused labs and reference implementations for CyberArk Secrets Manager, CyberArk Conjur Cloud, and Secrets Hub. The goal is to demonstrate secure, cloud-native secrets management patterns using identity-based authentication, zero-trust principles, and DevSecOps best practices.

## Why This Repository Exists
Most secrets management failures are design failures, not tooling failures. These labs demonstrate secure-by-design implementations to prevent credential leakage, secret sprawl, and over-permissioned access.

## Scope & Technologies
- CyberArk Secrets Manager
- CyberArk Secrets Hub
- IAM & JWT authentication
- CI/CD integrations
- Kubernetes workloads
- Multi-cloud (AWS, Azure, GCP)

## Architecture Overview
The labs demonstrate:
- Identity-based authentication (no static credentials)
- Centralized secrets governance
- Runtime secret injection
- Least-privilege access
- Auditability and resiliency

## Labs
### Lab 01 – IAM Authentication
Identity-based authentication using AWS IAM or Azure Managed Identity.

### Lab 02 – JWT Authentication for CI/CD
Secure CI/CD pipelines using short-lived JWT tokens.

### Lab 03 – Kubernetes Secret Injection
Secure runtime secret injection into Kubernetes workloads.

### Lab 04 – Secrets Hub
Centralized secrets governance with cloud-native secret stores.

## Security Principles
- Zero Trust
- Identity First
- Least Privilege
- Auditability
- No Hardcoded Secrets

## Disclaimer
For educational purposes only. No real secrets included.

## Author
Arun Vishwanath
