# On-Prem-File-Share-Discovery
Powershell script for Windows File share Discovery 
<#
File Share Discovery + Size + Top-Level Permissions + Share Type + Shared With (PowerShell 5.1, NO -Parallel)

Outputs:
  1) Inventory CSV
  2) Error CSV

Notes:
- Share enumeration uses WMI (Win32_Share)
- Size + NTFS ACL + Share ACL are collected via ONE Invoke-Command call per server
- If WinRM/PowerShell remoting is blocked, size/permissions will fail but share inventory still exports.
