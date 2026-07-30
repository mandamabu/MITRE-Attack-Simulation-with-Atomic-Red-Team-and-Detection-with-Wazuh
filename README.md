# MITRE-Att&ck-Simulation-with-Atomic-Red-Team-and-Detection-with-Wazuh
A simulation of MITRE ATT&CK techniques with Atomic Red Team and detection coverage in Wazuh SIEM. A purple team project covering brute force, scripting and obfuscated command execution, and valid account abuse. 
## Overview

This project validates real world detection coverage by simulating attacker behavior with Atomic Red Team and confirming whether Wazuh correctly detects it, this is the same workflow a SOC analyst uses to test and tune detection rules.

## Steps Taken:

1. Baseline Capture
For each technique, a "before" screenshot was taken in Wazuh prior to running any simulation, to provide a clean comparison point.
2. Attack Simulation
Each technique was executed using the `Atomic Red Team` tool
3. Detection Verification
After each simulation:
- Wazuh was checked first to confirm the raw event data reached the manager at all
- A fresh "after" screenshot was taken showing the new event/alert, for direct before/after comparison
For each of the 3 techniques, the following was documented in the Attack Playbook:
- Tactic, technique, and procedure breakdown
- Detection: how the technique was caught
- Response: a step-by-step incident response procedure a SOC analyst would follow if this were a real detection
## Lab Environment

- Attacker/Simulation host: Kali Linux VM (Atomic Red Team)
- Defender: Wazuh SIEM (Ubuntu manager + Kali agent)
- Network: Host-only, isolated lab network

## Techniques Simulated
 1- Brute Force: T1110    
 2- Command and Scripting Interpreter: T1059     
 3- Valid Accounts: Local Accounts (Account Creation) T1078.003 

## 
All tests were executed exclusively against isolated, self-owned VMs
on a host-only virtual network. No external systems were targeted, in
compliance with the Cybercrimes Act 2015.

