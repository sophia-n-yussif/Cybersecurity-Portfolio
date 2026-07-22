# Entry 1: Phishing-Based Account Compromise

**Investigation Date:** July 2026

## Description

An investigation was initiated after security monitoring detected two successful logins to an employee account from different geographic locations within a five-minute period. The account first authenticated from Ghana and approximately five minutes later authenticated from Romania.

Although a change in login location can sometimes be explained by legitimate travel or VPN usage, the combination of an impossible travel event, access to confidential company information, and an attempted mailbox forwarding rule indicated a likely account compromise. The investigation focused on determining the scope of unauthorized activity, assessing business impact, and identifying appropriate containment actions.

## Evidence Reviewed

- Authentication logs
- User account activity logs
- File access logs
- Email activity records
- Mailbox configuration changes

## Incident Summary (5 W's)

### Who caused the incident?

The investigation concluded that the activity was performed by an external threat actor who obtained valid employee credentials through a phishing attack. The attacker used the compromised credentials to access company resources while appearing as a legitimate user.

### What happened?

Authentication logs recorded a successful login from Ghana followed approximately five minutes later by another successful login originating from Romania.

Following authentication, the account accessed several confidential company files and attempted to create a mailbox forwarding rule.

While the geographic change alone could potentially be explained by VPN usage or legitimate travel, the subsequent access to sensitive information and the persistence attempt significantly increased confidence that the account had been compromised.

### When did the incident occur?

The incident was identified after security monitoring detected an impossible travel event followed by abnormal post-authentication activity.

### Where did the incident happen?

The incident occurred within Orion Logistics' identity and email environment. The compromised employee account was used to access confidential company resources and modify mailbox settings.

### Why did the incident happen?

The threat actor successfully obtained valid employee credentials through a phishing attack. The attacker appeared to be attempting to access confidential company information while establishing persistence through a mailbox forwarding rule that could allow continued monitoring of company communications.

## Impact Assessment

The compromised employee account represented a critical organizational asset because it provided legitimate access to internal systems and confidential business information.

Although no evidence confirmed that data was exfiltrated, the attacker successfully accessed confidential company files. As a result, the organization could no longer guarantee the confidentiality of the affected information because an unauthorized individual had sufficient opportunity to view sensitive resources during the compromise.

The attempted creation of a mailbox forwarding rule further increased the severity of the incident because it indicated a potential attempt to establish persistence and maintain long-term access.

The incident was classified as **High** severity due to the combination of unauthorized account access, exposure of confidential information, and indicators of persistence.

## Root Cause Analysis / Investigation Gaps

The investigation determined that the account compromise was likely caused by phishing-based credential exposure. This conclusion was based on the use of valid employee credentials, abnormal login activity, access to confidential files, and an attempted mailbox forwarding rule.

Further investigation would be required to determine:

- The exact phishing email or delivery method used to obtain the employee credentials
- Whether other employee accounts were targeted through similar phishing attempts
- Whether any additional persistence mechanisms were created
- Whether any confidential information was accessed beyond the identified files

Identifying the initial phishing method and full scope of attacker activity is necessary to prevent similar incidents from occurring in the future.

## Containment and Response Actions

Immediate response actions included:

- Disabling the compromised employee account
- Resetting the employee's credentials
- Removing the unauthorized mailbox forwarding rule
- Reviewing authentication and account activity logs
- Investigating all actions performed during the compromise period
- Determining whether any additional accounts had been affected

Long-term security improvements included:

- Implementing multi-factor authentication (MFA)
- Improving employee phishing awareness training
- Monitoring impossible travel events and abnormal authentication patterns
- Strengthening identity and access management controls

## Lessons Learned

This investigation demonstrated that geographic anomalies alone should not be treated as proof of compromise because legitimate travel or VPN usage may produce similar indicators.

However, multiple independent indicators—including an impossible travel event, unauthorized access to confidential information, and an attempted persistence mechanism—provided strong evidence that the account had been compromised.

