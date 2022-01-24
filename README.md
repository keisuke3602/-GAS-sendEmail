# -GAS-sendEmail

This is for sending emails to people with Google App Script at once.

• In the first "fileID", put the Google Spreadsheet's ID which contains the list of email.

• In the second "fileID", put the Google Doc's ID which has a body of email.

• In the third and fourth "fileID", put an ID of image file in Google Drive. This is optional.

In the row 2,

  `const sheet = SpreadsheetApp.openById('fileID').getSheetByName('NotInstalled');`

You can write it instead;

  `const sheet = SpreadsheetApp.openById('fileID').getActiveSheet();`

`getActiveSheet();` should be added to match the type of parameters. But this one is for when using one sheet.


For `getRange(row, column, optNumRows, optNumColumns)`, refer to the link below.

https://stackoverflow.com/questions/11947590/sheet-getrange1-1-1-12-what-does-the-numbers-in-bracket-specify

In the row 23,

  `MailApp.sendEmail(recipient,subject,body,options);`
  
It can be `GmailApp.sendEmail(recipient,subject,body,options);`, but if you want to use emoji, GmailApp cannot address it as far as I know.
