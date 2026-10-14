
### Phân Tích Hệ Thống

* **Mô hình IPO của chức năng lọc log:**
  * **Input:** Tệp nhật ký thô `log-he-thong.log` chứa toàn bộ các dòng log đa dạng mức độ.
  * **Process:** Sử dụng PowerShell Pipeline kết hợp `Get-Content` và `Select-String` để quét, trích lọc các dòng sự cố chứa từ khóa `CRITICAL` hoặc `ERROR` và đếm tổng số lượng lỗi.
  * **Output:** Tệp báo cáo tổng hợp `backup/bao-cao-su-co.txt` lưu trữ thời gian và danh sách chi tiết các sự cố cần xử lý.

* **Phân loại các phát biểu theo tư duy DIKW:**
  * **(b) Data:** *"2026-10-12 08:15:01 [ERROR] sensor-03 Connection TIMEOUT after 30s"* — Các sự kiện, thông số thô chưa qua xử lý ngữ cảnh.
  * **(c) Information:** *"Hôm nay hệ thống ghi nhận 8 sự cố, trong đó 4 sự cố đến từ trạm sensor-03."* — Dữ liệu đã được xử lý, tổ chức và đếm số lượng để thấy được bức tranh tổng quan.
  * **(d) Knowledge:** *"Trạm sensor-03 hay mất kết nối vào buổi chiều do sóng yếu, nên cần lắp thêm anten."* — Sự hiểu biết về mối quan hệ nhân - quả, quy luật hoạt động rút ra từ thông tin quá khứ.
  * **(a) Wisdom:** *"Quyết định thay modem trạm sensor-03 trước thứ Sáu."* — Hành động quyết định dựa trên sự thấu hiểu toàn diện vấn đề để đưa ra phương án giải quyết tối ưu.
