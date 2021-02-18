# Mirth Load Test

LoadTestPrep-Dicom-hl7 Channel reads from /opt/mirthconnect/appdata/sourcedicom DICOM files (*.dcm).*
Then the function loadMapsFromDICOM() initialize all the TAGS from the DICOM.

The channel randomly generates between 1-5 DICOM files with random generated data (firstname, lastname, dob, patientId, etc), and assigns the new data with the function setDICOMTags().
Each of the generated DICOM will contain the same TAGS, but ['tag00200013'] will be unique.

One HL7 File will be generated.

HL7 generated file: /opt/mirthconnect/appdata/genhl7
Filename: ${patientId}.hl7

DICOM generated file: /opt/mirthconnect/appdata/gendicom
Filename: ${patientId}_${count}.dcm
