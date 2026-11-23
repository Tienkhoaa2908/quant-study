# Thiết kế hệ thống Finance

Ngày 23/11/2026. Hướng chính: quant trader/developer có nền toán, tài chính và nghiên cứu; stock, crypto, forex. Người học có toán/Python căn bản, chưa học tài chính. Nguồn bắt buộc miễn phí hợp pháp.

## Quyết định mới nhất của người học

Triển khai hệ thống đầy đủ, không dừng ở pilot. Bỏ diễn giải vòng vo; viết tiếng Việt trực tiếp, tự nhiên. Tên bài là chủ đề, ví dụ P&L. Trước nội dung luôn có: học gì, để làm gì, ví dụ trong hệ thống giao dịch. Chia bước ngắn để đọc nhưng không cắt mất giả định, định nghĩa hoặc lập luận cần thiết. Có nút VI/EN.

## Các phần đã xây

36 bài, 108 phần nội dung và 108 bài tập trong 9 nhóm. Nguồn chính xác ở từng bài; sơ đồ tiên quyết được kiểm tra không có chu trình. Mỗi bài tập có gợi ý và lời giải; một số có kiểm tra kết quả số. Không khóa người học ở một bài vì chưa đánh dấu hoàn thành.

Các route chính: / (tổng quan), /path (lộ trình và tìm bài), /finance/[id] (reader), /daily (ôn và sao lưu), /resources (học liệu/dữ liệu), /projects (6 dự án), /lab (3 công cụ). /mathematics và các route bài toán ngày cũ là thư viện bổ sung có nguồn gốc riêng.

Mã Python tải trực tiếp từ public/projects. Các chương trình dùng thư viện chuẩn, dữ liệu mô phỏng và assertions. Checklist mô tả phần người học cần xây tiếp; tải mã không tự hoàn thành dự án. Capstone ghép data, tín hiệu, risk, execution, ledger và monitoring trong mô phỏng/paper trading.

## Biên tập tiếng Việt và kiểm tra ngôn ngữ

Viết nội dung từ khái niệm và tình huống trước, rồi đối chiếu bản Anh. Mỗi đoạn trả lời một câu hỏi cụ thể. Thuật ngữ chuyên ngành được giữ khi hữu ích và giải thích trong ngữ cảnh; không thay bằng ẩn dụ. Đơn vị, điều kiện, phủ định và ký hiệu phải giữ nguyên khi biên tập.

Bộ xử lý Markdown chỉ nhận công thức được đánh dấu rõ; không tự suy đoán một cặp tiền, ID hoặc câu tiếng Việt là toán. Lint kiểm văn bản rỗng, câu lặp liền nhau, escape lỗi, công thức VI/EN và KaTeX. Nó không tự đánh giá mức tự nhiên của tiếng Việt. Không có mô hình NLP/LLM bên ngoài hoặc chi phí inference ngầm; phần văn phong hiện được biên tập, không gắn nhãn là dịch máy đã qua model.

## Sư phạm

Tổng quan → khái niệm/giả định → suy ra công thức hoặc cơ chế → ví dụ → câu hỏi → gợi ý/lời giải → tự đối chiếu → ứng dụng/dự án. Độ dài tùy nội dung, không lấy số từ làm chuẩn chất lượng. Bước suy luận cần thiết phải có; phần phụ nằm ở nguồn đọc thêm. Bằng chứng nghiên cứu và giới hạn được giữ ở docs/research/pedagogy-evidence.md.

Lịch ôn là heuristic từ tự đánh giá: cần ôn lại sau 1 ngày; tự làm được tăng khoảng ôn đến tối đa 30 ngày. Lượt ôn mới cần cập nhật câu trả lời và đánh giá lại. Hoàn thành không phải điểm thành thạo; bấm nhiều lần không tăng khoảng ôn. Chưa đo hiệu quả trên người học theo thời gian.

## Tiến độ và dữ liệu

Tiến độ tài chính ở localStorage, phiên bản schema 1. Có bản nháp, đánh giá từng bài tập, lịch ôn, checklist; JSON import được kiểm cấu trúc/kích thước. Có nhận cập nhật từ tab khác và đọc lại trước khi ghi; đồng thời sửa cùng trường vẫn theo bản ghi cuối. Khi storage lỗi, giữ state phiên làm việc và hiện cách xuất bản sao. Không tự đồng bộ cloud hoặc hứa giữ dữ liệu nếu trình duyệt xóa storage.

Nguồn dữ liệu ở content/finance/datasets.ts: French, ALFRED, ECB, SEC EDGAR, Binance public data. Đây là liên kết/định hướng sử dụng; không lưu toàn bộ sách hoặc dataset trong repo. Truy cập miễn phí khác quyền phân phối. Dữ liệu tổng hợp/tham chiếu không dùng như giá khớp; vintage và thời điểm biết dữ liệu là một phần bài học.

## Phạm vi nâng cao

Giáo trình lõi kết nối các năng lực để làm dự án. Các chuyên môn như chứng minh giải tích ngẫu nhiên, định giá nhiều chiều, HFT và DeFi chuyên sâu cần tiếp tục đọc tài liệu chuyên ngành và làm nghiên cứu riêng. Thư viện toán kế thừa hỗ trợ mở rộng nền tảng; không tuyên bố một bài nhập môn thay thế cả môn học hoặc bảo đảm năng lực nghề nghiệp.

## Git và triển khai

Repo hiện hành: Tienkhoaa2908/quant-study. Main đã có lịch sử riêng từ da93ea8; attribution trong UPSTREAM.md. Không merge lịch sử gốc trở lại và không push repo upstream. Deployment dùng CLI máy dưới đúng tài khoản; không dùng plugin tài khoản khác. Site finance không cần MongoDB/OAuth để học; cấu hình dịch vụ bổ sung là việc riêng.
