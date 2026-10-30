# PERN Template

Bộ khung React + TypeScript + Vite và Express + TypeScript.
Chưa triển khai database, đăng nhập hay nghiệp vụ cụ thể.

## Tạo dự án mới

Sao chép thư mục mẫu sang thư mục mới, bỏ qua node_modules, dist, .env và .git.
Giữ package-lock.json để cài đúng phiên bản bằng npm ci.

## Backend — terminal thứ nhất

```powershell
cd backend
npm ci
Copy-Item .env.example .env
npm run dev
```

Chỉ sao chép .env khi file chưa tồn tại. Điền cấu hình riêng cho dự án vào đó.
Mở http://localhost:3000/api/health để kiểm tra server.
API health chưa cần PostgreSQL hoặc JWT_SECRET.

## Frontend — terminal thứ hai

```powershell
cd frontend
npm ci
Copy-Item .env.example .env
npm run dev
```

Mở địa chỉ Local mà Vite in ra. Nếu cổng khác 5173, sửa FRONTEND_URL
trong backend/.env và khởi động lại backend trước khi gọi API.
Trang React hiện chỉ có tiêu đề PERN App, chưa tự gọi backend.

## Build

Chạy npm run build trong từng thư mục backend và frontend.
Backend: npm start chạy bản JavaScript trong dist.
Frontend: npm run preview xem thử bản build.

Các file .gitkeep giúp Git giữ lại thư mục trống.
Thư viện đã có trong package.json; không cần cài lại từng tên gói.
