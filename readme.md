# Bài tập nhóm môn: Công nghệ phần mềm

---

## Đề tài: DLU Confession - Website mạng xã hội cho sinh viên Trường Đại học Đà Lạt

---

## Tác giả

- 2011401 - Trần Bảo Lâm - CTK44PM
- 2014478 - Nguyễn Xuân Phát - CTK44PM
- 2014508 - Nguyễn Trường Vũ - CTK44PM

---

## I. Yêu cầu phần mềm:

### 1. API:

- SQL Server
- Visual Studio
- Dịch vụ Internet Information Services (IIS)

### 2. Giao diện:

- Node v16.x.x
- npm v8.15.x

## II. Cài đặt:

### 1. Sửa tên server cơ sở dữ liệu:

- Mở dự án <b>dlu-confession-api</b> bằng Visual Studio
- Mở file <b>Web.config</b> và sửa tên server cơ sở dữ liệu cho phù hợp tại dòng số 12:

  <code>...connectionString="Data Source=<b>{ten-server}</b>;Initial Catalog=ConfessionDB;Integrated Security=True;"...</code>

### 2. Cập nhật cơ sở dữ liệu:

- Tại thanh công cụ, vào mục <b>Tools > NuGet Package Manager > Package Manager Console</b>
- Tại cửa sổ <b>Package Manager Console</b> gõ lệnh:

  <code>Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r</code>

- Sau khi chạy, chọn <b>Yes > Yes > Yes to All</b>
- Sau khi hoàn tất, gõ lệnh: <code>Update-Database</code> để cập nhật cơ sở dữ liệu

### 3. Chạy API

- Sau khi cập nhật cơ sở dữ liệu, nhấn tổ hợp phím <b>Ctrl + F5</b> để chạy dự án
- Sau khi chạy, trình duyệt web sẽ vào trang <b>https://localhost:44332</b> và xuất hiện thông báo lỗi:

  ### The resource cannot be found

  <b>Description: HTTP 404 ...</b>

  <b>Lưu ý:</b> Lỗi này do chưa có giao diện ở phía API nhưng sẽ không gây ảnh hưởng đến hệ thống

### 4. Cài đặt giao diện:

- Mở <b>cmd</b> tại thư mục <b>/dlu-confession/dlu-confession-ui/</b>

- Gõ lệnh <code>npm install</code> để cài đặt

- Sau khi hoàn tất, gõ lệnh <code>npm run build</code> để build dự án

- Sau khi hoàn tất, gõ lệnh <code>npm install -g serve</code> để cài đặt

- Sau khi hoàn tất, gõ lệnh <code>serve -s build</code> để chạy dự án

### 5. Đăng nhập vào hệ thống

- Sau khi chạy thành công, mở trình duyệt và vào trang <b>http://localhost:3000</b>

- Đăng nhập vào hệ thống với tài khoản admin mặc định:

  Tài khoản: <b>admin</b>

  Mật khẩu: <b>dluconfession@2022!</b>
