## Using ArchivesSpace Bulk Import Tools 

The bulk import tool allows an archivist to use Excel to load all series, sub-series, and folder titles in ASpace at once. It allows access to spell check making it easier to catch data entry errors.

The processing archivist prepares the bulk upload spreadsheet. Student Assistants may assist with data entry.

•	Notes:
- Recommend hiding all unnecessary columns until it matches exactly what we use in the rapid data entry in ASpace then let the student get to work.
-	The Hierarchy has to be in order. So if you enter a file in hierarchy #3 it needs to come after the correct series you want it in (not above it in a different series)
-	For Italics: Instead of italicizing things in the folder titles, wrap the words in code
Instead of writing this: Alert: Against Communism in California
You wrap the words with code instead:
```
<title render="italic">Alert: Against Communism in California</title>
<title render="italic"> goes before the words you want Italicized and </title> goes after the words you want italicized.
```
-	Highlight the folder title column only in order to perform spell check solely on the title text – that way you are not receiving spelling errors on the collection acronym, etc.
-	Add a filter to row 4 to sort and quickly identify mistakes and outliers. E.g. checking the barcodes using a filter it was easy for me to see that one of them was one digit short and fix it before uploading
-	Do Not enter in multiple folder numbers here. That is just for the physical folder. E.g. for physical folders with the titles “Meeting Minutes, 1990-1992 (1 of 4)” through (4 of 4) would only be one line in the s/s: “Meeting Minutes 1990-1992”
-	Before you import the Excel for real, do a test load by checking the “Only validate” box when doing “Load Spreadsheet.” ASpace will run a background job and create a spreadsheet report that shows you where the errors are (or things go great and there are no errors!). You’ll need to download the spreadsheet to view the report outside of ASpace.

•	Troubleshooting Failed Uploads:
-	We’ve had error messages when importing that were due to “Mixed Materials” missing the letter “s” on the end or for uncapitalized “m”.
-	If you get errors, make sure there isn't any data accidentally added to the hidden columns you're not using.
-	Dates
  - Begin and End date fields cannot include non-numerical characters. If you are entering “1969 August” it must be numerical: 1969-08. ASpace uses YYYY-MM-DD or YYYY-MM
  - For single dates, enter the date only in the begin date and date expression fields. ASpace will load a single date as the begin date and ignore the end date, but you’ll get a bunch of error messages that will make it difficult to see other more serious errors in the import validation report.
  - For circa dates, enter as “ca. 1900” or “ca. 1900-1910”. There has to be a period and one space after the “ca” and there has to be one hyphen with no spaces in between a range.
-	If you have some series with subseries, and other series without subseries, the number that goes into the hierarchy column can be counter intuitive. All folders in the collection with NOT have the same hierarchy number. The hierarchy numbers will need to look like:
  - Series I (Hierarchy: 1)
    - Subseries A (Hierarchy: 2)
      - I’m a folder title (Hierarchy: 3)
    - Subseries B (Hierarchy: 2)
      - I’m a folder title (Hierarchy: 3)
  - Series II (Hierarchy: 1)
    - I’m a folder title (Hierarchy: 2)
   
    ***
