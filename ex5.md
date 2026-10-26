
PHẦN 1. PHÂN TÍCH: CƠ CHẾ "GOOGLE SEARCH CỦA BẢNG TÍNH" (AUTOFILTER)
- Khái niệm & Cơ chế hoạt động:
  + AutoFilter trong Excel hoạt động giống như một công cụ tìm kiếm thu nhỏ (Google Search) cho từng cột dữ liệu. Khi kích hoạt bộ lọc, hệ thống sẽ quét qua toàn bộ các giá trị độc lập (unique values) trong cột và tạo ra danh sách tùy chọn cho phép người dùng chọn lọc hiển thị các dòng dữ liệu thỏa mãn điều kiện.
  + Cơ chế này giúp cô lập ngay lập tức các bản ghi vi phạm hoặc sự cố cần quan tâm trong hàng ngàn dòng nhật ký hệ thống mà không cần phải xóa hoặc di chuyển dữ liệu gốc.
- Ứng dụng trong báo cáo NetGuard:
  + Giúp chuyên gia an ninh mạng nhanh chóng lọc ra các loại mã độc cụ thể, mức độ nghiêm trọng (Critical, High, Medium, Low), hoặc các IP độc hại tấn công trong một khoảng thời gian nhất định từ nhật ký hệ thống khổng lồ.
PHẦN 2. TRIỂN KHAI: BÁO CÁO NETGUARD HOÀN CHỈNH
1. Xử lý dữ liệu Excel (Hàm VLOOKUP kết hợp TRIM):
   - Vấn đề thực tế: Dữ liệu mã độc từ bảng cảnh báo thô thường bị dính khoảng trắng thừa ở đầu hoặc cuối (trailing/leading spaces), khiến hàm VLOOKUP trả về lỗi #N/A dù mã nhìn có vẻ giống nhau.
   - Giải pháp khắc phục: Sử dụng hàm TRIM bọc bên ngoài giá trị dò tìm để làm sạch dữ liệu tự động trước khi đối chiếu sang "Cơ sở dữ liệu virus":
     + Công thức chuẩn: =VLOOKUP(TRIM(A2), 'CoSoDuLieuVirus'!A:B, 2, FALSE)
   - Kết quả: Kéo công thức xuống toàn bộ bảng "Nhật ký hệ thống", hệ thống tra cứu chính xác 100% tên mã độc tương ứng mà không bị ảnh hưởng bởi lỗi định dạng dữ liệu thô.
2. Quản lý tài liệu Word (Navigation Pane & Auto TOC):
   - Sử dụng Navigation Pane (Bật qua thẻ View -> Navigation Pane): Giúp quản lý cấu trúc báo cáo sự cố an ninh mạng một cách trực quan, cho phép kéo thả các đề mục để sắp xếp lại bố cục tài liệu dài trang dễ dàng.
   - Thiết lập Mục lục tự động (Auto TOC): 
     + Gán đúng nhãn Heading 1, Heading 2 cho các phần nội dung chính.
     + Vào thẻ References -> Table of Contents -> Chọn kiểu mục lục tự động. Khi tài liệu có sự thay đổi về số trang hoặc nội dung, chỉ cần nhấn Update Table để cập nhật lại toàn bộ số trang chính xác.
3. Trực quan hóa PowerPoint (Chiến lược phòng thủ 3 tầng):
   - Thiết kế sơ đồ phân cấp (Hierarchy Diagram) trình bày chiến lược phòng thủ 3 tầng (Tầng ngoại vi - Tầng mạng nội bộ - Tầng dữ liệu cốt lõi).
   - Quy định trình bày: Tuyệt đối không sử dụng font Times New Roman, thay thế bằng các font chữ hiện đại, không chân như Montserrat hoặc Inter để đảm bảo hiển thị rõ ràng, sắc nét khi chiếu lên màn hình lớn (Projector) trong các buổi họp kỹ thuật.
