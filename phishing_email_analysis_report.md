# Phishing Email Analysis Report

## Objective
Analyze a phishing email sample and identify phishing indicators.

## Phishing Indicators Found
### Indicator 1: Email spoofing
The sender address is suspicious because it does not belong to the official PayPal domain.

### Indicator 2: Urgent language
The email uses urgent language to pressure the recipient into taking immediate action.

### Indicator 3: Generic greeting
The email uses a generic greeting instead of addressing the recipient by name.

### Indicator 4: Suspicious link
The URL does not belong to PayPal and appears designed to deceive users.

### Indicator 5: Threatening message
The email threatens account closure to create fear and urgency.

### Indicator 6: Social engineering
The email uses social engineering tactics by creating urgency and fear.

## Header Analysis

Email authentication mechanisms help verify whether an email is legitimate.

### SPF (Sender Policy Framework)
SPF checks whether the sending mail server is authorized to send emails on behalf of the domain.

Result: Failed

### DKIM (DomainKeys Identified Mail)
DKIM verifies that the email content has not been altered during transmission.

Result: Failed

### DMARC (Domain-based Message Authentication, Reporting & Conformance)
DMARC uses SPF and DKIM results to determine whether an email should be trusted.

Result: Failed

### Conclusion
The email contains several phishing indicators including spoofed sender address, suspicious links, urgent language, and social engineering techniques. Therefore, it is identified as a phishing attempt.

## URL Analysis Using VirusTotal

The suspicious URL was analyzed using VirusTotal.

URL:
http://paypal-security-login.verify-user.com/

### Results
- 0 out of 92 security vendors flagged the URL as malicious.
- No known malware or phishing detection was reported at the time of analysis.

### Observations
- The URL does not belong to the official PayPal domain.
- The domain name contains the trusted brand name "PayPal" to appear legitimate.
- The actual domain is "verify-user.com", which is unrelated to PayPal.
- Attackers often use similar-looking domains to deceive users.

### Conclusion
Although VirusTotal did not flag the URL as malicious, the URL structure and domain mismatch indicate potential phishing behavior. Users should avoid clicking such links and verify website authenticity before entering credentials.

## Header Analysis Using MXToolbox

The email header was analyzed using the MXToolbox Email Header Analyzer.

### Header Information

| Field | Value |
|---------|---------|
| Return-Path | support@paypal-security.com |
| From | PayPal Security <support@paypal-security.com> |
| Subject | Urgent: Verify Your Account Immediately |
| Sending Server | unknown-server.com |
| Message-ID | 12345@unknown-server.com |

### Findings

1. The sender domain is not an official PayPal domain.
2. The email originated from an unknown server.
3. The subject line creates urgency to pressure the recipient.
4. The Message-ID references an unknown server instead of a trusted PayPal mail server.
5. The email exhibits characteristics commonly associated with phishing attacks.

### Conclusion

Based on the sender information, server details, and urgent language, the email displays multiple phishing indicators and should be treated as suspicious.