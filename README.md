# Digital Forensics Case Investigation Write-Up

This repository contains a detailed write-up of a major digital forensics project completed as part of the COMM069 module for my MSc in Cyber Security at the University of Surrey. The project involved a comprehensive analysis of a disk image in a simulated legal case, demonstrating a full forensic workflow from evidence handling to reporting.

***Note:*** *The case files and evidence image were provided by the university and cannot be shared publicly. This repository serves as a detailed description of the process and methodology used.*

## 📜 The Scenario
I acted as a forensic investigator for a fictional law firm, "Acme Lawyers." The task was to examine a USB stick disk image (`exhibit #DFT-USB-A-315`) for evidence that could potentially exonerate a client accused of possessing illegal "bamboo images." The core challenge was to determine the true history of the device and identify any signs of tampering or access by other parties that could support the client's claim of innocence.

## 🎯 Investigative Objectives
The investigation was guided by a set of key questions:
- Was there evidence of the illicit images on the USB stick?
- Could the origin of any images found be determined?
- Were there any signs of evidence planting or data manipulation?
- Could access by any other party be proven?
- Were there any other irregularities on the device?

## 🛠️ Methodology & Tools
The entire investigation was conducted using industry-standard open-source tools within the **Tsurugi Linux** digital forensics environment.

### 1. Evidence Integrity and Chain of Custody
To ensure the integrity of my findings, a strict chain of custody was maintained for my digital notes.
- **Contemporaneous Notes (CNs):** Detailed notes documenting every action, tool, command, and finding were maintained throughout the investigation.
- **Cryptographic Timestamping:** Using **OpenSSL** and the **FreeTSA.org Time Stamping Authority (TSA)**, I created verifiable, digitally signed timestamps of my CNs at regular intervals. This process provides auditable proof of when the notes were created and that they were not tampered with after the fact.

### 2. Forensic Analysis
- **Initial Triage:** The `.dd` image was ingested into **Autopsy**, a graphical forensic suite, to perform an initial analysis of the file system, partition data, and view metadata.
- **File System & Metadata Analysis:** I examined file system structures and metadata (MAC times) to build a timeline of events, identifying when files were created, modified, and accessed to look for anomalies.
- **Data Carving:** Tools like **Foremost** and **Scalpel** were used to perform data carving on unallocated space, successfully recovering deleted files and file fragments that were not visible in the standard file system.
- **Reporting:** The investigation concluded with a full report based on the findings documented in the Contemporaneous Notes.

## 💡 Skills Demonstrated
This project provided hands-on experience in the following areas:
- **End-to-End Digital Forensics Investigation**
- **Evidence Handling & Chain of Custody**
- **File System Analysis (using Autopsy)**
- **Data Carving & File Recovery (using Foremost, Scalpel)**
- **Timeline Reconstruction & Metadata Analysis**
- **Technical Reporting (Contemporaneous Notes)**
- **Use of Forensic Tools (Tsurugi Linux)**
- **Applied Cryptography for Evidence Integrity (OpenSSL, TSA)**# Forensic-Investigation-Project
