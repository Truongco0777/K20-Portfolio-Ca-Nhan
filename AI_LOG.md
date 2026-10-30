# AI LOG – BUỔI 7, TIẾT 3

> Nhật ký dựa trên quá trình làm bài thực tế. Những hạng mục chưa được kiểm tra trực tiếp được ghi rõ là “Chưa kiểm tra”.

## Thông tin sinh viên

- Họ và tên: Nguyễn Bá Trường
- Mã sinh viên – Lớp: 2071020217 – CNTT20-02
- Ngày thực hiện: 30/10/2026
- Link repository: https://github.com/Truongco0777/K20-Portfolio-Ca-Nhan
- URL website: Chưa kiểm tra / chưa xác nhận GitHub Pages đã triển khai thành công
- Tình huống: [x] Website của tôi  [ ] Repo luyện của giảng viên

## 1. Nhận định của tôi trước khi hỏi AI

- Trang/thao tác gặp lỗi: Chuẩn bị mã nguồn Portfolio để đưa lên GitHub và triển khai bằng GitHub Pages.
- Mong muốn và hiện tượng thực tế: Muốn các tệp `index.html`, `assets/` nằm tại thư mục gốc của repository, nhưng ban đầu mã nguồn nằm bên trong thư mục con `Portfolio-Website-main/`.
- Dữ kiện đã kiểm tra (cấu trúc tệp, Request URL, Status…): Trong VS Code, Explorer hiển thị thư mục dự án lồng nhau. Trên GitHub, lần đẩy đầu tiên hiển thị một thư mục con `Portfolio-Website-main` ở cấp cao nhất. Request URL/Status của trình duyệt: Chưa kiểm tra.
- Tôi nghi nguyên nhân là: Chưa có nhận định độc lập được ghi lại trước khi hỏi AI.
- Vì sao tôi nhận định như vậy: Chưa ghi nhận trong quá trình thực hiện.

## 2. Tôi hỏi AI và nhận được gợi ý

- Nguồn: [x] Công cụ AI: ChatGPT  [ ] Phản hồi mẫu của giảng viên
- Câu hỏi/prompt tôi đã gửi (trích các câu hỏi thực tế):

  “chuyển kiểu gì”; “sửa luôn ở đây k đc à”; “hiện tại là đang như này”; “đây đc chưa”. Các câu hỏi có gửi kèm ảnh màn hình VS Code.

- Gợi ý chính của AI:

  Chuyển các tệp và thư mục website từ thư mục con ra thư mục gốc Git đang quản lý; sau đó kiểm tra lại cấu trúc và dùng `git add -A`, `git commit`, `git push` để lưu lịch sử thay đổi lên GitHub.

## 3. Quyết định của tôi

- [x] Chấp nhận gợi ý
- [ ] Chỉnh sửa gợi ý rồi áp dụng
- [ ] Bác bỏ gợi ý

- Tôi quyết định làm gì: Sử dụng PowerShell trong Terminal VS Code để chuyển các tệp website ra thư mục gốc, tiếp tục dùng Git để tạo commit và push.
- Lý do, dựa trên dữ kiện nào: Cấu trúc trong Explorer và trên GitHub ban đầu cho thấy `index.html` nằm trong thư mục con; vị trí đó không khớp cách xuất bản từ `main` / `(root)` dự kiến.

## 4. Thực hiện và kiểm chứng

- Tệp/vị trí đã sửa: Chuyển các thư mục `assets/`, `experience/`, `projects/` và các tệp `index.html`, `404.html`, `README.md`, `skills.json` từ thư mục con lên thư mục gốc repository.
- Nội dung thay đổi hoặc cách xử lý khác: Đã sử dụng lệnh `Move-Item -Path ".\Portfolio-Website-main\*" -Destination ".\"`. Sau đó thực hiện thêm commit/push; tiếp tục chỉnh sửa nội dung Portfolio sang tiếng Việt.
- Commit của bản sửa, nếu có: Xem lịch sử tại https://github.com/Truongco0777/K20-Portfolio-Ca-Nhan/commits/main ; cần điền đúng SHA commit tương ứng sau khi đối chiếu trên GitHub.
- Bản sửa đã deploy: [ ] Có  [x] Chưa (chưa xác nhận bản triển khai GitHub Pages)  [ ] Không phát sinh bản sửa

| Nội dung kiểm tra | Trước xử lý | Sau xử lý/thử lại |
| --- | --- | --- |
| Request URL và Status của tài nguyên liên quan | Chưa kiểm tra Network | Chưa kiểm tra Network |
| Giao diện/chức năng trên URL website | Chưa kiểm tra URL công khai | Chưa kiểm tra URL công khai; không kết luận đã sửa thành công trên Pages |
| Cấu trúc tệp local | `index.html` ở thư mục con `Portfolio-Website-main/` | Ảnh VS Code sau khi chạy `Move-Item` cho thấy `index.html` và `assets/` ở cấp thư mục gốc |
| GitHub | Đã nhìn thấy thư mục con ở cấp gốc trong repo | Terminal cho thấy có lần `git push` hoàn tất; cần mở repository để kiểm tra cấu trúc cuối |

- Cách thử lại và kết quả thực tế: Đã xem lại cấu trúc thư mục trong VS Code và thực hiện `git push`; chưa đối chiếu với GitHub Pages bằng trình duyệt ẩn danh và DevTools Network.
- Căn cứ để đối chiếu: Repository https://github.com/Truongco0777/K20-Portfolio-Ca-Nhan ; các ảnh chụp VS Code/Terminal trong quá trình làm bài. Chưa lưu đường dẫn ảnh minh chứng vào repository.

## 5. Kết luận

- [ ] Đã xử lý được  [x] Xử lý được một phần  [ ] Chưa xử lý được
- Điều tôi rút ra hoặc việc cần làm tiếp: Cần kiểm tra vị trí `index.html` trước khi cấu hình Pages. Tiếp theo: mở repo kiểm tra cấu trúc mới nhất; bật GitHub Pages từ `main` / `(root)`; thử URL công khai, CSS, ảnh, liên kết; dùng DevTools Network ghi Request URL/Status và lưu ảnh minh chứng; đối chiếu SHA của bản đã deploy rồi cập nhật nhật ký.

---

*Tài liệu ghi rõ những phần chưa kiểm chứng. Nội dung về nhận định ban đầu và quyết định cá nhân cần được sinh viên rà soát, chỉnh lại nếu khác thực tế trước khi nộp.*