The investigation also reinforced that the absence of confirmed data exfiltration does not eliminate business impact. Unauthorized access to confidential information alone represents a significant confidentiality risk and should be treated accordingly.

# Entry 2: Brute Force Attack Investigation

**Investigation Date:** July 2026

## Description

An investigation was initiated after security monitoring detected **ten consecutive failed login attempts** against an employee account originating from a public IP address. The failed attempts were followed by a successful authentication using the same account.

Although occasional failed logins can occur during normal user activity, the account owner confirmed they had not attempted to access the account during the period of the observed activity. The combination of repeated failed authentication attempts, successful access, and abnormal post-login behavior warranted further investigation to determine the extent of the compromise and assess its impact on the organization.

## Evidence Reviewed

- Authentication logs
- Failed and successful login records
- User account activity logs
- File access logs
- Source IP address information

## Incident Summary (5 W's)

### Who caused the incident?

The investigation concluded that the activity was consistent with an external threat actor attempting to gain unauthorized access to the employee account. This assessment was based on repeated failed authentication attempts, the employee's confirmation that they did not initiate the activity, and the abnormal actions performed after successful authentication.

### What happened?

Authentication logs recorded **ten consecutive failed login attempts** from a public IP address, followed by a successful login to the employee account.

After authentication, the account accessed several confidential Human Resources (HR) files before the activity was detected and the account was secured.

The sequence of events indicated that the successful authentication was likely unauthorized.

### When did the incident occur?

The incident was identified after security monitoring detected repeated failed authentication attempts, a successful login, and abnormal account activity shortly afterward.

### Where did the incident happen?

The incident occurred within Orion Logistics' identity management environment. The compromised employee account was used to access confidential HR resources.

### Why did the incident happen?

Based on the available evidence, the activity was consistent with an attempt to obtain unauthorized access to the employee account. Following successful authentication, the attacker accessed sensitive HR information before containment measures were implemented.

## Impact Assessment

The compromised employee account represented a critical organizational asset because it provided access to confidential Human Resources information.

Although no evidence confirmed that HR files were exfiltrated, the attacker successfully viewed sensitive information. As a result, the organization could no longer guarantee the confidentiality of the affected data because an unauthorized individual had access to confidential resources during the compromise.

The incident was classified as **High** severity because unauthorized access was successfully achieved and confidential organizational information was exposed.

## Root Cause Analysis / Investigation Gaps

The investigation determined that the activity was consistent with an attempted brute force attack against an employee account. This conclusion was based on ten consecutive failed login attempts from a public IP address, followed by successful authentication and unauthorized access to confidential HR files.

Further investigation would be required to determine:

- How the attacker obtained successful access after the failed login attempts
- Whether the account password was guessed, reused from another breach, or obtained through another method
- Whether other accounts experienced similar authentication attempts
- Whether any additional systems or resources were accessed after compromise

Identifying how the attacker successfully authenticated is necessary to improve identity protection controls and prevent future account compromise.

## Containment and Response Actions

Immediate response actions included:

- Disabling the compromised employee account
- Resetting the employee's credentials
- Reviewing authentication logs to determine the scope of the compromise
- Identifying all files accessed during the incident
- Investigating whether any additional accounts had been affected

Long-term security improvements included:

- Implementing multi-factor authentication (MFA)
- Strengthening account lockout policies to limit repeated authentication attempts
- Encrypting sensitive HR information
- Reviewing user permissions and authentication controls

## Lessons Learned

This investigation demonstrated that repeated failed authentication attempts should never be dismissed, particularly when followed by successful access and confirmed abnormal user activity.

The combination of **ten consecutive failed login attempts**, a successful authentication, confirmation from the employee that they were not responsible for the activity, and unauthorized access to confidential HR files provided strong evidence of account compromise.

The investigation also reinforced that the absence of confirmed data exfiltration does not eliminate the impact of an incident. Once an unauthorized individual gains access to confidential information, the organization can no longer guarantee its confidentiality.

# Entry 3: Ransomware Incident Investigation

**Investigation Date:** July 2026

## Description

