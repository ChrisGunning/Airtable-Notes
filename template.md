# Template
A summary of the "TEMPLATE" base and its functions.

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

