# SOC Engineering & Automation Roadmap (6 Tháng - 80/20)

> **Mục tiêu:** Sau 6 tháng, bạn đủ kỹ năng và dự án để apply vị trí **SOC Automation Intern / SOC Analyst Tier 1–2**.  
> **Phương pháp:** 80/20 — tập trung vào 20% kiến thức cốt lõi giúp bạn thực hành, lab và tự động hóa nhanh nhất.

---

## Tổng quan 6 tháng

| Giai đoạn | Thời gian | Mục tiêu chính | Kết quả mong đợi |
|------------|------------|----------------|------------------|
| **1. Nền tảng SOC + Linux + Network + Python** | Tháng 1 | Hiểu cách SOC vận hành, dùng Linux & Python cơ bản | Chạy được log collector, alert script |
| **2. SIEM cơ bản (ELK, Wazuh, Splunk Free)** | Tháng 2 | Thu thập, phân tích, tạo alert log | Có lab SIEM hoạt động |
| **3. SOC Automation + SOAR** | Tháng 3 | Làm automation với API, playbook, Python | Workflow tự động hóa alert |
| **4. Threat Intelligence + Incident Response** | Tháng 4 | Phân tích IOC, correlation, MITRE ATT&CK | Report phân tích sự cố |
| **5. Xây SOC Lab hoàn chỉnh** | Tháng 5 | Tích hợp SIEM + SOAR + Honeypot + Alert | Mini SOC lab hoàn chỉnh |
| **6. Dự án thực chiến & Portfolio** | Tháng 6 | Dự án + báo cáo chuyên nghiệp | GitHub + CV sẵn sàng apply |

---

## Tháng 1: SOC, Linux, Network, Python

### Mục tiêu
- Hiểu quy trình SOC (alert → triage → investigate → respond)  
- Làm quen Linux, networking cơ bản  
- Học Python để parse log & automation nhỏ  

### Checklist
- [ ] Học SOC workflow cơ bản (alert lifecycle)  
- [ ] Ôn lại TCP/IP, DNS, HTTP, SSH, VPN  
- [ ] Làm lab trên Ubuntu VM  
- [ ] Viết Python script đọc `/var/log/syslog` → lọc từ khóa “failed” → gửi cảnh báo Discord/Webhook  

