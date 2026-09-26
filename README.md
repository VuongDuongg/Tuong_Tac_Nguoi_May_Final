# 🏥 HOSPITAL-ÔII - HỆ THỐNG QUẢN LÝ BỆNH VIỆN TÍCH HỢP

> **Dự án Môn học:** Tương tác Người - Máy (Human - Computer Interaction)  
> **Nhóm thực hiện:** Nhóm 01 (N01)  
> **Figma Design:** [Figma - N01_Hospital UI/UX](https://www.figma.com/design/dH8AxTiu2LHHLm8BEGjr4e/N01_Hospital?node-id=0-1&t=v896ZQQKmVKzyFga-1)

---

## 📌 Giới thiệu dự án

**HOSPITAL-ÔII** là hệ thống quản lý bệnh viện số hóa toàn diện, hỗ trợ quản lý quy trình khám chữa bệnh khép kín từ tiếp nhận bệnh nhân, khám chẩn đoán, xét nghiệm/chỉ định cận lâm sàng, kê đơn, thanh toán viện phí đến quản trị hệ thống và hỗ trợ người bệnh đặt lịch trực tuyến.

Dự án được xây dựng dựa trên nghiên cứu trải nghiệm người dùng (UX) và thiết kế giao diện (UI) hiện đại, trực quan, đảm bảo tính nhất quán và tối ưu thao tác cho từng nhóm đối tượng người dùng chuyên biệt.

---

## 🎨 Thiết kế Figma (UI/UX Prototype)

Toàn bộ luồng nghiệp vụ, hệ thống phân cấp màu sắc, typography và tương tác người máy được thiết kế chi tiết trên Figma:
* 🔗 **Figma Workspace:** [N01_Hospital Prototype & Design Specs](https://www.figma.com/design/dH8AxTiu2LHHLm8BEGjr4e/N01_Hospital?node-id=0-1&t=v896ZQQKmVKzyFga-1)

---

## 👥 Các phân hệ & Chức năng chính

Hệ thống được chia thành **5 phân hệ cốt lõi** phục vụ đầy đủ các vai trò:

### 1. 🌐 Phân hệ Người Dùng / Bệnh Nhân (`NguoiDung/`)
* **Trang chủ (`Trangchu/Menu.html`)**: Cung cấp thông tin bệnh viện, chuyên khoa, bảng giá dịch vụ và tin tức y tế.
* **Đặt lịch khám (`Datlichkham/booking.html`)**: Chọn chuyên khoa, chọn bác sĩ phụ trách, chọn khung giờ/ngày khám thuận tiện.
* **Lịch hẹn của tôi (`Lichhencuatoi/index.html`)**: Theo dõi lịch sử đặt khám, trạng thái lịch hẹn và nhận mã số phiếu hẹn.

### 2. 📋 Phân hệ Tiếp Tân (`TiepTan/index.html`)
* Tiếp nhận bệnh nhân tại quầy, check-in theo mã hẹn hoặc tiếp nhận bệnh nhân mới.
* Quản lý hồ sơ bệnh nhân, phân luồng phòng khám và cấp số thứ tự tự động.
* Cập nhật thông tin bảo hiểm y tế (BHYT) và thông tin cá nhân.

### 3. 👨‍⚕️ Phân hệ Bác Sĩ - EMR (`BacSi/index.html`)
* Hồ sơ bệnh án điện tử (Electronic Medical Record - EMR).
* Danh sách hàng đợi khám theo thời gian thực (Chờ khám, Đang khám, Chờ kết quả, Đã có KQ, Đã khám).
* Nhập kết quả khám lâm sàng, chỉ định xét nghiệm/chẩn đoán hình ảnh và kê đơn thuốc.

### 4. 💳 Phân hệ Thu Ngân - Tất Toán Viện Phí (`ThuNgan/index.html`)
* Tra cứu danh sách viện phí cần thanh toán của bệnh nhân.
* Bóc tách chi phí viện phí, khấu trừ BHYT và các khoản đồng chi trả.
* Hỗ trợ đa dạng phương thức thanh toán (Tiền mặt, Chuyển khoản QR code, Thẻ ngân hàng).
* Xuất hóa đơn và lịch sử thanh toán minh bạch.

### 5. 🛡️ Phân hệ Quản Trị Viên (`Admin/`)
* **Bảng điều khiển (`dashboard.html`)**: Thống kê số lượng bệnh nhân, doanh thu, tải trọng phòng khám và biểu đồ tổng quan.
* **Quản lý tài khoản (`account-management.html`)**: Phân quyền tài khoản y bác sĩ, nhân viên tiếp tân, thu ngân.
* **Quản lý vai trò & quyền hạn (`roles-permissions.html`)**: Ma trận phân quyền chi tiết (RBAC).
* **Quản lý sự cố & nhật ký hệ thống (`incident-management.html`)**: Theo dõi audit log và xử lý xung đột/sự cố vận hành.

---

## 🛠️ Công nghệ sử dụng

* **Frontend:** HTML5, CSS3, JavaScript (ES6+)
* **Framework & UI Libraries:** Tailwind CSS, Bootstrap 5, FontAwesome Icons, Bootstrap Icons
* **Thiết kế UI/UX:** Figma (Auto Layout, Component Variant, Interactive Prototyping)
* **Font chữ chuẩn:** `Inter`, `Segoe UI`, `Roboto`

---

## 📂 Cấu trúc thư mục dự án

```text
├── Admin/                     # Phân hệ Quản trị hệ thống
│   ├── account-management.html
│   ├── dashboard.html
│   ├── incident-management.html
│   └── roles-permissions.html
├── BacSi/                     # Phân hệ Bác sĩ khám bệnh (EMR)
│   └── index.html
├── NguoiDung/                 # Phân hệ Bệnh nhân / Khách hàng
│   ├── Datlichkham/
│   │   ├── booking.css
│   │   └── booking.html
│   ├── Lichhencuatoi/
│   │   ├── index.html
│   │   └── style.css
│   └── Trangchu/
│       ├── Menu.html
│       └── style.css
├── ThuNgan/                   # Phân hệ Thu ngân & Tất toán viện phí
│   └── index.html
├── TiepTan/                   # Phân hệ Tiếp đón & Phân luồng tiếp tân
│   └── index.html
└── README.md
```

---

## 🚀 Hướng dẫn chạy dự án

1. **Clone repository về máy:**
   ```bash
   git clone https://github.com/VuongDuongg/Tuong_Tac_Nguoi_May_Final.git
   cd Tuong_Tac_Nguoi_May_Final
   ```

2. **Chạy ứng dụng:**
   * Dự án là Web tĩnh thuần (Pure HTML/CSS/JS), không yêu cầu cài đặt môi trường backend phức tạp.
   * Bạn có thể mở trực tiếp bất kỳ file `.html` nào bằng trình duyệt web (Chrome, Edge, Firefox,...).
   * Khuyến nghị: Dùng tiện ích mở rộng **Live Server** trong VS Code để có trải nghiệm reload tự động tốt nhất:
     * Nhấp chuột phải vào file `.html` (ví dụ `NguoiDung/Trangchu/Menu.html` hoặc `Admin/dashboard.html`)
     * Chọn **"Open with Live Server"**.

---

## 📝 Đánh giá nguyên lý Tương tác Người - Máy (HCI)

Dự án áp dụng chặt chẽ các nguyên lý thiết kế tương tác:
* **Tính nhất quán (Consistency):** Đồng bộ màu sắc thương hiệu `#0A369D` / `#1A56DB`, kiểu dáng nút, typography trên toàn bộ các phân hệ.
* **Phản hồi người dùng (Feedback):** Trạng thái tương tác rõ ràng qua Hover, Focus, Active, thông báo Toast và Modals xác nhận.
* **Phòng ngừa lỗi (Error Prevention):** Kiểm tra form nhập liệu, cảnh báo trước khi hủy lịch hoặc xác nhận tất toán viện phí.
* **Giảm tải nhận thức (Cognitive Load Reduction):** Giao diện phân cấp thông tin rõ ràng, hỗ trợ tìm kiếm nhanh, lọc trạng thái trực quan bằng mã màu.
