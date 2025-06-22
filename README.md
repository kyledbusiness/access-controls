# What Are Access Controls?

Access controls are the foundation of modern identity and access management (IAM), determining **who** can access **what**, **when**, and **how**. This guide provides a beginner-friendly overview of the different types of access controls and how they apply across IAM, IGA, and PAM environments.

## Table of Contents

- [1. What Are Access Controls?](#1-what-are-access-controls)
- [2. Key Concepts](#2-key-concepts)
- [3. Types of Access Control Models](#3-types-of-access-control-models)
- [4. Access Control in IAM, IGA, and PAM](#4-access-control-in-iam-iga-and-pam)
- [5. Real-World Examples](#5-real-world-examples)
- [6. Common Misconfigurations](#6-common-misconfigurations)
- [7. Final Thoughts](#7-final-thoughts)

---

## 1. What Are Access Controls?

Access controls are mechanisms that define and enforce how users, systems, and services interact with digital resources. They answer the question: **“Is this entity allowed to perform this action on this resource?”**

---

## 2. Key Concepts

- **Subject**: The user or entity requesting access
- **Object**: The resource or system being accessed
- **Action**: What the subject is trying to do (read, write, delete, etc.)
- **Policy**: The rules that define who can do what

---

## 3. Types of Access Control Models

### Role-Based Access Control (RBAC)

- Access is granted based on assigned **roles**.
- Common in enterprise environments.
- Example: All users with the “HR” role can access payroll data.

### Attribute-Based Access Control (ABAC)

- Access is determined by attributes like department, location, time of day.
- More granular and flexible than RBAC.
- Example: Users in `Dept: Finance` and `Location: HQ` can view budget reports during business hours.

### Discretionary Access Control (DAC)

- Owners of a resource determine who gets access.
- Common in file-sharing systems.
- Example: You share a Google Doc with specific people.

### Mandatory Access Control (MAC)

- Access is enforced by a central authority based on sensitivity labels.
- Often used in government/military environments.
- Example: Users with `Top Secret` clearance can access `Top Secret` data only.

---

## 4. Access Control in IAM, IGA, and PAM

| Domain | Role of Access Control |
|--------|------------------------|
| **IAM** | Controls who can access which apps/resources |
| **IGA** | Manages the lifecycle of identities and enforces governance (e.g., access reviews) |
| **PAM** | Protects and restricts access to privileged accounts and elevated actions |

---

## 5. Real-World Examples

- **IAM**: Azure AD Conditional Access blocks sign-ins from unknown IPs.
- **IGA**: Access review removes users from groups after 90 days of inactivity.
- **PAM**: CyberArk grants temporary access to domain admin credentials, with full session recording.

---

## 6. Common Misconfigurations

- Over-permissioned users due to use of broad roles (e.g., “Owner” instead of “Reader”)
- Lack of separation between regular and privileged accounts
- Failure to implement access reviews or periodic re-certification
- Unused accounts with active access

---

## 7. Final Thoughts

Access control is one of the most important yet misunderstood aspects of cybersecurity. Whether you're new to IAM or expanding into PAM and IGA, understanding how access decisions are made—and enforced—is essential.
