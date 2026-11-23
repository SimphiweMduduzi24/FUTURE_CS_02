
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

## Conclusion

Email header analysis helps cybersecurity analysts investigate suspicious email activity and identify possible sender impersonation.

Note: This is a simulated training exercise. The authentication results are illustrative and have not been obtained from a real email server.
