<!DOCTYPE html>

<html lang="id">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Revan Parts</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        nav {
            background: #2c3e50;
            padding: 15px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
            padding: 10px;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .page {
            display: none;
            padding: 50px 20px;
            text-align: center;
        }
        .active {
            display: block;
        }
        h1, h2 {
            color: #2c3e50;
        }
        img {
            border-radius: 8px;
            margin-bottom: 20px;
        }
        form {
            background: #fff;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            display: inline-block;
            text-align: left;
        }
        input[type="text"],
        input[type="email"] {
            width: calc(100% - 22px);
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="submit"] {
            background-color: #3498db;
            color: white;
            font-weight: bold;
            border: none;
            border-radius: 5px;
            padding: 10px 15px;
            cursor: pointer;
            transition: background 0.3s;
        }
        input[type="submit"]:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>

    <nav>
        <a href="#" onclick="showPage('home')">Home</a>
        <a href="#" onclick="showPage('about')">About</a>
        <a href="#" onclick="showPage('contact')">Contact</a>
    </nav>

    <div id="home" class="page active">
        <h1>Revan Parts</h1>
        <img src="gambar.jpg" alt="Gambar Revan Parts" style="width:160px;height:160px;">
        <p>Selamat datang di Revan Parts, toko suku cadang terbaik!</p>
    </div>

    <div id="about" class="page">
        <h2>About</h2>
        <p>Revan Parts adalah toko yang menyediakan berbagai macam suku cadang berkualitas tinggi untuk kendaraan Anda.</p>
    </div>

    <div id="contact" class="page">
        <h2>Contact</h2>
        <form>
            <label for="nama">Nama :</label><br>
            <input type="text" id="nama" name="nama"><br><br>
        
            <label for="email">Email :</label><br>
            <input type="email" id="email" name="email"><br><br>
            
            <input type="submit" value="Kirim">
        </form>
    </div>

    <script>
        function showPage(pageId) {
            var pages = document.querySelectorAll('.page');
            pages.forEach(page => {
                page.classList.remove('active');
            });

            
            document.getElementById(pageId).classList.add('active');
        }
    </script>

</body>
</html>
