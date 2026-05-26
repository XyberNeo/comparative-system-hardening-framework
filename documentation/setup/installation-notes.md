# Installation Notes

## Installation Media

- Operating System: AlmaLinux 8.10
- Installation Method: Bootable USB Drive
- Installation Type: Minimal Install

---

## Installation Configuration

| Setting | Configuration |
|---|---|
| Filesystem | LVM |
| Boot Mode | UEFI |
| Network Configuration | Static IP |
| FirewallD | Enabled |
| SELinux | Enforcing |
| Root SSH Login | Enabled |

---

## Installation Objectives

The operating system was deployed using a minimal installation profile to reduce unnecessary packages and minimize the default attack surface.

Graphical packages, multimedia components, development environments, and non-essential services were intentionally excluded from the deployment.

The system was configured to reflect a realistic enterprise Linux server deployment environment commonly used in hosting infrastructure and production systems.