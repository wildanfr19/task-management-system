# Task Management API

Proyek ini adalah aplikasi **Task Management API** berbasis Laravel dengan fitur autentikasi, manajemen pengguna, tugas, dan workflow sederhana.  
Dokumentasi API tersedia dalam format **Swagger**.

## 🚀 Setup Project

1. Ekstrak file `.zip` project ini.  
2. Masuk ke folder project lewat terminal.  
3. Jalankan migrasi dan seeding database:
   ```bash
   php artisan migrate --seed


4. Jalankan server:

   php artisan serve

🔑 Default Akun Hasil Seeding

Gunakan akun berikut untuk login pertama kali:

# Manager
Email: manager1@example.com
Password: password123

# Staff

Email: staff1@example.com
Password: password123

📌 Endpoint List

# Auth

POST /api/auth/login
POST /api/auth/logout

# Users

POST /api/users
GET /api/users

# Tasks

POST /api/tasks
PUT /api/tasks/{id}
PATCH /api/tasks/{id}/status
PATCH /api/tasks/{id}/report
GET /api/tasks/{id}

# Swagger API Docs

Generate dokumentasi:

<li> php artisan l5-swagger:generate </li>


# Akses dokumentasi via browser:

XAMPP/yang lain
<li> http://localhost:8000/api/documentation </li>

Laragon
<li> http://localhost/kledo-assessment/public/api/documentation </li>

🧪 Menjalankan Test

# Untuk menjalankan test otomatis:

 php artisan test


# Hanya menjalankan flow utama:

  php artisan test --filter=AssessmentFlowTest


Jika semua benar, hasilnya akan PASS ✅

