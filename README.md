<h1>1. membuat lab4_box.html</h1>

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

![image](https://github.com/user-attachments/assets/587a8bcb-e59d-4e8f-97cc-cc75b547b202)


<h1>2. membuat box element</h1>

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

![image](https://github.com/user-attachments/assets/fd81fda8-ffe5-459f-93a4-8f5754ea8d24)

tiga kotak div berwarna merah,kuning dan hijau diatur secara sejajar horizontal
menggunakan properti float

<h1>3. mengatur clearfix element</h1>
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk
mengaturnya.

    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
    </section>
    
<h2>tambahkan property clear pada css</h2>

    .div4 {
    background-color: blue;
    clear: left;
    float: none;
    }
    
![Screenshot 2024-10-28 085910](https://github.com/user-attachments/assets/1477a34d-3b31-4f82-b678-ae39614a4f32)



menambahkan div 4 atau kotak keempat dengan warna biru lalu diatur clear pada property 
untuk menghentikan efek float dari elemen sebelumnya, kemudian kotak tersebut muncul
dibawah ketiga kotak diatas. ini berfungsi untuk memengatur aliran tata letak dalam
mendesain halaman

<h1>Membuat layout sederhana</h1>

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
    
<h1>kemudian buat kerangka layout dengan semantics element seperti berikut</h1>

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

![Screenshot 2024-10-28 090530](https://github.com/user-attachments/assets/5ec83b16-ce7d-468e-a174-7c7f11034528)


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


![Screenshot 2024-10-28 091737](https://github.com/user-attachments/assets/40b0d60c-fd30-4c3d-ae0f-c91ce364de6d)

<h1>membuat navigasi</h1>

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

![Screenshot 2024-10-28 092234](https://github.com/user-attachments/assets/f5c2d0a1-4e77-4dcd-b929-a2c0f0cdbe3a)


<h1>membuat hero panel</h1>

    <section id="hero">
                <h1>Hello World!</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                pretium ac.</p>
                <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
            </section>
<h2>css</h2>

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


![Screenshot 2024-10-28 092412](https://github.com/user-attachments/assets/d1cbedb2-7598-4b98-90b9-81ff90598a83)


<h1>mengatur layout main dan sidebar</h1>

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

<h1>membuat sidebar widget</h1>

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

<h1>menambahkan css</h1>

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

![image](https://github.com/user-attachments/assets/fcb788eb-2b32-4ebb-86cc-571e17474dd6)


<h1>mengatur footer</h1>

    /* footer */
    footer {
        clear:both;
        background-color:#1d1d1d;
        padding:20px;
        color:#eee;
    }

![image](https://github.com/user-attachments/assets/c1ff8137-dd0f-4f81-a06c-d45130206d37)

<h1>menambahkan elemen lainnya pada main content</h1>

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

<h1>css</h1>

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

![image](https://github.com/user-attachments/assets/b89b8074-e50e-4f2e-aff9-a02439291b6e)


<h1>menambahkan content artikel</h1>

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

<h1>tambahka css</h1>

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

![image](https://github.com/user-attachments/assets/0e6d219e-6a25-4cc7-82b5-286dbadb4197)

<h1>jawaban dan tugas</h1>

<h2>tambahkan layout untuk menu about</h2>

<H3>HTML</H3>

