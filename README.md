# Portfolio
Myportfolio  
History  
Aboutme  
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ยุทธวิชช์ โมบันดิษฐ์ — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Sarabun:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #FAF9F6;
    --bg-alt: #F1EFE9;
    --ink: #1E1D1B;
    --ink-soft: #5C5A54;
    --line: #DAD6CC;
    --accent: #6B7A5E;
    --accent-deep: #4A5740;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--ink);
    font-family: 'Sarabun', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    -webkit-font-smoothing: antialiased;
  }

  h1, h2, h3, .display {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 500;
    letter-spacing: 0.01em;
  }

  a { color: inherit; text-decoration: none; }

  ::selection { background: var(--accent); color: var(--bg); }

  .wrap {
    max-width: 980px;
    margin: 0 auto;
    padding: 0 32px;
  }

  /* ---------- NAV ---------- */
  header {
    position: sticky;
    top: 0;
    z-index: 20;
    background: rgba(250, 249, 246, 0.88);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--line);
  }
  nav {
    max-width: 980px;
    margin: 0 auto;
    padding: 20px 32px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem;
    letter-spacing: 0.05em;
  }
  .navlinks {
    display: flex;
    gap: 36px;
    font-size: 0.88rem;
    letter-spacing: 0.04em;
  }
  .navlinks a {
    position: relative;
    padding-bottom: 4px;
    color: var(--ink-soft);
    transition: color 0.25s ease;
  }
  .navlinks a:hover { color: var(--ink); }
  .navlinks a::after {
    content: '';
    position: absolute;
    left: 0; bottom: 0;
    width: 0%;
    height: 1px;
    background: var(--accent-deep);
    transition: width 0.3s ease;
  }
  .navlinks a:hover::after { width: 100%; }

  @media (max-width: 640px) {
    .navlinks { gap: 18px; font-size: 0.78rem; }
    .logo { font-size: 1.1rem; }
  }

  /* ---------- HERO ---------- */
  .hero {
    padding: 120px 0 100px;
    position: relative;
  }
  .eyebrow {
    font-size: 0.78rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--accent-deep);
    margin-bottom: 22px;
    display: inline-block;
  }
  .hero h1 {
    font-size: clamp(2.6rem, 7vw, 4.6rem);
    line-height: 1.08;
    max-width: 780px;
    font-style: italic;
  }
  .hero h1 em {
    font-style: normal;
    color: var(--accent-deep);
  }
  .hero p {
    margin-top: 28px;
    max-width: 520px;
    color: var(--ink-soft);
    font-size: 1.05rem;
  }
  .hero-cta {
    margin-top: 40px;
    display: flex;
    gap: 20px;
    align-items: center;
  }
  .btn {
    display: inline-block;
    padding: 13px 30px;
    border: 1px solid var(--ink);
    font-size: 0.85rem;
    letter-spacing: 0.05em;
    transition: all 0.3s ease;
  }
  .btn:hover {
    background: var(--ink);
    color: var(--bg);
  }
  .btn-ghost {
    border: none;
    color: var(--ink-soft);
    font-size: 0.85rem;
    letter-spacing: 0.03em;
    border-bottom: 1px solid var(--line);
    padding-bottom: 2px;
  }
  .btn-ghost:hover { border-color: var(--ink); color: var(--ink); }

  /* thin ornamental rule used as the page's signature device */
  .rule {
    width: 100%;
    height: 1px;
    background: linear-gradient(90deg, var(--line) 0%, var(--accent) 50%, var(--line) 100%);
    margin: 0;
  }

  /* ---------- SECTION SHELL ---------- */
  section { padding: 90px 0; }
  .section-head {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    margin-bottom: 56px;
    border-bottom: 1px solid var(--line);
    padding-bottom: 18px;
  }
  .section-head h2 {
    font-size: 2.1rem;
    font-style: italic;
  }
  .section-head .eyebrow { margin-bottom: 0; }

  /* ---------- ABOUT ---------- */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1.4fr;
    gap: 56px;
  }
  .about-grid p { color: var(--ink-soft); margin-bottom: 16px; }
  .facts { display: flex; flex-direction: column; gap: 18px; }
  .fact-label {
    font-size: 0.72rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--accent-deep);
  }
  .fact-value { font-size: 0.95rem; margin-top: 4px; }

  @media (max-width: 720px) {
    .about-grid { grid-template-columns: 1fr; }
  }

  /* ---------- PROJECTS ---------- */
  .projects { display: flex; flex-direction: column; }
  .project {
    display: grid;
    grid-template-columns: 90px 1fr auto;
    gap: 28px;
    align-items: baseline;
    padding: 30px 0;
    border-bottom: 1px solid var(--line);
    transition: padding-left 0.35s ease, background 0.35s ease;
  }
  .project:first-child { border-top: 1px solid var(--line); }
  .project:hover {
    padding-left: 14px;
    background: var(--bg-alt);
  }
  .project-year {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1rem;
    color: var(--ink-soft);
  }
  .project-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.6rem;
    font-style: italic;
  }
  .project-desc {
    grid-column: 2;
    color: var(--ink-soft);
    font-size: 0.92rem;
    margin-top: 6px;
    max-width: 520px;
  }
  .project-tags {
    grid-column: 2;
    display: flex;
    gap: 10px;
    margin-top: 12px;
    flex-wrap: wrap;
  }
  .tag {
    font-size: 0.72rem;
    letter-spacing: 0.04em;
    padding: 4px 10px;
    border: 1px solid var(--line);
    color: var(--ink-soft);
  }
  .project-link {
    font-size: 0.85rem;
    color: var(--accent-deep);
    white-space: nowrap;
    border-bottom: 1px solid transparent;
  }
  .project-link:hover { border-color: var(--accent-deep); }

  @media (max-width: 640px) {
    .project { grid-template-columns: 1fr; gap: 8px; }
    .project-desc, .project-tags { grid-column: 1; }
    .project-year { order: -1; }
  }

  /* ---------- SKILLS ---------- */
  .skills-row {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
  }
  .skill-pill {
    padding: 10px 20px;
    border: 1px solid var(--line);
    font-size: 0.88rem;
    color: var(--ink-soft);
    transition: border-color 0.25s ease, color 0.25s ease;
  }
  .skill-pill:hover {
    border-color: var(--accent-deep);
    color: var(--ink);
  }

  /* ---------- CONTACT ---------- */
  .contact {
    text-align: center;
    padding: 110px 0 130px;
  }
  .contact .eyebrow { margin-bottom: 20px; }
  .contact h2 {
    font-size: clamp(2.2rem, 6vw, 3.4rem);
    font-style: italic;
    margin-bottom: 30px;
  }
  .contact-links {
    display: flex;
    justify-content: center;
    gap: 34px;
    margin-top: 40px;
    flex-wrap: wrap;
    font-size: 0.92rem;
  }
  .contact-links a { color: var(--ink-soft); border-bottom: 1px solid var(--line); padding-bottom: 3px; }
  .contact-links a:hover { color: var(--ink); border-color: var(--ink); }

  footer {
    border-top: 1px solid var(--line);
    padding: 26px 0;
    text-align: center;
    font-size: 0.78rem;
    color: var(--ink-soft);
    letter-spacing: 0.03em;
  }

  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
    * { transition: none !important; }
  }

  a:focus-visible, .btn:focus-visible {
    outline: 2px solid var(--accent-deep);
    outline-offset: 3px;
  }
