# firewall-task
Cyber Security Internship – Task 4
# 🔥 Firewall Configuration Task (Windows)

## 🎯 Objective:
Demonstrate basic firewall rule creation and testing using **Windows Defender Firewall** to understand how network traffic can be filtered by ports.

---

## 🖥️ Platform:
- Operating System: **Windows 10/11**
- Tool: **Windows Defender Firewall with Advanced Security**
- Test tool: `telnet` via Command Prompt

---

## ✅ Steps Performed:

### 1. Checked Existing Firewall Rules
- Opened `Windows Defender Firewall with Advanced Security`
- Viewed current `Inbound` and `Outbound Rules`

### 2. Added a Rule to Block Port 23 (Telnet)
- Created new **Inbound Rule**
  - Type: `Port`
  - Protocol: `TCP`
  - Port: `23`
  - Action: `Block the connection`
  - Applied to all profiles (Domain, Private, Public)
  - Named it: `Block Telnet Port 23`

### 3. Tested Connection to Port 23 Using Telnet
- Ran the following command:
  ```bash
  telnet 127.0.0.1 23
  Result before adding the rule:
Connect failed — This is expected since no Telnet service is running on the system by default.

Result after adding the rule:
Same failure (Connect failed) — Now the port is also blocked by the firewall, confirming the rule is effective.

### 4. Removed the Firewall Rule
Deleted the custom rule (Block Telnet Port 23) to restore the original firewall configuration.
