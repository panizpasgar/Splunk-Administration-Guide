# Splunk Enterprise Installation on Ubuntu Server 24.04.3 LTS

This guide provides a step-by-step procedure for installing and configuring Splunk Enterprise on Ubuntu Server 24.04.3 LTS.

## Environment

| Component | Version |
|---|---|
| Operating System | Ubuntu Server 24.04.3 LTS |
| Architecture | amd64 |
| Splunk | Splunk Enterprise |
| Installation Type | Single Instance |

## Installation Steps

1. [Prerequisites](#1-prerequisites)
2. [Operating System Preparation](#2-operating-system-preparation)
3. [Download Splunk](#3-download-splunk)
4. [Install Splunk](#4-install-splunk)
5. [Start Splunk](#5-start-splunk)
6. [Enable Splunk at Boot](#6-enable-splunk-at-boot)
7. [Access Splunk Web](#7-access-splunk-web)
8. [Initial Configuration](#8-initial-configuration)
9. [Verify Installation](#9-verify-installation)

---

## 1. Prerequisites

Before installing Splunk Enterprise, verify that the server meets the required specifications.

### Server Specifications

- Ubuntu Server 24.04.3 LTS
- 64-bit AMD64 architecture
- Static IP address
- Internet access
- Sufficient CPU, RAM and disk resources

### Verify Operating System

```bash
cat /etc/os-release
