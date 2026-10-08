# Risk Register

## Scoring Approach
Risk priority is based on qualitative **likelihood** and **impact** for the fictional student portal.

| ID | Asset | Threat | STRIDE | Likelihood | Impact | Priority | Rationale |
|---|---|---|---|---|---|---|---|
| R01 | Student/Admin accounts | Account takeover | Spoofing | High | High | Critical | Authentication endpoints can be targeted by credential abuse; compromise can expose account data or privileged functions. |
| R02 | Student records | Unauthorized modification | Tampering | Medium | High | High | Incorrect authorization could allow unauthorized changes to important records. |
| R03 | Student personal information | Unauthorized disclosure | Information Disclosure | Medium | High | High | Excessive access or missing authorization can expose confidential student information. |
| R04 | Admin functionality | Student-to-admin privilege escalation | Elevation of Privilege | Medium | Critical | High | Successful privilege escalation could provide broad control over administrative functions. |
| R05 | Audit logs | Missing accountability | Repudiation | Medium | Medium | Medium | Incomplete logging can make investigation and accountability difficult. |
| R06 | Application availability | Excessive request abuse | Denial of Service | Medium | Medium | Medium | Resource-intensive request abuse can reduce availability for legitimate users. |

## Mitigation and Verification

| ID | Recommended Mitigation | Verification Step |
|---|---|---|
| R01 | Strong password policy, secure password hashing, login rate limiting, secure sessions | Verify repeated failed logins trigger rate limiting and confirm passwords are not stored in plaintext. |
| R02 | Server-side authorization and object ownership checks | Verify a user cannot modify another user's records through direct requests. |
| R03 | Server-side access control and data minimization | Verify users receive only information they are authorized to access. |
| R04 | Server-side role enforcement and least privilege | Verify a student account is denied access to administrative endpoints and actions. |
| R05 | Security event and administrative-action logging | Verify authentication, privilege changes, and sensitive administrative actions generate useful audit events. |
| R06 | Rate limiting and resource/request controls | Verify excessive requests are limited while normal users remain able to access the application. |

## Recommended Remediation Order
1. R01 – Account takeover
2. R02 – Unauthorized record modification
3. R03 – Student data exposure
4. R04 – Privilege escalation
5. R05 – Missing audit trail
6. R06 – Excessive request abuse
