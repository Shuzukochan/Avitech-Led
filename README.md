# Avitech-Led

Mạch LED Driver/Indicator nhỏ gọn được thiết kế bằng **KiCad**. Dự án đã được đóng gói thư viện cục bộ (Self-contained / Portable), có thể mở và xem mô hình 3D trên bất kỳ máy tính nào mà không lo thiếu thư viện hay lỗi missing footprint/symbol/3D model.

## 📌 Thông số & Cấu trúc phần cứng

- **Phần mềm thiết kế**: KiCad (tương thích KiCad 8.x / 9.x / 10.x)
- **Linh kiện chính**:
  - `D1, D2`: LED SMD 2835 (`LED_SMD:LED_PLCC_2835`)
  - `R1, R2`: Điện trở 100Ω SMD 0805 (`Resistor_SMD:R_0805_2012Metric`)
  - `TP1, TP2`: Test Points Pad 2.0x2.0mm
  - `H1, H2`: Lỗ bắt ốc M3 (3.2mm)
- **Kích thước**: Mạch nhỏ gọn, 2 lớp (Top & Bottom Copper)

## 📁 Cấu trúc thư mục dự án

```text
Avitech-Led/
├── Avitech-Led.kicad_pro     # File cấu hình dự án KiCad
├── Avitech-Led.kicad_sch     # Sơ đồ nguyên lý (Schematic)
├── Avitech-Led.kicad_pcb     # Thiết kế mạch in (PCB Layout)
├── sym-lib-table             # Bảng quản lý Symbol cục bộ
├── fp-lib-table              # Bảng quản lý Footprint cục bộ
├── .gitignore                # Danh sách loại trừ file tạm của KiCad
├── README.md                 # Tài liệu dự án
└── libs/                     # Thư viện dùng riêng cho dự án
    ├── Avitech-Led.kicad_sym # Thư viện Symbol cục bộ
    ├── Avitech-Led.pretty/   # Thư viện Footprint cục bộ
    └── 3dmodels/             # Toàn bộ mô hình 3D (.step)
```

## 🚀 Hướng dẫn mở dự án trên máy khác

1. Tải hoặc `git clone` dự án về máy:
   ```bash
   git clone https://github.com/Shuzukochan/Avitech-Led.git
   ```
2. Khởi động KiCad, chọn **File > Open Project...**
3. Mở file `Avitech-Led.kicad_pro`.
4. Mọi linh kiện, footprint và mô hình 3D sẽ tự động load qua biến `${KIPRJMOD}` mà không cần cấu hình thêm bất kỳ đường dẫn nào!
