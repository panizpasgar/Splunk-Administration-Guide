# Splunk Enterprise Installation on Ubuntu Server 24.04.3 LTS

This guide provides a step-by-step procedure for installing and configuring Splunk Enterprise on Ubuntu Server 24.04.3 LTS.

## Environment

| Component         | Version                   |
| ----------------- | ------------------------- |
| Operating System  | Ubuntu Server 24.04.3 LTS |
| Architecture      | amd64                     |
| Splunk            | Splunk Enterprise         |
| Installation Type | Single Instance           |

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

Before installing Splunk Enterprise, verify that the server meets the required prerequisites.

### Operating System

This guide is based on Ubuntu Server 24.04.3 LTS.

Verify the operating system version:

```bash
cat /etc/os-release

```
![Ubuntu Version](images/01-ubuntu-version.png)

### System Architecture

Verify the system architecture:

```bash
uname -m
```

![System Architecture](images/02-system-architecture.png)

## 2. Operating System Preparation

Before installing Splunk Enterprise, update the Ubuntu package repository.

### Update Package Repository

Run the following command:

```bash
sudo apt update
```

![APT Update](images/03-apt-update.png)

### Install Required Utilities

Install `wget` and `curl` to download and transfer files during the installation process.

```bash
sudo apt install wget curl -y
```

Verify the installation:

```bash
wget --version
curl --version
```

![Install Wget and Curl](images/04-install-wget-curl.png)
---

## 3. Download Splunk

Splunk Enterprise provides different installation packages for Linux.

For Ubuntu Server, the Debian (`.deb`) package is used in this guide.

### Download the Splunk Enterprise Package

Log in to your Splunk account and download the latest available Splunk Enterprise `.deb` package for Linux x86-64.

![Splunk Download](images/05-splunk-download.png)

The downloaded package should have a filename similar to:

```text
splunk-<version>-<build>-Linux-amd64.deb
```

The package can then be transferred to the Ubuntu server.
