<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lishan Li | Phonetics & Dialectology</title>
    <style>
        /* === 全局设置 === */
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            background-color: #f4f7f6; /* 稍微灰一点的背景，更有质感 */
            color: #333;
            margin: 0;
            line-height: 1.6;
            padding-top: 60px; /* 给固定导航栏留位置 */
        }
        a { color: #0056b3; text-decoration: none; transition: color 0.2s;}
        a:hover { color: #003d82; text-decoration: underline; }

        /* === 顶部导航栏 (新增) === */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px); /* 毛玻璃效果，很潮 */
            border-bottom: 1px solid #eaeaea;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .nav-container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 60px;
        }
        .nav-logo { font-weight: 700; font-size: 1.2em; color: #333; }
        .nav-links { display: flex; gap: 25px; }
        .nav-links a { color: #555; font-weight: 500; font-size: 0.95em; }
        .nav-links a:hover { color: #0056b3; text-decoration: none; }

        /* === 页面主体布局 === */
        .container {
            display: flex;
            max-width: 1100px;
            margin: 40px auto;
            padding: 20px;
            gap: 50px;
        }

        /* === 左侧边栏 (Sidebar) === */
        .sidebar {
            flex: 0 0 260px;
            text-align: center;
        }
        .avatar {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            border: 4px solid #fff;
            margin-bottom: 15px;
            transition: transform 0.3s;
        }
        .avatar:hover { transform: scale(1.05); } /* 鼠标放上去会放大一点 */
        
        .name { font-size: 1.6em; font-weight: 700; margin-bottom: 5px; color: #222; }
        .title { color: #666; font-size: 0.95em; margin-bottom: 20px; font-weight: 400; }
        
        .contact-box {
            text-align: left;
            font-size: 0.9em;
            color: #555;
            background: #fff;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }
        .contact-item { margin-bottom: 12px; display: flex; align-items: center; }
        .icon { margin-right: 10px; width: 20px; text-align: center; }
        .btn-cv {
            display: block;
            background-color: #0056b3;
            color: white !important;
            text-align: center;
            padding: 8px 0;
            border-radius: 6px;
            margin-top: 15px;
            font-weight: 600;
            text-decoration: none !important;
            transition: background 0.3s;
        }
        .btn-cv:hover { background-color: #004494; }

        /* === 右侧内容 (Main Content) === */
        .main-content {
            flex: 1;
            background: #fff;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.03);
        }
        
        /* 章节样式 */
        section { margin-bottom: 50px; scroll-margin-top: 80px; /* 防止被导航栏挡住 */ }
        h2 { 
            font-size: 1.5em; 
            margin-bottom: 20px; 
            color: #111; 
            border-bottom: 2px solid #f0f0f0; 
            padding-bottom: 10px;
            display: flex;
            align-items: center;
        }
        h2 span { margin-right: 10px; }

        /* 列表与文章样式 */
        .news-list { list-style: none; padding: 0; }
        .news-list li { margin-bottom: 12px; padding-left: 20px; position: relative; color: #444; }
        .news-list li::before { content: "•"; color: #0056b3; font-weight: bold; position: absolute; left: 0; }
        
        .paper-item { margin-bottom: 25px; }
        .paper-title { font-weight: 700; color: #222; font-size: 1.05em; }
        .paper-authors { color: #555; font-size: 0.95em; margin: 4px 0; }
        .paper-venue { font-style: italic; color: #0056b3; font-size: 0.9em; }
        
        .project-item { margin-bottom: 25px; }
        .project-title { font-weight: 700; font-size: 1.1em; color: #333; margin-bottom: 5px;}
        .project-desc { color: #555; font-size: 0.95em; text-align: justify;}

        /* 手机适配 */
        @media (max-width: 768px) {
            .container { flex-direction: column; gap: 30px; margin-top: 20px; }
            .sidebar { width: 100%; }
            .navbar .nav-links { display: none; } /* 手机上暂时隐藏导航链接，保持简洁 */
            .navbar .nav-logo { margin: 0 auto; }
        }
    </style>
</head>
<body>

<nav class="navbar">
    <div class="nav-container">
        <a href="#" class="nav-logo">Lishan Li</a>
        <div class="nav-links">
            <a href="#home">Home</a>
            <a href="#news">News</a>
            <a href="#research">Research</a>
            <a href="#publications">Publications</a>
        </div>
    </div>
</nav>

<div class="container" id="home">
    <aside class="sidebar">
        <img src="https://avatars.githubusercontent.com/u/9919?v=4" alt="Lishan Li" class="avatar">
        
        <div class="name">Lishan Li (李丽珊)</div>
        <div class="title">M.A. in Chinese Linguistics<br>Beijing Normal University</div>
        
        <div class="contact-box">
            <div class="contact-item"><span class="icon">📍</span> Beijing, China</div>
            <div class="contact-item"><span class="icon">📧</span> lilishan0121@gmail.com</div>
            <div class="contact-item"><span class="icon">🏫</span> School of Chinese Language & Lit, BNU</div>
            
            <a href="./Lishan_Li_CV_2025.pdf" class="btn-cv">Download CV</a>
        </div>
    </aside>

    <main class="main-content">
        
        <section id="about">
            <h2>👋 Introduction</h2>
            <p>
                Hello! I am a linguistics researcher passionate about <strong>Phonetics</strong> and <strong>Dialectology</strong>.
            </p>
            <p>
                My research interests lie in the evolution of tones in Chinese dialects, specifically how they merge over time and how they interact with musical melodies. I combine traditional <strong>fieldwork</strong> (recording diverse dialect speakers) with <strong>computational modeling</strong> (using Python/R) to decode the mechanism of sound change.
            </p>
            <p>
                I obtained my M.A. from <strong>Beijing Normal University</strong> [cite: 4, 5] and B.A. from <strong>Shandong University</strong>[cite: 11, 12].
            </p>
        </section>

        <section id="news">
            <h2>🔥 News</h2>
            <ul class="news-list">
                <li><strong>[Aug 2025]</strong> Presented our work on <em>Cantonese Tone Merging</em> orally at <strong>Interspeech 2025</strong>. [cite: 27, 28]</li>
                <li><strong>[Jun 2025]</strong> Graduated from Beijing Normal University. [cite: 7]</li>
                <li><strong>[2024]</strong> Paper on dialect loss published in <strong>JASA</strong>. [cite: 20, 21]</li>
            </ul>
        </section>

        <section id="research">
            <h2>🧪 Research Projects</h2>
            
            <div class="project-item">
                <div class="project-title">Tone-Melody Interaction Across Chinese Dialects</div>
                <div class="project-desc">
                    Constructed a large-scale corpus of 2,000 Chinese folk songs to align melody (MIDI) with dialectal phonological data. Developed a computational pipeline to quantify tone-melody correspondence, revealing high tonal consistency in Cantonese and Minnan dialects. [cite: 52, 54, 55, 56]
                </div>
            </div>

            <div class="project-item">
                <div class="project-title">Mechanism of Tone Acquisition in Bilingual Environments</div>
                <div class="project-desc">
                    Investigated Mandarin tone acquisition in children with dialect exposure. Recorded 182 children during fieldwork and found that dialect exposure causes persistent pitch target interference. [cite: 58, 60, 61, 62]
                </div>
            </div>

            <div class="project-item">
                <div class="project-title">Mechanisms of Chinese Tone Category Change</div>
                <div class="project-desc">
                    Investigated sound change mechanisms in Cantonese and Min dialects using acoustic experiments. Found that tone mergers in production are influenced by lexical competition and socioeconomic factors. [cite: 63, 66, 68, 69]
                </div>
            </div>
        </section>

        <section id="publications">
            <h2>📝 Publications</h2>

            <div class="paper-item">
                <div class="paper-title">The influence of dialect loss on tone perception: Diminishing voice quality cues in preserved tone contrast</div>
                <div class="paper-authors">Zhang, Y., <strong>Li, L.</strong>, Lai, W., & Xu, X. (2024)</div>
                <div class="paper-venue">Journal of the Acoustical Society of America (JASA), 156(6):3707-3722. [cite: 20, 21, 22]</div>
                <div>[<a href="#">PDF</a>]</div>
            </div>

            <div class="paper-item">
                <div class="paper-title">Lexical competition in the process of Cantonese tone merging: Diverse Impact Mechanisms Across Different Individuals and Tone Pairs</div>
                <div class="paper-authors"><strong>Li, L.</strong>, Zhou, Y., & Xu, X. (2025)</div>
                <div class="paper-venue">In Proc. of Interspeech 2025 (Oral Presentation). [cite: 27, 28]</div>
            </div>

            <div class="paper-item">
                <div class="paper-title">Level-Tone Merger in Production and Perception: Study in two Chinese Min Dialects</div>
                <div class="paper-authors">Wu, Y., <strong>Li, L.</strong>, & Xu, X. (2025)</div>
                <div class="paper-venue">In Proc. of International Conference on Asian Language Processing (IALP). [cite: 29, 30]</div>
            </div>
            
            <div class="paper-item">
                <div class="paper-title">Multiple Patterns of Merging Guangzhou Cantonese Tones in Production and Perception: Study on Youth Groups</div>
                <div class="paper-authors"><strong>Li, L.</strong> & Xu, X. (2024)</div>
                <div class="paper-venue">In Proc. of ISCSLP 2024 (Oral Presentation). [cite: 31, 32]</div>
            </div>

        </section>

    </main>
</div>

</body>
</html>
