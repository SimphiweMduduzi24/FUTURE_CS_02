
# Email Header Analysis

## Introduction
Email header analysis is used to examine information about an email's origin, sender and authentication results.

This investigation uses a simulated email header for educational purposes.

## Email Under Investigation

Sender: security-alert@bank-example.invalid

Reply-To: support@unknown-example.invalid

Return-Path: bounce@unknown-example.invalid

## Authentication Results

### 1. SPF – FAIL
The sending server failed the SPF authentication check.

### 2. DKIM – FAIL
The email failed the DKIM signature verification check.

### 3. DMARC – FAIL
The email failed the DMARC authentication and alignment checks.

## Findings

The email contains several warning signs:

- The sender uses an unfamiliar domain.
- The Reply-To address differs from the displayed sender address.
- SPF authentication failed.
- DKIM authentication failed.
- DMARC authentication failed.

## Risk Classification

Risk Level: High

Classification: Suspicious / Likely Phishing

Reason: The authentication failures and unusual sender information, combined with the threatening message content, indicate a potential phishing attempt.

## Recommendations

- Do not reply to suspicious emails.
- Do not click unfamiliar links.
- Verify the sender through official communication channels.
- Check SPF, DKIM and DMARC results.
- Report suspected phishing emails to the relevant organisation.

- ## Additional Demonstration: Google Admin Toolbox Messageheader

### Tool Used
Google Admin Toolbox – Messageheader

### Purpose
The tool was used to examine an example email header and understand how email authentication and delivery information can be analysed.

### Observed Results

| Authentication Check | Result |
|---|---|
| SPF | PASS |
| DKIM | PASS |
| DMARC | PASS |

### Findings

The example email passed all three authentication checks.

- **SPF:** The sending server passed the sender-policy authentication check. The displayed IP address was unknown.
- **DKIM:** The email's cryptographic signature passed verification for contoso.com.
- **DMARC:** The email passed the domain authentication and alignment check.

The message travelled from mail.contoso.com to Google's mail server. The displayed delivery time was approximately 10 seconds.

### Security Interpretation

Passing SPF, DKIM and DMARC is a positive authentication result. However, these checks do not guarantee that an email is harmless. Users must still inspect the sender, message content, links and attachments.

### Limitations

This was a demonstration using an example header. It was not one of the three fictional phishing samples created for this project, and it does not establish that any of those samples passed or failed authentication.

### Tool Reference
Google Admin Toolbox Messageheader: https://toolbox.googleapps.com/apps/messageheader/

Google Workspace documentation: https://knowledge.workspace.google.com/admin/security/troubleshoot-dmarc-issues

## Conclusion

Email header analysis helps cybersecurity analysts investigate suspicious email activity and identify possible sender impersonation.

Note: This is a simulated training exercise. The authentication results are illustrative and have not been obtained from a real email server.
