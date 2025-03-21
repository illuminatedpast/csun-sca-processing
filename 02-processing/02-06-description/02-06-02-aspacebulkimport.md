## Using ArchivesSpace Bulk Import Tools 

The bulk import tool allows an archivist to use Excel to load all series, sub-series, and folder titles in ASpace at once. It allows access to spell check, and other methods of data clean up. The processing archivist prepares the [bulk upload spreadsheet](https://mycsun.box.com/s/tsu7fjrd0a2tfiklcs49lt4hdyd3dfnp) (internal link). Student Assistants may assist with data entry.

### Preparing the Bulk Upload Spreadsheet for Box Lists

- Hide all unnecessary columns until it matches exactly what we use in the rapid data entry in ASpace
-	The Hierarchy has to be in order. So if you enter a file in hierarchy #3 it needs to come after the correct series you want it in (not above it in a different series)
-	For Italics: Instead of italicizing things in the folder titles, wrap the words in code. So for a folder titled, "Alert: Against Communism in California" you would wrap it in the following code to get it to display *Alert: Against Communism in California* in the finding aid:

```

<title render="italic">Alert: Against Communism in California</title>

```

-	Highlight the folder title column only in order to perform spell check solely on the title text to avoid receiving spelling errors on the collection acronym, etc.
-	Add a filter to row 4 to sort and quickly identify mistakes and outliers. E.g. checking the barcodes using a filter it is easy to see if one is missing a digit
-	Do not enter in multiple folder numbers here. That is just for the physical folder. E.g. for physical folders with multiple folder numbers, e.g. “Meeting Minutes, 1990-1992 (1 of 4)", only include the titles and dates in the spreadsheet, and NOT (1 of 4)
-	If there is a "graphic content" warning on the physical folder, do not add that to the ASpace folder title.
-	Before importing the Excel for real, do a test load by checking the “Only validate” box when doing “Load Spreadsheet.” ASpace will run a background job and create a spreadsheet report that shows where the errors are (or things go great and there are no errors!). Download the spreadsheet to view the report outside of ASpace.


### Troubleshooting Failed Box List Uploads

-	Check if “Mixed Materials” is missing the letter “s” on the end or if there is an uncapitalized “m”.
-	If you get errors, make sure there isn't any data accidentally added to the hidden columns you're not using.
-	Begin and End date fields cannot include non-numerical characters. If you are entering “1969 August” it must be numerical: 1969-08. ASpace uses YYYY-MM-DD or YYYY-MM
- For single dates, enter the date only in the begin date and date expression fields. ASpace will load a single date as the begin date and ignore the end date, but you’ll get a bunch of error messages that will make it difficult to see other more serious errors in the import validation report.
- For circa dates, enter as “ca. 1900” or “ca. 1900-1910”. There has to be a period and one space after the “ca” and there has to be one hyphen with no spaces in between a range.
-	If you have some series with subseries, and other series without subseries, the number that goes into the hierarchy column can be counter intuitive. All folders in the collection with NOT have the same hierarchy number. The hierarchy numbers will need to look like:

>  - Series I (Hierarchy: 1)
>    - Subseries A (Hierarchy: 2)
>      - I’m a folder title (Hierarchy: 3)
>    - Subseries B (Hierarchy: 2)
>      - I’m a folder title (Hierarchy: 3)
>  - Series II (Hierarchy: 1)
>    - I’m a folder title (Hierarchy: 2)

***

[Back to the CSUN SC/A Processing Guide Start Page](https://illuminatedpast.github.io/csun-sca-processing/)
