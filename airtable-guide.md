# Airtable Notes

## Features
This section describes the main features of airtable.

**Table Organization:**
- Fields
- Records
- Cells
  
**Organizational Hierarchy:**
- Workspaces:
	- Overarching structure, contains bases.
- Bases:
	- A structure that consists of tables
- Tables:
	- The main structure that holds data.
- Views:
	- Different views of the same table. Allows organization and while maintaining centralization.

**Templates:**
- This is a way to automatically create records
- Do NOT use. Has a limit of 100 records per template and there is a max number of records that can be saved from all of the templates; therefore it can only be used in smaller situations, NOT when creating templates for the BOM.

**Extensions**
- Extensions allow you to pul from creator generated content to help optimize your workflow.
- Most extensions do not anything significant; however, the scripting automation is extremely useful and is used in the airtable base that was created.

**Grouping/Filtering/Sort**
- These are similar to smartsheet's functionality with Grouping/Filtering/Sort: however, grouping is visually nicer and has more options.

**Automations:**
- A system that allows you update, create, and automate processes within your table. The template developed mainly uses it for the connecting of databases to worksheets.
- Somewhat limited in what it can do, though through code (scripting only allowed through pro version) it should be able to do pretty much anything.
- Pro version has a maximum of 50,000 automations per month. If implementing a automation, be weary of this as managing a lot of data can use up many automations quickly.
- Individual automations can only use 1 if/else statement or 1 loop statement.
- A big limitation that I ran into was that the search feature of the automation was only able to search for a maximum of 100 records at a time. Be weary of this limitation when trying to implement an automation.
- There are descriptions of what individual automation does in airtable.

**Interface**
- I believe the interface to be very limited in what it can do. It is relatively new to airtable so there will be new features in the future.
- It does not allow you to effectively compare data between two tables or views efficiently.
- Tables are extremely confusion due to the way they pull data.
- Good with bare data and can assist in the process of filling out worksheets or databases.
