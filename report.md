# Basic design

## Structure folder

```
HOUSECAN/
├── docs/
│   ├── overview/
│   │   ├── README.md                       # Giới thiệu tổng quan về dự án
│   │   └── changelog.md                    # Nhật ký thay đổi của tài liệu/dự án
│   ├── design/
│   │   ├── architecture.md                 # Kiến trúc hệ thống
│   │   ├── database.md                     # Thiết kế cơ sở dữ liệu
│   │   └── ui-ux.md                        # Thiết kế giao diện người dùng
│   ├── screens/
│   │   ├── FE001/
│   │   │   ├── images/
│   │   │   │   ├── mockup_img.jpg          # Hình ảnh mockup của màn hình FE001
│   │   │   ├── README.md                   # Mô tả chi tiết màn hình FE001
│   │   │   └── flow.md                     # Luồng hoạt động của màn hình
│   │   ├── FE002/
│   │   │   ├── README.md                   # Mô tả chi tiết màn hình FE002
│   │   │   └── flow.md                     # Luồng hoạt động của màn hình
│   │   └── ...                             # Các thư mục màn hình khác (FE003, FE004, ...)
│   ├── development/
│   │   ├── setup.md                        # Hướng dẫn cài đặt môi trường
│   │   ├── coding-guidelines.md            # Quy tắc viết code
│   │   └── api-reference.md                # Tài liệu tham khảo API
│   ├── testing/
│   │   ├── test-plan.md                    # Kế hoạch kiểm thử
│   │   └── test-cases.md                   # Các trường hợp kiểm thử
│   ├── deployment/
│   │   ├── deployment-guide.md             # Hướng dẫn triển khai
│   │   └── infrastructure.md               # Cấu hình cơ sở hạ tầng
├── README.md                               # Giới thiệu tổng quan về dự án và cách sử dụng thư mục
└── LICENSE.md                              # Thông tin giấy phép (nếu cần)
```

## Prompting 

```
Prompt CREATE – Generate Basic Design (10 sections) + Evaluation & Next Action

C – Context: 
- Bạn nhận được URL hoặc file giao diện màn hình (Figma/HTML/URL). 
- Nhiệm vụ là phân tích UI và tạo tài liệu Basic Design gồm 10 hạng mục chuẩn công ty để phục vụ Dev/QA/AI.
- Mô tả chi tiết nghiệp vụ của màn hình: 
  [context]

R – Role: 
- Bạn là Business Designer + System Analyst, am hiểu UI/UX, phân tích hệ thống, có khả năng viết tài liệu chuẩn hóa để AI, Dev, QA đều sử dụng được. 
- Source: ảnh đính kèm

E – Expectation: 
• Xuất 01 file Markdown duy nhất, theo format chuẩn công ty với 10 hạng mục: 
1. Business Purpose 
2. Target Role 
3. Screen Layout (Figma URL + Screenshot placeholder) 
4. User Flow / 操作フロー 
5. Initial Load Behavior (On Page Load) 
6. UI Field Spec (gộp nội dung của Simplified Table & Extended Table thành 1 bảng, bao gồm cả placeholder)
7. Trigger & Event Mapping (chi tiết cả Frontend validation + Backend processing + Response handling) 
8. Security Control / セキュリティ制御 
9. Message / Error Handling (có MessageID, JP/EN, dùng chung được cho màn hình khác) 
10. Other Notes / Additional Logic: Liệt kê những spec yêu cầu khác nằm ngoài 10 mục nhưng lưu ý cần cho nghiệp vụ trang này. 
  • Giữ nguyên thuật ngữ tiếng Nhật quan trọng như: メッセージ, エラー, セキュリティ制御. 
  • Nếu thiếu thông tin: ghi TBD và mô tả assumption. Tham khảo template đính kèm

A – Action: 
1. Phân tích DOM để liệt kê field, control, event (nút bấm, select, link, pagination…). 
2. Nếu là Figma: đọc tên component để suy ra field/event. 
3. Đề xuất MaxLength, DefaultValue, Display Format nếu không lấy được từ UI (đánh dấu assumed). 
4. Đặt placeholder ảnh: 
5. ![ScreenShot](./images/[screen_id].png) 
6. Liệt kê Event Detail rõ ràng theo thứ tự: 
o Validation (liệt kê các use-cases có thể xảy ra đối với nghiệp vụ của màn hình này)
o Backend Logic 
o Response Handling

T – Tone: 
Ngắn gọn, rõ ràng, có tính kỹ thuật, dễ đọc cho cả Dev, QA, AI.

E – Extra constraints: 
• Output duy nhất là Markdown, không kèm giải thích thêm ngoài nội dung BD. 
• Mỗi bảng phải có header rõ ràng. 
• Ghi chú assumption nếu không xác định được từ UI. 
• Dùng tiếng Anh cho nội dung chính, giữ JP cho thuật ngữ hệ thống.

V – Evaluation (Kiểm tra kết quả): 
Sau khi tạo tài liệu BD, tự đánh giá: 
• ✅ Có đủ 10 hạng mục không? 
• ✅ Có giữ nguyên JP term? 
• ✅ Mỗi bảng có đầy đủ header và dữ liệu hợp lý? 
• ✅ Có placeholder screenshot đúng format? 
• ✅ Có ghi chú assumption rõ ràng? 
• ✅ Event flow có phân tách rõ Frontend/Backend?

N – Next Action (Hành động tiếp theo): 
• Nếu thiếu dữ liệu từ UI → yêu cầu Designer/Dev bổ sung. 
• Nếu format chưa đúng → chỉnh lại theo template chuẩn công ty. 
• Nếu logic chưa rõ → làm việc với BA/PM để xác nhận. 
• Lưu file .md vào repo tài liệu dự án. 
• Tích hợp vào pipeline AI để tái sử dụng cho các bước Dev/QA/TestCase.
```

## Guidelines
