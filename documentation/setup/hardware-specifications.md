# Comparative System Hardening Framework

## Repository File Content Templates

---

# documentation/setup/hardware-specifications.md

```markdown
# Hardware Specifications

## Research System Configuration

| Component | Specification |
|---|---|
| CPU | Intel Core i7-2600 |
| RAM | 8 GB DDR3 |
| Storage Device | Samsung SATA SSD |
| Storage Capacity | 128 GB |
| Motherboard | H61M2 |
| Network Interface | Integrated 1 Gbps Ethernet |
| Installation Method | Bootable USB Drive |

---

## Experimental Environment

The research environment was designed to evaluate Linux system hardening techniques under controlled conditions using enterprise-style minimal server deployment practices.

The server hardware represents low-resource production infrastructure commonly found in small business hosting environments, legacy enterprise systems, and lightweight virtualization deployments.

The environment was intentionally configured with modest hardware resources to evaluate the operational impact and effectiveness of practical hardening controls on constrained systems.
```

---

# documentation/setup/baseline-system.md

```markdown
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

The baseline system was intentionally maintained in its default enterprise Linux configuration prior to the application of hardening controls. This ensured that all comparative measurements reflected the impact of implemented security measures rather than differences in initial deployment configuration.
```

---

# documentation/setup/installation-notes.md

```markdown
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
```

---

# documentation/setup/network-topology.md

```markdown
# Network Topology

## Experimental Architecture

The experimental environment consists of a single AlmaLinux research server connected to a testing workstation over a controlled network.

The testing workstation functions as the attacker and analysis system for:

- Network scanning
- SSH brute-force simulation
- Vulnerability assessment
- Service enumeration
- Traffic monitoring
- Comparative attack analysis

---

## Topology Diagram

Laptop (Attacker/Test System)
        |
        |
   Network / Switch
        |
        |
AlmaLinux Research Server

---

## Network Characteristics

| Parameter | Value |
|---|---|
| Connection Speed | 1 Gbps |
| IP Allocation | Static |
| Access Method | SSH |
| Test Environment | Controlled Local Network |

---

## Research Purpose

The network design was intentionally simplified to isolate the effects of operating system hardening controls and minimize environmental variability during comparative testing.
```

---

# documentation/methodology/hardening-methodology.md

```markdown
# Hardening Methodology

## Objective

The objective of this research is to evaluate the effectiveness of practical Linux hardening techniques through controlled comparative analysis.

The study compares the security posture of a default enterprise Linux deployment against the same system after systematic hardening implementation.

---

## Hardening Areas

The following security domains are included in the hardening process:

- SSH hardening
- Firewall rule optimization
- Kernel parameter hardening
- Service minimization
- Password policy enforcement
- File permission hardening
- SELinux enforcement validation
- Intrusion prevention using Fail2Ban
- Audit logging improvements
- File integrity monitoring using AIDE

---

## Research Approach

1. Deploy baseline system
2. Record default security state
3. Perform baseline attack simulation
4. Apply hardening controls incrementally
5. Re-test using identical attack methodology
6. Compare results and analyze improvements

---

## Measurement Areas

The following metrics are evaluated:

- Open ports
- Running services
- Attack surface exposure
- SSH brute-force resistance
- Logging visibility
- Security audit scores
- Resource utilization
- Operational impact
```

---

# documentation/methodology/testing-methodology.md

```markdown
# Testing Methodology

## Testing Objective

The testing phase evaluates the effectiveness of implemented hardening controls by comparing the baseline and hardened system states using identical attack and enumeration procedures.

---

## Testing Categories

### Network Enumeration

- Port scanning using Nmap
- Service detection
- Version enumeration
- TCP exposure analysis

### Authentication Testing

- SSH brute-force simulation
- Password policy validation
- Login restriction testing

### Security Auditing

- Lynis security auditing
- CIS benchmark analysis
- Firewall validation
- SELinux verification

### System Monitoring

- Log generation analysis
- Audit event monitoring
- Service activity observation
- Intrusion prevention analysis

---

## Comparative Analysis

Each test is executed:

1. Before hardening
2. After hardening

Results are then compared to evaluate:

- Reduction in attack surface
- Improvement in security posture
- Resistance against common attacks
- Operational overhead introduced by hardening controls
```

