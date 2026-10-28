# NexaReports Release Notes (Updated)

## A. Draft Release Notes

### New Features

#### Export Reports to CSV
Users with the **report-export permission** can now export report data from the report results page in CSV format.

- The export includes the data currently displayed in the report, including any applied filters.
- The downloaded CSV file contains the report's displayed columns and rows.
- Exported files use the filename format: `report-name_YYYY-MM-DD.csv`.
- The existing on-screen report view remains unchanged.
- Users without the report-export permission cannot use the export function.

### Enhancements

#### Configurable Session Timeout
Administrators can now configure how long a user's session may remain inactive before the user is signed out.

- A session-timeout setting has been added to the administration page.
- Administrators can select one of the following timeout values:
  - 15 minutes
  - 30 minutes
  - 45 minutes
  - 60 minutes
- Only users with the administrator role can change this setting.
- The selected value is saved and displayed when the setting is reopened.
- The default timeout is 30 minutes when no change has been made.
- The configured timeout applies to both new and existing sessions after the user's next sign-in.

### Bug Fixes

#### Improved Message for Searches with No Results
Corrected the message displayed when a search completes successfully but returns no matching records.

- Searches that complete successfully and return zero records now display:

  > No records found. Try changing your search criteria.

- Successful searches that return matching records continue to display search results.
- Failed searches continue to display the existing error message.

---



