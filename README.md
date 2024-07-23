# Project Description: Threat Hunting Analyis Using Cowrie Honeypot and Splunk

## Overview
Threat Hunting Analysis Using Cowrie Honeypot and Splunk is a cybersecurity project focused on simulating SSH/Telnet servers to analyze and understand attacker behavior patterns. By deploying a Cowrie honeypot, the project aims to identify vulnerabilities in SSH and Telnet services, measure the time from honeypot deployment to the first attacker connection, and provide actionable insights for securing these services. The project utilizes Splunk for a comprehensive data exploration and visualization.

## Problem Statement
Remote device access protocols such as SSH and Telnet are essential for network administration but can be highly vulnerable to brute force and other security attacks. Businesses need to understand how quickly attackers can target these services and the common tactics, techniques, and procedures (TTPs) used. Without this knowledge, it is challenging to implement effective defenses and protect critical systems from unauthorized access.

## Solution
The project employs a Cowrie honeypot to simulate a vulnerable UNIX system with SSH and Telnet services. By capturing and analyzing attacker interactions, the project provides insights into attacker behavior, frequency, and timing of attacks. Splunk is used to visualize the collected data, offering a clear and actionable understanding of potential vulnerabilities and how to mitigate them.

## Project Objectives
Simulate SSH/Telnet server with Cowrie honeypot.
Highlight vulnerabilities of SSH and Telnet services.
Calculate time from honeypot deployment to first attacker connection.
Analyze attack frequency and timing for persistence.
Conduct data exploration and visualization in Splunk.
Provide actionable recommendations for securing SSH and Telnet services.

## Honeypots
Honeypots are decoy servers or systems designed to attract attackers. They are used to gather information about attacker behavior patterns (TTPs) and distract attackers from real targets. This project uses a Cowrie honeypot due to its ease of setup, realistic command responses, and detailed logging capabilities.

## Why Cowrie Honeypot?
Easy setup and configuration.
Emulates a UNIX system with a fake filesystem.
Provides realistic command responses for attackers.
Automatically logs activity with log rotation.
Stores session logs and collects attacker downloads.

## SSH (Port 22)
Network protocol for remote device access.
Data is encrypted via a secure channel.
Can be vulnerable to brute force attacks.

## Telnet (Port 23)
Standard TCP/IP protocol for virtual terminal service.
Highly vulnerable to security attacks.
Transfers data in plain text.
Shouldn’t be used on any device.

## Cowrie Setup
Installed on Linode VPS running Ubuntu.
Installed Cowrie-specific dependencies.
Modified sshd_config to change port 22 to 9022.
Configured iptables for NAT.
