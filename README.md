# SOC Email Investigation — CNN Newsletter

## Project Overview
This project documents a hands-on email security investigation conducted in the **MyDFIR SOC Simulator** using Microsoft Defender XDR.

**Objective:** Determine whether a CNN-branded newsletter represented a phishing threat or legitimate email activity.

**Final Verdict: Likely Benign**

## Tools Used
- Microsoft Defender XDR
- Advanced Hunting (KQL)
- Microsoft Message Header Analyzer
- VirusTotal
- AbuseIPDB

## Investigation Methodology
1. Examined the email sender, recipient, subject, and delivery status.
2. Verified SPF, DKIM, and DMARC authentication results.
3. Investigated the sender's IP address and domain reputation.
4. Used KQL to review email delivery and URL-click telemetry.
5. Analyzed embedded URLs and sandbox results.
6. Correlated findings to determine whether containment was necessary.

## Key Findings
- The message was successfully delivered to the recipient's inbox.
- SPF, DKIM, and DMARC authentication passed.
- VirusTotal reported no malicious detections for the investigated sender IP and newsletter domain.
- AbuseIPDB reported a 3% abuse confidence score for the sender IP.
- No matching URL-click events were returned by the targeted hunting queries.
- Direct email preview was restricted by simulator permissions.

## Conclusion
**Likely Benign — No confirmed malicious activity**

The available evidence was consistent with legitimate newsletter delivery. There was insufficient evidence to justify blocking the sender, isolating devices, or disabling accounts.

The investigation was limited by email-preview permissions and available telemetry.

## Full Investigation Report
[View the SOC Email Investigation Report](CNN_Email_Investigation_Portfolio_Final.pdf)

## Lab Environment
This investigation was conducted in the isolated MyDFIR SOC Simulator for cybersecurity training and portfolio development. No live production systems were modified.
