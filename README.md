# Windows Forensic Investigation – Suspicious Script Activity

## Overview

This project presents a forensic analysis of a Windows disk image following suspicious activity on the system. The goal was to reconstruct events, identify executed actions, and determine whether any unauthorized behavior occurred.

## Objective

* Identify suspicious files and activity
* Reconstruct a chronological timeline of events
* Analyze user behavior and intent
* Correlate artifacts to form a complete narrative

## Tools Used

* Autopsy (disk analysis and timeline reconstruction)
* Hashing tools (SHA256 integrity verification)
* Manual artifact correlation

## Key Findings

* A disguised batch script (`notepab.bat`) was created and executed
* The script opened Notepad as a decoy while performing hidden actions
* System and network information was collected into multiple files
* Sensitive data (`login.txt`) was created and later deleted
* Evidence of cleanup activity (file and folder deletion) was observed
* Collected data was compressed into a ZIP archive

## What Happened

The user searched for WiFi sniffing techniques, then created a script disguised as a normal application.
When executed, the script collected system and network information while appearing harmless.
After collecting data, some files were deleted and the remaining data was packaged into a ZIP file.

## Project Structure

* `evidence/` – Image integrity and disk details
* `timeline/` – Chronological reconstruction of events
* `artifacts/` – Analysis of execution, network, and user behavior
* `screen_shot/` – Supporting forensic evidence
* `report/` – Final investigation report

## Full Report

See `report/final_report.md`

## Takeaway

This project demonstrates the ability to correlate multiple artifacts and reconstruct a clear, evidence-based forensic narrative.
