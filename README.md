# Honeypot-Attack-Map

## Description

This project simulates a vulnerable cloud infrastructure within Microsoft Azure and showcases how to use Sentinel and Log Analytics for real-time threat detection and geolocation analysis.

## Overview

The goal of this lab is to build and monitor a security-focused Azure environment using Microsoft Sentinel. It demonstrates how to ingest and correlate security logs from a Windows virtual machine, visualize global attack patterns, and pinpoint threat origins using custom watchlists and KQL queries.

## Architecture & Setup

- **Azure Resource Group**: Hosts all resources related to this project.
- **Virtual Network & Subnet**: Enables connectivity for cloud assets.
- **Network Security Group (NSG)**: Deliberately configured with open inbound rules to emulate a vulnerable setup.
- **Windows 10 Virtual Machine**: Used as the attack target to simulate brute-force logon attempts.
- **Log Analytics Workspace**: Centralized log repository for all security-related events.
- **Azure Monitoring Agent (AMA)**: Installed on the VM to forward event logs to the workspace.
- **Microsoft Sentinel**: Connected to Log Analytics to enable SIEM capabilities.

## Threat Detection Workflow

1. Configured Sentinel to collect logs from the Log Analytics Workspace.
2. Uploaded a **Geo-IP Watchlist** (CSV containing over 50,000 IP-location mappings).
3. Used **Kusto Query Language (KQL)** to:
   - Monitor failed logon attempts on the VM.
   - Cross-reference source IPs with the watchlist.
   - Extract and visualize attacker locations globally.
4. Populated a custom **Attack Map Dashboard** to display malicious IP origins and identify hotspots.

## Key Skills & Tools

- Azure Cloud Services  
- Microsoft Sentinel  
- Log Analytics & AMA  
- Network Security Groups (NSG)  
- KQL (Kusto Query Language)  
- Geo-IP enrichment using watchlists  
- Real-world simulation of brute-force attacks  

## Insights

This project provides hands-on experience in:
- Configuring cloud-native SIEM environments.
- Detecting and analyzing malicious activity in real-time.
- Mapping attack vectors to geographic origins.
- Simulating vulnerable infrastructure for learning and experimentation.

## World map of incoming attacks after 6 hours
