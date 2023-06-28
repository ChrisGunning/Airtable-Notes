# AIRTABLE-NOTES
Guide for features, pros, cons, and general notes about Airtable.

## Contents

### General Notes
- Features
- Pros
- Cons

### Template Notes
- Changes
- Features

# GENERAL NOTES
Notes regarding airtable and its features.

## Features

**Table Organization:**
- Fields
- Records
- Cells
  
**Automations:**
- Allows you update,create, automate processes.
- Somewhat limited in what it can do, though through code it should be able to do pretty much anything
- more complex, but allows a system where you can input several
  
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
- Do NOT use .Has a limit of 100 records per template; therefore it can only be used in smaller situations, NOT when creating templates for the BOM.

## Pros
- Easily able to share data from base to base and table to table.
- Interface is clean, not flashy looking though
- It is possible to have almost everything done from an interface (though there may need to be occasional visits to the database as it might not be perfect and it will be hard to make everything 100% part of the interface) 
- It has several interfaces (such as calendar, gallery, list, ect.). unsure if this is part of smartsheets though
- has extensions that can print or email autoformatted things.
- template + automations can do a lot.

## Cons
- If you have a formula for a specific column (field) you are unable to make further edits to the  column easily. Additionally, it is difficult to create unique boxes inside a field (column). 
- There is only a certain way to link tables, and with this method, you are unable to change values. There are 2 ways around this, either develop an automation system that links things or you have separate override fields that you use to override these fields. Both options are time consuming, and the latter is not user friendly.
-  Summing together data requires a workaround as you cannot sum data (from a column) and put it into a slot on the same table. In order to do this, you must 2 more fields, one that links to the designated field, and another to sum up those values that you select with the field.
- Interface is very limited in what you can do. Many workarounds but it will not look flashy and may not be the best organized. Additionally, it will be hard to implement the same amount of data that is on smartsheet to airtable
- Pro plan is per person/per workspace (unsure if I will need it by the end of the project)
- Little table organization, must be smart and efficient the way one structures data. It will be hard to add more to the database once it is established. Additionally, there is a limited number of airtable syncs (20 per base no matter the plan) meaning that I do not think it is possible to recreate the entirety of smartsheet onto airtable, as you cannot conglomerate data into a large overall folder. You can sync more airtable data through other programs such as unito or zapier, which also cost money (unsure of the limitations of those other websites though). Unito can connect airtable to smartsheets though, 
- Does occasionally get slow (i'm unsure if that is my computer or not). Additionally, the automations are not automatic so if you are filling data fast, it will not keep up with you. 
- Not as flexible to how you can structure a table (limited colors, only can edit columns) 
- Automations Cost Money, same with scripting for automations (only able to do with enterprise plan)
- Templates only have 100 Records limit, cannot be used for widespread usage of templates of rooms;. To increase limit, a enterprise plan is needed. 
- Airtable’s automations can only have up to 25 actions in them, you can only have 50 automations in a base, and you can only find up to 100 records in an action. Syncing has major limitations as well.

# TEMPLATE
A summary of the "TEMPLATE" base and its function.

## Changes

**Equipment Database:**
The "Rack parts Database" as well as the "Cables Database" has been merged into a sole Equipment database. (ask if I should implement an organizational structure to that database)
Contractor Database:
The contractor database was split in two. One is for CIT AV Furnishing Cables and the other for the Contractor Furnishing Cables. 

**Template Database:** 
This is an additional database "Templates" which mimics Smartsheet's BOM templates. Records from here are pulled from the BOM when a specific space type is created. 
- To change a template, either add a record, or change an item. If you select an item, the "model part" and "make" will be automatically imported from the equipment database. You must also determine if it is OFE as well as the quantity.
- To add a template, you must first create a new option for the "Template" column in the "Space List" worksheet. Then go to the hidden field:  "Room" in the "Templates" table and create a new option with the exact same name. Then assign the "Room" as well as the hidden field:  "Category". NOTE: If the new template exceeds more than 100 records, select half of the records and check the hidden field: "Half". If it exceeds over 200 records, a new automation and field must be created.
- Red colored record: The record is incomplete.
  
**Space List:**
- It now has a selector for which template you want to select. NOTE: If you select a template once, you cannot change it. To change it, store the record.

**BOM:**
- The BOM does not initially have anything inside of it. It is populated automatically once a template is chosen from the space list.
- Red colored record: The record is incomplete.
- Adding/editing BOM: Must change the part name (through selection) and then everything will auto populate. 

## Features

Deleting/Hiding rooms:
- To delete a room completely, go to the the Space List and click the "Delete" button. This will delete the room and its corresponding records in other tables.
- If you do not want a specific room inside the estimating summary BUT you do not want to delete it, go to the "Estimating Summary" and to the TOTALS row and the hidden field: "Change Totals". In that cell, add or remove only the rooms that you want to display in the totals. From here it will be updated corresponding to your selected rooms both in the table and the interface.
Filling out the worksheets:
- To create a new space, create a new record inside the Space List. This populates all of the records for the other worksheets. From there, follow smart sheets order: Space List -> BOM -> AV Labor -> Contractor -> Network -> TCO. The estimating summary should automatically update.
- When creating another space, try to not name them the same name as it messes up the organization of the BOM and is hard to differentiate throughout the database.

## Random

**Hidden Fields:**
- (Imported):
	- Was used for reference when creating a database. Can ignore/Delete.
- (Automation)
	- Used for an automation in the designated table. Can ignore.
- (Formula)
	- Used for a formula in the designated table. Can ignore.
- (Pull)
	- Used for linking of databases through automations or formulas. Can ignore.
