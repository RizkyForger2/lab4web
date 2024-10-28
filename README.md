<h2>1.membuat lab4_box.html</h2>
  
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>box element</title>
  </head>
  <body>
      <header>
          <h1>box element</h1>
      </header>
  
  </body>
  </html>

  ![image](https://github.com/user-attachments/assets/7c2470d5-0fec-43c4-b29f-d366638363d7)

<h2>2.membuat box element</h2>

  <section>
      <div class="div1">Div 1</div>
      <div class="div2">Div 2</div>
      <div class="div3">Div 3</div>
  </section>

<h2>menambahkan css float property</h2>

  <style>
      div {
      float:left;
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
  </style>

  ![Screenshot 2024-10-28 114635](https://github.com/user-attachments/assets/8bcbe165-1217-4aa5-87bd-84a877938b8d)

  <h2>3. mengatur clearfix element</h2>
  
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk mengaturnya.

  <section>
      <div class="div1">Div 1</div>
      <div class="div2">Div 2</div>
      <div class="div3">Div 3</div>
      <div class="div4">Div 4</div>
  </section>

tambahkan property clear pada css
  .div4 {
  background-color: blue;
  clear: left;
  float: none;
  }

![Screenshot 2024-10-28 115131](https://github.com/user-attachments/assets/a57c34ca-5c5b-467e-a48a-fb109418b4a1)

menambahkan div 4 atau kotak keempat dengan warna biru lalu diatur clear pada property untuk menghentikan efek float dari elemen sebelumnya, kemudian kotak tersebut muncul dibawah ketiga kotak diatas. ini berfungsi untuk memengatur aliran tata letak dalam mendesain halaman

Membuat layout sederhana

  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Layout Sederhana</title>
      <link rel="stylesheet" href="style.css">
  </head>
  <body>
      <div id="container">

    
  </body>
  </html>
kemudian buat kerangka layout dengan semantics element seperti berikut

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

![Screenshot 2024-10-28 120115](https://github.com/user-attachments/assets/348433aa-5b94-43f1-8188-4c3e9a129654)

kemudian tambahkan kode css untuk membuat layoutnya

  /* import google font */
  @import
  url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
  @import
  url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');
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

  ![Screenshot 2024-10-28 120800](https://github.com/user-attachments/assets/e6fbefc2-8501-4a3d-bf10-ded4ad5e2434)

  membuat navigasi
  
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

![Screenshot 2024-10-28 121007](https://github.com/user-attachments/assets/90f67309-33c5-4149-a0cf-bdbef0547ca6)

membuat hero panel

  <section id="hero">
              <h1>Hello World!</h1>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
              elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
              vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
              pretium ac.</p>
              <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
          </section>
css

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

![Screenshot 2024-10-28 121157](https://github.com/user-attachments/assets/5dad355e-899c-4f5e-9da2-b0390b31a7ea)

mengatur layout main dan sidebar

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
  
membuat sidebar widget

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
          
menambahkan css

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

     ![Screenshot 2024-10-28 121729](https://github.com/user-attachments/assets/765da1bb-8e82-48d1-8b3b-61f3f48041f4)

mengatur footer

  /* footer */
  footer {
      clear:both;
      background-color:#1d1d1d;
      padding:20px;
      color:#eee;
  }

  ![Screenshot 2024-10-28 121902](https://github.com/user-attachments/assets/76e328dc-c5e4-4a89-8e5a-4400a1893710)

  menambahkan elemen lainnya pada main content
  
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
             
css

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

  ![Screenshot 2024-10-28 125027](https://github.com/user-attachments/assets/83ed0fb5-4115-41a7-b0ce-7f9f172553fc)
  
menambahkan content artikel

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
          
tambahka css

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

  ![Screenshot 2024-10-28 125306](https://github.com/user-attachments/assets/97ac9fd1-e361-45bf-b84d-d070136397aa)

<h1>jawaban dan tugas <h1/>
tambahkan layout untuk menu about
HTML

    <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>About Us</title>
      <link rel="stylesheet" href="portofolio.css">
  </head>
  <body>
      <div class="container">
          <section class="header">
              <h1>Tentang Kami</h1>
              <p>Menjelajahi siapa kami dan apa yang kami lakukan</p>
          </section>
          <section class="description">
              <h2>Deskripsi</h2>
              <p>Kami adalah tim yang berdedikasi untuk menyediakan layanan terbaik bagi pelanggan kami. Visi kami adalah...</p>
              <img src="kairiizky.png" alt="Our Team" class="team-image">
          </section>
          <section class="portfolio">
              <h2>Portfolio</h2>
              <div class="portfolio-item">
                  <img src="wallpaperflare.com_wallpaper(8).jpg" alt="Project 1">
                  <h3>Project 1</h3>
                  <p>Deskripsi singkat tentang proyek 1.</p>
              </div>
              <div class="portfolio-item">
                  <img src="wallpaperflare.com_wallpaper(4).jpg" alt="Project 2">
                  <h3>Project 2</h3>
                  <p>Deskripsi singkat tentang proyek 2.</p>
              </div>
          </section>
          <section class="team">
              <h2>Tim Kami</h2>
              <div class="team-member">
                  <img src="8264511.jpg" alt="Member 1">
                  <h3>Nama Anggota</h3>
                  <p>Posisi dan deskripsi singkat.</p>
              </div>
          </section>
        <div class="container">
            <section class="header">
                <h1>Hubungi Kami</h1>
                <p>Isi formulir di bawah ini untuk menghubungi kami</p>
            </section>
            <section class="contact-form">
                <form action="#" method="POST">
                    <label for="name">Nama:</label>
                    <input type="text" id="name" name="name" required>
    
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>
    
                    <label for="phone">Telepon (Opsional):</label>
                    <input type="text" id="phone" name="phone">
    
                    <label for="message">Pesan:</label>
                    <textarea id="message" name="message" rows="4" required></textarea>
    
                    <button type="submit">Kirim</button>
                </form>
            </section>
        </div>
      </div>
  </body>
  </html>

![Screenshot 2024-10-28 134901](https://github.com/user-attachments/assets/88ad4d1f-4950-4f95-99b4-e1ddb752b2f8)
![Screenshot 2024-10-28 134915](https://github.com/user-attachments/assets/3811e749-2ec6-4963-aea0-42fa6d4ac8e7)

CSS

    /* Reset */
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    /* General Styling */
    .container {
        max-width: 1000px;
        margin: auto;
        padding: 20px;
        font-family: Arial, sans-serif;
    }
    
    header, section {
        margin-bottom: 40px;
    }
    
    h1, h2, h3 {
        color: #333;
    }
    
    p {
        color: #555;
    }
    
    /* Header Section */
    .header {
        text-align: center;
        margin-bottom: 20px;
    }
    
    /* Description Section */
    .description {
        text-align: center;
    }
    
    .description .team-image {
        width: 100%;
        max-width: 600px;
        margin-top: 10px;
        border-radius: 8px;
    }
    
    /* Portfolio Section */
    .portfolio {
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
        justify-content: space-around;
    }
    
    .portfolio-item {
        width: 100%;
        max-width: 300px;
        text-align: center;
    }
    
    .portfolio-item img {
        width: 100%;
        border-radius: 8px;
    }
  
    /* Team Section */
    .team {
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
        justify-content: space-around;
    }
    
    .team-member {
        width: 100%;
        max-width: 200px;
        text-align: center;
    }
    
    .team-member img {
        width: 100%;
        border-radius: 50%;
    }
    
        /* Contact Form */
    .contact-form {
        max-width: 600px;
        margin: auto;
    }
    
    .contact-form label {
        display: block;
        margin-top: 15px;
        color: #333;
    }
    
    .contact-form input, .contact-form textarea {
        width: 100%;
        padding: 10px;
        margin-top: 5px;
        border: 1px solid #ccc;
        border-radius: 4px;
        font-size: 16px;
    }
    
    .contact-form button {
        margin-top: 20px;
        padding: 10px 20px;
        background-color: #333;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
    }
    
    .contact-form button:hover {
        background-color: #555;
    }

![Screenshot 2024-10-28 135932](https://github.com/user-attachments/assets/7f2a75bd-c7c3-437b-8c4b-e2a6b58a562e)




