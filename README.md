# Phishing SOC Investigation & Incident Response

## Project Overview
A simulated Microsoft 365 phishing incident investigation
focused on email analysis, authentication monitoring,
unauthorized account access, Data Loss Prevention (DLP),
incident response, and risk assessment.

## Scenario
An employee at fictional Oakwood Financial Services
received a suspicious Microsoft 365 verification email.

The investigation examined whether the employee interacted
with the phishing link, whether unauthorized access occurred,
and whether sensitive financial information was exposed.

## Tools and Frameworks
- Kali Linux
- Linux grep and command-line utilities
- Microsoft Entra ID-style authentication evidence
- Microsoft 365-style audit evidence
- Microsoft Purview DLP-style evidence
- NIST SP 800-53

## Investigation Process
1. Examined phishing email indicators.
2. Reviewed simulated SPF, DKIM, and DMARC results.
3. Investigated browser activity.
4. Correlated authentication and Microsoft 365 audit events.
5. Reviewed employee verification evidence.
6. Evaluated DLP policy effectiveness.
7. Assessed risk and recommended incident response actions.

## Key Findings
- Suspicious email impersonated Microsoft 365 Support.
- Employee reported submitting credentials.
- Unfamiliar account access occurred afterward.
- Mailbox and financial document access were recorded.
- DLP detected 12 sensitive-information matches.
- AuditOnly policy permitted a sensitive-file download.

## Risk Assessment
Current Risk: 9/9 (High)
Projected Residual Risk: 3/9 (Medium)

The residual rating is a projection, not a validated outcome.

## NIST SP 800-53 Mapping
- IA-2: Identification and Authentication
- AC-2: Account Management
- SI-4: System Monitoring
- AU-6: Audit Record Review, Analysis, and Reporting
- AC-4: Information Flow Enforcement

## Project Structure
- evidence/ - Simulated investigation evidence
- analysis/ - Indicators, timeline, risk, and response
- reports/ - Final incident investigation report
- screenshots/ - Selected investigation screenshots

## Key Takeaway
Correlating email, authentication, user verification,
audit, and DLP evidence can support defensible incident
classification and reveal security-control gaps.

## Disclaimer
This is a fictional training scenario using synthetic
evidence. No real Microsoft 365 tenant was investigated,
and no live accounts or policies were modified.
