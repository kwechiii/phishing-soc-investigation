# PHISH-001: Phishing Incident Investigation Report

## 1. Executive Summary

A simulated Microsoft 365 phishing email targeted an employee
at Oakwood Financial Services.

The employee visited a suspicious website and reported
entering their Microsoft 365 password.

Subsequent synthetic authentication records showed an
unfamiliar successful sign-in, followed by mailbox access
and a sensitive financial report download.

The correlated evidence supports classifying this scenario
as a confirmed unauthorized account-access incident.

## 2. Investigation Scope

Evidence reviewed:
- Reported phishing email
- Simulated email authentication headers
- Browser activity records
- Microsoft Entra ID sign-in logs
- Employee verification statement
- Microsoft 365 audit logs
- Microsoft Purview DLP events

All evidence was created for a fictional training scenario.

## 3. Phishing Indicators

- Sender impersonated Microsoft 365 Support.
- Email threatened account suspension.
- Message directed the employee to an unrelated domain.
- Synthetic headers showed SPF failure, no DKIM
  signature, and DMARC failure.

## 4. Authentication Findings

- Employee visited the suspicious URL.
- Employee reported entering their password.
- Two failed sign-ins followed from an unfamiliar IP.
- A successful sign-in occurred from the same IP.
- MFA was recorded as not required.

The reason MFA was not required remains undetermined.

## 5. Microsoft 365 Audit Findings

After the unfamiliar sign-in:
- Mailbox access was recorded.
- Inbox items were accessed.
- Finance-Q4-Report.xlsx was accessed.
- The finance report was downloaded.

The employee denied authorizing the unfamiliar activity.

## 6. DLP Investigation

The simulated Purview DLP evidence showed:
- 12 financial account number matches
- Policy: Finance-Data-Protection
- Action: AuditOnly
- Download: Allowed

The policy detected sensitive information but did not
prevent the download.

Further distribution of the downloaded file was not
established.

## 7. Incident Classification

Classification:
Confirmed unauthorized account access (simulated).

Priority:
High.

Rationale:
Correlated phishing, authentication, user verification,
and audit evidence supports unauthorized account activity
involving sensitive financial information.

## 8. Risk Assessment

Current likelihood: 3/3
Current impact: 3/3
Current risk score: 9/9 (High)

Projected residual likelihood: 1/3
Projected residual impact: 3/3
Projected residual risk score: 3/9 (Medium)

Residual risk is a projection dependent on successful
implementation and validation of recommended controls.

## 9. NIST SP 800-53 Control Mapping

IA-2: Identification and Authentication
AC-2: Account Management
SI-4: System Monitoring
AU-6: Audit Record Review, Analysis, and Reporting
AC-4: Information Flow Enforcement

## 10. Recommended Incident Response

1. Block affected account sign-in.
2. Revoke active sessions and refresh tokens.
3. Reset compromised credentials.
4. Review MFA methods and Conditional Access.
5. Investigate mailbox and file-access activity.
6. Review DLP enforcement and exceptions.
7. Configure alerts for suspicious downloads.
8. Validate remediation before incident closure.

## 11. Limitations

- All evidence is simulated.
- No live Microsoft 365 environment was investigated.
- No real accounts were modified.
- No malware was executed.
- External redistribution of the finance report was
  not established.
- Recommended controls were not implemented or tested.

## 12. Conclusion

This investigation demonstrates how email analysis,
authentication logs, user verification, Microsoft 365
audit records, and DLP findings can be correlated to
support incident classification and risk assessment.

The scenario highlights the importance of phishing
prevention, account security, security monitoring,
and appropriate DLP enforcement.
