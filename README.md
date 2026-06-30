# enterprise-ad-itsm-lab
A production-grade, multi-server corporate environment integrating a Windows Active Directory Domain Controller with an optimized Ubuntu Linux LAMP stack to deploy a fully federated, automated ITSM service desk framework.
# Enterprise Active Directory & ITSM Infrastructure Integration Lab

## 📌 Project Overview
This production-grade engineering project demonstrates the end-to-end design, deployment, and federation of a corporate IT infrastructure sandbox. The lab bridges a Windows Server Active Directory Domain Controller with an open-source Linux (Ubuntu) LAMP web application stack to deliver a functional, highly automated Help Desk and Identity Management ecosystem. 

All systems are securely siloed within an isolated VirtualBox private NAT network framework to mimic true on-premise corporate server environments.

## 🛠️ Core Skills Demonstrated
- **Directory Services:** Active Directory Domain Controller configuration, Domain (`mydomain.local`) design, and administrative security mapping.
- **Linux Systems Administration:** Full provisioning of an Ubuntu Server node running an optimized Apache, MySQL, and PHP (LAMP) framework.
- **Directory Federation:** Advanced application bridging utilizing secure LDAP protocols to pull user identity verification natively from Windows Server.
- **Network Mail Architecture:** Deployment and testing of a local SMTP mail trap relay (`MailHog`) handling port mappings on 1025/8025 to monitor real-time automated system workflows.
- **ITSM & Operations Engineering:** Creation of an enterprise service catalog complete with custom triage configurations and high-priority Service Level Agreements (SLAs).

---

## 🏗️ Architecture & Component Matrix
- **Domain Controller VM:** Windows Server (`Active Directory Domain Services`)
- **Application VM:** Ubuntu Server (`Apache2`, `MySQL`, `PHP 8.x`)
- **Core Platform:** osTicket Help Desk Platform
- **Mail Integration Server:** MailHog SMTP service (Local Sandbox Node)

---

## ⚙️ Phase Execution & Implementation Steps

### Phase 1: Bare-Metal Virtualization & Platform Provisioning
- Established separate Linux and Windows virtual appliances inside VirtualBox.
- Configured individual port forwarding pathways (`8080` for web, `22` for SSH, `8025` for Mail UI), allowing clean administration from the host machine browser.
- Deployed the functional core database and application layers.

### Phase 2: LDAP Authentication & Directory Cross-Federation
- Linked the Linux web stack to the Active Directory domain controller.
- Integrated the `auth-ldap` plugin engine within osTicket to route all portal and agent login requests down to the Windows server backend database.

### Phase 3: Access Control Lists & Enterprise Agent Mapping
- Established explicit security boundaries separating regular domain accounts from Help Desk administrators.
- Configured the dashboard layout for internal tier-support users (e.g., `Jane Smith`).

### Phase 4: Local SMTP Mail Loop & SLA Automation (Go-Live)
- Compiled and deployed a local `MailHog` instance on port `1025` to safely route and review automated alert tickets without triggering outside networks.
- Formulated an enterprise-tier ticketing catalog, building custom workflows including a **Critical Response 4-Hour SLA** for high-priority incidents like Account Lockouts.

---

## 🏁 End-to-End Operational Validation
The deployment was fully verified by submitting a simulation ticket (`Password Reset / Account Lockout`) via the corporate end-user landing portal. The transaction was successfully processed through the system's routing logic, initiated the internal timer clock, and generated an automated system notification caught flawlessly by the localized MailHog SMTP relay.
