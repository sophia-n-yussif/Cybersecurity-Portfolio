# NexaHealth Security Risk Assessment

## 1. Assessment Overview

### Purpose

NexaHealth requested a security risk assessment to evaluate the security posture of its cloud-based healthcare platform after several security concerns were identified within the organization.

The objective of this assessment is to identify critical assets, analyze existing threats and vulnerabilities, evaluate associated risks, prioritize risks based on business impact, and recommend security improvements to strengthen NexaHealth's overall security posture.



# 2. Scope

## In Scope

The assessment covers:

- Cloud-based healthcare platform
- Cloud infrastructure
- Patient database
- Employee endpoints
- Identity and Access Management (IAM)
- Email platform
- Security monitoring practices
- Backup and recovery processes
- Access management practices

## Out of Scope

The assessment does not include:

- Third-party vendor systems
- Physical clinic locations
- Systems outside the cloud environment



# 3. Critical Assets

| Asset | Business Importance |
|---|---|
| Patient Database | Stores sensitive patient information that must remain confidential, accurate, and available. A compromise could result in regulatory penalties, loss of patient trust, and reputational damage. |
| Cloud Infrastructure | Hosts critical healthcare applications, services, and organizational resources. A compromise could result in unauthorized access, data exposure, service disruption, and operational downtime. |
| Identity Management System | Controls authentication and authorization for users accessing company resources. Weaknesses could allow unauthorized individuals to gain access to sensitive systems. |
| Employee Endpoints | Provide access to organizational resources and may serve as entry points for attackers through phishing, malware, or credential theft. |
| Email Platform | Supports business communication and represents a common attack surface for phishing and credential compromise. |
| Security Logs | Provide visibility into system activity and are essential for detecting, investigating, and responding to security incidents. |



# 4. Identified Security Concerns

The assessment was initiated after NexaHealth identified several security issues within the organization, including:

- Three phishing emails successfully deceived employees.
- A former employee account remained active for eight days after employment ended.
- Multiple failed login attempts from foreign IP addresses targeting employee accounts.
- Employees possess more permissions than required for their roles.
- Multi-factor authentication (MFA) is not implemented.
- Patient information is encrypted during transmission but not consistently encrypted while stored.
- Data retention policies are unclear.
- Security logs exist but are rarely reviewed.
- No formal incident response process exists.
- Backups exist but have never been tested.
- Employees receive limited cybersecurity awareness training.



## 5. Risk Assessment Findings


# Risk 1: Identity and Access Management Weaknesses

 # Evidence

- No MFA implemented.
- Employees have more permissions than required.
- Former employee accounts remained active after departure.
- Successful phishing attempts have occurred.

# Likelihood

High.

The likelihood of account compromise is increased due to weak authentication controls, excessive user privileges, delayed account deactivation, and evidence that employees have already been targeted through phishing attacks.

# Business Impact

Attackers who compromise employee accounts may gain unauthorized access to sensitive systems and cloud resources, access patient information, modify or delete critical data, and disrupt business operations.

Because NexaHealth operates a cloud-based environment, excessive permissions and weak authentication controls increase the possibility of attackers moving throughout the environment after compromising an account.

The organization may face regulatory penalties, financial losses, operational disruption, and reputational damage.

# Overall Risk Rating

High


# Risk 2: Data Protection Weaknesses

# Evidence

- Patient information is encrypted during transmission but not consistently encrypted while stored.
- Data retention policies are unclear.
- The organization manages sensitive healthcare information.

# Likelihood

High.

Sensitive healthcare information is at increased risk of exposure if unauthorized individuals gain access to systems containing patient data.

# Business Impact

Unauthorized access, disclosure, modification, or deletion of patient information could result in regulatory violations, financial penalties, loss of patient trust, and damage to NexaHealth's reputation.

# Overall Risk Rating

High



# Risk 3: Detection and Incident Response Gaps

# Evidence

- Security logs exist but are rarely reviewed.
- No formal incident response process exists.
- Suspicious login attempts from foreign IP addresses have been identified.

# Likelihood

High.

Limited monitoring capabilities reduce NexaHealth's ability to quickly identify malicious activity and investigate potential security incidents.

