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
    <h2>Form Validasi</h2>
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
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/72371d61-0f6d-458c-8f3e-0c91d1113fb6" />

# Cara Kerja Program
1. Pengguna mengisi form (nama, email, dan password).
2. Saat tombol “Kirim” ditekan, fungsi validasiForm() dijalankan.
3. Program akan memeriksa:
   - Apakah kolom sudah diisi semua.
   - Apakah format email benar.
   - Apakah password minimal 6 karakter.
4. Jika ada kesalahan → muncul pesan alert sesuai jenis error-nya.
5. Jika semua benar → muncul alert “Data berhasil dikirim!” dan form berhasil disubmit.

# Instruksi Praktikum
1. Persiapkan text editor misalnya VSCode.
2. Buat folder baru dengan nama lab5_javascript.
3. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya.
4. Lakukan validasi dokumen html dengan mengakses http://validator.w3.org
Langkah-langkah Praktikum
Persiapan membuat dokumen HTML dengan nama file lab5_javascript.html seperti berikut.
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
<title>Mengenal JavaScript</title>
</head>
<body>
<h1>Pengenalan JavaScript</h1>
<h3>Contoh document.write dan console.log</h3>
<script>
document.write("Hello World");
console.log("Hello World");
</script>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb1" src="https://github.com/user-attachments/assets/b902ae6c-6684-438b-90e8-feb7f2a4b0bf" />

# Javascrip Dasar
Pemakaian Alert sebagai property window.
```HTML
<html>
<head>
    <title>alert box</title>
</head>
<body>
<script language="javascript">
<!--
    window.alert("ini merupakan pesan untuk anda");
//-->
</script>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb2" src="https://github.com/user-attachments/assets/084732a7-a340-44d0-9223-194639df1cd0" />

Pemakaian method dalam objek
```HTML
<html>
<head>
    <title>skrip javascript</title>
</head>
<body>
    percobaan memakai javascript:<br>
<script language = "javascript">
<!--
    document.write("selamat mencoba javascript<br>");
    document.write("semoga sukses!");
//-->
</script>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb3" src="https://github.com/user-attachments/assets/52af134d-c39a-466e-bd37-2ada81c97caf" />

Pemakaian Prompt
```HTML
<html>
<head>
    <title>pemasukan data</title>
</head>
<body>
<script language = "javascript">
<!--
    var nama = prompt("siapa nama anda?", "masukkan nama anda");
    document.write("hai, " + nama);
//-->
</script>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb4" src="https://github.com/user-attachments/assets/ba63ab5f-e428-402c-9ff0-529c068658ba" />
<img width="1366" height="768" alt="pemweb5" src="https://github.com/user-attachments/assets/7622e1f1-4360-4240-8ad6-adf12386e004" />

Pembuatan fungsi dan cara pemanggilannya
```HTML
<html>
<head>
    <title>contoh program javascript</title>
    <script language="javascript">
        function pesan() {
            alert("memanggil javascript lewat body onload")
        }
    </script>
</head>
<body onload=pesan()>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb6" src="https://github.com/user-attachments/assets/d1528455-74c5-493b-9b91-0fb1d29727b5" />

Dasar Pemrograman Di Javascript
Operasi dasar aritmatika
```HTML
<html>
<head>
    <title>contoh program javascript</title>

    <script language="javascript">
    function test(val1, val2) 
    {
        document.write("<br>" + "Perkalian : val1*val2 "+"<br>")
        document.write(val1*val2)
        document.write("<br>" + "Pembagian : val1/val2 "+"<br>")
        document.write(val1/val2)
        document.write("<br>" + "Penjumlahan : val1+val2 "+"<br>")
        document.write(val1+val2)
        document.write("<br>" + "Pengurangan : val1-val2 "+"<br>")
        document.write(val1-val2)
        document.write("<br>" + "Modulus : val1%val2 "+"<br>")
        document.write(val1%val2)
    }
    </script>
</head>
<body>
    <input type="button" name="button1" value="arithmetic" onclick="test(9,4)">
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb7" src="https://github.com/user-attachments/assets/ec129912-5f30-4028-a463-5b65feaaf045" />
<img width="1366" height="768" alt="pemweb8" src="https://github.com/user-attachments/assets/21c6d9db-dbe4-4d38-9ad6-f475da53e9d4" />

Seleksi kondisi (if..else)
```HTML
<html>
<head>
    <title>contoh if-else</title>
</head>
<body>
    <script language = "javascript">
    <!--
    var nilai = prompt("nilai (0-100):", 0);
    var hasil = "";
    if (nilai >= 60)
        hasil = "lulus";
    else
        hasil = "tidak lulus";
    document.write("hasil: " + hasil);
    //-->
    </script>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb9" src="https://github.com/user-attachments/assets/270e79b6-54a7-4c5f-820d-257f4943e3e6" />
<img width="1366" height="768" alt="pemweb10" src="https://github.com/user-attachments/assets/171bc89e-23e8-47b1-9c71-5c0740a0c2fd" />

