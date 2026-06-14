# Remote User Unable to Access Shared Drive

## Ticket Number
Ticket-002

## Issue Reported
A remote Marketing employee reported being unable to access the Marketing shared drive. The user received "The network path was not found" when attempting to open the drive. Internet and email were working normally.

## Information Gathered
- User: Sarah Mitchell
- Department: Marketing
- Location: Remote / working from home
- Internet access working
- Email working
- Computer restart did not resolve issue
- Mapped drives appeared disconnected
- User accessed the drive successfully yesterday
- User reported no recent changes to laptop, password, or work location

## Initial Assessment
Because the user was remote and unable to access shared network drives while internet/email still worked, the initial suspected cause was a disconnected VPN.

## Troubleshooting Steps
1. Connected to the user's workstation using Remote Support.
2. Opened the VPN client and found the corporate VPN disconnected.
3. Connected the VPN.
4. Verified VPN tunnel became active.
5. Confirmed workstation received a corporate network IP address.
6. Checked File Explorer and observed the Marketing drive still appeared offline.
7. Asked the user to test access again; user reported the drive still showed "The network path was not found."
8. Checked FILESERV01 in Server Room and confirmed it was online.
9. Reviewed mapped drives using `net use`.
10. Checked Active Directory group membership.
11. Confirmed user was a member of Domain Users, Marketing, and Printer-Users.

## Root Cause
The simulator identified the disconnected VPN as the intended root cause. However, additional validation suggested the issue may have required further troubleshooting in a real-world environment because the user still reported the drive was inaccessible after VPN reconnection.

## Resolution
Reconnected the user's corporate VPN and verified the VPN tunnel was active.

## Outcome
The simulator marked the fix as applied, but a point penalty occurred after closing the ticket, likely because the user had not confirmed successful access before closure.

## Additional Real-World Follow-Up
If this were a real help desk ticket, I would not close it until the user confirmed access was restored. Next steps would include:
- Rechecking the mapped drive path
- Remapping the Marketing shared drive
- Testing access to `\\FILESERV01\Marketing`
- Confirming whether other Marketing users were affected
- Reviewing share permissions
- Escalating to systems/network support if the share remained inaccessible

## Skills Demonstrated
- VPN troubleshooting
- Remote support
- Network drive troubleshooting
- Server status review
- Active Directory group review
- Command-line diagnostics
- User communication
- Root cause analysis
- Ticket documentation

## Key Lesson Learned
A ticket should not be closed just because a fix appears to be applied. The technician should verify that the user can access the affected resource before closing the ticket.