# Business Impact

Attackers may remain undetected for extended periods, increasing the potential impact of a breach.

Limited monitoring of cloud activity may prevent NexaHealth from identifying unauthorized access, suspicious configuration changes, or malicious activity occurring within its environment.

The organization may experience increased recovery costs, prolonged downtime, and difficulty determining the scope of a security incident.

# Overall Risk Rating

High


# Risk 4: Backup and Recovery Weaknesses

# Evidence

- Backups exist but have never been tested.

# Likelihood

Medium-High.

Untested backups do not necessarily increase the likelihood of an attack, but they create uncertainty regarding whether NexaHealth can successfully recover systems and data following a security incident.

# Business Impact

Failure to restore systems successfully could result in prolonged downtime, disruption of healthcare services, inability to access patient information, and financial losses.

# Overall Risk Rating

Medium-High


# Risk 5: Security Awareness Weaknesses

# Evidence

- Employees have limited cybersecurity awareness training.
- Three phishing emails successfully deceived employees.

# Likelihood

Medium.

Employees remain vulnerable to phishing and social engineering attacks. However, technical controls such as MFA, access restrictions, and email security solutions can reduce the impact of compromised credentials.

# Business Impact

Successful phishing attacks could result in credential theft, unauthorized access, malware infections, and exposure of sensitive organizational information.

# Overall Risk Rating

Medium



# 6. Risk Prioritization

| Priority | Risk | Rating | Reason |
|---|---|---|---|
| 1 | Identity and Access Management Weaknesses | High | Weak authentication controls, excessive permissions, and delayed account removal create a direct pathway for unauthorized access to critical systems and cloud resources. |
| 2 | Data Protection Weaknesses | High | NexaHealth handles sensitive healthcare information, and inadequate protection could result in regulatory penalties and significant reputational damage. |
| 3 | Detection and Incident Response Gaps | High | Limited monitoring and lack of response procedures may allow attackers to remain undetected and increase the impact of incidents. |
| 4 | Backup and Recovery Weaknesses | Medium-High | Untested backups may not increase the likelihood of an attack but could significantly increase downtime and recovery challenges after an incident. |
| 5 | Security Awareness Weaknesses | Medium | Employee awareness gaps increase phishing risk, but technical controls such as MFA can reduce the impact of compromised accounts. |

Identity and Access Management was prioritized first because it represents a foundational security control. A compromised identity can provide attackers with access to multiple organizational resources, especially when excessive permissions and weak authentication practices exist.



# 7. Recommendations

## Identity and Access Management

- Implement Multi-Factor Authentication (MFA) for all user accounts.
- Implement Role-Based Access Control (RBAC).
- Immediately deactivate accounts of departing employees.
- Conduct regular access reviews to ensure users only maintain required permissions.
- Apply the principle of least privilege across all systems.


## Data Protection

- Encrypt sensitive data while stored.
- Develop clear data classification and handling policies.
- Establish data retention and secure disposal procedures.
- Ensure security practices align with applicable regulatory requirements.



## Detection and Incident Response

- Implement centralized security log monitoring.
- Regularly review logs for suspicious activity.
- Monitor cloud activity and configuration changes.
- Develop a formal Incident Response Plan.
- Conduct incident response exercises to improve readiness.


## Backup and Recovery

- Regularly test backup restoration procedures.
- Establish documented recovery procedures.
- Ensure backups are secure, current, and protected from unauthorized modification.
- Define recovery objectives to understand acceptable downtime.


## Security Awareness

- Establish an ongoing cybersecurity awareness program.
- Train employees on identifying phishing attempts.
- Create clear procedures for reporting suspicious emails and security incidents.
- Conduct regular phishing simulations.


# 8. Conclusion

The assessment identified several security weaknesses affecting NexaHealth's ability to protect sensitive patient information and maintain reliable healthcare services.

The most significant risks involve identity and access management, data protection, security monitoring, incident response readiness, backup recovery, and employee security awareness.

By implementing the recommended security improvements, NexaHealth can reduce the likelihood and impact of cyber threats, improve regulatory compliance, strengthen incident response capabilities, and better protect critical healthcare information.
