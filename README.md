# IT Help Desk Simulation

> A practical IT Support portfolio project built around realistic incidents, structured troubleshooting, Jira Service Management workflows and documented technical evidence.

[![Project Status](https://img.shields.io/badge/Status-In%20Progress-f59e0b?style=flat-square )](https://github.com/anudoranador87/help-desk-simulation )
[![Environment](https://img.shields.io/badge/Environment-Windows%2011%20%7C%20Hyper--V-0078D6?style=flat-square&logo=windows )](documentation/)
[![Ticketing](https://img.shields.io/badge/Ticketing-Jira%20Service%20Management-0052CC?style=flat-square&logo=jira )](tickets/)
[![Focus](https://img.shields.io/badge/Focus-IT%20Support%20%7C%20Help%20Desk-2ea44f?style=flat-square )](tickets/)

---

## Project Overview

This project simulates a real-world IT Help Desk environment in which technical incidents are received, investigated, resolved and documented through a structured support workflow.

A Windows 11 virtual machine represents the end-user workstation of a fictional employee:

| User | Department | Company |
|---|---|---|
| Maria Garcia | Finance | Fabrikam Inc. |

Each incident is introduced in a controlled way and handled as it would be in a professional support environment:

1. Receive and classify the ticket
2. Confirm the reported symptoms
3. Gather technical and user-context information
4. Establish possible causes
5. Test the most likely hypotheses
6. Apply the appropriate resolution
7. Verify that the issue has been resolved
8. Document the root cause and final outcome
9. Close the ticket with clear technical notes

The purpose is not only to show the final fix, but also to demonstrate the reasoning and documentation behind it.

---

## What This Project Demonstrates

- Incident triage and prioritisation
- Help Desk and Service Desk workflows
- Jira Service Management ticket documentation
- Windows 11 troubleshooting
- Hyper-V virtual machine administration
- Network and DNS investigation
- Printer troubleshooting
- Disk-space analysis
- Shared-folder permissions
- Password-reset procedures
- Root-cause analysis
- Technical evidence collection
- User-focused communication
- Resolution verification
- Knowledge-base documentation

---

## Simulated Support Environment

| Component | Configuration |
|---|---|
| **End-user workstation** | Windows 11 virtual machine |
| **Hostname** | `WIN11-USER01` |
| **User** | Maria Garcia |
| **Department** | Finance |
| **Organisation** | Fabrikam Inc. |
| **Virtualisation** | Hyper-V |
| **Ticketing system** | Jira Service Management |
| **Repository purpose** | Public documentation, evidence and portfolio presentation |

The real tickets are managed in Jira Service Management. This repository contains a readable, version-controlled representation of each ticket together with supporting documentation and evidence.

> No real company data, credentials or sensitive user information should be stored in this repository.

---

## Incident Lifecycle

```mermaid
flowchart LR
    A["Ticket received"] --> B["Triage and prioritisation"]
    B --> C["Reproduce the issue"]
    C --> D["Collect evidence"]
    D --> E["Test probable causes"]
    E --> F["Apply resolution"]
    F --> G["Verify functionality"]
    G --> H["Document and close"]
    H --> I["Create or update knowledge base article"]
```

Each ticket follows the same documentation structure:

- **Investigation**
- **Evidence**
- **Root Cause**
- **Resolution**
- **Verification**
- **User-facing outcome**
- **Lessons learned**

---

## Portfolio Tickets

| ID | Incident or Request | Type | Current Status |
|---|---|---|---|
| [HD-001](tickets/HD-001-unable-to-access-websites.md) | Unable to access websites | Incident | In progress |
| [HD-002](tickets/HD-002-no-internet-connection.md) | No Internet connection | Incident | Planned |
| [HD-003](tickets/HD-003-printer-offline.md) | Printer appears offline | Incident | Planned |
| [HD-004](tickets/HD-004-disk-full-low-disk-space.md) | Disk full / low disk-space warning | Incident | Planned |
| [HD-005](tickets/HD-005-access-denied-shared-folder.md) | Access denied to a shared folder | Incident | Planned |
| [HD-006](tickets/HD-006-password-reset-request.md) | Password reset request | Service request | Planned |

> Ticket statuses will be updated as each scenario is executed, verified and documented with evidence.

---

## Ticket Documentation Model

Each ticket is written as a practical case study rather than a simple list of commands.

A completed ticket should answer the following questions.

### Investigation

- What did the user report?
- What was the impact?
- Can the issue be reproduced?
- What was checked first?
- Which hypotheses were considered?

### Root Cause

- What actually caused the issue?
- Which assumptions were ruled out?
- What evidence confirmed the cause?

### Resolution

- What corrective action was performed?
- Was the change safe and reversible?
- Could the resolution affect other users or systems?

### Verification

- What tests confirmed that the issue was resolved?
- Did the original user workflow work again?
- Was any additional preventive action required?

---

## Repository Structure

```text
help-desk-simulation/
├── tickets/
│   ├── HD-001-unable-to-access-websites.md
│   ├── HD-002-no-internet-connection.md
│   ├── HD-003-printer-offline.md
│   ├── HD-004-disk-full-low-disk-space.md
│   ├── HD-005-access-denied-shared-folder.md
│   └── HD-006-password-reset-request.md
│
├── evidence/
│   ├── screenshots/
│   └── videos/
│
├── knowledge-base/
│   └── Reusable troubleshooting and support articles
│
├── documentation/
│   ├── Virtual machine configuration
│   ├── PowerShell scripts
│   └── Technical notes
│
└── README.md
```

---

## Evidence and Documentation

Evidence may include:

- Screenshots of relevant Windows configuration
- Command output
- PowerShell or Command Prompt results
- Jira ticket screenshots
- Network diagnostics
- Event Viewer information
- Device Manager status
- File-system and disk-usage results
- Screen recordings of troubleshooting sessions
- Before-and-after verification results

Evidence is included to demonstrate the technical reasoning behind each action.

The objective is not to collect screenshots without context. Every piece of evidence should help answer one of these questions:

- What was the initial state?
- What was tested?
- What changed?
- How was the result verified?

---

## Support Methodology

The project follows a structured troubleshooting approach based on standard IT Support and CompTIA-style methodology:

1. **Identify the problem**
2. **Establish a theory of probable cause**
3. **Test the theory**
4. **Plan and implement the solution**
5. **Verify full system functionality**
6. **Document findings, root cause and preventive actions**

This approach helps avoid random troubleshooting and creates a repeatable process for future incidents.

---

## Knowledge Base

The `knowledge-base/` directory will contain reusable support documentation created from the completed incidents.

Planned knowledge-base topics include:

- Diagnosing web-access problems
- Checking DNS and TCP/IP configuration
- Troubleshooting Windows network connectivity
- Resolving offline printer status
- Investigating low disk-space warnings
- Understanding NTFS and share permissions
- Handling password-reset requests securely
- Documenting incident resolution effectively

A knowledge-base article should be written so that another support technician can understand and repeat the procedure.

---

## Project Roadmap

### Phase 1 — Environment Preparation

- [x] Define the simulated organisation and end-user scenario
- [x] Create the Windows 11 virtual-machine concept
- [x] Define the Jira Service Management project
- [x] Create the initial ticket set
- [ ] Document the complete VM configuration
- [ ] Add reusable PowerShell support scripts

### Phase 2 — First Completed Incident

- [ ] Inject the first controlled fault
- [ ] Create or update the Jira ticket
- [ ] Reproduce the issue
- [ ] Record the initial evidence
- [ ] Investigate possible causes
- [ ] Apply the resolution
- [ ] Verify the user workflow
- [ ] Add screenshots or video evidence
- [ ] Document the final root cause
- [ ] Close the ticket

### Phase 3 — Additional Incidents

- [ ] Complete the Internet-connectivity scenario
- [ ] Complete the printer scenario
- [ ] Complete the disk-space scenario
- [ ] Complete the shared-folder permissions scenario
- [ ] Complete the password-reset service request

### Phase 4 — Knowledge and Review

- [ ] Create knowledge-base articles from completed incidents
- [ ] Review all ticket documentation for consistency
- [ ] Remove or anonymise sensitive information
- [ ] Add final verification checklists
- [ ] Link the project from the main portfolio
- [ ] Record lessons learned from the complete simulation

---

## Project Status

**Current status:** In progress

The project is currently focused on validating the base Windows 11 environment and completing **HD-001** from start to finish:

```text
Controlled fault injection
        ↓
Ticket creation in Jira
        ↓
Issue reproduction
        ↓
Investigation and troubleshooting
        ↓
Resolution
        ↓
Evidence collection
        ↓
Verification
        ↓
Ticket closure
```

The remaining scenarios will be completed progressively using the same documentation and verification standard.

---

## Why This Project Matters

A support technician is not only responsible for knowing commands. Effective IT Support also requires the ability to:

- Ask the right questions
- Understand the user's impact
- Prioritise incidents correctly
- Work from evidence
- Communicate clearly
- Avoid unnecessary changes
- Verify the solution
- Document the result for future technicians

This project is designed to demonstrate that complete process.

---

## Related Projects

- [IT Support Labs](https://github.com/anudoranador87/it-support-labs )
- [Endpoint Health Toolkit](https://github.com/anudoranador87/endpoint-health-toolkit )
- [GitHub Profile](https://github.com/anudoranador87 )

---

## Portfolio Contact

- **LinkedIn:** [linkedin.com/in/joseaparicio87](https://www.linkedin.com/in/joseaparicio87/ )
- **GitHub:** [@anudoranador87](https://github.com/anudoranador87 )
- **Portfolio:** [Jose Maria — Portfolio](https://anudoranador87.github.io/JoseMaria-Frontend-Portfolio/ )

---

> **Reproduce. Investigate. Resolve. Verify. Document.**
