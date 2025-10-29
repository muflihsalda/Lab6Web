# Lab6Web
# Praktikum 6: Twitter Bootstrap


## LANGKAH 1 — Setup Bootstrap (CDN)

Menyertakan library Bootstrap melalui CDN agar framework bisa digunakan tanpa instalasi lokal.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Praktikum 6 Bootstrap</title>

  <link 
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"  
    rel="stylesheet"  
    integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"  
    crossorigin="anonymous">
</head>
<body>
  <div class="container">
    <h1>Halo, Bootstrap!</h1>
    <button class="btn btn-primary">Ini Tombol Bootstrap</button>
  </div>

  <script 
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"  
    integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"  
    crossorigin="anonymous"
  ></script>
</body>
</html>
```

Screenshot: Tampilan teks “Halo, Bootstrap!” dan tombol biru.

<img width="1332" height="269" alt="image" src="https://github.com/user-attachments/assets/dc3cf9be-cc0c-4990-81eb-c098903c7358" />


## LANGKAH 2 — Container 
Bootstrap menyediakan dua jenis container:

.container → lebar tetap, otomatis menyesuaikan ukuran layar

.container-fluid → lebar penuh (100%)

```html
<div class="container">
  <p>Ini container biasa.</p>
</div>
```
Hasil countiner 
<img width="1332" height="269" alt="image" src="https://github.com/user-attachments/assets/dc3cf9be-cc0c-4990-81eb-c098903c7358" />

```html
<div class="container-fluid">
  <p>Ini container-fluid.</p>
</div>
```
Hasil container-fluid.

<img width="1086" height="288" alt="image" src="https://github.com/user-attachments/assets/54e7bc06-0260-4cf8-94de-1a87940a9853" />



## LANGKAH 3 — Grid System
Membuat layout responsif menggunakan sistem 12 kolom. dan menambahkan background di belakngnya

```html
<div class="container text-center mt-5">
  <div class="row mb-3">
    <div class="col-4 bg-primary text-white p-3 border border-white rounded-3">Kolom 1</div>
    <div class="col-4 bg-success text-white p-3 border border-white rounded-3">Kolom 2</div>
    <div class="col-4 bg-danger text-white p-3 border border-white rounded-3">Kolom 3</div>
  </div>

  <div class="row">
    <div class="col-md-8 bg-info text-dark p-3 border border-white rounded-3">Kolom Lebar 8</div>
    <div class="col-md-4 bg-warning text-dark p-3 border border-white rounded-3">Kolom Lebar 4</div>
  </div>
</div>
```
 Screenshot: 3 kolom sejajar, serta kombinasi 8–4 kolom di bawahnya.
 
 <img width="1230" height="192" alt="image" src="https://github.com/user-attachments/assets/2320a6f2-850d-4e8f-bfbe-2549f7ed7501" />


## LANGKAH 4 — Komponen: Button

Bootstrap menyediakan class untuk tombol dengan berbagai warna dan fungsi.
```html
<div class="container mt-5">
  <button class="btn btn-primary">Primary</button>
  <button class="btn btn-secondary">Secondary</button>
  <button class="btn btn-success">Success</button>
  <button class="btn btn-danger">Danger</button>
</div>
```
 Screenshot: Tampilkan semua tombol dengan warna berbeda.
 
 <img width="481" height="124" alt="image" src="https://github.com/user-attachments/assets/a9309477-1d87-4aa1-8ae6-c9d04cc5bbd6" />


## LANGKAH 5 — Komponen: Navbar
Membuat navigasi responsif yang otomatis berubah menjadi hamburger menu di layar kecil.

```html
<div class="container mt-5">
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Praktikum 6</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
      </ul>
    </div>
  </div>
</nav>
</div>
```

Screenshot: Navbar hitam dengan tulisan “Praktikum 6”.

<img width="1134" height="90" alt="image" src="https://github.com/user-attachments/assets/4d6735d7-f4a9-4c9b-9f55-8a9faf6d6b83" />


## LANGKAH 6 — Komponen: Card
Card digunakan untuk menampilkan konten dengan tampilan rapi.

```html
<div class="container mt-5">
<div class="card" style="width: 10rem;">
  <img src="c:\Users\LENOVO\Downloads\Logo UPB.jpg" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Judul Card</h5>
    <p class="card-text">Ini adalah deskripsi singkat di dalam card.</p>
    <a href="#" class="btn btn-primary">Lihat Detail</a>
  </div>
</div>
</div>
```

Screenshot: Tampilkan card dengan gambar dan tombol.

<img width="196" height="354" alt="image" src="https://github.com/user-attachments/assets/558d02d1-9ff2-4bfc-9ad2-0f246a5883fc" />

LANGKAH 7 — Komponen: Form
Menata input dan textarea agar tampil seragam.

```html
<div class="mb-3">
  <label for="emailInput" class="form-label">Alamat Email</label>
  <input type="email" class="form-control" id="emailInput" placeholder="nama@contoh.com">
</div>

<div class="mb-3">
  <label for="pesanText" class="form-label">Pesan</label>
  <textarea class="form-control" id="pesanText" rows="3"></textarea>
</div>

<button type="submit" class="btn btn-primary">Kirim</button>
```
Screenshot: Form input email dan textarea pesan.

<img width="1365" height="264" alt="image" src="https://github.com/user-attachments/assets/b6d1faaa-aeb7-49a5-9c46-d57dd48fe6b8" />

