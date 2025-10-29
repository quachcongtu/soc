# BASE rất quan trọng !

I.Cơ bản

Mục tiêu: hiểu hạ tầng CNTT, mạng, hệ điều hành, khái niệm bảo mật cơ bản.
Kiến thức nền tảng

- Kiến thức mạng:
    - Mô hình OSI, TCP/IP, subnetting, VLAN, routing, switching.
    - Thiết bị mạng (router, switch, firewall, IDS/IPS).

- Hệ điều hành:
    - Windows Server (Active Directory, GPO, Firewall, Logging).
    - Linux (Permission, service, log, SSH...).

- Bảo mật cơ bản:
    - CIA Triad (Confidentiality, Integrity, Availability).
    - Kiểm soát truy cập, chính sách bảo mật, mã độc, hacker ..
    - Cơ bản về mã hóa (hashing, symmetric/asymmetric encryption).

- Công cụ cơ bản:
    - Wireshark, nmap, netcat, nslookup, ipconfig/ifconfig, ping/traceroute.

II.Lộ trình chuyên sâu:
 
1.NETWORK SECURITY (BẢO MẬT MẠNG)

`Mục tiêu`: Bảo vệ hạ tầng mạng (LAN/WAN/VPN) khỏi xâm nhập, tấn công, dò quét.

- `Kiến thức trọng tâm:`
    - TCP/IP, VLAN, ACL, Routing, NAT, Firewall, VPN, IDS/IPS.
    - Bảo mật thiết bị: switch, router, wireless AP, firewall.
    - Segment network, zero-trust, DMZ.

- `Công cụ:`
    - Cisco Packet Tracer, GNS3, EVE-NG
    - Firewall: pfSense, Fortigate, Palo Alto, Cisco ASA
    - IDS/IPS: Snort, Suricata
    - Wireshark, Nmap, tcpdump

- `Công việc cụ thể:`
    - Thiết kế và triển khai mạng an toàn.
    - Cấu hình firewall, VPN, VLAN tách biệt.
    - Phát hiện và xử lý tấn công mạng (DoS, ARP spoofing, port scan…).
    - Giám sát lưu lượng và audit cấu hình thiết bị mạng.


2.SYSTEM SECURITY (BẢO MẬT HỆ THỐNG)

`Mục tiêu:` Bảo vệ server, OS, ứng dụng và dữ liệu người dùng.

- `Kiến thức trọng tâm:`
    - Windows Server, Linux (Ubuntu, CentOS, Debian).
    - File permission, log, hardening, patch management.
    - Service security (SSH, RDP, IIS, Apache, MySQL).

- `Công cụ:`
    - Windows Event Viewer, Group Policy, PowerShell
    - Linux tools: auditd, ufw, iptables, fail2ban
    - Vulnerability scanner: Lynis, OpenVAS

- `Công việc cụ thể:`
    - Thiết lập quyền truy cập, vá lỗi hệ thống.
    - Giám sát log, phát hiện xâm nhập trái phép.
    - Tạo backup và khôi phục hệ thống.
    - Kiểm tra an toàn cấu hình và dịch vụ hệ thống.


3.ETHICAL HACKING / PENETRATION TESTING

`Mục tiêu:` Mô phỏng tấn công để phát hiện lỗ hổng trước hacker thật.

- `Kiến thức trọng tâm:`
    - Hacking lifecycle: Recon → Scanning → Exploit → Privilege escalation → Report.
    - Web/App Security, SQLi, XSS, AD attack, C2 framework.
    - Network exploitation và social engineering.

- `Công cụ:`
    - Kali Linux, Parrot OS
    - Nmap, Metasploit, Burp Suite, Hydra, Nikto, SQLmap
    - Mimikatz, BloodHound, Empire, Cobalt Strike

- `Công việc cụ thể:`
    - Thực hiện pentest hệ thống, web, mạng nội bộ.
    - Viết báo cáo chi tiết về lỗ hổng, đề xuất khắc phục.
    - Thử nghiệm tấn công AD, kiểm tra quyền người dùng.
    - Tham gia diễn tập Red Team.


4.BLUE TEAM / SOC ANALYST

`Mục tiêu:` Giám sát, phát hiện, phân tích và phản ứng với sự cố bảo mật.

- `Kiến thức trọng tâm:`
    - SIEM , log correlation, detection rule.
    - MITRE ATT&CK, incident response procedure.
    - EDR/XDR, threat hunting, network visibility.

- `Công cụ:`
    - SIEM: Splunk, ELK Stack, Wazuh, QRadar
    - EDR: CrowdStrike, SentinelOne, Microsoft Defender
    - Wireshark, Sysmon, Sysinternals, Sigma rules

- `Công việc cụ thể:`
    - Giám sát log sự kiện trong thời gian thực.
    - Phân tích cảnh báo (alert triage).
    - Điều tra nguồn gốc và phạm vi tấn công.
    - Viết báo cáo sự cố (incident report) và khắc phục.


5.CLOUD SECURITY

`Mục tiêu:` Bảo vệ hạ tầng và dữ liệu trên môi trường đám mây (AWS, Azure, GCP).

- `Kiến thức trọng tâm:`
    - IAM, S3 security, network segmentation, encryption.
    - Shared Responsibility Model.
    - Cloud logging & compliance.

- `Công cụ:`
    - AWS Security Hub, GuardDuty, CloudTrail, Azure Defender
    - Terraform, CloudFormation
    - ScoutSuite, Prowler, Pacu

- `Công việc cụ thể:`
    - Đánh giá cấu hình cloud và phân quyền IAM.
    - Giám sát log và cảnh báo bất thường.
    - Thiết kế chính sách bảo mật cloud.
    - Kiểm tra tuân thủ bảo mật (CIS Benchmark, ISO 27017).



6.DEVSECOPS / APPSEC

`Mục tiêu:` Tích hợp bảo mật vào vòng đời phát triển phần mềm và hạ tầng CI/CD.

- `Kiến thức trọng tâm:`
    - Secure SDLC, SAST, DAST, container security.
    - CI/CD pipelines, IaC, GitOps, Docker/Kubernetes.

- `Công cụ:`
    - OWASP ZAP, Burp Suite, SonarQube
    - Docker, Kubernetes, Jenkins, GitHub Actions
    - Trivy, Clair, Checkov

- `Công việc cụ thể:`
    - Tích hợp quét bảo mật vào pipeline build.
    - Phân tích lỗ hổng trong code và dependency.
    - Quản lý secret và policy trong container.
    - Xây dựng quy trình DevSecOps chuẩn hóa.


7.CLOUD & VIRTUAL INFRASTRUCTURE  storage ( SAN /NAS  +  cloud ) 

`Mục tiêu:` Thiết kế và vận hành hạ tầng ảo hóa và hybrid cloud an toàn.

- `Kiến thức trọng tâm:`
    - Virtual network, hypervisor, container, backup & HA.
    - Cloud migration, VPN, multi-tenant security.
- `Công cụ:`
    - VMware vSphere , Hyper-V, Proxmox
    - Docker, Kubernetes, Terraform
    - AWS VPC, Azure VNets
- `Công việc cụ thể:`
    - Triển khai và bảo mật môi trường ảo hóa.
    - Quản lý mạng ảo, snapshot, backup, HA.
    - Đảm bảo phân vùng mạng và phân quyền user.
    - Thiết kế kiến trúc hybrid cloud an toàn.