</style>
</head>
<body>

<header>
  <nav>
    <div class="logo">ชื่อของคุณ</div>
    <div class="navlinks">
      <a href="#about">เกี่ยวกับ</a>
      <a href="#work">ผลงาน</a>
      <a href="#skills">ทักษะ</a>
      <a href="#contact">ติดต่อ</a>
    </div>
  </nav>
</header>

<div class="wrap">
  <section class="hero">
    <span class="eyebrow">นักพัฒนาซอฟต์แวร์ · Frontend / Full-stack</span>
    <h1>สร้างงานที่<em>เรียบ</em>แต่<em>ตั้งใจ</em>ในทุกรายละเอียด</h1>
    <p>รับออกแบบและพัฒนาเว็บแอปพลิเคชันตั้งแต่แนวคิดจนถึงงานจริง เน้นโค้ดที่อ่านง่ายและอินเตอร์เฟซที่ใช้งานได้จริง</p>
    <div class="hero-cta">
      <a class="btn" href="#work">ดูผลงาน</a>
      <a class="btn-ghost" href="#contact">ติดต่อฉัน</a>
    </div>
  </section>
</div>

<div class="rule"></div>

<div class="wrap">
  <section id="about">
    <div class="section-head">
      <h2>เกี่ยวกับ</h2>
      <span class="eyebrow">01</span>
    </div>
    <div class="about-grid">
      <div class="facts">
        <div>
          <div class="fact-label">ที่ตั้ง</div>
          <div class="fact-value">กรุงเทพฯ, ประเทศไทย</div>
        </div>
        <div>
          <div class="fact-label">ประสบการณ์</div>
          <div class="fact-value">3+ ปี</div>
        </div>
        <div>
          <div class="fact-label">พร้อมรับงาน</div>
          <div class="fact-value">ใช่ — โปรเจกต์ฟรีแลนซ์</div>
        </div>
      </div>
      <div>
        <p>ผมเป็นนักพัฒนาที่สนใจเรื่องรายละเอียดเล็กๆ ที่ทำให้ผลิตภัณฑ์ใช้งานดีขึ้น ทั้งความเร็วในการโหลด การจัดวางที่สบายตา และโค้ดที่ทีมอื่นอ่านต่อได้ง่าย</p>
        <p>ก่อนหน้านี้ทำงานร่วมกับทีมสตาร์ทอัพและธุรกิจขนาดเล็ก ช่วยแปลงไอเดียให้กลายเป็นผลิตภัณฑ์ที่ใช้งานได้จริง ตั้งแต่การออกแบบระบบไปจนถึงการดูแลหลังเปิดใช้งาน</p>
      </div>
    </div>
  </section>
