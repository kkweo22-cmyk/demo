# Xây Dựng Hệ Thống Mạng LAN Cho UBND

## Giới thiệu

Đây là mô hình mạng LAN cho UBND được xây dựng theo cấu trúc Star Topology (mạng hình sao) bằng Cisco Packet Tracer.

Hệ thống sử dụng Switch trung tâm để kết nối các phòng ban nhằm giúp quản lý mạng hiệu quả, tăng tính ổn định và hỗ trợ liên lạc nội bộ giữa các bộ phận.

Mô hình được chia VLAN để tăng bảo mật và hỗ trợ quản lý mạng dễ dàng hơn.

---

## Mô hình hệ thống

![Topology](topology.png)

---

## Mô hình mạng sử dụng

- Star Topology (Mạng hình sao)
- Switch đóng vai trò thiết bị trung tâm
- Router hỗ trợ định tuyến giữa các VLAN
- Access Point hỗ trợ kết nối WiFi

---

## Phân chia VLAN

| VLAN | Phòng ban | Dải IP |
|---|---|---|
| VLAN 10 | Văn phòng | 192.168.10.0/24 |
| VLAN 20 | Kế toán | 192.168.20.0/24 |
| VLAN 30 | Lãnh đạo | 192.168.30.0/24 |

---

## Thiết bị sử dụng

- Router Cisco 2811
- Switch Cisco 2950-24
- Server-PT
- PC-PT
- Access Point

---

## Chức năng hệ thống

- Kết nối các phòng ban trong UBND
- Chia VLAN để tăng bảo mật
- Hỗ trợ mạng không dây
- Quản lý hệ thống tập trung
- Liên lạc giữa các VLAN
- Hỗ trợ truy cập Server nội bộ

---

## Danh sách Server

| Server | Địa chỉ IP |
|---|---|
| Server tầng 1 | 192.168.10.200 |
| Server tầng 2 | 192.168.20.100 |
| Server tầng 3 | 192.168.30.100 |

---

## Kiểm tra hoạt động hệ thống

Có thể kiểm tra hoạt động của mô hình bằng các cách sau:

### 1. Kiểm tra kết nối giữa các máy tính

Sử dụng lệnh:

```bash
ping 192.168.10.2
```

Nếu xuất hiện phản hồi:

```text
Reply from ...
```

thì kết nối thành công.

---

### 2. Kiểm tra kết nối giữa các VLAN

Thực hiện ping giữa các phòng ban khác nhau:

- VLAN 10 → VLAN 20
- VLAN 20 → VLAN 30

Ví dụ:

```bash
ping 192.168.20.1
```

Nếu ping thành công nghĩa là Router đã định tuyến Inter-VLAN hoạt động đúng.

---

### 3. Kiểm tra Access Point

- Kết nối thiết bị vào WiFi
- Kiểm tra nhận địa chỉ IP
- Ping đến PC hoặc Server khác

---

### 4. Kiểm tra Server

Thực hiện ping đến Server:

```bash
ping 192.168.10.200
```

Nếu có phản hồi thì Server hoạt động bình thường.

---

## Kết quả đạt được

- Các thiết bị hoạt động ổn định
- Các VLAN hoạt động chính xác
- Kết nối giữa các phòng ban thành công
- Hệ thống WiFi hoạt động tốt
- Các Server phản hồi thành công

---

## File dự án

- DEMO.pkt

---

## Công nghệ sử dụng

- Cisco Packet Tracer
- VLAN
- Inter-VLAN Routing
- TCP/IP
- Wireless Network

---

## Tác giả

- Họ tên: KA KY WEO
- Lớp: DCT22
