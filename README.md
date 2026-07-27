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
        }

        .card:hover{
            transform:translateY(-8px);
        }

        .card h3{
            margin-bottom:15px;
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
    <h1>Hello, I'm <span>Yutthawit</span></h1>
    <p>
        An odinary student who enjoys trveling,
        love to talk with many people, and hardworking.
    </p>

    <a href="#projects" class="btn">View My Work</a>
</section>

<section id="about">
    <h2>About Me</h2>

    <div class="about">
        <p>
            I'm a student with experience in interact with many people from different country with english language while trying too learn their language aswell,
            for example like English , Chinese, and Japanese.
            I enjoy talking and exchange our oppinion, talk about daily life, and give each other a compliment or advice.
        </p>
    </div>
</section>

<section id="projects">
    <h2>Projects</h2>

    <div class="projects">

        <div class="card">
            <h3>History</h3>
            <p>My name is Yutthawit Mobandit. I am 18 years old. I live in </p>
        </div>

        <div class="card">
            <h3>Weather App</h3>
            <p>Weather application using an API with real-time forecasts.</p>
        </div>

        <div class="card">
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
    © 2026 Your Name. All Rights Reserved.
</footer>

</body>
</html>
