# lab4web
#### Disini saya akan menjelaskan sedikit tentang praktikum ke 4
## A. Membuat Element BOX
masukan kode dibawah ini :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Element</title>
 </head>
<body>
  <header>
    <h1>Box Element</h1>
  </header>
  <section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
    <div class="div4">Div 4</div>
  </section>
</body>
</html>
```

Setelah itu tambahkan CSS nya :
```
<style>
    div{
      float: left;
      padding: 10px;
    }
      .div1 {
        background: red;
      }
      .div2 {
        background: yellow;
      }
      .div3 {
        background: green;
      }
      .div4 {
        background-color: blue;
        clear: both;
        float: none;
      }
  </style>
```
Jika semua sudah digabungkan maka kodenya full nya akan seperti ini :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Element</title>
  <style>
    div{
      float: left;
      padding: 10px;
    }
      .div1 {
        background: red;
      }
      .div2 {
        background: yellow;
      }
      .div3 {
        background: green;
      }
      .div4 {
        background-color: blue;
        clear: both;
        float: none;
      }
  </style>
</head>
<body>
  <header>
    <h1>Box Element</h1>
  </header>
  <section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
    <div class="div4">Div 4</div>
  </section>
</body>
</html>
```
dan hasilnya seperti ini :

![4 hasil clearfix](https://user-images.githubusercontent.com/101393632/161830325-5dccce32-8a1c-461b-ac82-2127180c4a89.jpg)

dibawah ini hasil both

![5 clear both](https://user-images.githubusercontent.com/101393632/161830357-5b7f9ca8-c379-4766-b59d-364977ae7175.jpg)

dan ini hasil right

![5 clear right](https://user-images.githubusercontent.com/101393632/161830359-822a7b03-82b9-49fc-bb7b-f0bf956134e8.jpg)

## B. Membuat Layout sederhana.
Buat file baru dengan nama `home.html` lalu masukkan kode seperti dibawah ini :
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <div id="container">
      <header>
        <h1>Layout Sederhana</h1>
      </header>
    </div>
</body>
</html>
```

Lalu ketik kode seperti dibawah ini : 
```
<header>
 <h1>Layout Sederhana</h1>
</header>
<nav>
 <a href="home.html" class="active">Home</a>
 <a href="artikel.html">Artikel</a>
 <a href="about.html">About</a>
 <a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
 <section id="main"></section>
 <aside id="sidebar"></aside>
</section>
<footer>
 <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```
maka hasilnya akan seperti ini :

![7 hasilnya](https://user-images.githubusercontent.com/101393632/161831524-6946f957-7d0e-459b-869f-85debf74f262.jpg)

Selanjutnya ketik kode CSS :
```
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400
;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0
,300;0,700;1,300&display=swap');
/* Reset CSS */
* {
 margin: 0;
 padding: 0;
}
body {
 line-height:1;
 font-size:100%;
 font-family:'Open Sans', sans-serif;
 color:#5a5a5a;
}
#container {
 width: 980px;
 margin: 0 auto;
 box-shadow: 0 0 1em #cccccc;
}
/* header */
header {
 padding: 20px;
}
header h1 {
 margin: 20px 10px;
 color: #b5b5b5;
}
```
maka hasilnya akan seperti ini :

![9 tampilan akan seperti ini](https://user-images.githubusercontent.com/101393632/161831685-8324ed83-cc3d-4d3c-93eb-6096c4eb8901.jpg)

Lalu kita buat Navigasi, kita ketik kode ini di CSS agar mudah : 
```
/* navigasi */
nav {
 display: block;
 background-color: #1f5faa;
}
nav a {
 padding: 15px 30px;
 display: inline-block;
 color: #ffffff;
 font-size: 14px;
 text-decoration: none;
 font-weight: bold;
}
nav a.active,
nav a:hover {
 background-color: #2b83ea;
}
```
begini hasilnya :

![10 hasil](https://user-images.githubusercontent.com/101393632/161831883-1fe74346-be77-45dd-b835-fbec65d8b8b9.jpg)

Sekarang kita akan membuat Hero Panel, tambahkan kode pada HTML dan CSS :
HTML
```
<section id="hero">
 <h1>Hello World!</h1>
 <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
pretium ac.</p>
 <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
css
```
/* Hero Panel */
#hero {
 background-color: #e4e4e5;
 padding: 50px 20px;
 margin-bottom: 20px;
}
#hero h1 {
 margin-bottom: 20px;
 font-size: 35px;
}
#hero p {
 margin-bottom: 20px;
 font-size: 18px;
 line-height: 25px;
}
/* main content */
#wrapper {
 margin: 0;
}
#main {
 float: left;
 width: 640px;
 padding: 20px;
}
/* sidebar area */
#sidebar {
 float: left;
 width: 260px;
 padding: 20px;
}
```
Jika sudah, kita langsung lanjut membuat sidebar widget :
```
<aside id="sidebar">
 <div class="widget-box">
 <h3 class="title">Widget Header</h3>
 <ul>
 <li><a href="#">Widget Link</a></li>
 <li><a href="#">Widget Link</a></li>
 <li><a href="#">Widget Link</a></li>
 <li><a href="#">Widget Link</a></li>
 <li><a href="#">Widget Link</a></li>
 </ul>
 </div>
 <div class="widget-box">
 <h3 class="title">Widget Text</h3>
 <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt 
arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer 
pharetra est nunc, nec pretium nunc pretium ac.</p>
 </div>
</aside>
```
Kode CSS :
```
/* widget */
.widget-box {
 border:1px solid #eee;
 margin-bottom:20px;
}
.widget-box .title {
 padding:10px 16px;
 background-color:#428bca;
 color:#fff;
}
.widget-box ul {
 list-style-type:none;
}
.widget-box li {
 border-bottom:1px solid #eee;
}
.widget-box li a {
 padding:10px 16px;
 color:#333;
 display:block;
 text-decoration:none;
}
.widget-box li:hover a {
 background-color:#eee;
}
.widget-box p {
 padding:15px;
 line-height:25px;
}
```
Hasilnya akan muncul seperti ini :

![13 hasilnya akan muncul seperti ini](https://user-images.githubusercontent.com/101393632/161832813-8154b513-dd7b-4111-b8f9-7a18c02f3363.jpg)

Lalu kita akan mengatur Footernya dengan kode :
```
/* footer */
footer {
 clear:both;
 background-color:#1d1d1d;
 padding:20px;
 color:#eee;
 }
```
Hasilnya akan muncul seperti ini

![14 hasil footer](https://user-images.githubusercontent.com/101393632/161833013-492183ad-4c6b-49fc-8de3-fe3bac0222a0.jpg)

menambahkan elemen lainya pada main content :
```
<section id="main">
 <div class="row">
 <div class="box">
 <img src="https://dummyimage.com/120/db7d25/fff.png" alt=""
class="image-circle">
 <h3>Heading</h3>
 <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
euismod.</p>
 <a href="#" class="btn btn-default">View detail</a>
 </div>
 <div class="box">
 <img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
class="image-circle">
 <h3>Heading</h3>
 <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
euismod.</p>
 <a href="#" class="btn btn-default">View detail</a>
 </div>
 <div class="box">
 <img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""
class="image-circle">
 <h3>Heading</h3>
 <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
euismod.</p>
 <a href="#" class="btn btn-default">View detail</a>
 </div>
 </div>
</section>
```
Kode CSS nya :
```
/* box */
.box {
 display:block;
 float:left;
 width:33.333333%;
 box-sizing:border-box;
 -moz-box-sizing:border-box;
 -webkit-box-sizing:border-box;
padding:0 10px;
 text-align:center;
}
.box h3 {
 margin: 15px 0;
}
.box p {
 line-height: 20px;
 font-size: 14px;
 margin-bottom: 15px;
}
box img {
 border: 0;
 vertical-align: middle;
}
.image-circle {
 border-radius: 50%;
}
.row {
 margin: 0 -10px;
 box-sizing: border-box;
 -moz-box-sizing: border-box;
 -webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
 content:'';
 display:table;
}
.row:after,
.entry:after {
 clear:both;
}
```
lihat hasilnya di browser :

![17 tampilan ](https://user-images.githubusercontent.com/101393632/161833338-5a311a68-47c8-4d2a-851c-65628ec33a8e.jpg)

lalu menambah artikel :
```
<hr class="divider" />
<article class="entry">
 <h2>First featurette heading.</h2>
 <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
 <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
pretium ac.</p>
</article>
<hr class="divider" />
<article class="entry">
 <h2>First featurette heading.</h2>
 <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
class="right-img">
 <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
pretium ac.</p>
</article>
```
kode CSSNya : 
```
.divider {
 border:0;
 border-top:1px solid #eeeeee;
 margin:40px 0;
}
/* entry */
.entry {
 margin: 15px 0;
}
.entry h2 {
 margin-bottom: 20px;
}
.entry p {
 line-height: 25px;
}
.entry img {
 float: left;
 border-radius: 5px;
 margin-right: 15px;
}
.entry .right-img {
 float: right;
}
```

## TUGAS
#### 1. layout di menu About
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>About</title>
    <link rel="stylesheet" href="styleabout.css" />
  </head>

  <body>
    <div id="container">
      <header>
        <h1>Layout About</h1>
      </header>

      <!-- Menambah Navigasi -->
      <nav>
        <a href="home.html">Home</a>
        <a href="artikel.html">Artikel</a>
        <a href="about.html" class="active">About</a>
        <a href="kontak.html">Kontak</a>
      </nav>

      <!-- Menambah panel hero -->
      <section id="hero">
        <h1>Apa itu HTML ?</h1>
        <p>Jika kita ingin membuat sebuah artikel didalam web, maka kita harus
          menggunakan HTML untuk membuat artikel tersebut. Kenapa kita wajib banget
          belajar HTML sebelum kita membuat sebuah web artikel ? Karena, HTML adalah
          salah satu komponen website yang sangat penting.
        </p> 
        <a href="artikel.html" class="btn btn-large">Pelajari lebih banyak &raquo;</a>
      </section>
      <!-- Menambah wrapper yang didalamnya ditambahkan hr dan article -->
      <section id="wrapper">
        <section id="main">
          <div class="row">
            <div class="box">
              <img
                src="tutwuri.jpg"
                title="Logo SD"
                class="image-circle"
                width="120px 120px"
              />
              <h3>Permata Pertiwi</h3>
              <p>
                Saya bersekolah di TK-SD Permata Pertiwi Cikarang utara.
              </p>
              <a href="https://sekolah.data.kemdikbud.go.id/index.php/chome/profil/00A33413-2CF5-E011-90FB-89A80F085030" class="btn btn-default">Lihat Selengkapnya</a>
            </div>

            <div class="box">
              <img
                src="logostit.png"
                title="Logo Haen"
                class="image-circle"
                width="120px 120px"
              />
              <h3>Hidayatunnajah</h3>
              <p>
                ini adalah Ponpes saat saya SMP-SMA. Saya ddi pesantren ini selama 6 tahun.
              </p>
              <a href="https://www.hidayatunnajah.or.id/" class="btn btn-default">Lihat Selengkapnya</a>
            </div>

            <div class="box">
              <img
                src="logo UPB.png"
                title="Logo UPB"
                class="image-circle"
                width="160px"
              />
              <h3>Universitas Pelita Bangsa</h3>
              <p>
                Ini adalah Universitas Pelita Bangsa, tempat saya berkuliah mengambil jurusan IT.
              </p>
              <a href="https://www.pelitabangsa.ac.id/" class="btn btn-default">Lihat Selengkapnya</a>
            </div>
          </div>

          <hr class="divider">
          <article class="entry">
              <h2>Biodata</h2>
              <img 
              src="alfian.png" 
              title="Foto Alfian"
              class="image-circle"
              width="150px"
              />
              <p>Nama saya adalah Alfiansyah Rambe, atau biasa dikenal Alfian. Saya adalah
              seorang mahasiswa Universitas Pelita Bangsa Cikarang. Saya mengambil Jurusan 
              Teknik Informatika, atau yang biasa dikenal oleh kalangan masyarakat yaitu IT.
              Saya lahir di Subang pada Tanggal 14 Maret 1999, yang dimana saya darah campuran
              antara sunda dan batak. Riwayat sekolah saya pada TK - SD bersekolah di Permata pertiwi
              dan SMP-SMA saya bersekolah di pondok pesantren <a href="https://www.hidayatunnajah.or.id/" style="text-decoration: none; color:black" target="_blank">Hidayatunnajah</a>
              . Setelah selesai dari pondok pesantren, saya langsung mengajar di sebuah sekolah yang berada di
              Cikarang Timur, yaitu <a href="https://rabbaanii.sch.id/" style="text-decoration: none; color:black" target="_blank">Rabbaanii Islamic School</a>. 
              Di sekolah tersebut, saya mengajar Bahasa Arab, PAI, Al Quran, Fiqih dan TIK. Status saya saat ini menikah dan sudah memiliki
              1 anak laki-laki. Sampai saat ini saya masih mengajar di Rabbaanii Islamic School.
              </p>
          </article>
        </section>

        <aside id="sidebar">
          <div class="widget-box">
            <h3 class="title">My Social Media</h3>
            <ul>
              <li><a href="https://www.facebook.com/profile.php?id=100011359782916" target="_blank">Facebook</a></li>
              <li><a href="https://www.instagram.com/piyanrambe/" target="_blank">Instagram</a></li>
              <li><a href="https://github.com/piyanrambe" target="_blank">Github</a></li>
            </ul>
          </div>

          <div class="widget-box">
            <h3 class="title">Hobi saya</h3>
            <p>
              Saya menyukai hal yang berbau Olahraga. Salah satu Olahraga yang saya tekuni sampai saat ini
              adalah Basket. Tidak hanya basket, saya juga menyukain olahraga lainnya seperti : Futsal, Renang,
              Fitness, Bulutangkis. Bahkan saya juga memiliki kemampuan berkuda dan memanah.
              Memancing pun juga menjadi salah satu hobi saya.
            </p>
          </div>
        </aside>
      </section>
      
      <footer>
        <p>&copy; 2021 - Universitas Pelita Bangsa - Alfiansyah Rambe - 312010338</p>
      </footer>
    </div>
  </body>
</html>
```
dan Hasilnya :
![18 Layout ABout](https://user-images.githubusercontent.com/101393632/161833667-7fae3af1-9c27-4325-9dab-ba19e7ed23bf.jpg)

### 2. menu COntact
```
<!DOCTYPE html>
<html lang="id" dir="ltr">
  <head>
    <meta charset="utf-8" />
    <title>kontak</title>
    <link rel="stylesheet" href="stylekontak.css">
  </head>

  <body class="bg">
    <div id="container">
      <header>
        <h1>Layout Sederhana</h1>
      </header>

      <!-- Menambah Navigasi -->
      <nav>
        <a href="home.html">Home</a>
        <a href="artikel.html">Artikel</a>
        <a href="about.html">About</a>
        <a href="kontak.html" class="active">Kontak</a>
      </nav>

      <!-- Menambah panel HERO -->
      <section id="hero">
        <h1>Pembuat Artikel ini.</h1>
        <p>
          Alfiansyah Rambe, dia adalah sesosok pemuda yang telah membuat artikel ini.
          Beliau bekerja di sebuah sekolah yang bernama Rabbaanii Islamic School, dan ia juga 
          melanjutkan pendidikan di Universitas Pelita Bangsa.
        </p>
        <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
      </section>

      <section id="wrapper">
        <section id="main">
          <div class="row">
            <fieldset>
              <legend>
                Hubungi Kami
              </legend>

              <div class="txtb">
                  <label>Nama Lengkap :</label>
                  <input type="text" name="nama Lengkap" placeholder="Ketik Nama disini...">
              </div>

              <div class="txtb">
                <label for="alamat">Alamat Email :</label>
                <input type="text" name="alamat" placeholder="Ketik Email disini...">
              </div>

              <div class="txtb">
                <label>Nomor HP :</label>
                <input type="text" name="" value="" placeholder="Ketik Nomor HP disini...">
              </div>

              <div class="txtb">
                <label>Pesan :</label>
                <textarea name="" id="" cols="5" rows="5" placeholder="Ketik pesan disini..."></textarea>
              </div>
              <a class="btnsend">Kirim</a>
            </fieldset>
          </div>
        </section>

        <aside id="sidebar">
          <div class="widget-box">
            <h3 class="title">Atau klik link dibawah ini</h3>
            <ul>
              <li><a href="https://www.facebook.com/profile.php?id=100011359782916" target="_blank">Facebook</a></li>
              <li><a href="https://www.instagram.com/piyanrambe/" target="_blank">Instagram</a></li>
              <li><a href="https://github.com/piyanrambe" target="_blank">Github</a></li>
            </ul>
            <h3 class="title">Atau Hubungi</h3>
            <ul>
              <li class="text">alfiansyahrambe140301@gmail.com</li>
              <li class="text">08123456789</li>
            </ul>
          </div>

          
        </aside>

      </section>
      <footer>
        <p>&copy; 2022 - Universitas Pelita Bangsa - Alfiansyah Rambe - 312010338</p>
      </footer>
    </div>
    
  </body>
</html>

```
dan Hasilnya :
![18 layout kontak](https://user-images.githubusercontent.com/101393632/161833799-79bb876a-ecb2-42a2-9f52-95d2104c21c7.jpg)

=============TERIMAKASIH============
