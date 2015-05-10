# fhir-etl
This project provides a set of Kettle transformations (Pentaho Data Integration ETL tool) that allows to export/import FHIR resources (both XML,JSON) from FHIR servers to Excel/database and vice versa.

# Installation
* Download Kettle from http://community.pentaho.com/projects/data-integration/
* Copy fhir-etl/etc/extlib directory to your %KETTLE% directory. This folder contains HAPI-FHIR libraries and dependencies (update libraries if needed from http://jamesagnew.github.io/hapi-fhir/download.html).
* Modify %KETTLE%/launcher/launcher.properties and add reference to "../extlib" into library path before "../lib".  Example is provided in fhir-etl/etc/launcher.properties.sample

# Working with fhir-etl
Use kettle/download_valueset_xml_to_excel.ktr to download single ValueSet from XML-compatible FHIR server to modify the ValueSet in Excel. 
Use kettle/download_all_valuesets.ktr to download all ValueSets from XML-compatible FHIR server to modify the ValueSet in Excel. 
Use kettle/upload_valueset_from_excel_using_hapi.ktr to upload ValueSets from Excel to XML/JSON compatible FHIR server.
Use kettle/upload_changed_valuesets.ktr to to upload all changed Excel files containing ValueSets to XML/JSON compatible FHIR server.

Before running transformation check transformation parameters (Edit -> Settings -> Parameters from menu), such as source and destination FHIR URIs and local directory for Excel files.