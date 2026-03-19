# 🛒 MARKETPLACE DIGITAL PRODUCT API

Mini project REST API untuk platform marketplace produk digital, dibuat dengan Laravel. Semua fitur sudah diuji dan siap digunakan!


## 📋 FITUR UTAMA 
- CRUD lengkap untuk kategori produk
- CRUD lengkap untuk produk digital
- Relasi antar tabel kategori & produk
- Fitur filter, search, dan sorting produk
- Klasifikasi rating produk (Top Rated, Popular, Regular)
- Validasi input yang sesuai standar


## 🛠️ CARA INSTALASI & SETUP

### 1. Clone Repositori
```bash
git clone https://github.com/[username-kamu]/marketplace-digital-product-api.git
cd marketplace-digital-product-api
 
 
### 2. Install Dependensi
 
bash
  
composer install 
 
 
### 3. Konfigurasi Environment
 
Salin file  .env.example  menjadi  .env  dan isi konfigurasi database:
 
env
  
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=marketplace_digital
DB_USERNAME=root
DB_PASSWORD=
 
 
### 4. Jalankan Migrasi & Seeder
 
bash
  
# Jalankan migrasi database
php artisan migrate

# Isi data awal (kategori & produk contoh)
php artisan db:seed --class=ProductCategorySeeder
php artisan db:seed --class=ProductSeeder
php artisan db:seed --class=UserSeeder
 
 
### 5. Jalankan Server
 
bash
  
php artisan serve
 
 
Server akan berjalan di  http://127.0.0.1:8000 
 
📌 ENDPOINT API YANG TERSEDIA
 
**MANAJEMEN KATEGORI PRODUK**

METHOD ENDPOINT DESKRIPSI 
GET /api/categories Ambil semua kategori beserta produknya 
GET /api/categories/{id} Ambil detail satu kategori beserta produknya 
POST /api/categories Tambahkan kategori produk baru 
PUT /api/categories/{id} Perbarui data kategori produk 
DELETE /api/categories/{id} Hapus kategori (hanya jika tidak ada produk) 

**MANAJEMEN PRODUK**
 
METHOD ENDPOINT DESKRIPSI 
GET /api/products Ambil semua produk + fitur filter/search 
GET /api/products/{id} Ambil detail satu produk 
POST /api/products Tambahkan produk digital baru 
PUT /api/products/{id} Perbarui data produk digital 
DELETE /api/products/{id} Hapus produk digital 
 
 
 
🎁FITUR BONUS
 
**Filter & Search Produk**
 
Contoh penggunaan parameter pada endpoint  /api/products :
 
- Search     : /api/products?search=Laptop
- Filter Kategori : /api/products?category_id=1
- Sorting Harga   : /api/products?sort_by=price&order=asc
- Kombinasi Semua : /api/products?search=Laptop&category_id=1&sort_by=rating&order=desc
 
**Klasifikasi Rating**
 
Setiap produk akan mendapatkan label otomatis berdasarkan skor rating:
 
- Top Rated  : Rating ≥ 8.5
- Popular    : Rating 7.0 - 8.4
- Regular    : Rating < 7.0
 
📧 KONTAK
 
Jika ada pertanyaan atau ingin berkontribusi, silakan hubungi:
 
- GitHub: [https://github.com/bahrul000000111-cmd]
- Email: [bahrul000000111@gmail.com]
