# hotel-management
# Hotel Management System (HMS) - Business Analysis & System Design

> **Dự án:** Phân tích và Thiết kế Hệ thống Quản lý Đặt phòng Khách sạn & Dịch vụ
> **Vai trò:** Business Analyst (BA) & Quản trị Yêu cầu  
> **Thời gian:** 05/2026 – 08/2026  
> **Tác giả:** Trần Thị Điệp (Đại học Thăng Long)
---

## 1. Tổng quan dự án (Project Overview)
Hệ thống Quản lý Khách sạn (HMS) được thiết kế nhằm số hóa và tối ưu hóa toàn bộ quy trình vận hành buồng phòng, dịch vụ lưu trú và quản lý khách hàng cho khách sạn vừa và nhỏ. Dự án giải quyết các vấn đề tồn đọng từ quy trình thủ công: chậm trễ cập nhật trạng thái phòng, rủi ro trùng lịch (overbooking), thất thoát doanh thu và thời gian làm thủ tục nhận/trả phòng kéo dài.

### Mục tiêu chính:
- **Tự động hóa luồng vận hành:** Đồng bộ hóa quy trình Check-in, Check-out, đổi phòng và thanh toán theo thời gian thực.
- **Tối ưu hóa quản lý buồng phòng:** Trực quan hóa sơ đồ trạng thái phòng (Trống, Đang ở, Đang dọn dẹp, Bảo trì).
- **Chuẩn hóa dữ liệu khách lưu trú:** Quản lý lịch sử đặt phòng, thông tin khách hàng và xuất hóa đơn minh bạch.

---
##2. Vai trò & Trách nhiệm (My Role as a Business Analyst)

- **Khảo sát & Thu thập yêu cầu:** Tiếp cận nghiệp vụ thực tế ngành Khách sạn, phân loại yêu cầu chức năng và phi chức năng .
- **Phân tích & Đặc tả yêu cầu phần mềm:** 
  - Soạn thảo tài liệu đặc tả yêu cầu phần mềm (**SRS**) chi tiết.
  - Xây dựng danh sách **15+ User Stories** kèm tiêu chí nghiệm thu rõ ràng (**Acceptance Criteria - AC**).
  - Viết kịch bản ca sử dụng chi tiết (**Use Case Specifications**) cho các luồng: tra cứu phòng trống, đặt phòng, nhận/trả phòng và xử lý hủy lịch.
- **Mô hình hóa quy trình & Luồng nghiệp vụ (Diagrams):**
  - **Use Case Diagram:** Xác định ranh giới hệ thống và phân quyền tác nhân (Khách hàng, Lễ tân, Quản lý).
  - **Business Flow & Activity Diagram (BPMN):** Chuẩn hóa quy trình vận hành Check-in, Check-out, đổi phòng và thanh toán theo dạng làn bơi (Swimlane).
  - **Sequence Diagram:** Mô tả trực quan luồng trao đổi thông tin giữa Giao diện người dùng (UI) và Máy chủ xử lý dữ liệu.
- **Thiết kế Giao diện mẫu (UI/UX Prototype):**
---

## 🔗 3. Liên kết tài nguyên (Project Artifacts & Demos)
-  **Figma Interactive Prototype:** [Trải nghiệm giao diện tương tác trên Figma](https://www.figma.com/proto/xxxx) *(Thay link của bạn)*
-  **Draw.io Diagrams Workspace:** [Xem chi tiết các sơ đồ quy trình nghiệp vụ](https://app.diagrams.net/xxxx) *(Thay link của bạn)*
-  **Tài liệu SRS chi tiết (PDF):** [Xem file đặc tả SRS trong thư mục docs/](docs/SRS_Hotel_Management_System.pdf)
-  **Bộ kịch bản Test Case & UAT:** [Xem bảng kịch bản kiểm thử](docs/TestCases_and_UAT_Checklist.xlsx)

---

## 👥 4. Phân quyền & Tác nhân hệ thống (System Actors)
- **Khách hàng (Customer):** Tra cứu phòng trống, xem biểu phí dịch vụ, yêu cầu đặt/hủy phòng.
- **Lễ tân (Receptionist):** Tiếp nhận đặt phòng, thực hiện Check-in / Check-out, cập nhật dịch vụ phát sinh, in hóa đơn.
- **Quản lý khách sạn (Admin/Manager):** Cấu hình danh mục phòng/giá dịch vụ, phân quyền tài khoản, theo dõi báo cáo công suất và doanh thu.
- 
---

## 5. Phân tích & Thiết kế Hệ thống (Analysis & Diagrams)

### 5.1. Sơ đồ Ca sử dụng tổng quan (Use Case Diagram)
Mô tả phạm vi chức năng và sự tương tác giữa các tác nhân với hệ thống:
![Use Case Diagram](diagrams/use-case-diagram.png)

### 5.2. Luồng quy trình nghiệp vụ chính (Business Flows & Activity Diagram)
Chuẩn hóa luồng Check-in, Check-out và xử lý thanh toán:
![Check-in & Check-out Flow](diagrams/activity-diagram-booking-flow.png)

---

##  7. Cấu trúc thư mục kho lưu trữ (Repository Structure)

```text
hotel-management-system/
│
├── docs/                                # Tài liệu đặc tả & kiểm thử
│   ├── SRS_Hotel_Management_System.pdf  # Đặc tả yêu cầu phần mềm chi tiết
│   └── TestCases_and_UAT_Checklist.xlsx # Kịch bản kiểm thử nghiệp vụ
│
├── diagrams/                            # Sơ đồ phân tích & luồng xử lý
│   ├── use-case-diagram.png             # Sơ đồ tổng quan ca sử dụng
│   ├── activity-diagram-booking.png     # Quy trình đặt phòng & check-in
│   ├── sequence-diagram-payment.png     # Sơ đồ tuần tự xử lý thanh toán
│   └── erd-database-schema.png          # Lược đồ cơ sở dữ liệu quan hệ
│
├── design/                              # Khung giao diện UI/UX
│   ├── wireframes/                      # Ảnh chụp màn hình wireframe
│   └── README.md                        # Link Figma Prototype tương tác
│
├── sql/                                 # Lược đồ và truy vấn CSDL
│   ├── schema_tables.sql                # File DDL tạo bảng và ràng buộc khóa
│   └── sample_queries.sql               # File truy vấn đối soát dữ liệu & báo cáo
│
└── README.md                            # Tài liệu giới thiệu dự án
