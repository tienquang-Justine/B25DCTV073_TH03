## Thông tin sinh viên
1. Họ và tên: Nguyễn Quang Tiến
2. Mã sinh viên: B25DCTV073

## Hướng dẫn chạy dự án

**Phần A**
1. Mở terminal, di chuyển vào thư mục: `cd part-a-class`
2. Cài đặt các gói phụ thuộc: `npm install`
3. Khởi động ứng dụng: `npm start` (hoặc `npm run dev` nếu dùng Vite)

**Phần B**
1. Mở terminal, di chuyển vào thư mục: `cd ../part-b-hooks`
2. Cài đặt các gói phụ thuộc: `npm install`
3. Khởi động ứng dụng: `npm start` (hoặc `npm run dev` nếu dùng Vite)

## Trả lời câu hỏi
Hooks đã giúp khắc phục các thách thức của Class ở những chỗ nào trong bài?"

1. Gom nhóm logic (useEffect vs Lifecycle): Trong Class (Phần A), việc quản lý đồng hồ phải chia ra 2 nơi là componentDidMount (bật) và componentWillUnmount (tắt). Với Hooks, useEffect gom chung thao tác bật/tắt vào cùng một block code, dễ đọc và tránh quên dọn dẹp bộ nhớ.
2. Tái sử dụng code (Custom Hook): Lấy dữ liệu API được tách riêng ra thành useFetch. Nếu có nhiều component khác cần gọi API, chỉ cần gọi lại hook này thay vì phải viết lại logic fetch/loading/error lặp đi lặp lại như Class.
3. Ngắn gọn hơn: Loại bỏ hoàn toàn từ khóa this rườm rà và constructor, giúp code dễ viết và ít gặp lỗi ngữ cảnh (bind this).