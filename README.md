# Incident Response Plan Template

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![NIST SP 800-61](https://img.shields.io/badge/NIST-SP_800--61_Rev_2-blue.svg)]()
[![Framework](https://img.shields.io/badge/Framework-PICERL-green.svg)]()

A free, customizable **incident response plan template** for organizations of all sizes. Based on the NIST SP 800-61 Computer Security Incident Handling Guide, this template provides a structured framework for preparing for, detecting, containing, eradicating, and recovering from cybersecurity incidents.

> **Maintained by [Petronella Technology Group](https://petronellatech.com)** — A cybersecurity firm based in Raleigh, NC with 23+ years of experience helping organizations build and test incident response capabilities. For professional cybersecurity services, visit our [Cyber Security page](https://petronellatech.com/cyber-security/).

---

## Table of Contents

- [Why You Need an Incident Response Plan](#why-you-need-an-incident-response-plan)
- [Incident Response Frameworks](#incident-response-frameworks)
- [Incident Response Plan Template](#incident-response-plan-template-1)
  - [1. Plan Overview and Purpose](#1-plan-overview-and-purpose)
  - [2. Scope](#2-scope)
  - [3. Incident Response Team](#3-incident-response-team)
  - [4. Incident Classification](#4-incident-classification)
  - [5. Incident Response Phases](#5-incident-response-phases)
  - [6. Communication Plan](#6-communication-plan)
  - [7. Regulatory Notification Requirements](#7-regulatory-notification-requirements)
  - [8. Incident Response Playbooks](#8-incident-response-playbooks)
  - [9. Post-Incident Activities](#9-post-incident-activities)
  - [10. Plan Maintenance](#10-plan-maintenance)
- [Incident Response Playbooks](#incident-response-playbooks)
  - [Ransomware Response Playbook](#ransomware-response-playbook)
  - [Phishing Incident Playbook](#phishing-incident-playbook)
  - [Data Breach Playbook](#data-breach-playbook)
  - [Business Email Compromise (BEC) Playbook](#business-email-compromise-bec-playbook)
- [Tabletop Exercise Scenarios](#tabletop-exercise-scenarios)
- [Downloadable Templates](#downloadable-templates)
- [Additional Resources](#additional-resources)
- [About](#about)

---

## Why You Need an Incident Response Plan

Cybersecurity incidents are not a matter of *if* but *when*. An incident response plan is essential because:

1. **Regulatory compliance** — Required by CMMC, HIPAA, PCI DSS, NIST 800-171, SOX, and many other frameworks
2. **Reduced impact** — Organizations with tested IR plans contain breaches significantly faster and at lower cost
3. **Legal protection** — Demonstrates due diligence and can reduce liability
4. **Insurance requirements** — Most cyber insurance policies require a documented IR plan
5. **Business continuity** — Enables faster recovery and reduces operational downtime
6. **Stakeholder confidence** — Shows customers, partners, and regulators that you take security seriously

### The Cost of Not Having a Plan

According to industry breach cost research, organizations without an incident response team and tested IR plan experience significantly higher costs and longer breach lifecycles compared to those with mature IR capabilities.

## Incident Response Frameworks

This template is based on the **NIST SP 800-61 Rev. 2** framework, which defines six phases of incident response (PICERL):

| Phase | Description |
|-------|-------------|
| **P**reparation | Build IR capability before an incident occurs |
| **I**dentification | Detect and confirm that an incident has occurred |
| **C**ontainment | Limit the damage and prevent further spread |
| **E**radication | Remove the threat from the environment |
| **R**ecovery | Restore systems to normal operations |
| **L**essons Learned | Document what happened and improve for next time |

This is also compatible with SANS incident response methodology and can be adapted for ISO 27035 or CISA incident response guidance.

---

## Incident Response Plan Template

> **Instructions**: Copy this template, customize the bracketed fields `[ORGANIZATION NAME]`, and adapt each section to your environment. Remove this instruction block when done.

### 1. Plan Overview and Purpose

**Document Title**: `[ORGANIZATION NAME]` Incident Response Plan

**Version**: 1.0

**Effective Date**: `[DATE]`

**Last Reviewed**: `[DATE]`

**Document Owner**: `[CISO/IT DIRECTOR NAME AND TITLE]`

**Purpose**: This Incident Response Plan (IRP) establishes the procedures, roles, and responsibilities for responding to cybersecurity incidents affecting `[ORGANIZATION NAME]` information systems, data, and operations. The plan ensures a coordinated, efficient, and effective response to minimize impact and restore normal operations.

**Authority**: This plan is authorized by `[CEO/EXECUTIVE NAME AND TITLE]` and applies to all employees, contractors, and third parties with access to `[ORGANIZATION NAME]` systems and data.

### 2. Scope

This plan applies to:
- All information systems owned or operated by `[ORGANIZATION NAME]`
- All data processed, stored, or transmitted by `[ORGANIZATION NAME]`, including:
  - `[Controlled Unclassified Information (CUI)]`
  - `[Protected Health Information (PHI)]`
  - `[Personally Identifiable Information (PII)]`
  - `[Payment Card Data]`
  - `[Intellectual Property]`
  - `[Other sensitive data types]`
- All employees, contractors, and third-party users
- All facilities, including remote work locations
- Cloud services and third-party hosted environments

### 3. Incident Response Team

#### Core Team Members

| Role | Name | Contact | Backup |
|------|------|---------|--------|
| **Incident Response Lead** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |
| **IT Security Analyst** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |
| **System Administrator** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |
| **Network Administrator** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |
| **Legal Counsel** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |
| **HR Representative** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |
| **Communications/PR** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |
| **Executive Sponsor** | `[Name]` | `[Phone/Email]` | `[Backup Name]` |

#### External Resources

| Resource | Contact | Account/Contract # |
|----------|---------|-------------------|
| **Managed Security Provider** | `[Provider Name, Phone]` | `[Contract #]` |
| **Cyber Insurance Carrier** | `[Carrier Name, Phone]` | `[Policy #]` |
| **Forensics Firm** (retainer) | `[Firm Name, Phone]` | `[Retainer #]` |
| **Legal Counsel** (external) | `[Firm Name, Phone]` | `[Matter #]` |
| **Law Enforcement (FBI)** | `[Local Field Office Phone]` | |
| **CISA** | 1-888-282-0870 | |

### 4. Incident Classification

#### Severity Levels

| Severity | Description | Examples | Response Time | Escalation |
|----------|-------------|----------|--------------|------------|
| **Critical (S1)** | Active compromise with significant data exposure or operational impact | Active ransomware, confirmed data exfiltration, complete system outage | Immediate (within 15 min) | Executive team, legal, insurance, potentially law enforcement |
| **High (S2)** | Confirmed incident with potential for significant impact | Compromised admin account, malware on multiple systems, partial outage | Within 1 hour | IR Lead, management, MSP |
| **Medium (S3)** | Confirmed incident with limited scope | Single compromised workstation, successful phishing (no data access), policy violation | Within 4 hours | IR Lead, IT security |
| **Low (S4)** | Suspicious activity requiring investigation | Failed login attempts, suspicious email reported, minor policy violation | Within 24 hours | IT security analyst |

#### Incident Categories

| Category | Description |
|----------|-------------|
| **Malware/Ransomware** | Malicious software including ransomware, trojans, worms, viruses |
| **Phishing/Social Engineering** | Email or voice-based attacks targeting employees |
| **Unauthorized Access** | Unauthorized access to systems, networks, or data |
| **Data Breach/Exfiltration** | Confirmed or suspected loss or theft of sensitive data |
| **Denial of Service** | Attacks disrupting availability of systems or services |
| **Insider Threat** | Malicious or negligent actions by employees or contractors |
| **Business Email Compromise** | Email account takeover for fraud or data theft |
| **Physical Security** | Unauthorized physical access, stolen devices, tailgating |
| **Supply Chain** | Compromise through third-party vendors or software |
| **Web Application Attack** | SQL injection, XSS, or other attacks on web applications |

### 5. Incident Response Phases

#### Phase 1: Preparation

**Objective**: Ensure the organization is ready to respond to incidents.

- [ ] Maintain this incident response plan and review at least annually
- [ ] Conduct security awareness training for all employees
- [ ] Deploy and maintain security monitoring tools (SIEM, EDR, IDS/IPS)
- [ ] Establish and test backup and recovery procedures
- [ ] Maintain incident response toolkit and forensic tools
- [ ] Conduct tabletop exercises at least annually
- [ ] Maintain current contact lists and escalation procedures
- [ ] Review and test communication channels (out-of-band if primary is compromised)
- [ ] Ensure legal review of notification obligations
- [ ] Maintain cyber insurance policy and understand coverage

#### Phase 2: Identification

**Objective**: Detect, validate, and classify the incident.

**Detection Sources**:
- Security Information and Event Management (SIEM) alerts
- Endpoint Detection and Response (EDR) alerts
- Intrusion Detection/Prevention System (IDS/IPS) alerts
- User reports (phishing, suspicious activity)
- Third-party notifications (vendors, partners, law enforcement)
- Threat intelligence feeds
- External vulnerability scanning

**Initial Triage Checklist**:
- [ ] Date and time of detection
- [ ] Source of detection (who/what identified it)
- [ ] Description of the event
- [ ] Systems, networks, and data affected
- [ ] Current status (ongoing, contained, resolved)
- [ ] Initial severity classification
- [ ] Assign incident tracking number
- [ ] Begin incident log documentation
- [ ] Notify IR Lead if severity warrants

#### Phase 3: Containment

**Objective**: Limit the scope and impact of the incident.

**Short-Term Containment** (immediate actions):
- [ ] Isolate affected systems from the network (do NOT power off if forensics needed)
- [ ] Block malicious IPs, domains, or email addresses
- [ ] Disable compromised user accounts
- [ ] Change credentials for affected accounts
- [ ] Preserve evidence (memory dumps, disk images, logs)
- [ ] Activate out-of-band communications if primary channels compromised
- [ ] Document all containment actions taken

**Long-Term Containment** (temporary fixes):
- [ ] Apply temporary security controls
- [ ] Implement network segmentation changes
- [ ] Set up enhanced monitoring of affected areas
- [ ] Coordinate with third-party providers as needed
- [ ] Brief management on containment status

#### Phase 4: Eradication

**Objective**: Remove the threat and close the attack vector.

- [ ] Identify root cause and attack vector
- [ ] Remove malware from all affected systems
- [ ] Close exploited vulnerabilities (patch, configuration change)
- [ ] Reset all potentially compromised credentials
- [ ] Review and update firewall/IDS rules
- [ ] Scan all systems for additional compromise (lateral movement)
- [ ] Verify eradication through re-scanning and monitoring
- [ ] Document eradication activities

#### Phase 5: Recovery

**Objective**: Restore systems to normal operations securely.

- [ ] Develop a recovery plan with prioritized system restoration order
- [ ] Restore systems from known-good backups (verify backup integrity)
- [ ] Rebuild compromised systems from clean images if necessary
- [ ] Re-enable disabled services and accounts
- [ ] Implement enhanced monitoring during recovery period
- [ ] Validate system functionality and data integrity
- [ ] Confirm with system owners that operations are restored
- [ ] Monitor for signs of re-compromise for at least 30 days
- [ ] Document recovery activities and timeline

#### Phase 6: Lessons Learned

**Objective**: Improve future incident response capabilities.

- [ ] Conduct post-incident review meeting within 2 weeks
- [ ] Document timeline of events, actions taken, and outcomes
- [ ] Identify what worked well and what needs improvement
- [ ] Update incident response plan based on findings
- [ ] Update detection rules and monitoring based on attack indicators
- [ ] Implement preventive measures to address root cause
- [ ] Share anonymized lessons learned with relevant teams
- [ ] Update training materials if human factors contributed
- [ ] Archive incident documentation per retention policy

### 6. Communication Plan

#### Internal Communication

| Audience | When to Notify | Method | Responsible |
|----------|---------------|--------|-------------|
| Executive team | S1 within 30 min; S2 within 4 hours | Phone, then email | IR Lead |
| IT department | All severities, immediately | Teams/Slack, phone | IT Security |
| Legal counsel | S1/S2 immediately; S3 within 24 hours | Phone | IR Lead |
| HR | If employee involved | Phone | IR Lead |
| Affected department heads | After initial assessment | Email or meeting | IR Lead |
| All employees | If awareness needed | Email from management | Communications |

#### External Communication

| Audience | When to Notify | Method | Responsible |
|----------|---------------|--------|-------------|
| Cyber insurance carrier | S1/S2 within 24 hours | Phone | Legal/IR Lead |
| Law enforcement | If criminal activity suspected | Phone to FBI field office | Legal |
| Affected customers/individuals | Per regulatory requirements | Written notice | Legal/Communications |
| Regulatory bodies | Per applicable regulations | Official channels | Legal |
| Media | Only if necessary, after legal review | Press release/statement | Communications |
| Business partners | If partner data affected | Phone/email | IR Lead |

### 7. Regulatory Notification Requirements

| Regulation | Trigger | Deadline | Report To |
|-----------|---------|----------|-----------|
| **DFARS 252.204-7012** | Cyber incident affecting CUI | 72 hours | DIBNet |
| **HIPAA** | Breach of unsecured PHI | 60 days (individuals); annual (HHS if <500) | HHS OCR |
| **PCI DSS** | Cardholder data compromise | Immediately | Acquirer/card brands |
| **State Breach Laws** | PII exposure | Varies by state (typically 30-60 days) | State AG and/or affected individuals |
| **SEC** (public companies) | Material cybersecurity incident | 4 business days (Form 8-K) | SEC |
| **GDPR** | EU personal data breach | 72 hours | Supervisory authority |
| **CISA** | Critical infrastructure incidents | 72 hours (24 hours for ransom payments) | CISA |

### 8. Incident Response Playbooks

Detailed playbooks for common incident types are provided below and in the [`playbooks/`](playbooks/) directory.

### 9. Post-Incident Activities

- Complete incident report within 30 days of incident closure
- Present lessons learned to management
- Update risk assessment with new findings
- Modify security controls based on lessons learned
- Update training materials as needed
- Retain incident documentation for `[6 years / per retention policy]`

### 10. Plan Maintenance

| Activity | Frequency | Responsible |
|----------|-----------|-------------|
| Full plan review and update | Annually | IR Lead |
| Contact list verification | Quarterly | IT Security |
| Tabletop exercise | Annually (minimum) | IR Lead |
| Technical exercise/drill | Semi-annually | IT Security |
| Post-incident plan updates | After each significant incident | IR Lead |
| Distribution to stakeholders | After each update | IR Lead |

---

## Incident Response Playbooks

### Ransomware Response Playbook

**Trigger**: Ransomware detected or suspected on any system.

**Immediate Actions (First 15 Minutes)**:
1. **DO NOT** pay the ransom without executive and legal approval
2. **DO NOT** power off affected systems (preserve evidence in memory)
3. Disconnect affected systems from the network (pull ethernet, disable WiFi)
4. Alert the IR Lead and initiate S1 response
5. Activate out-of-band communication (personal phones, separate email)
6. Take photos of any ransom notes displayed on screens

**Containment (First Hour)**:
1. Identify the scope — how many systems are affected?
2. Determine the ransomware variant (ransom note, file extension, IOCs)
3. Check for available decryptors at [No More Ransom Project](https://www.nomoreransom.org/)
4. Block known C2 (command and control) domains and IPs at the firewall
5. Disable file sharing services (SMB, NFS)
6. Isolate network segments containing affected systems
7. Preserve at least one encrypted system for forensic analysis

**Assessment**:
1. Determine the entry point (phishing, RDP, vulnerability, supply chain)
2. Assess data exfiltration — check for double extortion indicators
3. Evaluate backup integrity — are backups intact and uncompromised?
4. Notify cyber insurance carrier
5. Engage forensics firm if needed

**Recovery**:
1. Rebuild affected systems from clean images
2. Restore data from verified clean backups
3. Reset all credentials (domain admin, service accounts, user accounts)
4. Apply patches that address the entry point vulnerability
5. Implement enhanced monitoring before reconnecting systems
6. Monitor for re-infection for 90 days

### Phishing Incident Playbook

**Trigger**: Employee reports a suspicious email or clicks a suspected phishing link.

**If the user only received/reported (did not click)**:
1. Thank the user for reporting
2. Analyze the email headers, links, and attachments in a sandbox
3. Block the sender domain/IP at the email gateway
4. Search for the same email across all mailboxes
5. Remove all instances of the phishing email
6. Update email filtering rules

**If the user clicked a link or opened an attachment**:
1. Immediately isolate the user's workstation from the network
2. Have the user change their password from a different, clean device
3. Check for credential harvesting — was a login page spoofed?
4. If credentials were entered: force password reset, revoke active sessions, check for MFA bypass
5. Run full endpoint scan on affected workstation
6. Check email rules for unauthorized forwarding rules
7. Review audit logs for the compromised account

### Data Breach Playbook

**Trigger**: Confirmed or suspected unauthorized access to or exfiltration of sensitive data.

**Immediate Actions**:
1. Classify the type and volume of data potentially exposed
2. Identify affected individuals and data subjects
3. Preserve all relevant logs and evidence
4. Engage legal counsel for notification obligations
5. Notify cyber insurance carrier

**Investigation**:
1. Determine how access was gained
2. Identify the full scope of data accessed or exfiltrated
3. Determine if data was encrypted in transit/at rest
4. Check network logs for data exfiltration indicators
5. Assess whether data was actually viewed or just accessible

**Notification** (per legal guidance):
1. Prepare notification letters for affected individuals
2. File required regulatory notifications
3. Establish a call center or FAQ page if large-scale breach
4. Offer credit monitoring if PII was exposed

### Business Email Compromise (BEC) Playbook

**Trigger**: Email account takeover, fraudulent wire transfer request, or vendor impersonation detected.

**Immediate Actions**:
1. If a wire transfer was initiated: contact the bank immediately to halt/reverse the transfer
2. Disable the compromised email account
3. Check for email forwarding rules added by the attacker
4. Review sent items for fraudulent messages
5. Alert finance/accounting team of the compromise

**Investigation**:
1. Determine how the account was compromised (credential theft, token theft, etc.)
2. Review email access logs for unauthorized access from unusual IPs/locations
3. Check for OAuth app consent grants
4. Identify all contacts who received fraudulent emails
5. Assess financial impact

**Recovery**:
1. Reset the account password and revoke all active sessions
2. Remove unauthorized forwarding rules and app permissions
3. Notify recipients of fraudulent emails
4. Review and strengthen MFA configuration
5. Implement additional BEC protections (DMARC, impersonation protection)

---

## Tabletop Exercise Scenarios

Use these scenarios for annual tabletop exercises to test your IR plan:

### Scenario 1: Ransomware Attack
> On a Monday morning, multiple employees report that their files have been encrypted and a ransom note demands $500,000 in Bitcoin. IT discovers that the file server, domain controller, and 40% of workstations are affected. The attacker claims to have exfiltrated customer data and threatens to publish it.

**Discussion Questions**:
- Who do we notify first?
- Do we have clean backups? How quickly can we restore?
- How do we determine if data was actually exfiltrated?
- What is our position on ransom payment?
- What are our notification obligations?

### Scenario 2: Insider Data Theft
> HR notifies you that a senior engineer submitted their resignation. The next day, the SIEM alerts that the engineer copied 50GB of files to a personal cloud storage account, including source code and customer databases, outside of normal working hours.

### Scenario 3: Supply Chain Compromise
> A critical software vendor announces that their update server was compromised and a malicious update was distributed to all customers over the past 30 days. Your organization deployed this update to all servers two weeks ago.

### Scenario 4: Business Email Compromise
> The CFO receives an urgent email from the CEO (who is traveling abroad) requesting an immediate wire transfer of $250,000 to a new vendor. The finance team processes the transfer. Two hours later, the real CEO calls in and denies sending the email.

---

## Downloadable Templates

- [`incident-response-plan-template.md`](incident-response-plan-template.md) — Full IR plan in markdown (this document without the overview sections)
- [`incident-report-form.md`](incident-report-form.md) — Individual incident documentation form
- [`playbooks/ransomware.md`](playbooks/ransomware.md) — Standalone ransomware playbook
- [`playbooks/phishing.md`](playbooks/phishing.md) — Standalone phishing playbook

## Additional Resources

### Official Sources
- [NIST SP 800-61 Rev. 2](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final) — Computer Security Incident Handling Guide
- [CISA Incident Reporting](https://www.cisa.gov/report) — Report incidents to CISA
- [FBI IC3](https://www.ic3.gov/) — Report internet crimes
- [No More Ransom Project](https://www.nomoreransom.org/) — Free ransomware decryption tools

### Related Open-Source Resources
- [CMMC Compliance Checklist](https://github.com/capetron/cmmc-compliance-checklist) — CMMC Level 2 self-assessment
- [HIPAA Security Risk Assessment Template](https://github.com/capetron/hipaa-security-risk-assessment-template) — HIPAA SRA template
- [Cybersecurity Awareness Training Materials](https://github.com/capetron/cybersecurity-awareness-training-materials) — Free training resources

### Professional Cybersecurity Services

For organizations needing expert guidance on incident response planning and cybersecurity, [Petronella Technology Group](https://petronellatech.com/cyber-security/) provides:

- **Incident response planning** and plan development
- **Tabletop exercise facilitation** with realistic scenarios
- **Managed detection and response (MDR)** services
- **Digital forensics and incident response (DFIR)** retainers
- **Security Operations Center (SOC)** services
- **Vulnerability assessment and penetration testing**

> Visit [petronellatech.com/cyber-security/](https://petronellatech.com/cyber-security/) to learn more about our cybersecurity services.

---

## About

This incident response plan template is maintained by **[Petronella Technology Group](https://petronellatech.com)**, a cybersecurity and IT compliance firm headquartered in Raleigh, North Carolina. Founded in 2002, Petronella Technology Group has over 23 years of experience helping organizations prepare for, detect, and respond to cybersecurity incidents.

### Other Security Resources
- [CMMC Compliance Checklist](https://github.com/capetron/cmmc-compliance-checklist)
- [HIPAA Security Risk Assessment Template](https://github.com/capetron/hipaa-security-risk-assessment-template)
- [NIST 800-171 Controls Matrix](https://github.com/capetron/nist-800-171-controls-matrix)
- [Cybersecurity Awareness Training Materials](https://github.com/capetron/cybersecurity-awareness-training-materials)

---

*This template is provided for informational purposes and should not be considered legal advice. Organizations should consult with qualified cybersecurity and legal professionals for their specific incident response needs.*

*Licensed under [CC-BY-SA-4.0](LICENSE). Contributions welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).*
