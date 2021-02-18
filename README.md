# Mirth Load Test

The Channel LoadTestPrep-Dicom-hl7 process DICOM files from `/opt/mirthconnect/appdata/sourcedicom`.

`loadMapsFromDICOM()` initialize all the TAGS from the DICOM.
`setDICOMTags()` assigns the new randomly generated data into the DICOM tags.

The channel randomly generates between 1-5 DICOM files with random generated data (firstname, lastname, dob, patientId, etc).
Each of the generated DICOM will contain the same TAGS data, but `['tag00200013']` will be unique.

Only one HL7 file will be generated.

**HL7 generated file:** `/opt/mirthconnect/appdata/genhl7`
**Filename:** `${patientId}.hl7`

**DICOM generated file:** `/opt/mirthconnect/appdata/gendicom`
**Filename:** `${patientId}_${count}.dcm`
