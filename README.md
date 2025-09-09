# Task Management API 🚀

[![Laravel Version](https://img.shields.io/badge/Laravel-12.x-red)](https://laravel.com/) 
[![PHP Version](https://img.shields.io/badge/PHP-8.2-blue)](https://www.php.net/) 
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

Proyek ini adalah aplikasi **Task Management API** berbasis Laravel dengan fitur autentikasi, manajemen pengguna, tugas, dan workflow sederhana.  
Dokumentasi API tersedia dalam format **Swagger**.

---

## 🛠️ Setup Project

1. Ekstrak file `.zip` project ini.  
2. Masuk ke folder project lewat terminal.  
3. Jalankan migrasi dan seeding database:

```bash
php artisan migrate --seed
```

4. Jalankan server:
```bash
php artisan serve
```

Jika ketika download projek zipnya dan file .env hilang
maka tinggal generate ulang dengan cara
Salin file .env.example menjadi .env
```bash
cp .env.example .env
```

Edit konfigurasi database di file .env
```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=task_api
DB_USERNAME=root
DB_PASSWORD=
```

Lalu generate app key:
```bash
php artisan key:generate
```

kemudian create database nya dengan nama task_api


🔑 Default Akun Hasil Seeding

| Role    | Email                                               | Password    |
| ------- | --------------------------------------------------- | ----------- |
| Manager | [manager1@example.com](mailto:manager1@example.com) | password123 |
| Staff   | [staff1@example.com](mailto:staff1@example.com)     | password123 |


📌 API Endpoints

| Module | Method | Endpoint               | Keterangan              |
| ------ | ------ | ---------------------- | ----------------------- |
| Auth   | POST   | /api/auth/login        | Login pengguna          |
| Auth   | POST   | /api/auth/logout       | Logout pengguna         |
| Users  | POST   | /api/users             | Membuat user baru       |
| Users  | GET    | /api/users             | Mendapatkan list user   |
| Tasks  | POST   | /api/tasks             | Membuat task baru       |
| Tasks  | PUT    | /api/tasks/{id}        | Update task             |
| Tasks  | PATCH  | /api/tasks/{id}/status | Update status task      |
| Tasks  | PATCH  | /api/tasks/{id}/report | Update laporan task     |
| Tasks  | GET    | /api/tasks/{id}        | Mendapatkan detail task |


📄 Swagger API Docs
Generate dokumentasi
```bash
php artisan l5-swagger:generate
```

Akses dokumentasi via browser
| Environment            | URL                                                                                                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| XAMPP/Environment Lain | [http://localhost:8000/api/documentation](http://localhost:8000/api/documentation)                                       |
| Laragon                | [http://localhost/kledo-assessment/public/api/documentation](http://localhost/kledo-assessment/public/api/documentation) |


🧪 Menjalankan Test
Jalankan semua test otomatis:
```bash
php artisan test
```


Jalankan hanya flow utama:
```bash
php artisan test --filter=AssessmentFlowTest
```

Jika semua benar, hasilnya akan PASS ✅

📌 Catatan

- Pastikan PHP, Composer, dan database MySQL sudah terinstall.
- Sesuaikan .env untuk koneksi database.
- Dokumentasi Swagger akan otomatis ter-generate sesuai perubahan endpoint


