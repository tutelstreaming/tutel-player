To create the Macro to parse your Google Sheets with usernames (streamkeys), follow the instructions below.  Please have your Google Sheets page formated just like the example screenshot.

<img src="https://user-images.githubusercontent.com/58894818/218328971-161729e5-d79c-4e01-9b50-ee4a2a595eb2.png" width="20%">


Go to https://script.google.com/home/

Click on 'New Project'

Paste in the below:

```
function doGet(e) {
  const id = e.parameter.spreadsheetId;
  const sheetName = e.parameter.sheetName;
  const sheet = SpreadsheetApp.openById(id).getSheetByName(sheetName);
  const values = sheet.getDataRange().getValues();
  return ContentService.createTextOutput(JSON.stringify({values: values})).setMimeType(ContentService.MimeType.JSON);
}
```

Click 'Deploy' in top right.

Type in a Description.

Set 'Execute as' to 'Me (email@gmail.com)'

Set 'Who has access' to 'Anyone'

Click 'Deploy' to finalize it.

Copy the 'Web app' URL

Modify the URL to point to your spreadsheet and sheetname.

"https://script.google.com/macros/s/<deployment_id>/exec?spreadsheetId=<spreadsheet_id>&sheetName=<sheet_name>"


You can get your 'spreadsheetId' by generating a sharing link to your Google Sheet.

For example: ```https://docs.google.com/spreadsheets/d/1n2nkqB8SeDvvqyczUnVD66Wn53Q2bNUYehoKax1i6kY/edit?usp=sharing```

Your 'spreadsheetId' is the string of seemingly random characters between the '/d/' and '/edit?'

For this example the spreadsheetId is ```1n2nkqB8SeDvvqyczUnVD66Wn53Q2bNUYehoKax1i6kY```


For the 'sheetName', that is what the sheet inside the spreadsheet is titled as.  In this example it will be 'Sheet1'


Full URL example to execute the Macro:

```https://script.google.com/macros/s/AKfycbwB8LFwf8_4-XS-0idbaZkWDIr3GF2s1Iba7gonbc2QllPnT9NG_rwB0dQkEZRXeGO_/exec?spreadsheetId=1n2nkqB8SeDvvqyczUnVD66Wn53Q2bNUYehoKax1i6kY&sheetName=Sheet1```


That is the URL that your player webpage or webapp will use to populate the dropdown menu.
