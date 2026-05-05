
# Final Forensic Report

## 1. Objective

The objective of this investigation was to analyze a Windows disk image to identify suspicious activity, reconstruct a timeline of events, and determine the nature of user actions on the system.

## 2. Methodology

The investigation followed a structured forensic approach:

* Disk image integrity verified using SHA256 and md5sum hashing
* Analysis performed using Autopsy
* Timeline reconstruction based on file system and system artifacts
* Correlation of user, execution, and network artifacts

## 3. Findings

### 3.1 User Intent

Web history analysis showed that the user searched for WiFi sniffing techniques prior to any suspicious activity.
This indicates premeditated intent to perform network-related actions.

### 3.2 Preparation Phase

A file named `logins.txt` was created containing usernames and passwords.
A batch script named `notepab.bat` was later created.
The script was designed to appear legitimate while executing hidden commands.

### 3.3 Execution Phase

The script performed the following actions:

* Opened Notepad as a visible decoy
* Collected network configuration using system commands
* Performed traceroute to an external domain
* Captured running processes

Outputs were written to:

* `capture.txt` (network information)
* `log.txt` (traceroute results)
* `user.txt` (running processes)

### 3.4 Data Collection

Multiple files containing system and network data were created within a short time frame, indicating automated execution and structured data collection.

### 3.5 Cleanup Activity

Evidence indicates attempts to remove traces:

* `logins.txt` was deleted after creation
* A folder named `hacks` was deleted

This behavior suggests an attempt to conceal activity.

### 3.6 Data Packaging

A ZIP archive was created after data collection, indicating that collected information was grouped for storage or transfer.

## 4. Timeline Reconstruction

* 00:53–00:54 – User searched for WiFi sniffing techniques
* 00:57 – `logins.txt` created (contains credentials)
* 01:22 – `notepab.bat` created
* 01:25 – `login.txt` deleted
* 01:26 – ZIP file created
* 01:27 – "hackers" folder deleted
* 01:28 – Multiple output files created (`capture.txt`, `log.txt`, `user.txt`)

## 5. Conclusion

The system was used to execute a disguised batch script designed to collect system and network information while appearing legitimate.

The sequence of actions demonstrates:

* Intent (web searches)
* Preparation (script and credential file creation)
* Execution (script activity)
* Collection (system and network data)
* Cleanup (file and folder deletion)
* Packaging (ZIP archive creation)

This pattern indicates deliberate and controlled activity.

## 6. Final Assessment

The observed activity is consistent with intentional reconnaissance and data collection behavior, followed by partial cleanup and organization of collected data.
