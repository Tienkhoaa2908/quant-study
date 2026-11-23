# Finance — Quant Learning

Nền tảng tự học tài chính bằng tiếng Việt, có bản tiếng Anh, hướng quant trader/developer và năng lực nghiên cứu. Repository: https://github.com/Tienkhoaa2908/quant-study.

**Website:** https://finance-tienkhoaa2908.vercel.app · [Bài P&L](https://finance-tienkhoaa2908.vercel.app/finance/pnl)

## Hệ thống hiện tại

- 36 bài học trong 9 nhóm: tài chính, toán/xác suất, Python/dữ liệu, nghiên cứu chiến lược, thống kê, stock/FX/crypto, phái sinh, hệ thống giao dịch, danh mục.
- Mỗi bài có tổng quan, mục đích, ứng dụng; nội dung chia bước với 108 bài tập, gợi ý, lời giải và nguồn đọc theo mục. Tiêu đề gọi đúng chủ đề, văn phong Việt được biên tập trực tiếp.
- Lộ trình có tiên quyết, tìm kiếm và chuyển VI/EN. Bản nháp, tự đánh giá, lịch ôn và checklist dự án lưu ở trình duyệt; xuất/nhập JSON để sao lưu.
- Lab tương tác: P&L, lợi suất tích lũy và backtest có chi phí. Sáu dự án có mã Python chạy được với dữ liệu mô phỏng, kèm yêu cầu mở rộng.
- Thư viện nguồn miễn phí và 5 nguồn dữ liệu có mô tả phạm vi sử dụng. Thư viện toán gốc vẫn là phần bổ sung, không đổi nhãn thành bài tài chính.

Các bài tập tự luận được người học tự đối chiếu, không chấm bằng AI. Kiểm tra số chỉ xác nhận kết quả trong dung sai, không chấm lập luận. Mã dự án là nền thực hành cần mở rộng, không phải hệ thống giao dịch tiền thật. Giáo trình lõi không thay thế mọi chuyên môn quant nâng cao.

## Chạy trên máy

Node.js 24+, npm và Python 3.13+ để chạy dự án thực hành.

~~~sh
npm ci
npm run dev
npm run finance:audit
npm test
npm run build
npm start
~~~

Ứng dụng học tài chính hoạt động không cần biến môi trường, database hay đăng nhập. Các API đồng bộ và OAuth kế thừa là tùy chọn, chưa được dùng cho tiến độ tài chính. Nếu cấu hình, dùng .env.example và tài khoản riêng; không dùng dịch vụ của upstream.

~~~sh
TEST_BASE_URL=http://localhost:3000 npm run test:e2e
python public/projects/ledger.py
~~~

Trên PowerShell đặt biến bằng $env:TEST_BASE_URL='http://localhost:3000'. Bộ E2E finance ở tests/e2e; bộ UI toán cũ được giữ riêng ở tests/legacy-e2e để tham khảo. Kiểm thử logic và audit render toán cũ vẫn chạy.

## Kiến trúc và nội dung

Next.js App Router, React, TypeScript; KaTeX/Markdown cho nội dung. Schema ở lib/finance-types.ts; nội dung ở content/finance; state ở lib/finance-progress.ts và components/finance-state.tsx. Mỗi thay đổi nội dung phải qua finance:audit: cấu trúc, tiên quyết, công thức song ngữ và render. Đây là kiểm tra kỹ thuật, không chứng nhận đúng khoa học hoặc hiệu quả học.

Xem [thiết kế và biên tập](docs/finance-rebuild.md), [nghiên cứu nghề nghiệp](docs/research/quant-competencies.md), [bằng chứng sư phạm](docs/research/pedagogy-evidence.md), [danh mục nguồn](docs/research/source-catalog.md) và [audit upstream](docs/research/upstream-audit.md).

## Nguồn gốc

[UPSTREAM.md](UPSTREAM.md) ghi nhận And I Wonder và tác giả gốc; [README nguyên bản](docs/upstream/README.md) giữ ngữ cảnh lịch sử. Lịch sử Git riêng không biến code kế thừa thành sáng tác ban đầu của người nhập.