An investigation was initiated after multiple employees reported that their files had become inaccessible. A suspicious README file was discovered on affected desktops, indicating that the organization may have experienced a ransomware attack.

The investigation focused on identifying the scope of the incident, determining the impact on business operations, understanding attacker activity, identifying the possible attack path, and recommending appropriate containment and recovery actions.

## Evidence Reviewed

- Reports from affected employees
- Encrypted file samples
- Suspicious README ransom note
- Endpoint activity records
- User and administrative account activity
- Backup availability and status
- System and network activity logs

## Incident Summary (5 W's)

### Who caused the incident?

The incident was caused by an external threat actor who deployed ransomware within the Orion Logistics environment.

The identity of the attacker and the method used to gain initial access were not confirmed during the initial investigation.

### What happened?

Multiple employees reported that their files had been encrypted and were no longer accessible. A suspicious README file discovered on affected desktops indicated that ransomware had been deployed.

The presence of encrypted files across multiple employee systems suggested that the attacker may have gained broader access within the environment before deploying the ransomware. Further investigation was required to determine whether lateral movement or the use of privileged accounts contributed to the spread of the attack.

### When did the incident occur?

The incident was identified after multiple employees reported inaccessible files and discovered suspicious ransom-related messages on their systems.

Further investigation would be required to determine how long the attacker had access to the environment before the ransomware deployment.

### Where did the incident happen?

The incident affected Orion Logistics' internal systems and employee workstations. The full scope of affected assets required further investigation.

### Why did the incident happen?

The attacker likely deployed ransomware to disrupt business operations and potentially pressure the organization into paying a ransom.

The attacker's full objectives, including whether they attempted to steal information before encryption, could not be confirmed during the initial investigation.

## Impact Assessment

The incident was classified as **Critical** due to the potential impact on business operations and the availability of organizational data.

The encryption of employee files created a significant availability risk because affected users could no longer access resources required to perform their duties.

The incident also created potential confidentiality and integrity concerns because the attacker may have accessed systems or data before deploying the ransomware.

Although backups were available, their condition, completeness, and ability to support recovery needed to be verified before determining recovery options.

## Root Cause Analysis / Investigation Gaps

The investigation confirmed that ransomware was deployed within the Orion Logistics environment; however, the exact initial access method could not be confirmed based on the available evidence.

Further investigation would be required to determine whether the attacker gained access through methods such as:

- Phishing or compromised employee credentials
- Exploitation of an unpatched vulnerability
- Compromise of an administrative account
- Another unauthorized access method

Additional investigation is also required to determine:

- How long the attacker had access to the environment before encryption occurred
- Whether lateral movement was performed between systems
- Whether sensitive information was accessed or exfiltrated before encryption
- Which accounts or systems were compromised during the attack
- Whether privileged accounts were used to deploy ransomware

Identifying the root cause and full attack path is necessary to prevent recurrence and improve security controls.

## Containment and Response Actions

Immediate response actions included:

- Isolating affected devices from the network
- Preventing further spread of the ransomware
- Identifying all affected systems and encrypted files
- Investigating the source of initial access
- Reviewing administrative account activity
- Preserving evidence for further investigation

Recovery actions included:

- Assessing backup availability and integrity
- Confirming backups were clean and not compromised
- Restoring systems from verified backups where possible
- Resetting compromised credentials
- Reviewing privileged account permissions

Long-term security improvements included:

- Improving email security controls and phishing detection
- Strengthening endpoint detection and response capabilities
- Implementing stronger access controls for administrative accounts
- Regularly testing backup and recovery procedures
- Improving security monitoring to detect suspicious activity earlier

## Lessons Learned

This investigation demonstrated that ransomware incidents require more than simply restoring encrypted files. Understanding how attackers gained access, what systems were affected, and whether sensitive information was accessed is essential for preventing future incidents.

The incident reinforced the importance of reliable backups, strong identity controls, privileged access management, and early detection capabilities.

A backup strategy is only effective if backups are regularly tested, protected from compromise, and capable of supporting recovery during a major security incident.
