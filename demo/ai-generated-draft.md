# Draft Release Notes

## New Features
Export Reports to CSV (NXR-101)

Users with the report-export permission can now export report results to a CSV file from the report results page.

The exported file contains the columns and rows currently displayed in the report, including any applied filters. Exporting does not change the existing on-screen report view.

Downloaded files use the filename format:

report-name_YYYY-MM-DD.csv

Users who do not have the report-export permission cannot use the export function.

**Jira ID**: NXR-101

## Enhancements
Configurable Session Timeout (NXR-102)

Administrators can now configure how long a user's session may remain inactive before the user is signed out.

A new session-timeout setting is available on the administration page. Administrators can select one of the following timeout values:

15 minutes
30 minutes
45 minutes
60 minutes

The default timeout is 30 minutes when no changes have been made.

Only users with the administrator role can modify this setting. The selected value is saved and displayed when the setting is reopened.

Changes take effect for new and existing users' sessions after the next sign-in.

**Jira ID**: NXR-102

## Bug Fixes
Corrected Message for Searches with No Results (NXR-103)

NexaReports now displays the following message when a search completes successfully but returns no matching records:

No records found. Try changing your search criteria.

This message is displayed only when a search completes successfully and returns zero records.

Successful searches that return matching records continue to display search results. Failed searches continue to display the existing error message.

Jira ID: NXR-103

# Questions for Product/Engineering

**NXR-101**

- What date should be used in the YYYY-MM-DD portion of the exported filename (for example, export date, report run date, or another date)?
- Should the release notes reference the exact location or label of the CSV export option on the report results page, or should this remain unspecified?

**NXR-102**

- Is the configured timeout based strictly on user inactivity, or are there any activities that reset the inactivity timer that should be documented?
- Should users receive any warning before automatic sign-out due to session timeout, or is no warning displayed?
- Does the session-timeout setting apply globally to all users in the environment or can it vary by user, role, or group?

**NXR-103**

- Should the new no-results message be displayed in all search experiences within NexaReports, or only in the specific search functionality covered by this ticket?

# Claims That Should Be Verified Before Publication
1. Users with the report-export permission can export report data and users without that permission cannot use the export function.
2. CSV exports contain only the currently displayed columns and rows, including the report's applied filters.
3. Exported files use the filename format report-name_YYYY-MM-DD.csv.
4. The export feature leaves the existing on-screen report view unchanged.
5. The default session timeout is 30 minutes.
6. Available session-timeout values are 15, 30, 45, and 60 minutes.
7. Session-timeout changes take effect only after the user's next sign-in.
8. Only users with the administrator role can change the session-timeout setting.
9. The no-results message is exactly:
  -   "No records found. Try changing your search criteria."
11. Failed searches continue to display the existing error message and successful searches with results continue to display those results.
