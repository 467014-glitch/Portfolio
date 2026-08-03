# Portfolio
Myportfolio  
History  
Aboutme  
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Portfolio</title>

    <style>
        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
            font-family:Arial, Helvetica, sans-serif;
        }

        body{
            background:#0f172a;
            color:#fff;
            line-height:1.6;
        }

        header{
            background:#111827;
            padding:20px 10%;
            display:flex;
            justify-content:space-between;
            align-items:center;
            position:sticky;
            top:0;
            z-index:100;
        }

        nav a{
            color:white;
            text-decoration:none;
            margin-left:20px;
            transition:.3s;
        }

        nav a:hover{
            color:#38bdf8;
        }

        .hero{
            display:flex;
            justify-content:center;
            align-items:center;
            height:90vh;
            text-align:center;
            flex-direction:column;
            padding:20px;
        }

        /* ===== รูปโปรไฟล์ ===== */
        .hero .avatar{
            width:150px;
            height:150px;
            border-radius:50%;
            object-fit:cover;
            border:4px solid #38bdf8;
            margin-bottom:20px;
            box-shadow:0 0 25px rgba(56,189,248,.4);
        }

        .hero h1{
            font-size:55px;
        }

        .hero span{
            color:#38bdf8;
        }

        .hero p{
            max-width:600px;
            margin:20px auto;
            color:#cbd5e1;
        }

        .btn{
            display:inline-block;
            padding:12px 25px;
            background:#38bdf8;
            color:#000;
            text-decoration:none;
            border-radius:8px;
            font-weight:bold;
            transition:.3s;
            border:none;
            cursor:pointer;
            font-size:16px;
        }

        .btn:hover{
            transform:translateY(-3px);
            background:#0ea5e9;
        }

        section{
            padding:70px 10%;
        }

        h2{
            text-align:center;
            margin-bottom:40px;
            font-size:36px;
        }

        .about{
            text-align:center;
            max-width:800px;
            margin:auto;
        }

        .projects{
            display:grid;
            grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
            gap:25px;
        }

        .card{
            background:#1e293b;
            padding:25px;
            border-radius:10px;
            transition:.3s;
            overflow:hidden;
        }

        .card:hover{
            transform:translateY(-8px);
        }

        /* ===== รูปภาพในการ์ดโปรเจกต์ ===== */
        .card img{
            width:100%;
            height:160px;
            object-fit:cover;
            border-radius:8px;
            margin-bottom:15px;
            display:block;
        }

        .card h3{
            margin-bottom:15px;
        }

        /* ===== การ์ด History ที่กดขยายได้ ===== */
        .card.expandable{
            cursor:pointer;
        }

        .card.expandable .more-hint{
            display:inline-block;
            margin-top:10px;
            color:#38bdf8;
            font-size:14px;
            font-weight:bold;
        }

        .contact{
            text-align:center;
        }

        footer{
            text-align:center;
            padding:20px;
            background:#111827;
            color:#94a3b8;
        }

        /* ===== Modal ส่วนขยายประวัติ ===== */
        .modal-overlay{
            display:none;
            position:fixed;
            top:0;
            left:0;
            width:100%;
            height:100%;
            background:rgba(0,0,0,.7);
            z-index:1000;
            justify-content:center;
            align-items:center;
            padding:20px;
        }

        .modal-overlay.active{
            display:flex;
        }

        .modal-box{
            background:#1e293b;
            max-width:600px;
            width:100%;
            border-radius:12px;
            padding:35px;
            position:relative;
            max-height:85vh;
            overflow-y:auto;
        }

        .modal-box img{
            width:120px;
            height:120px;
            border-radius:50%;
            object-fit:cover;
            border:3px solid #38bdf8;
            display:block;
            margin:0 auto 20px;
        }

        .modal-box h3{
            text-align:center;
            margin-bottom:20px;
            font-size:26px;
            color:#38bdf8;
        }

        .modal-box p{
            margin-bottom:12px;
            color:#cbd5e1;
        }

        .modal-close{
            position:absolute;
            top:15px;
            right:20px;
            background:none;
            border:none;
            color:#fff;
            font-size:26px;
            cursor:pointer;
            line-height:1;
        }

        .modal-close:hover{
            color:#38bdf8;
        }

        @media(max-width:768px){
            header{
                flex-direction:column;
            }

            nav{
                margin-top:15px;
            }

            .hero h1{
                font-size:38px;
            }
        }
    </style>
