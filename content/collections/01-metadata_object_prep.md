---
section: Creating Collections
nav_order: 1
title: Objects and Metadata
---

Collection creation starts with the digital objects and metadata. 
This is often work completed with students, fellows, and other collaborators.

The processes for creating objects and metadata from scratch are described in other sections of these Docs.
When ready, there are a few steps to prepare for creating a new collection.

## Objects

Once the full quality objects have been prepared, they should be gathered in a single folder.
Filenames and extensions should be carefully checked over to ensure they exactly match the "filename" field in your metadata (this is case sensitive!).

Spec, students, and collaborators focus on scanning and creating the full archival quality objects which are transferred to the CDIL team.
Generally, the CDIL team will complete the final processing to create derivative images ready for the web.

## Metadata

Descriptive metadata can be created at the same time as scanning or done after processing the group of objects.
Once the descriptive metadata is complete, you should ensure all required fields are completed and fill out the technical fields required for CollectionBuilder:

- Ensure all "objectid" are filled in and unique.
- Ensure metadata follows [formatting best practices](https://collectionbuilder.github.io/cb-docs/docs/metadata/formatting/).
- Fill in ["display_template"](https://collectionbuilder.github.io/cb-docs/docs/metadata/csv_metadata/#display-template) with the appropriate value.
- Fill in [object location fields](https://collectionbuilder.github.io/cb-docs/docs/metadata/csv_metadata/#object-location-fields) using the url for the libobjects server, following the patterns:
    - "object_location": `https://objects.lib.uidaho.edu/collectionstub/filename.extension`
    - "image_small": `https://objects.lib.uidaho.edu/collectionstub/small/filename_sm.jpg`
    - "image_thumb": `https://objects.lib.uidaho.edu/collectionstub/thumbs/filename_th.jpg`
    - *Note: this can be done in bulk using equations or OpenRefine, or automatically generated. Please ask if you have questions!*

If you have been using Excel, the XLSX file will need to be uploaded to Google Sheets (Excel cannot create a properly formatted CSV). 
From Google Sheets or OpenRefine, export a CSV version of your metadata and rename to match the collection stub (and do not accidentally open the CSV in Excel!). 

## Transfer 

Share the completed folder of objects and metadata to the CDIL team via shared drive, and submit the information using the [Collection Update Form](https://forms.office.com/r/8S0dZ8viDJ).
The CDIL team will:

- QC objects
- [Generate derivatives](https://collectionbuilder.github.io/cb-docs/docs/objects/derivatives/#generate-derivatives-rake-task) using `rake generate_derivatives`
- Copy the folder to the libobjects server (in a folder matching the collection name)
- Copy the full quality objects and metadata to the archive drive (if this has not already been completed)
