# Baseline System Documentation

## Operating System Information

| Parameter | Value |
|---|---|
| Operating System | AlmaLinux |
| Version | AlmaLinux 8.10 (Cerulean Leopard) |
| Kernel Version | 4.18.0-553.el8_10.x86_64 |
| Installation Type | Minimal Install |
| Boot Mode | UEFI |
| Filesystem Layout | LVM |
| IP Configuration | Static |

---

## Partition Layout

| Partition | Size |
|---|---|
| /boot | 2 GB |
| swap | 2 GB |
| / | 115.24 GB |

---

## Initial Security Configuration

| Component | Status |
|---|---|
| SELinux | Enabled (Enforcing) |
| FirewallD | Enabled |
| SSH Root Login | Enabled |
| SSH Service | Active |
| Time Synchronization | Enabled via Chrony |

---

## Running Services

- auditd
- chronyd
- crond
- dbus
- firewalld
- irqbalance
- NetworkManager
- polkit
- rsyslog
- sshd
- tuned

Total Running Services: 16

---

## Network Exposure

| Port | Protocol | Service | Exposure |
|---|---|---|---|
| 22 | TCP | SSH | External |
| 323 | UDP | Chrony | Localhost Only |

---

## SELinux Status

| Parameter | Value |
|---|---|
| SELinux Status | Enabled |
| Current Mode | Enforcing |
| Policy Type | Targeted |
| Memory Protection | Secure |

---

## Research Notes

The baseline system was intentionally maintained in its default enterprise Linux