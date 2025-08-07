A Back-up clone of: https://github.com/franjoWi/ConverterMetasonicToStandardPASS#

# Metasonic2PASS-OWL Converter

This tool converts process models from the Metasonic Suite (.jpp files) into the PASS OWL exchange standard. It was developed as part of a bachelor's thesis at the University of Münster.

## Features

- Reading Metasonic XML files
- Mapping model elements to OWL structures
- Export as a standards-compliant OWL model
- Support for subjects, states, transitions, messages, and more

## Requirements

- `alps.net.api` library (e.g., via NuGet or include locally)

## Usage

```csharp
string sourcePath = @"Path\to\model.jpp";
string destinationPath = @"Path\to\model.owl";
string baseuri = "http://www.example.org/myprocess";

var converter = new PASSConverterMetasonicToStandard(sourcePath);
converter.convertMetasonicModelToOWLStandard(destinationPath, baseuri);
