A research-oriented cybersecurity project focused on implementing, benchmarking, and comparing Linux server hardening techniques in a controlled experimental environment.

This project evaluates the effectiveness of practical system hardening measures by comparing two identically configured Linux servers:
Baseline Server — Default system configuration
Hardened Server — Security-hardened implementation using defensive controls and best practices
The goal is to create a reproducible comparative framework for analyzing improvements in system security posture, attack surface reduction, and operational resilience.

Project Objectives

- Build a practical Linux system hardening framework
- Compare security posture before and after hardening
- Measure attack surface reduction using real benchmarking tools
- Document security configurations and implementation procedures
- Generate reproducible research-oriented results
- Create automation-ready hardening workflows
- Experimental Setup
- Hardware Configuration

Both systems are configured identically to ensure fair comparison, sourced from byteistic.com 

Component	Specification
OS - Almalinux
Gigabit LAN COnnection


The hardened server implementation focuses on:
- SSH Hardening
- Firewall Configuration
- Fail2Ban Protection
- Service Minimization
- Kernel Parameter Hardening
- File Permission Security
- Audit Logging
- Intrusion Prevention
- Authentication Policies
- Secure Remote Access
- System Update Policies
- AppArmor / SELinux Policies
- Sysctl Security Tuning
- Technologies & Tools
- Category	Tools
- Security Auditing	Lynis, OpenSCAP
- Network Analysis	Nmap
- Intrusion Prevention	Fail2Ban
- Firewall	nftables / iptables
- Monitoring	auditd
- Automation	Bash, Ansible
- Logging	systemd-journald
- Benchmarking	Custom scripts
- Benchmarking Methodology
- The framework compares both systems using:
- Security Benchmarks
- Lynis security scoring
- OpenSCAP compliance checks
- Running services comparison
- Open port analysis
- Firewall rule validation
- Authentication policy analysis
- Attack Surface Evaluation
- Network exposure assessment
- SSH enumeration comparison
- Service accessibility analysis
- Privilege escalation resistance
- Performance Impact Analysis
- CPU utilization
- Memory overhead
- Boot time comparison
- Service startup impact
- Disk usage comparison
- Example Evaluation Metrics
- Metric	Baseline Server	Hardened Server
- Open Ports	Higher	Reduced
- Running Services	Default	Minimized
- Lynis Score	Lower	Improved
- Brute Force Resistance	Weak	Enhanced
- Audit Logging	Minimal	Comprehensive


Disclaimer

This project is intended strictly for educational, research, and defensive security purposes.
All testing is performed within controlled and authorized environments.

Author

Aditya Chaturvedi(t.me/@Clawser / ac79043@gmail.com)
