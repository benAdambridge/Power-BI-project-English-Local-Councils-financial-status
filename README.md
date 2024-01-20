# Power-BI-project-Local-Councils-financial-status _as of Jan 2024_

English Councils, as of January 2024, are coming under scrutiny due to their debt totals, fuelled partly by taking on risky loans to make up for funding gaps due to austerity, straining their capabilities to provide local services.
This project takes the Local Councils of England, determines their financial status - bankrupt, in financial risk, or neither - and maps them to create an interactive dashboard.

I used the 2023 map local council boundaries provided by the UK's Open Geography Portal - https://geoportal.statistics.gov.uk/datasets/2f0b8074b6ab4af6a1ec30eb66317d12_0/explore.

**#To create a shapefile for importing into Power BI
Find shapefile that you want, for example, https://geoportal.statistics.gov.uk/datasets/ons::local-authority-districts-may-2023-boundaries-uk-bgc/explore
Download as GeoJSON
Open QGIS
Layer
Add Layer
Add Vector Layer
Click on three dots to pick the GeoJSON folder downloaded earlier
Add
Right click on the file under the ribbon left hand side named 'Layers'
Export
Save Feature As
Press three dots next to File name and place this where you want it
Change CRS to 'WGS84'
Change Resize to 'YES'
OK
Should've saved as a Shapefile
Open up 'mapshaper'
Import what should be about 6 documents that QGIS just spewed out
Export as TopoJSON into folder of choosing (power BI accepts TopoJSON shapefiles)
- make sure to untick the box saying 'Save to Clipboard'
Job done
- use LAD name, LSOA name for the Location row in Power BI


#Collecting the data#

Find councils in financial risk data

Find full details council data (Council name, Region etc., any extra info about the Councils you feel you need).
- match to 'councils in financial risk data'

If it doesn't come with Region column then match this
-I had to get LAD22 match with LAD23, then match to Region by LAD22 download (was the most up to date I could find)

