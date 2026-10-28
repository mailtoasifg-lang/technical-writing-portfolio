# NexaReports Release Notes

## A. Draft Release Notes

### New Features

#### Export Reports to CSV
Users with the appropriate report export permission can now export report data from the report results page in CSV format.

- The export includes the data currently displayed in the report, including any applied filters.
- The downloaded CSV file contains the same columns and rows shown in the report results.
- Exported files use the filename format: `report-name_YYYY-MM-DD.csv`.
- The existing on-screen report view remains unchanged.
- Users without report export permission cannot use the export function.

### Enhancements

#### Configurable Session Timeout
Administrators can now configure how long a user's session may remain inactive before the user is signed out.

- A session timeout setting has been added to the administration page.
- Administrators can select one of the following timeout values:
  - 15 minutes
  - 30 minutes
  - 45 minutes
  - 60 minutes
- Only users with the administrator role can change this setting.
- The selected value is saved and displayed when the setting is reopened.
- The default timeout is 30 minutes unless it has been changed.
- Changes take effect after the user's next sign-in, including for users with existing sessions.

### Bug Fixes

#### Improved Message for Searches with No Results
Corrected the message displayed when a search completes successfully but returns no matching records.

- Searches that return zero records now display:

  > No records found. Try changing your search criteria.

- Successful searches that return matching records continue to display search results.
- Failed searches continue to display the existing error message.

---

## B. Questions for Product/Engineering

1. For CSV exports, should the release notes refer to a specific permission name, or is "report export permission" the intended customer-facing terminology?
2. For the CSV filename format, should the release notes clarify which date is used in `YYYY-MM-DD` (for example, export date or another date), or is that detail intentionally omitted?
3. For session timeout behavior, should "inactive" be defined more precisely for customers, or is the existing wording sufficient?
4. For the session timeout enhancement, should release notes explicitly state whether the timeout applies to all users or only selected user groups? The ticket implies all users, but does not state this explicitly.
5. For the search message fix, should the new message be considered customer-facing text that is fixed and localized as written, or will it vary by language/locale?

---

## C. Claims That Should Be Verified Before Publication

1. The CSV export option is available on the report results page.
2. Only users with the required export permission can export report data.
3. CSV exports contain only the columns and rows currently displayed in the report and reflect applied filters.
4. Exported filenames follow the format `report-name_YYYY-MM-DD.csv`.
5. The session timeout setting is available on the administration page.
6. Only users with the administrator role can modify the session timeout setting.
7. Available timeout values are exactly 15, 30, 45, and 60 minutes.
8. The default session timeout is 30 minutes.
9. Session timeout changes take effect after the user's next sign-in.
10. A successful search with zero results displays the message: "No records found. Try changing your search criteria."
11. Failed searches continue to display the existing error message without change.