Penggunaan operator switch untuk seleksi kondisi
```HTML
<html>
<head>
    <title>contoh program javascript</title>

    <script language="javascript">
    function test() 
    {
        val1=window.prompt("input nilai (1-5):")
        switch (val1)
        {
            case "1":
                document.write("bilangan satu")
                break;
            case "2":
                document.write("bilangan dua")
                break;
            case "3":
                document.write("bilangan tiga")
                break;
            case "4":
                document.write("bilangan empat")
                break;
            case "5":
                document.write("bilangan lima")
                break;
            default:
                document.write("bilangan lainnya")
        }
    }
    </script>
</head>
<body>
    <input type="button" name="button1" value="switch" onclick="test()">
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb11" src="https://github.com/user-attachments/assets/6eed6dcf-ba5f-4657-8920-37b39afe1f55" />
<img width="1366" height="768" alt="pemweb12" src="https://github.com/user-attachments/assets/2ebc844b-6a55-4443-a39e-6034eff06769" />
<img width="1366" height="768" alt="pemweb13" src="https://github.com/user-attachments/assets/136318df-76ec-419f-b3a5-bf1622b96777" />

Pembuatan Form
Form Input
```HTML
<html>
<head>
    <script language="javascript">
    function test() {
        var val1=document.kirim.T1.value
        if (val1%2==0)
            document.kirim.T2.value = "bilangan genap"
        else
            document.kirim.T2.value ="bilangan ganjil"
    }
    </script>
</head>
<body>
    <form method="POST" name="kirim">
        <p>BIL <input type="text" name="T1" size="20">
        MERUPAKAN BIL <input type="text" name="T2" size="20"></p>
        <p><input type="button" value="TEBAK" name="B1" onclick="test()"></p>
    </form>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb14" src="https://github.com/user-attachments/assets/71cfd703-c9e4-4d45-ac27-359db26d4d0d" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/3c644d98-dfba-49cd-9f22-f218250d3d59" />

Form Button.
```HTML
<html>
<head>
    <title>objek document</title>
</head>
<body>
    <script language = "javascript">
    <!--
    function ubahWarnaLB(warna) {
        document.bgColor = warna;
    }
    function ubahWarnaLD(warna) {
        document.fgColor = warna;
    }
    //-->
    </script>
    
    <h1>tes</h1>
    <form>
        <input type="button" value="Latar Belakang Hijau" onClick="ubahWarnaLB('GREEN')">
        <input type="button" value="Latar Belakang Putih" onClick="ubahWarnaLB('WHITE')">
        <input type="button" value="Teks Kuning" onClick="ubahWarnaLD('YELLOW')">
        <input type="button" value="Teks Biru" onClick="ubahWarnaLD('BLUE')">
    </form>
    <script language = "javascript">
        <!--
        document.write("Dimodifikasi terakhir pada " + 
        document.lastmodified);
        //-->
        </script>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb15" src="https://github.com/user-attachments/assets/cb8427ad-3f7a-4987-a1b1-9ff7833b293f" />
<img width="1366" height="768" alt="pemweb16" src="https://github.com/user-attachments/assets/f2d644e9-f7c7-4d6b-9a09-e7f227c97d87" />
<img width="1366" height="768" alt="pemweb17" src="https://github.com/user-attachments/assets/bb82d1c4-2e08-45bd-897e-a65d6227b61b" />
<img width="1366" height="768" alt="pemweb18" src="https://github.com/user-attachments/assets/03c872e9-1b95-4d31-8b1c-3875406767a6" />
<img width="1366" height="768" alt="pemweb19" src="https://github.com/user-attachments/assets/61dd0c42-cba8-4937-bb1f-8cf8c0d1e536" />

HTML DOM
Pilihan menggunakan checkBox dengan perhitungan otomatis
```HTML
<html>
<head>
    <title>Daftar Menu</title>
    <script>
        function hitung(ele) {
            var total = document.getElementById('total').value;
                total = (total ? parseInt(total) : 0);
            var harga = 0;

            if (ele.checked) {
                harga = ele.value;
                total += parseInt(harga);
            } else {
                harga = ele.value;
                if (total > 0)
                    total -= parseInt(harga);
            }

            document.getElementById('total').value = total;
    }
 </script>
</head>
<body>
    <h1>Daftar Menu Makanan</h1>
    <label><input type="checkbox" value="5000" id="menu1" onclick="hitung(this);"> Ayam Goreng Rp. 5.000</label><br />
    <label><input type="checkbox" value="500" id="menu2" onclick="hitung(this);"> Tempe Goreng Rp. 500</label><br >
    <label><input type="checkbox" value="2500" id="menu3" onclick="hitung(this);"> Telur Dadar Rp. 2.500</label><br>
    <strong>Total Bayar: Rp. <input id="total" type="text"></strong>
</body>
</html>
```

# Tampilan Output
<img width="1366" height="768" alt="pemweb22" src="https://github.com/user-attachments/assets/88d5ff1e-382b-4a83-b505-046ddb4d2f57" />

# TERIMAKASIH
