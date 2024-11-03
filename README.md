# crud-movies
Proyek ini adalah aplikasi CRUD (Create, Read, Update, Delete) sederhana untuk mengelola data film. Aplikasi ini dibangun menggunakan Go dan Gorilla Mux sebagai router.

## Fitur

- Menambahkan film baru
- Mengambil daftar semua film
- Mengambil detail film berdasarkan ID
- Mengupdate informasi film
- Menghapus film
  
## Endpoints API

Berikut adalah daftar endpoint API yang tersedia:

### 1. Mendapatkan Semua Film

- **URL:** `/movies`
- **Method:** `GET`
- **Response:** Mengembalikan daftar semua film dalam format JSON.

### 2. Mendapatkan Film Berdasarkan ID

- **URL:** `/movies/{id}`
- **Method:** `GET`
- **Response:** Mengembalikan detail film berdasarkan ID dalam format JSON.

### 3. Menambahkan Film Baru

- **URL:** `/movies`
- **Method:** `POST`
- **Body:** 
    ```json
    {
        "id": "string",
        "isbn": "string",
        "title": "string",
        "director": {
            "firstname": "string",
            "lastname": "string"
        }
    }
    ```
- **Response:** Mengembalikan film yang baru ditambahkan dalam format JSON.

### 4. Mengupdate Film

- **URL:** `/movies/{id}`
- **Method:** `PUT`
- **Body:**
    ```json
    {
        "isbn": "string",
        "title": "string",
        "director": {
            "firstname": "string",
            "lastname": "string"
        }
    }
    ```
- **Response:** Mengembalikan film yang telah diperbarui dalam format JSON.

### 5. Menghapus Film

- **URL:** `/movies/{id}`
- **Method:** `DELETE`
- **Response:** Mengembalikan daftar film setelah penghapusan.

## Menguji API dengan Postman

1. **Instal Postman**: Pastikan Anda sudah menginstal Postman di komputer Anda.
2. **Buka Postman**: Luncurkan aplikasi Postman.
3. **Pilih Metode HTTP**: Pilih metode HTTP yang sesuai (GET, POST, PUT, DELETE) sesuai dengan endpoint yang ingin diuji.
4. **Masukkan URL**: Masukkan URL endpoint API yang ingin Anda akses, misalnya `http://localhost:8000/movies`.
5. **Menambahkan Body** (jika perlu): Untuk metode POST dan PUT, pilih tab "Body" dan pilih format JSON. Masukkan data yang sesuai.
6. **Kirim Permintaan**: Klik tombol "Send" untuk mengirim permintaan ke API Anda.
7. **Lihat Respons**: Periksa respons yang diterima di bagian bawah Postman untuk memastikan API berfungsi seperti yang diharapkan.

## Instalasi dan Menjalankan Proyek

1. **Clone Repository**
   ```bash
   git clone https://github.com/fadhilah-hub/crud-movies.git
