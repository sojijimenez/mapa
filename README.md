# MAPA - Map Audit: Plot Assistant

**Download: https://bit.ly/MAPA-download**

MAPA turns an Excel or CSV list of sites and links into a KML/KMZ file you open in Google Earth. Nothing leaves your computer. There is no map inside the app: you check the result in Google Earth.

Developed by: Soji Jimenez

## Install

1. Go to the **Releases** page of this repository and download `MAPA-Setup-<version>.exe` from the newest release.
2. Double-click the file. Windows may warn that the program is not code-signed: click **More info**, then **Run anyway**.
3. No administrator rights are needed. MAPA installs for your user only.

## Use

1. Open MAPA and click **Open file...**. Choose an `.xlsx`, `.xls` or `.csv` file.
2. Rows with problems are marked **Error** with the reason. Fix a bad cell by typing in the table; the row is checked again. The **Category** column shows the folder each row will go to; type a different category there to move a row.
3. Pick how to group and color the result (the default is by category), then click **Export KML / KMZ...**.
4. Open the saved file in Google Earth.

## Columns

| Column | Needed | Notes |
|---|---|---|
| Project_Name | yes | Also accepted: Project, Name, Site Name, Site |
| Start_Lat | yes | Also accepted: Lat, Latitude, Start Latitude |
| Start_Lon | yes | Also accepted: Lon, Long, Lng, Longitude, Start Long |
| End_Lat, End_Lon | no | Both filled = a **link** (a line). Both blank = a **building** (a pin). One filled alone = an error. |
| Category | no | One of the category names (see below). Short forms such as Road, Bridge, School, Hospital, Flood, Building are also accepted. The column can also be called Project Type or Type. A blank cell is guessed from the project name; a filled value that is not a category goes to Others. |

All other columns are kept, shown in the table and in the Google Earth click balloon. The template has these optional project-detail columns: Contract ID, Contractor, Total Contract Cost, Date Started, Reported Completion Date, Target Date and % of Completion. Dates, costs and percentages are shown in the balloon exactly as they appear in the Excel cell (for example 11/16/2026, 1,500,000.00, 45%).

Coordinates can be decimal degrees (14.5995), text, or degrees-minutes-seconds (14°35'58"N). If latitude and longitude look swapped for a place in the Philippines, MAPA swaps them back and shows a warning.

## Categories and colors

The categories below are the starting list. Click **Set up categories...** in the side panel (or Help, then Set up categories) to rename them, add your own, delete or reorder them, pick any pin color, and change the keywords used to guess a category from the project name. Others is the catch-all: it always stays last and cannot be renamed or deleted. Your list is remembered, applies to the loaded file at once, and also fills the Category drop-down in the downloaded Excel template.

The starting categories, which are also the Google Earth folders in this order (empty folders are left out), are: Roads (orange), School Buildings (red), Hospital/ Super Health Centers (green), Other Buildings (gold), Flood Management Projects (blue), Bridges (purple) and Others (grey). If the file has no Category column, or a Category cell is blank, MAPA guesses from the project name (for example road, avenue, school, classroom, hospital, health, hall, flood, dike, bridge) and shows the guess in the table so you can correct it. If a name matches several categories, the keyword that comes first in the name wins. Links are drawn as bright lines in the same color as their pins (white for Others).

The **Download Excel template** button saves a ready-made file in this order: Contract ID, Project_Name, Category (drop-down), Start_Lat, Start_Lon, End_Lat, End_Lon, Contractor, Total Contract Cost, Date Started, Reported Completion Date, Target Date, % of Completion. Two sample rows show a building and a link; replace them with your own.

## Updates

MAPA shows a notice when a newer version is out. It never downloads or installs anything by itself. Turn the check off under **Help, then Check for updates automatically**.
