# Prioritized Hardening Checklist

## Priority 1 – Authentication and Account Security
- [ ] Enforce a strong password policy.
  - **Verify:** Test password validation using approved local test accounts.
- [ ] Store passwords using a secure password-hashing mechanism.
  - **Verify:** Confirm plaintext passwords are not retained.
- [ ] Implement login rate limiting.
  - **Verify:** Repeated failed login attempts trigger a temporary delay or rate limit.
- [ ] Use secure session handling.
  - **Verify:** Confirm session cookies have appropriate security attributes and sessions expire as intended.

## Priority 2 – Authorization and Privilege Separation
- [ ] Enforce authorization on the server side.
  - **Verify:** A normal student cannot perform a privileged action.
- [ ] Separate student and administrator permissions.
  - **Verify:** A student account cannot access administrator-only functions.
- [ ] Apply least privilege.
  - **Verify:** Accounts and components have only required permissions.
- [ ] Verify ownership before allowing access to records.
  - **Verify:** A student cannot access or modify another student's records.

## Priority 3 – Data Protection
- [ ] Protect sensitive data in transit.
  - **Verify:** Confirm sensitive traffic is protected by HTTPS in the intended deployment environment.
- [ ] Minimize sensitive information returned by application responses.
  - **Verify:** Review responses and confirm only required information is returned.
- [ ] Use safe database access practices.
  - **Verify:** Review database interactions and confirm user-controlled input is handled safely.

## Priority 4 – Logging and Monitoring
- [ ] Log authentication events.
  - **Verify:** Successful and failed authentication events appear in security logs.
- [ ] Log privilege-sensitive actions.
  - **Verify:** Administrative actions and privilege changes generate identifiable events.
- [ ] Protect security logs from unauthorized modification.
  - **Verify:** Normal application users cannot alter or delete audit records.
- [ ] Monitor repeated authentication failures and abnormal request patterns.
  - **Verify:** Controlled test events can be identified in logs.

## Priority 5 – Availability
- [ ] Rate-limit sensitive or resource-intensive endpoints.
  - **Verify:** Excessive requests are restricted while normal requests remain available.
- [ ] Define basic request/resource limits.
  - **Verify:** Abnormal request volume does not consume unrestricted application resources.

## Final Verification
- [ ] Re-check all Critical and High risks after controls are implemented.
- [ ] Record evidence for each completed verification.
- [ ] Remove secrets and personal data from screenshots/reports before publication.
