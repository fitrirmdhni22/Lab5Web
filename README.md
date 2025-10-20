# Lab5Web
# Nama : Fitri Ramadhani
# NIM : 312410085
# Kelas : TI.24.A.1
# Mata Kuliah : Pemrograman Web 1
# Dosen Pengampu : Agung Nugroho, S.Kom., M.Kom.

# Laporan Praktikum
1. Buatlah repository baru dengan nama Lab5Web.
2. Kerjakan semua latihan yang diberikan sesuai urutannya.
3. Screenshot setiap perubahannya.
4. Buatlah file README.md dan tuliskan penjelasan dari setiap langkah praktikum beserta
screenshotnya.
5. Commit hasilnya pada repository masing-masing.
6. Kirim URL repository pada e-learning ecampus

# Pertanyaan dan Tugas
1. Buat script untuk melakukan validasi pada isian form.

# Input Program
```HTML
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Validasi Form</title>
    <script>
        function validasiForm() {
            // ambil nilai input
            var nama = document.getElementById("nama").value;
            var email = document.getElementById("email").value;
            var password = document.getElementById("password").value;

            // pola email sederhana
            var polaEmail = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

            // cek apakah ada yang kosong
            if (nama == "" || email == "" || password == "") {
                alert("Semua kolom harus diisi!");
                return false;
            }

            // cek format email
            if (!polaEmail.test(email)) {
                alert("Format email tidak valid! Contoh: nama@gmail.com");
                return false;
            }

            // cek panjang password
            if (password.length < 6) {
                alert("Password minimal 6 karakter!");
                return false;
            }

            // kalau semua valid
            alert("Data berhasil dikirim!");
            return true;
        }
    </script>
</head>
<body>
    <h2>Form Validasi JavaScript</h2>
    <form onsubmit="return validasiForm()">
        <label>Nama:</label><br>
        <input type="text" id="nama"><br><br>

        <label>Email:</label><br>
        <input type="text" id="email"><br><br>

        <label>Password:</label><br>
        <input type="password" id="password"><br><br>

        <input type="submit" value="Kirim">
    </form>
</body>
</html>
```

# Output Program
<img width="1366" height="768" alt="PEMWEBTUGAS" src="https://github.com/user-attachments/assets/1fe0560d-e89b-42d8-ba28-09289add5495" />

# Cara Kerja Program
1. Pengguna mengisi form (nama, email, dan password).
2. Saat tombol “Kirim” ditekan, fungsi validasiForm() dijalankan.
3. Program akan memeriksa:
4. Apakah kolom sudah diisi semua.
5. Apakah format email benar.
6. Apakah password minimal 6 karakter.
7. Jika ada kesalahan → muncul pesan alert sesuai jenis error-nya.
8. Jika semua benar → muncul alert “Data berhasil dikirim!” dan form berhasil disubmit.