### Công cụ & Lab
- `tcpdump`, `journalctl`, `syslog-ng`  
- TryHackMe: [SOC Level 1 Learning Path](https://tryhackme.com/path/outline/soclevel1) :contentReference[oaicite:0]{index=0}  
- BlueTeamLabs: [Blue Team Labs Online](https://blueteamlabs.online/) :contentReference[oaicite:1]{index=1}  

---

## Tháng 2: SIEM Cơ Bản (ELK / Wazuh / Splunk)

### Mục tiêu
- Hiểu cơ chế SIEM: log → parser → correlation → alert  
- Cài đặt và tạo dashboard cảnh báo  

### Checklist
- [ ] Cài Wazuh Manager + ELK trên Ubuntu  
- [ ] Tạo 1 endpoint Windows gửi log về SIEM  
- [ ] Viết Python script lấy alert từ Wazuh API → gửi Discord webhook  
- [ ] Dùng Splunk Free thử query cơ bản  

### Lab setup
- VM1: Ubuntu (Wazuh)  
- VM2: Kali Linux (attacker)  
- VM3: Windows (endpoint)  

**Tài liệu:**  
- [Wazuh Docs](https://documentation.wazuh.com/current/)  
- [Elastic Stack Guide](https://www.elastic.co/guide/index.html)  

---

## Tháng 3: SOC Automation & SOAR

### Mục tiêu
- Làm quen SOAR: automation playbook, API, response flow  

### Checklist
- [ ] Học REST API & JSON cơ bản  
- [ ] Setup **Shuffle SOAR** (cloud hoặc self-hosted)  
  - Docs chính thức: [Shuffle Docs](https://shuffler.io/docs) :contentReference[oaicite:2]{index=2}  
- [ ] Tạo workflow: Lấy alert → Enrich IP bằng VirusTotal → Gửi Slack  
- [ ] Viết script tự động phản hồi cảnh báo đơn giản  

**Công cụ:**  
- [Shuffle Automation](https://shuffler.io/) :contentReference[oaicite:3]{index=3}  

---

## Tháng 4: Threat Intelligence & Incident Analysis

### Mục tiêu
- Hiểu IOC, phân tích log, sử dụng MITRE ATT&CK  

### Checklist
- [ ] Học IOC: IP, domain, hash, URL  
- [ ] Sử dụng API: VirusTotal, AbuseIPDB  
- [ ] Làm lab trên BTLO / TryHackMe (Threat Hunting rooms)  
- [ ] Viết playbook tự động enrich IOC & cảnh báo độc hại  

**Công cụ:** Wireshark, Zeek, VirusTotal API, MITRE ATT&CK Navigator  

---

## Tháng 5: Xây SOC Mini-Lab Hoàn Chỉnh

### Mục tiêu
- Tích hợp toàn bộ: SIEM + SOAR + Honeypot + Automation  

### Checklist
- [ ] Setup Wazuh + Shuffle hoặc TheHive  
- [ ] Thêm Honeypot: Cowrie hoặc T-Pot  
- [ ] Viết Python script auto-block IP brute-force  
- [ ] Log visualization bằng Grafana / Kibana  

**Tham khảo:**  
- [DetectionLab (Chris Long) GitHub](https://github.com/clong/DetectionLab)  
- [Wazuh Docker Deploy](https://documentation.wazuh.com/current/deploying-with-docker/index.html)  

---

## Tháng 6: Dự án Thực Chiến & Portfolio

### Mục tiêu
- Làm **5 dự án** để chứng minh kỹ năng thực tế  

### Dự án Gợi Ý  
| Dự án | Mô tả | Kỹ năng luyện | Độ khó |
|--------|-------|----------------|--------|
| [ ] **1. Log Parser Bot** | Script Python phân tích `/var/log/auth.log`, gửi cảnh báo fail login | Linux log, Python | ★☆☆☆☆ |
| [ ] **2. Wazuh Alert Collector** | Dùng Wazuh API → lưu MongoDB → visualize bằng Grafana | API, log management | ★★☆☆☆ |
| [ ] **3. IP Reputation Enricher** | Tự động enrich alert bằng VirusTotal API | Threat intel, SOAR | ★★★☆☆ |
| [ ] **4. SOC Mini-Lab** | Tích hợp Wazuh + Shuffle + Honeypot + Alert | SIEM, SOAR, automation | ★★★★☆ |
| [ ] **5. Auto Incident Responder** | Playbook tự động phát hiện brute-force → enrich IP → block firewall | End-to-end automation | ★★★★★ |

---

## Sau 6 tháng, bạn nên có

- [ ] GitHub chứa scripts Python, config lab, playbook SOAR  
- [ ] 2–3 báo cáo Incident thực tế (Markdown hoặc PDF)  
- [ ] 1 CV kỹ thuật (SOC Automation / Blue Team Intern)  

**Kỹ năng ghi trên CV:**  
> SIEM (Wazuh, Splunk), SOAR (Shuffle, TheHive), Python, REST API, Threat Intel, MITRE ATT&CK  

---

## Nguồn Tài Nguyên Đề Xuất

- TryHackMe: [SOC Level 1 Learning Path](https://tryhackme.com/path/outline/soclevel1) :contentReference[oaicite:4]{index=4}  
- Blue Team Labs Online: [Blue Team Labs Online](https://blueteamlabs.online/) :contentReference[oaicite:5]{index=5}  
- Shuffle SOAR Docs: [Shuffle Docs](https://shuffler.io/docs) :contentReference[oaicite:6]{index=6}  
- LetsDefend: [LetsDefend Blue Team Training](https://letsdefend.io/) :contentReference[oaicite:7]{index=7}  

---

### Gợi ý mở rộng sau 6 tháng
- Học thêm YARA rules & Sigma rules  
- Tìm hiểu automation với Ansible / Python asyncio  
- Học container hóa SOC bằng Docker Compose  
- Apply intern SOC Automation hoặc Analyst Tier 1  

---

**Tác giả:** Roadmap dành cho người mới bắt đầu muốn trở thành **SOC Automation Engineer**.  
> Keep tracking progress, update checklist, commit your journey 

