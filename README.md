# fhir-etl
This project provides a set of Kettle transformations (Pentaho Data Integration ETL tool) that allows you to export/import FHIR resources (both xml and json) from FHIR REST servers to Excel/Google Spreadsheet and vice versa

# Installation
* Download Kettle from http://community.pentaho.com/projects/data-integration/
* Copy fhir-etl/etc/extlib directory to your %KETTLE% directory
* Add /extlib to %KETTLE%/launcher/launcher.properties like in fhir-etl/etc/launcher.properties.sample

# Working with fhir-etl
Use kettle/download_valueset_xml_to_excel.ktr for download single ValueSet from FHIR server in xml representation to Excel
Use kettle/download_all_valuesets.ktr for download single ValueSet in xml representation to Excel
Use kettle/upload_valueset_from_excel_using_hapi.ktr for upload valueSet from Excel to FHIR server
Use kettle/upload_changed_valuesets.ktr for download single ValueSet in xml representation to Excel

Before running transformation check transformation parameters (Edit -> Settings -> Parameters from menu), such as source and destination FHIR URIs and local directory for Excel files

 
 
