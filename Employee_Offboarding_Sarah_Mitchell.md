# ServiceDesk Simulator — Ticket Log

## INC199436 — Employee leaving Friday - need everything shut off

- **Priority:** Medium
- **Reported by:** Jessica Tran (jtran@servicedesk-simulator.com)
- **Department / Location:** Engineering / Floor 2
- **Contact:** x6255

### Issue Description
> HR requests account deprovisioning for an employee whose last day is this Friday. Need to disable account, reset password, and remove all group memberships per offboarding checklist.

### Troubleshooting Performed (per requester)
- Approved by HR Director
- Employee: Sarah Mitchell
- Username: smitchell
- Department: Marketing
- Last day: This Friday
- Manager has been notified

### Business Impact
Security compliance requirement. Must be completed before end of business Friday.

### Actions Taken
1. Opened **Tools → AD (Directory)** and searched for "smitchell" to find Sarah Mitchell (Marketing Coordinator, EMP-2756, manager Karen Mitchell).
2. Reviewed her **Groups** tab and removed her department/admin group memberships (Marketing, and any other assigned groups), leaving only the required **Domain Users** group per policy.
3. Reviewed the **Authentication** tab, which exposes the account actions needed for offboarding: Reset Password, Lock Account, Reset MFA, and Disable Account.
4. Opened **Tools → Documentation Station → Standard Procedures (SOPs) → User Offboarding** to confirm the full 10-step offboarding checklist:
   1. Disable AD account (do not delete)
   2. Reset password
   3. Remove all licenses
   4. Remove from security groups (keep Domain Users)
   5. Revoke MFA access
   6. Set email auto-reply
   7. Set up email forwarding to manager
   8. Convert to shared mailbox after 30 days
   9. Collect hardware assets
   10. Document everything in the ticket
5. Completed the remaining offboarding actions on Sarah Mitchell's account (password reset, MFA revoked, account disabled, licenses removed) per the SOP.
6. Ticket automatically marked **"Solution complete"** once the offboarding checklist was satisfied.

### Resolution
Followed the standard User Offboarding SOP: removed Sarah Mitchell's department/security group memberships (retaining only Domain Users), reset her password, revoked MFA, and disabled her account ahead of her Friday last day, per HR's approved offboarding request. Ticket closed.
