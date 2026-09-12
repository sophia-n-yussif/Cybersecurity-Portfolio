## Network Traffic Analysis

### Overview
This section contains network traffic analysis investigations focused on examining packet captures, identifying indicators of compromise, and tracing malicious activity back to its source. The projects demonstrate my ability to work directly with raw network evidence rather than pre-processed logs or alerts, using protocol analysis to answer specific investigative questions.

## Investigative Framework
Rather than memorizing specific Wireshark filters, I approach each investigation by working through a consistent set of questions, expanding outward from a single starting point:

1. Orient - What protocols exist in this capture before filtering on anything specific?
2. Follow the alert - What traffic matches the exact detail given (IP, port, protocol, time)?
3. Identify the machine - What internal IP and MAC address generated that traffic?
4. Identify the person - Which protocol is most likely to reveal identity information, and why? Protocols tied to automatic, routine activity (such as Kerberos authentication during a normal Windows login) are checked before protocols that only appear when something deliberately queries account details (such as SAMR or LDAP).
5. Reconstruct the activity - What does the traffic itself show about what happened, distinguishing confirmed evidence from reasonable inference.
6. Extract evidence - What indicators of compromise, screenshots, and findings support the conclusions drawn.

An empty or unreadable result from any given protocol is treated as information rather than a dead end, and is used to decide the next protocol to check rather than a reason to stop.

### Traffic Analysis Investigations

1. Lumma Stealer Victim Identification
An investigation into a signature alert for Lumma Stealer fingerprinting activity detected on an internal network. This scenario focuses on using a packet capture to identify the infected host, the associated user account, and the malicious domain behind the alert, working from a single IP address and timestamp as the only starting information.

### NIST Cybersecurity Framework Alignment
This project aligns with the NIST Cybersecurity Framework (CSF) 2.0, particularly the Detect and Respond functions.

Detect
- Identify indicators of compromise within raw network traffic.
- Analyze protocol behavior to distinguish expected activity from malicious activity.

Respond
- Determine the identity and scope of an affected host from limited alert information.
- Extract indicators of compromise to support containment and blocking decisions.

### Skills Demonstrated
- Packet capture analysis
- Protocol identification and filtering
- Indicator of compromise extraction
- Host and user attribution from network evidence
- Evidence-based troubleshooting when initial approaches fail
- Technical documentation of an investigative process

### Key Takeaways
Through this investigation, I developed a stronger understanding of how identity and activity can be traced through raw network traffic rather than relying on pre-built alerts or dashboards. This project helped me practice:
- Reasoning about which protocols are likely to appear in a capture, based on how they are actually generated on a network, rather than guessing filters at random.
- Treating an empty filter result as information rather than a dead end, and adjusting my approach accordingly.
- Working methodically from a single piece of alert information outward to a full picture of host, user, and malicious infrastructure.
- Documenting a technical investigation clearly enough that another analyst could follow the same reasoning.
