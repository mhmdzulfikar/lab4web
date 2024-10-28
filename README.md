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

![image](https://github.com/user-attachments/assets/37199344-9650-4ae5-a7e9-0a729af52d53)

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

![image](https://github.com/user-attachments/assets/2000f4dd-f616-4fe8-9de0-83a49267f798)

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

![image](https://github.com/user-attachments/assets/faa9cd48-85ff-46e1-a497-a97f74bf4866)

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

![image](https://github.com/user-attachments/assets/f60fe218-e634-4aed-a231-cd4d391a95f7)

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

![image](https://github.com/user-attachments/assets/e25eeb8b-d83a-4638-82f5-5c9b26ed19ae)


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

            <section class="section">
                <div class="header">
                    <h1>About Me</h1>
                </div>
                <div class="about-content">
                    <img src="image.png" alt="About Me" width="300">
                    <div class="about-text">
                        <p>Hello! I'm Agus sunardi, a passionate developer and designer. I specialize in creating beautiful and user-friendly interfaces with a focus on simplicity and elegance.</p>
                        <p>With a background in both design and development, I bring a unique perspective to every project. I love tackling complex problems and turning them into delightful user experiences.</p>
                    </div>
                </div>
            </section>
    
            <!-- Portfolio Section -->
            <section class="section">
                <div class="header">
                    <h1>My Portfolio</h1>
                </div>
                <div class="portfolio">
                    <!-- Portfolio Item 1 -->
                    <div class="portfolio-item">
                        <img src="project1.jpg" alt="Project 1">
                        <h3>Project Title 1</h3>
                        <p>Short description of the project.</p>
                    </div>
                    <!-- Portfolio Item 2 -->
                    <div class="portfolio-item">
                        <img src="project2.jpg" alt="Project 2">
                        <h3>Project Title 2</h3>
                        <p>Short description of the project.</p>
                    </div>
                    <!-- Add more portfolio items as needed -->
                </div>
            </section>

<h3>CSS</h3>


    .section {
        padding: 40px 0;
    }
    
    .header {
        text-align: center;
        padding-bottom: 20px;
    }
    
    .header h1 {
        font-size: 2.5em;
        color: #333;
    }
    
    .about-content {
        display: flex;
        align-items: flex-start;
        gap: 20px;
    }
    
    .about-content img {
        max-width: 100%;
        height: auto;
        border-radius: 10px;
    }
    
    .about-text {
        max-width: 600px;
    }
    
    .about-text p {
        color: #555;
        line-height: 1.6;
    }
    
    .portfolio {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        margin-top: 40px;
    }
    
    .portfolio-item {
        background-color: #fff;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease;
    }
    
    .portfolio-item:hover {
        transform: translateY(-10px);
    }
    
    .portfolio-item img {
        max-width: 100%;
        height: auto;
        border-radius: 5px;
    }
    
    .portfolio-item h3 {
        margin-top: 15px;
        font-size: 1.2em;
        color: #333;
    }

![image](https://github.com/user-attachments/assets/d480788f-d358-444c-b647-8c47783f5f80)


<h2>2. menambahkan layout untuk menu contact</h2>

<h3>HTML</h3>

        <section class="section">
            <div class="header">
                <h1>Contact Me</h1>
            </div>
            <div class="contact-form">
                <form action="#" method="post">
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" rows="5" required></textarea>
                    </div>
                    <button type="submit">Send Message</button>
                </form>
            </div>
        </section>

<h3>CSS</h3>

    .contact-form {
        max-width: 600px;
        margin: 0 auto;
        padding: 20px;
        background-color: #fff;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    
    .contact-form form {
        display: flex;
        flex-direction: column;
    }
    
    .form-group {
        margin-bottom: 15px;
    }
    
    .form-group label {
        font-weight: bold;
        color: #333;
        margin-bottom: 5px;
        display: block;
    }
    
    .form-group input,
    .form-group textarea {
        width: 100%;
        padding: 10px;
        border-radius: 5px;
        border: 1px solid #ddd;
        font-size: 1em;
        color: #333;
    }
    
    .form-group input:focus,
    .form-group textarea:focus {
        border-color: #555;
        outline: none;
    }
    
    button[type="submit"] {
        background-color: #333;
        color: #fff;
        padding: 12px;
        border: none;
        border-radius: 5px;
        font-size: 1em;
        cursor: pointer;
        transition: background-color 0.3s;
    }
    
    button[type="submit"]:hover {
        background-color: #555;
    }

![image](https://github.com/user-attachments/assets/1621cc6c-cac2-4b01-9000-b622bc72b866)
