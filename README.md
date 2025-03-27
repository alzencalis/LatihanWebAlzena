<!DOCTYPE html>
<html>
<head>
    <title>About Me</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            background: 
                radial-gradient(circle, rgba(255,255,255,0.2) 10%, transparent 10%) 0px 0px / 50px 30px,
                linear-gradient(135deg, #ff416c, #ff4b2b );
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Poppins', sans-serif;
            overflow: hidden;
            transition: background 0.5s ease;
        }

        @keyframes twinkle {
            0% { opacity: 0.3; }
            50% { opacity: 1; }
            100% { opacity: 0.3; }
        }
        
        .slider-container {
            width: 380px;
            height: 580px;
            position: relative;
            overflow: hidden;
            border-radius: 20px;
            box-shadow: 0px 8px 32px rgba(0, 0, 0, 0.2);
        }

        .slider {
            display: flex;
            width: 200%;
            height: 100%;
            transition: transform 0.6s ease-in-out;
        }
        
        .card1 {
            background: rgba(255, 182, 193, 0.2);
            box-shadow: 0px 8px 32px rgba(0, 0, 0, 0.2);
            border-radius: 20px;
            padding: 25px 30px;
            width: 350px; 
            height: 550px; 
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            border: 1px solid rgba(255, 255, 255, 0.5);
            position: relative;
        }

        .card2 {
            background: rgba(255, 182, 193, 0.2);
            box-shadow: 0px 8px 32px rgba(0, 0, 0, 0.2);
            border-radius: 20px;
            padding: 25px 30px;
            width: 350px; 
            height: 550px; 
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            border: 1px solid rgba(255, 255, 255, 0.5);
            position: relative;
        }

        h1 {
            color: white;
            font-size: 2.7rem;
            font-weight: 900;
            margin-bottom: 3px;
            margin-top: 1px;
            text-shadow: 0px 0px 10px violet;
        }

        h2 {
            color: white;
            font-size: 0.8rem;
            font-weight: 800;
            background-color: #E30E4E;
            padding: 8px 15px;
            border-radius: 15px;
            width: 75%;
            margin-bottom: 15px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5);
        }
        
        h3 {
            color: white;
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 3px;
            margin-top: 5px;
            text-shadow: 0px 0px 10px violet;
        }

        .bio {
            width: 85%;
            text-align: justify;
            color: white;
            font-size: 0.7rem;
            font-weight: 500;
            margin: 3px 0;
            padding: 3px;
            border: 1px solid white;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.1);
        }

        .bio b {
            color: white;
        }
        
        .bio2 {
            width: 95%;
            text-align: justify;
            color: white;
            font-size: 0.7rem;
            font-weight: 500;
            margin: 3px 0;
            padding: 3px;
            border: 1px solid white;
            text-indent: 20px; /* Menjorok ke depan */
            display: block;             
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.1);
        }

        .bio2 b {
            color: white;
        }


        a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        a:hover {
            color: khaki;
        }

        img {
            width: 150px; 
            height: 130px;
            border-radius: 15px;
            margin-bottom: 15px;
            object-fit: cover;
            border: 2px solid pink;
            box-shadow: 0px 0px 10px violet;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        img:hover {
            transform: scale(1.05);
            box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.3);
        }

        .warp-button {
            background-color: #fff;
            color: #ff416c;
            border: none;
            padding: 10px 20px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 10px;
            cursor: arrow;
            margin-top: 15px;
            box-shadow: 0px 4px 10px rgba(255, 255, 255, 0.5);
            transition: background 0.3s ease, color 0.3s ease;
        }

        .warp-button:hover {
            background-color: #ff416c;
            color: pink;
        }

        .nav-buttons {
            position: absolute;
            width: 96%;
            bottom: 10px;
            display: flex;
            justify-content: space-between;
            padding: 5px;

        }

        .nav-button {
            background: rgba(255, 255, 255, 0.7);
            border: none;
            border-radius: 50%;
            width: 35px;
            height: 35px;
            cursor: pointer;
            padding: 8px 12px;
            color: #ff416c;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
            transition: background 0.5s ease, transform 0.5s ease;
        }

        .nav-button:hover {
            background: khaki;
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <div class="slider-container">
        <div class="slider" id="slider">
     <!-- Card 1 -->
    <div class="card1">
        <h1>About Me</h1>
        <h2>Hi, it's Zen! Nice to know you!</h2>
        <img src="ALZENA.jpg" alt="Foto Zena">
        <p class="bio"><b>Nama Lengkap:</b> Alzena Calista Salsabila</p>
        <p class="bio"><b>Nama Panggilan:</b> Zena</p>
        <p class="bio"><b>Usia:</b> 20 Tahun</p>
        <p class="bio"><b>Alamat:</b> Ciledug, Tangerang</p>
        <p class="bio"><b>Agama:</b> Islam</p>
        <p class="bio"><b>Pendidikan:</b> 
            <a href="https://feb.uns.ac.id/feb/s1_bisnisdigital/">Bisnis Digital</a>, 
            <a href="https://uns.ac.id/id/">UNS</a>
        </p>
        <p class="bio"><b>Instagram:</b> 
            <a href="https://www.instagram.com/alzenacalis?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==">@Alzencalis</a>
        </p>
    </div>
    <!-- Card 2 -->
            <div class="card2">
                <h3>A little introduction of me</h3>
                <p class="bio2">
                    I am a third-year Digital Business student, Known for being a fast learner and adaptable, always eager to take on new challenges and continuously improve. Also, expertise in social media marketing, content creation, and business strategy. I have led initiatives that increased brand visibility and community engagement, securing partnerships with 40+ media outlets and 5 influencers. My work has resulted in a 25% rise in engagement, 20% follower growth, and a 15% increase in event participation.</p>
                    
           <p class="bio2"> My intermediate English proficiency, both spoken and written, helps me communicate well and build valuable partnerships. With a strong interest in marketing and public relations, I enjoy developing impactful campaigns that connect with audiences and promote positive brand growth. Additionally, as a TikTok creator (@zenzenca), I share beauty, food, and lifestyle content, focusing on authenticity and innovation.My content includes product and place reviews, personal updates, and innovative ideas, with a focus on continuous growth.
                </p>
            <a href="https://www.linkedin.com/in/alzenacalistasalsabila" target="_blank" rel="noopener noreferrer">
            <button class="warp-button">Let's Connect!</button>
        </a>
            </div>
        </div>

        <!-- Tombol Navigasi -->
        <div class="nav-buttons">
            <button class="nav-button" onclick="prevSlide()"><</button>
            <button class="nav-button" onclick="nextSlide()">></button>
        </div>
    </div>

    <script>
        let currentIndex = 0;
        const slider = document.getElementById('slider');

        function nextSlide() {
            currentIndex = (currentIndex + 1) % 2;
            slider.style.transform = `translateX(-${currentIndex * 50}%)`;
        }

        function prevSlide() {
            currentIndex = (currentIndex - 1 + 2) % 2;
            slider.style.transform = `translateX(-${currentIndex * 50}%)`;
        }

        setInterval(nextSlide, 10000);
        
    </script>
    
</body>
</html>
