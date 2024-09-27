# Metasploitable-Nessus-Scan-Windows
# Internship Training: Metasploitable 2 Vulnerability Scan with Nessus on Windows

## Overview
This repository contains the documentation and results of a vulnerability scan performed on the Metasploitable 2 virtual machine using Nessus, as part of my internship training. The process involves installing and configuring Nessus on a Windows environment, setting up the network on Oracle VM VirtualBox, and conducting a comprehensive scan.

## Table of Contents
- [Installation and Setup of Nessus](#installation-and-setup-of-nessus)
- [Network Configuration for Oracle VM](#network-configuration-for-oracle-vm)
- [Configuring and Launching the Nessus Scan](#configuring-and-launching-the-nessus-scan)
- [Summary of Identified Vulnerabilities](#summary-of-identified-vulnerabilities)
- [Screenshots](#screenshots)
- [Learnings and Reflections](#learnings-and-reflections)

## Installation and Setup of Nessus
### Steps:
1. **Download Nessus:**
   - Download the Windows version from the [Tenable Nessus website](https://www.tenable.com/products/nessus).

2. **Install Nessus:**
   - Run the installer and follow the instructions to complete the installation on your Windows machine.

3. **Start Nessus:**
   - After installation, Nessus will automatically start. You can access the Nessus interface by navigating to `https://localhost:8834` in your web browser.

4. **Initial Setup:**
   - Create a Nessus user account.
   - Enter the activation code received via email to activate the product.

## Network Configuration for Oracle VM
### Steps:
1. **Set Up Oracle VM VirtualBox:**
   - Import the Metasploitable 2 VM into VirtualBox.

2. **Configure the Network Adapter:**
   - In the VirtualBox settings for Metasploitable 2, go to `Settings > Network`.
   - Set the adapter to `Bridged Adapter` to ensure that your Windows host (running Nessus) and Metasploitable 2 VM are on the same network.

3. **Verify Network Communication:**
   - Start the Metasploitable 2 VM.
   - Use the `ipconfig` command on Windows to check the IP address and ensure both machines are on the same network.

## Configuring and Launching the Nessus Scan
### Steps:
1. **Create a New Scan:**
   - In the Nessus interface, navigate to the "Scans" tab and select "New Scan".
   - Choose the "Basic Network Scan" template.

2. **Configure the Scan:**
   - **Name:** "Metasploitable 2 Vulnerability Scan".
   - **Target:** Enter the IP address of the Metasploitable 2 VM.

3. **Launch the Scan:**
   - Save the scan configuration and click "Launch".
   - Wait for the scan to complete.

# Vulnerability Assessment Summary

## Summary of Identified Vulnerabilities

### Results:
- **Critical Vulnerabilities:** 
  - Vulnerabilities such as outdated VSFTPD and OpenSSH services, which could lead to remote code execution.
- **High-Risk Vulnerabilities:** 
  - Issues like Apache and MySQL misconfigurations.
- **Medium and Low-Risk Vulnerabilities:** 
  - Information disclosure and weaker encryption protocols.

## Screenshots
Screenshots of the scan configuration, results, and network setup are stored in the [Screenshots Directory](https://github.com/sammyoflightup/Metasploitable-Nessus-Scan-Windows/tree/main/Screenshots).

## Learnings and Reflections

### Key Takeaways:
- **Understanding Nessus:** This exercise provided hands-on experience with Nessus, including installation, configuration, and running vulnerability scans.
- **Network Configuration:** Setting up a bridged network in VirtualBox was essential for ensuring that the Nessus scanner could reach the Metasploitable 2 target.
- **Vulnerability Analysis:** Reviewing the scan results offered insights into common vulnerabilities found in legacy systems and the importance of regular security assessments.

