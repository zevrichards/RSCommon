# RSCommon

Shared utility library (Delphi/Pascal) used across all [Richer Simulations](https://richersimulations.com) desktop tools. Contains common functions for simulator detection, file operations, registry access, XML parsing, and UI helpers.

## What it does

Rather than duplicating code across multiple projects, RSCommon centralises functionality that is used by RSSCT, OBJ2XPMesh, FSGP2XP and other tools in the Richer Simulations workflow.

**Simulator utilities**
- Detects installed versions of X-Plane, FSX and Prepar3D
- Resolves simulator install paths from registry
- Detects installed Richer Simulations products
- Checks for SODE and ACM installations

**File and config utilities**
- Reads and writes `scenery.cfg` entries for X-Plane
- Edits `LW.cfg` configuration files
- Copies, deletes and moves files with Windows shell integration
- Logs status messages to a log file

**XML utilities**
- Searches and replaces entries in XML files by position
- Returns tag content as strings

**String utilities**
- `ReturnStringBetween` / `ReturnStringBetweenText` — extract substrings between delimiters
- `DeegreesMinutesToDecimalDegrees` — coordinate format conversion
- `SurroundingQuotes` — detects quote character type surrounding a string
- Various type conversion helpers (bool to int, bool to string, endian swap)

**UI helpers**
- Custom message dialog with configurable button captions
- Image resource loader from module
- State save/restore for form components
- Toggle switch and trackbar helpers

**Registry helpers**
- Read/write product install locations
- Query arbitrary registry string values

**Version utilities**
- Read version strings and integers from EXE resources
- Compare version integers

## Tech stack

- Delphi (Object Pascal) — VCL library unit
- Windows API (registry, shell, file operations)

## Usage

Add `RSCommonFunctions` to the `uses` clause of any Delphi project. Ensure the unit path is added to your project's library search path in Delphi's project options.

## Building

No separate build step required — this is a unit library. Include it as a source dependency in any of the dependent projects (RSSCT, OBJ2XPMesh, FSGP2XP, etc.).
