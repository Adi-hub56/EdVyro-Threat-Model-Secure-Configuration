# EdVyro Cyber Security Internship – Threat Model and Secure Configuration

## Project Overview
This project presents a threat model and prioritized hardening plan for a **fictional student portal** running on localhost or an isolated VM.

The objective is to identify realistic assets and abuse cases, categorize threats using **STRIDE**, prioritize risks using likelihood and impact, and recommend proportionate defensive controls.

## Scope
- Environment: Fictional student portal
- Intended environment: Localhost or isolated VM
- Assessment type: Defensive threat modeling
- Methodology: STRIDE
- Output: Threat-model diagram, risk register, prioritized hardening checklist
- External systems: No external systems are tested or scanned

## Assumptions
The task brief does not provide a detailed implementation architecture. Therefore, these are **threat-modeling assumptions**, not findings from a live application:
- Students use a web browser to access the portal.
- An administrator has access to an administrative interface.
- The web application communicates with a database.
- The application may use an email service for notifications.
- Authentication and authorization are handled by the application.

## Repository Contents
- `threat-model.md` – system context, assets, trust boundaries, STRIDE analysis, and diagram
- `risk-register.md` – prioritized risk register with mitigation and verification
- `hardening-checklist.md` – prioritized defensive controls with verification steps
- `diagram.md` – standalone GitHub-rendered Mermaid diagram

## Methodology
Threats were considered using STRIDE:
- Spoofing
- Tampering
- Repudiation
- Information Disclosure
- Denial of Service
- Elevation of Privilege

Risk priority is based on qualitative likelihood and impact.

## Disclaimer
This is a defensive threat-modeling exercise for an authorized fictional/local environment. No external systems were tested or scanned.
