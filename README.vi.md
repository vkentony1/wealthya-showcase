# Wealthya (bản tóm tắt tiếng Việt)

**Nền tảng quản lý tài sản có hỗ trợ AI: ứng dụng web và di động, ưu tiên chạy cục bộ, giúp tổ chức thông tin tài chính, theo dõi danh mục và hỗ trợ con người ra quyết định.**

[English README](README.md) · [Case study 2 phút](docs/portfolio-summary.md) · [Quyết định sản phẩm](docs/product-decisions.md) · [Trạng thái và lộ trình](docs/status-and-roadmap.md)

> **Trong một phút:** tôi xác định một bài toán thật của chủ tài sản, chuyển thành quy trình sản phẩm, điều phối AI thực hiện phần triển khai và rà soát kết quả. Wealthya chỉ hỗ trợ quyết định; ứng dụng không đặt lệnh hay giao dịch.

## Tóm tắt

| | |
|---|---|
| **Bài toán** | Hồ sơ tài sản, dữ liệu thị trường và các câu hỏi cần điều tra nằm rải rác, nên mỗi quyết định đều bắt đầu bằng việc ghép lại bức tranh. |
| **Đã xây** | Ứng dụng web/PWA, ứng dụng gốc SwiftUI cho iPhone và Mac, cùng API tách biệt theo từng tenant. |
| **Vai trò của tôi** | Chủ sản phẩm và người thiết kế hệ thống. Công cụ AI thực hiện phần triển khai theo đặc tả và sự rà soát của tôi. |
| **Ranh giới cứng** | Chỉ hỗ trợ quyết định. Không có chức năng giao dịch hay đặt lệnh. |
| **Giai đoạn** | Riêng tư, chưa ra mắt. Không tuyên bố người dùng, doanh thu hay hiệu quả đầu tư. |

## Vai trò của tôi

- Xác định bài toán và yêu cầu sản phẩm.
- Thiết kế quy trình và hệ thống.
- Chuyển yêu cầu kinh doanh thành hành vi phần mềm.
- Điều phối triển khai có AI hỗ trợ và rà soát đầu ra.
- Kiểm thử, lặp lại, ưu tiên và ra quyết định sản phẩm.

Tôi không tự viết toàn bộ mã nguồn và không định vị mình là kỹ sư phần mềm truyền thống. Giá trị tôi mang lại là biến một bài toán kinh doanh thật thành phần mềm chạy được, với cách dùng AI có kỷ luật.

## Điểm nổi bật về tư duy sản phẩm

- **Chỉ thông tin, không hành động:** không có chức năng giao dịch.
- **Con số xác định, AI ở rìa:** số liệu chính thức đến từ mã đã kiểm thử, không phải từ mô hình AI.
- **Mọi con số đều có nguồn:** hiển thị nhà cung cấp, thời điểm quan sát và độ mới.
- **Chặn cổng trước khi ra mắt:** xác thực, cách ly dữ liệu, xoá dữ liệu và bản quyền dữ liệu phải đạt trước khi phát hành.

Lý do và đánh đổi của từng quyết định nằm trong [Quyết định sản phẩm](docs/product-decisions.md) (tiếng Anh).

## Bản công khai này thể hiện điều gì

- Biến bài toán kinh doanh thật thành sản phẩm công nghệ chạy được.
- Tư duy sản phẩm và hệ thống, từ dữ liệu đến quy trình và quyết định của con người.
- Dùng công cụ AI hiện đại để xây dựng và lặp lại, không chỉ dừng ở viết prompt.
- Học nhanh ở các lĩnh vực kỹ thuật mới: web, ứng dụng gốc, dữ liệu, thiết kế API.
- Rà soát có kỷ luật thay vì chấp nhận đầu ra do AI tạo ra một cách mù quáng.
- Thẳng thắn về phạm vi: nói rõ phần chưa xong và điều sản phẩm từ chối làm.

## Quyền riêng tư

Bản công khai không chứa mã nguồn riêng tư, cấu hình vận hành hay dữ liệu tài chính thật. Đây là một quyết định kỹ thuật có chủ đích. Dữ liệu mẫu trong [sample-data](sample-data/) hoàn toàn là dữ liệu giả.

*Bản portfolio công khai: mã nguồn sản xuất và mã nguồn riêng tư được loại trừ có chủ đích.*
