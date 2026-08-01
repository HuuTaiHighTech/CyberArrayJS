# Ghi chú: Các thư viện được sử dụng trong trang web

> Phân tích từ mã nguồn HTML của trang "HỆ THỐNG HỌC TẬP CYBERSOFT" (chungnhan.cybersoft.edu.vn)

## 🎯 Thư viện chạy hiệu ứng chính: Lottie (lottie-web / bodymovin)

**Bằng chứng nhận diện:**
- Các thẻ `<clipPath id="__lottie_element_2">`, `__lottie_element_4`, `__lottie_element_8`... là dấu hiệu đặc trưng của animation được export từ **After Effects → Bodymovin/Lottie**.
- Cấu trúc SVG phức tạp với nhiều `<g>` lồng nhau, `transform`, `opacity` thay đổi theo từng lớp — đúng kiểu Lottie render ra SVG tại runtime.
- Đây chính là hiệu ứng "pháo hoa / ngôi sao vàng bay ra" khi hiện dòng chữ **"Chúc mừng bạn đã hoàn thành bài tập"**.

Lottie là thư viện phổ biến để nhúng animation từ Adobe After Effects vào web dưới dạng file JSON, sau đó render bằng SVG hoặc Canvas.

## 📚 Các thư viện khác xuất hiện trong trang

| Thư viện | Dấu hiệu nhận biết trong mã nguồn | Chức năng |
|---|---|---|
| **SweetAlert2** | class `.swal2-popup`, `.swal2-icon`, `.swal2-success`... | Hộp thoại alert/confirm đẹp |
| **SweetAlert (bản 1)** | class `.swal-modal`, `.swal-icon--success` | Cùng mục đích, phiên bản cũ hơn |
| **Ant Design (antd)** | class `.ant-menu`, `.ant-steps`, `.ant-modal`, `.ant-progress`... | Bộ UI Components (React) — dùng cho sidebar, timeline lộ trình học, modal bài tập |
| **Material-UI (MUI)** | class `.MuiPaper-root`, `.MuiCard-root` | Component Card hiển thị file tài liệu (zip) |
| **Google Identity Services** | script `accounts.google.com/gsi/client`, class `.nsm7Bb-HzV7m-LgbsSe` | Đăng nhập bằng tài khoản Google |
| **jQuery (slim)** | `jquery.slim.min.js` | Thao tác DOM cơ bản |
| **Bootstrap** | `bootstrap.bundle.min.js` | Framework CSS/JS |
| **Font Awesome** | class `fa-solid`, `fa-regular` | Bộ icon |
| **React (webpack runtime)** | các file `.chunk.js` (react-pdf, chart, main...) được nạp qua webpack | Framework nền tảng dựng toàn bộ giao diện |

## Tóm tắt

- **Hiệu ứng chúc mừng hoàn thành bài tập** → chạy bằng **Lottie animation**.
- **Giao diện tổng thể** (sidebar, lộ trình học, modal) → xây bằng **React + Ant Design**, có xen thêm vài component từ **Material-UI**.
- **Thông báo/hộp thoại** → dùng **SweetAlert / SweetAlert2**.
- **Đăng nhập** → tích hợp **Google Identity Services**.