</div>

<div class="rule"></div>

<div class="wrap">
  <section id="work">
    <div class="section-head">
      <h2>ผลงานคัดสรร</h2>
      <span class="eyebrow">02</span>
    </div>
    <div class="projects">

      <div class="project">
        <div class="project-year">2026</div>
        <div class="project-title">ชื่อโปรเจกต์หนึ่ง</div>
        <div class="project-desc">แพลตฟอร์มจัดการงานสำหรับทีมขนาดเล็ก ออกแบบใหม่ทั้งระบบเพื่อลดเวลาการทำงานซ้ำซ้อน</div>
        <div class="project-tags">
          <span class="tag">React</span>
          <span class="tag">Node.js</span>
          <span class="tag">PostgreSQL</span>
        </div>
        <a class="project-link" href="#" target="_blank" rel="noopener">ดูโปรเจกต์ →</a>
      </div>

      <div class="project">
        <div class="project-year">2025</div>
        <div class="project-title">ชื่อโปรเจกต์สอง</div>
        <div class="project-desc">เว็บแอปสำหรับติดตามค่าใช้จ่ายส่วนตัว พร้อมกราฟสรุปรายเดือนแบบเรียลไทม์</div>
        <div class="project-tags">
          <span class="tag">Vue</span>
          <span class="tag">Firebase</span>
        </div>
        <a class="project-link" href="#" target="_blank" rel="noopener">ดูโปรเจกต์ →</a>
      </div>

      <div class="project">
        <div class="project-year">2025</div>
        <div class="project-title">ชื่อโปรเจกต์สาม</div>
        <div class="project-desc">API สำหรับระบบจองคิวออนไลน์ รองรับผู้ใช้งานพร้อมกันหลักพันคน</div>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag">FastAPI</span>
          <span class="tag">Docker</span>
        </div>
        <a class="project-link" href="#" target="_blank" rel="noopener">ดูโปรเจกต์ →</a>
      </div>

    </div>
  </section>
</div>

<div class="rule"></div>

<div class="wrap">
  <section id="skills">
    <div class="section-head">
      <h2>ทักษะ &amp; เครื่องมือ</h2>
      <span class="eyebrow">03</span>
    </div>
    <div class="skills-row">
      <span class="skill-pill">JavaScript / TypeScript</span>
      <span class="skill-pill">React</span>
      <span class="skill-pill">Node.js</span>
      <span class="skill-pill">Python</span>
      <span class="skill-pill">PostgreSQL</span>
      <span class="skill-pill">Docker</span>
      <span class="skill-pill">Git &amp; GitHub</span>
      <span class="skill-pill">Figma</span>
    </div>
  </section>
</div>

<div class="wrap">
  <section id="contact" class="contact">
    <span class="eyebrow">04 — ติดต่อ</span>
    <h2>มาคุยกันเรื่องงานถัดไป</h2>
    <p style="color: var(--ink-soft); max-width: 460px; margin: 0 auto;">เปิดรับโปรเจกต์ใหม่และโอกาสร่วมงาน ทักมาได้เลยครับ</p>
    <div class="contact-links">
      <a href="mailto:youremail@example.com">youremail@example.com</a>
      <a href="https://github.com/yourusername" target="_blank" rel="noopener">GitHub</a>
      <a href="https://linkedin.com/in/yourusername" target="_blank" rel="noopener">LinkedIn</a>
    </div>
  </section>
</div>

<footer>
  © 2026 ชื่อของคุณ · สร้างด้วยความตั้งใจ
</footer>

</body>
</html>
