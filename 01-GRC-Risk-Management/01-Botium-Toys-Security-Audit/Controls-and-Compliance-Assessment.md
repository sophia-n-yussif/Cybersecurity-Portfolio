# Botium Toys Controls and Compliance Assessment

## Overview

This assessment evaluates Botium Toys' existing security controls and compliance practices based on the provided scope, goals, and risk assessment documentation. The purpose was to identify implemented controls, control gaps, and areas where improvements are required to strengthen the organization's security posture.


# Controls Assessment

## Access Control

### Least Privilege

**Status:** Not Implemented

**Observation:**
All employees currently have access to internally stored data, including potentially sensitive customer information. Access restrictions based on job responsibilities have not been implemented.

**Security Impact:**
Excessive access permissions increase the risk of unauthorized data exposure or misuse of sensitive information.


### Separation of Duties

**Status:** Not Implemented

**Observation:**
Separation of duties controls have not been established within the organization.

**Security Impact:**
A lack of separation between responsibilities may increase the risk of unauthorized actions going undetected.


# Data Protection

## Encryption

**Status:** Not Implemented

**Observation:**
Customer payment information is accepted, processed, transmitted, and stored internally without encryption controls.

**Security Impact:**
Sensitive payment data may be exposed if unauthorized individuals gain access to internal systems.


# Authentication and Password Management

## Password Policy

**Status:** Partially Implemented

**Observation:**
A password policy exists; however, the requirements do not align with stronger password security practices.

**Security Impact:**
Weak password requirements increase the risk of account compromise.


## Password Management System

**Status:** Not Implemented

**Observation:**
Botium Toys does not have a centralized password management system to enforce password requirements.

**Security Impact:**
Security policies may not be consistently applied across user accounts.


# Business Continuity

## Disaster Recovery Plans

**Status:** Not Implemented

**Observation:**
The organization does not currently have a disaster recovery plan.

**Security Impact:**
The company may experience extended downtime and difficulty recovering after security incidents or system failures.


## Backups

**Status:** Not Implemented

**Observation:**
Critical business data is not currently backed up.

**Security Impact:**
Data loss from incidents such as ransomware or system failure could significantly affect business operations.


# Security Monitoring

## Firewall

**Status:** Implemented

**Observation:**
A firewall is currently configured to block network traffic based on defined security rules.

**Security Impact:**
The firewall provides a layer of protection against unauthorized network activity.


## Antivirus Software

**Status:** Implemented

**Observation:**
Antivirus software is installed and monitored regularly by the IT department.

**Security Impact:**
Antivirus controls help detect and prevent known malicious software threats.


## Intrusion Detection System (IDS)

**Status:** Not Implemented

**Observation:**
An intrusion detection system has not been deployed.

**Security Impact:**
The organization has reduced visibility into suspicious network activity and potential attacks.


# Physical Security Controls

## Physical Access Controls

**Status:** Implemented

**Observation:**
The physical location has appropriate locks, CCTV surveillance, and fire detection/prevention systems.

**Security Impact:**
Existing physical controls help protect company assets and facilities.


# Compliance Assessment

## PCI DSS

**Assessment: Requires Improvement**

### Identified Gaps:
- Customer payment information is not encrypted.
- Access to cardholder data is not restricted using least privilege.
- Password management practices require improvement.

### Risk:
Weak protection of payment information could result in unauthorized access, data exposure, and compliance issues.


## GDPR

**Assessment: Partially Implemented**

### Existing Controls:
- A breach notification plan exists to notify EU customers within 72 hours.
- Privacy policies and procedures have been established.

### Identified Gaps:
- Employee access to stored customer data is not sufficiently restricted.
- Data classification and inventory practices require improvement.

### Risk:
Insufficient protection of personal data may result in privacy violations and regulatory consequences.


## SOC Principles

**Assessment: Requires Improvement**

### Existing Controls:
- Data integrity and availability controls are currently supported.
- Firewall and antivirus protections are implemented.

### Identified Gaps:
- User access controls require improvement.
- Sensitive data confidentiality requires stronger protection.
- Additional monitoring capabilities are needed.


# Summary

The assessment identified that Botium Toys has some foundational security controls in place, including firewall protection, antivirus software, physical security measures, and privacy procedures. However, significant gaps remain in access control, data protection, authentication, recovery planning, and security monitoring.

Addressing these gaps through prioritized security improvements will help reduce risk and improve the organization's overall security posture.
