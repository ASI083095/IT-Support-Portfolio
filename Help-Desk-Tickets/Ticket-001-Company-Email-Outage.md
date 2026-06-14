# Company-Wide Email Outage

## Ticket Number
Ticket-001

## Date Completed
June 2026

## Issue Reported

A finance department user reported that nobody in the company could send or receive email. Outlook displayed "Disconnected" for all users, and webmail was also unavailable.

## Information Gathered

- Entire company affected
- Outlook showed "Disconnected"
- Webmail unavailable
- Multiple users impacted
- Business communications halted

## Initial Assessment

Because the issue affected all users rather than a single workstation, the problem was determined to be a server-side or infrastructure issue rather than a user account or device problem.

## Troubleshooting Steps

1. Reviewed ticket details and determined issue scope.
2. Confirmed the problem affected the entire organization.
3. Ruled out individual user account issues.
4. Investigated server infrastructure using the Server Room tool.
5. Reviewed server health and status information.
6. Identified EXCH01 (Email Server) as operating in a degraded state.
7. Observed abnormally high CPU and memory utilization on the email server.
8. Restarted the affected email server.

## Root Cause

The organization's email server (EXCH01) was operating in a degraded state, preventing users from accessing email services.

## Resolution

The degraded email server was restarted, restoring normal email functionality for the organization.

## Outcome

Email services were successfully restored.

Users were able to reconnect to Outlook and access email through webmail.

## Skills Demonstrated

- Incident triage
- Troubleshooting methodology
- Infrastructure awareness
- Server monitoring
- Root cause analysis
- Documentation
- Critical issue assessment

## Key Lesson Learned

When multiple users experience the same issue, investigate shared infrastructure before troubleshooting individual devices or user accounts. Large-scale outages often indicate server, network, or service failures rather than workstation problems.
