This is a fictional product name: **NexaReports**

## Jira ID: NXR 101 - New Feature
## Export reports to CSV
**Description**: Users currently view generated reports in the NexaReports application. They need an option to export report data for further analysis in spreadsheet applications.

**Requirements**
- Add a CSV export option to the report results page.
- Export the data currently displayed in the report, including its applied filters.
- Use the filename format report-name_YYYY-MM-DD.csv.
- Keep the existing on-screen report view unchanged.
  
**Acceptance criteria**
- Users with report-export permission can export the displayed report data.
- The downloaded file contains the report's displayed columns and rows.
- The filename follows the specified format.
- Users without export permission cannot use the export function.

## Jira ID: NXR 102 - Enhancement
## Configure session timeout
**Description**: Administrators need to control how long a user's session can remain inactive before the application signs the user out.

**Requirements**
- Add a session-timeout setting to the administration page.
- Allow administrators to select 15, 30, 45 or 60 minutes.
- Apply the selected timeout to new and existing sessions after the next sign-in.
- Set the default timeout to 30 minutes.
  
**Acceptance criteria**
- Only users with the administrator role can change the setting.
- The selected value is saved and displayed when the setting is reopened.
- The configured timeout takes effect after the next sign-in.
- The default value is 30 minutes when no change has been made.

## Jira ID: NXR 103 - Bug fix

**Correct the empty search results message**
**Description**: When a search returns no matching records, NexaReports displays the message "Search completed successfully" instead of informing the user that no records were found.

**Requirements**
- Display the message "No records found. Try changing your search criteria."
- Display the message only when a search completes successfully and returns zero records.
- Continue displaying the existing error message when a search fails.
  
**Acceptance criteria**
- A successful search with zero matching records displays the new message.
- A successful search with matching records continues to display the results.
- A failed search continues to display the existing error message.
