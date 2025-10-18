# SOC workflow basic (alert lifecycle)

## Quy trình vận hành của SOC

### Giám sát và phát hiện (Monitoring & Detection)
SOC giám sát dữ liệu log từ hệ thống và phát hiện các dấu hiệu bất thường như:

- `Lưu lượng mạng bất thường` (Ví dụ: DDoS, dữ liệu outbound lớn bất thường).
- `Hành vi đáng ngờ` (tấn công brute-force, đăng nhập trái phép).
- `Tấn công từ malware, ransomware`.

### Phân tích và điều tra (Analyst & Investigation)
Sau khi phát hiện cảnh báo, chuyên gia SOC tiến hành điều tra để xác định bản chất của mối đe dọa. Các kĩ thuật phổ biến gồm:

- `Phân tích log hệ thống`: Kiểm tra dấu vết của cuộc tấn công.
- `Threat hunting`: Sử dụng công cụ threat intelligence để tìm kiếm dấu hiệu của APTs.
- `Digital Forensics`: Phân tích dữ liệu sau sự cố để hiểu rõ hơn về kỹ thuật tấn công.

### Phản ứng và xử lí sự cố (Incident Response & Remediation)
SOC thực hiện các bước khắc phục, có thể bao gồm:

- Cô lập hệ thống bị xâm nhập.
- Triển khai các biện pháp phòng thủ (blocking IP, update firewall rules).
- Phối hợp với các bộ phận IT để khôi phục hệ thống.

### Báo cáo và cải tiến (Post-Incident Review & Improvement)
Sau mỗi sự cố, SOC đánh giá lại hiệu quả phản ứng, cập nhật chính sách bảo mật và cải thiện các quy trình vận hành.