---

# documentation/methodology/attack-scenarios.md

```markdown
# Attack Scenarios

## Objective

The attack simulation phase evaluates how effectively the hardened system mitigates common network-based and authentication-based threats.

---

## Simulated Attack Categories

### SSH Brute-Force Attempts

Tools:
- Hydra
- SSH login scripts

Objective:
Evaluate authentication protections and intrusion prevention mechanisms.

---

### Network Enumeration

Tools:
- Nmap

Objective:
Measure visible attack surface and service exposure.

---

### Service Detection

Objective:
Identify unnecessary or exposed services prior to and after hardening.

---

### Firewall Validation

Objective:
Verify port restrictions and packet filtering effectiveness.

---

### SELinux Enforcement Testing

Objective:
Validate mandatory access control enforcement behavior.

---

## Research Ethics

All testing activities are performed exclusively within a controlled environment on personally owned infrastructure.

No unauthorized systems or public infrastructure are targeted during experimentation.
```

---

# documentation/findings/observations.md

```markdown
# Observations

## Baseline System Observations

The baseline deployment demonstrated a relatively low default attack surface due to the use of a minimal enterprise Linux installation.

Only SSH was externally exposed by default.

SELinux was enabled in enforcing mode, and FirewallD was active immediately after installation.

The default service count remained limited, reducing unnecessary exposure.

---

## Expected Hardening Impact

The hardening process is expected to:

- Reduce attack surface visibility
- Improve authentication resistance
- Increase monitoring visibility
- Strengthen kernel-level protections
- Improve logging and auditing capabilities
- Restrict unauthorized access attempts
```

---

# documentation/findings/conclusions.md

```markdown
# Conclusions

This research project evaluates practical Linux hardening methodologies using a controlled comparative experimental approach.

The study focuses on measurable improvements in system security posture through the implementation of enterprise-grade hardening controls.

The project demonstrates how layered security mechanisms such as firewall optimization, SSH hardening, intrusion prevention, audit logging, and kernel parameter tuning collectively improve system resilience against common attack scenarios.

Future work may include:

- Automated hardening deployment
- Container security evaluation
- Kernel-level exploit mitigation analysis
- SIEM integration
- Advanced intrusion detection systems
```

---

# README.md

```markdown
# Comparative System Hardening Framework

## Overview

A research-oriented cybersecurity project focused on implementing and evaluating Linux server hardening techniques using controlled comparative analysis.

The project evaluates the effectiveness of practical security controls by comparing a baseline enterprise Linux deployment against the same system after systematic hardening implementation.

---

## Objectives

- Analyze baseline Linux security posture
- Implement practical hardening controls
- Perform comparative security evaluation
- Measure attack surface reduction
- Evaluate operational impact of hardening
- Document reproducible security methodology

---

## Technology Stack

| Component | Technology |
|---|---|
| Operating System | AlmaLinux 8.10 |
| Firewall | FirewallD |
| Intrusion Prevention | Fail2Ban |
| Auditing | auditd |
| File Integrity Monitoring | AIDE |
| Security Auditing | Lynis |
| Network Testing | Nmap |

---

## Repository Structure

- documentation/ → Setup and methodology documentation
- results/ → Security scan and benchmark outputs
- configs/ → Hardened configuration files
- scripts/ → Automation and testing scripts
- screenshots/ → Visual evidence and testing screenshots
- logs/ → Security and system logs
- diagrams/ → Network and architecture diagrams
- paper/ → Research paper drafts and final version

---

## Research Areas

- Linux system hardening
- SSH security
- Firewall optimization
- Kernel security
- Intrusion prevention
- Security auditing
- Attack surface reduction
- Comparative security analysis

---

## License

This project is intended for educational and research purposes only.
```
