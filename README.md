# -GAS-sendEmail

This is for sending emails to people with Google App Script at once.

• In the first "fileID", put the Google Spreadsheet's ID which contains the list of email.

• In the second "fileID", put the Google Doc's ID which has a body of email.

• In the third "fileID", put an ID of image file in Google Drive. This is optional.

In the row 2,

  `const sheet = SpreadsheetApp.openById('fileID').getActiveSheet();`

`getActiveSheet();` should be added to match the type of parameters.


For `getRange(row, column, optNumRows, optNumColumns)`, refer to the link below.

https://stackoverflow.com/questions/11947590/sheet-getrange1-1-1-12-what-does-the-numbers-in-bracket-specify