</head>
<body>

<header>
    <h2>MyPortfolio</h2>

    <nav>
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section class="hero">
    <!-- ใส่รูปโปรไฟล์ของคุณตรงนี้ เปลี่ยน src เป็นลิงก์รูปหรือไฟล์รูปของคุณ -->
    <img class="avatar" src="https://via.placeholder.com/150" alt="รูปโปรไฟล์ของ Yutthawit">

    <h1>Hello, I'm <span>Yutthawit</span></h1>
    <p>
        An ordinary student who enjoys traveling,
        loves to talk with many people, and is hardworking.
    </p>

    <a href="#projects" class="btn">View My Work</a>
</section>

<section id="about">
    <h2>About Me</h2>

    <div class="about">
        <p>
            I'm a student with experience interacting with many people from different countries in English while trying to learn their language as well,
            for example English, Chinese, and Japanese.
            I enjoy talking and exchanging opinions, discussing daily life, and giving each other compliments or advice.
        </p>
    </div>
</section>

<section id="projects">
    <h2>Projects</h2>

    <div class="projects">

        <!-- การ์ด History: กดแล้วจะเปิดส่วนขยาย (modal) แสดงประวัติแบบเต็ม -->
        <div class="card expandable" onclick="openHistoryModal()">
            <img src="https://via.placeholder.com/300x160" alt="History">
            <h3>History</h3>
            <p>My name is Yutthawit Mobandit. I am 18 years old...</p>
            <span class="more-hint">คลิกเพื่ออ่านเพิ่มเติม &raquo;</span>
        </div>

        <div class="card">
            <!-- ใส่รูปโปรเจกต์ตรงนี้ -->
            <img src="https://via.placeholder.com/300x160" alt="Weather App">
            <h3>Weather App</h3>
            <p>Weather application using an API with real-time forecasts.</p>
        </div>

        <div class="card">
            <!-- ใส่รูปโปรเจกต์ตรงนี้ -->
            <img src="https://via.placeholder.com/300x160" alt="To-Do App">
            <h3>To-Do App</h3>
            <p>A task management app with local storage support.</p>
        </div>

    </div>
</section>

<section id="contact">
    <h2>Contact</h2>

    <div class="contact">
        <p>Email: your@email.com</p>
        <p>GitHub: github.com/yourusername</p>
        <p>LinkedIn: linkedin.com/in/yourusername</p>
    </div>
</section>

<footer>
    <p>&copy; 2026 Yutthawit Mobandit. All rights reserved.</p>
</footer>

<!-- ===== Modal ส่วนขยายของ History ===== -->
<div class="modal-overlay" id="historyModal" onclick="closeHistoryModal(event)">
    <div class="modal-box" onclick="event.stopPropagation()">
        <button class="modal-close" onclick="closeHistoryModal()">&times;</button>
        <img src="https://via.placeholder.com/120" alt="รูปประวัติ">
        <h3>My History</h3>
        <p>My name is Yutthawit Mobandit. I am 18 years old and I live in Bangkok, Thailand.</p>
        <p>
            I would describe myself as an ordinary student, but one who is genuinely curious
            about the world around me. Traveling is one of my biggest passions — every new
            place I visit teaches me something about how differently people live, think, and
            connect with one another.
        </p>
        <p>
            That same curiosity is what pushed me to learn languages beyond my own. Besides
            English, I have been studying Chinese and Japanese, not just to speak them, but
            to better understand the cultures behind them. I love striking up conversations
            with people from different countries, exchanging opinions, talking about daily
            life, and simply learning from one another.
        </p>
        <p>
            I try to bring the same hardworking attitude into everything I do, whether it's
            my studies or personal projects like this portfolio. Right now I'm focused on
            building my skills in web development, and I'm excited to keep growing — both
            as a student and as someone who genuinely enjoys connecting with people.
        </p>
    </div>
</div>

<script>
    function openHistoryModal(){
        document.getElementById('historyModal').classList.add('active');
    }

    function closeHistoryModal(e){
        document.getElementById('historyModal').classList.remove('active');
    }
</script>

</body>
</html>
