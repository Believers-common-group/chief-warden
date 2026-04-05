# Excel linkage design

This repo is linked to the Observer Cop Excel master structure.

## Workbook structure
- `Record_Snippets` -> raw row and column snippet records
- `Main_Master` -> selected record pulled into a master view
- `PAGE_01`, `PAGE_02`, `PAGE_03` -> page-specific linked views
- `Page_Link_Map` -> helper routing sheet
- `Display_Master` -> final linked display layer
- `Formula_Snippets` -> exact formulas used

## Link flow
1. `Main_Master!B4` selects a `Record_ID`
2. Main master pulls source page, row key, column key, title, snippet, device, location, time, status, and score
3. Each page sheet is driven by a `Page_ID` in `B4`
4. `Display_Master` reads directly from the page sheets

## Core formulas
- `VLOOKUP`
- `COUNTIF`
- `SUMIF`
- `INDEX`
- `IF`

## Intended repo role
This repository should become the single source of truth for:
- Excel workbook structure
- formula governance
- page display logic
- future API/runtime integration
