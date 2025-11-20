<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lishan Li | Phonetics & Computation</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Newsreader:ital,wght@0,400;0,600;1,400&family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

    <style>
        /* === 全局变量 === */
        :root {
            --primary-color: #0056b3; /* 学术蓝 */
            --bg-color: #f8f9fa;
            --text-color: #212529;
            --header-height: 350px; /* 顶部背景图高度 */
            --container-width: 1100px; /* 宽屏设定 */
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            line-height: 1.7;
        }

        h1, h2, h3 { font-family: 'Newsreader', serif; color: #000; }
        a { color: var(--primary-color); text-decoration: none; transition: 0.2s; }
        a:hover { text-decoration: underline; color: #003d82; }

        /* === 顶部导航栏 (修复版) === */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98); /* 不透明度调高，防止看不清 */
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #ddd;
            z-index: 9999; /* 确保层级最高，不被图片遮挡 */
            padding: 12px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        .nav-content {
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between; /* 左右分布 */
            align-items: center;
        }
        .nav-brand { 
            font-weight: 700; 
            font-size: 1.3rem; 
            color: #222; 
            font-family: 'Newsreader', serif;
        }
        .nav-links {
            display: flex;
            gap: 25px; /* 菜单间距 */
        }
        .nav-links a { 
            font-size: 0.95rem; 
            color: #555; 
            font-weight: 600;
            text-transform: uppercase; /* 大写显得更像导航 */
            letter-spacing: 0.5px;
        }
        .nav-links a:hover {
            color: var(--primary-color);
            text-decoration: none;
        }

        /* === Hero Header (大背景图) === */
        .hero-header {
            height: var(--header-height);
            /* 这里引用你上传的 bg.jpg */
            background-image: url('./bg.jpg');
            background-size: cover;
            background-position: center;
            position: relative;
            margin-top: 50px; /* 给固定导航栏留出一点位置，防止遮挡背景图 */
        }
        .hero-overlay {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.4));
        }

        /* === 主容器 === */
        .container {
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 0 20px;
            position: relative; 
        }

        /* === 悬浮头像与个人信息 === */
        .profile-section {
            margin-top: -100px; 
            margin-bottom: 50px;
            position: relative;
            z-index: 10;
            display: flex;
            align-items: flex-end;
            gap: 35px; 
        }
        
        .avatar {
            width: 210px;
            height: 210px;
            border-radius: 12px; 
            border: 5px solid #fff;
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
            object-fit: cover;
            background: #fff;
            flex-shrink: 0;
        }

        .profile-info {
            padding-bottom: 5px;
        }
        .profile-name {
            font-size: 2.8rem;
            font-weight: 700;
            margin: 0;
            line-height: 1.1;
            color: #222;
            text-shadow: 2px 2px 4px rgba(255,255,255,0.8);
        }
        .profile-title {
            font-size: 1.15rem;
            color: #444;
            margin-top: 12px;
            margin-bottom: 18px;
            line-height: 1.4;
        }
        .social-links {
            margin-top: 10px;
        }
        .social-btn {
            display: inline-block;
            padding: 6px 16px;
            border: 1px solid #ddd;
            border-radius: 20px;
            font-size: 0.9rem;
            margin-right: 10px;
            color: #555;
            background: #fff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            margin-bottom: 5px;
        }
        .social-btn:hover { background: #f0f0f0; text-decoration: none; color: #0056b3; }

        /* === 内容区域 === */
        .content-section {
            background: #fff;
            padding: 50px;
            margin-bottom: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.04);
            border: 1px solid #f0f0f0;
            scroll-margin-top: 80px; /* 点击导航跳转时，留出空隙，不被遮挡 */
        }

        h2 {
            border-bottom: 2px solid #f0f0f0;
            padding-bottom: 15px;
            margin-top: 0;
            margin-bottom: 25px;
            font-size: 1.6rem;
            color: #111;
        }
        
        h3 {
            font-size: 1.25rem;
            margin-top: 35px;
            margin-bottom: 15px;
            color: #333;
        }

        p { 
            margin-bottom: 15px; 
            text-align: justify; 
            color: #444; 
            max-width: 850px; 
        }
        
        ul { padding-left: 20px; color: #444; max-width: 850px; }
        li { margin-bottom: 8px; }
        
        /* News 列表 */
        .news-list { list-style: none; padding: 0; }
        .news-list li { margin-bottom: 12px; padding-left: 25px; position: relative; }
        .news-list li::before { content: "•"; color: #0056b3; font-weight: bold; position: absolute; left: 5px; font-size: 1.2em; line-height: 1; }

        /* 论文列表 */
        .pub-item { margin-bottom: 30px; }
        .pub-title { font-weight: 700; color: #000; display: block; margin-bottom: 6px; font-size: 1.05rem;}
        .pub-meta { font-size: 0.95rem; color: #555; font-family: 'Newsreader', serif; }
        .pub-links { margin-top: 5px; }
        .pub-links a { font-size: 0.85rem; margin-right: 10px; font-weight: 600;}

        /* === 手机/平板适配 (重要修复) === */
        @media (max-width: 768px) {
            .nav-content {
                flex-direction: column; /* 上下排列 */
                gap: 10px;
            }
            .nav-links {
                display: flex; /* 强制显示！ */
                gap: 15px;
                font-size: 0.85rem;
                flex-wrap: wrap; /* 放不下自动换行 */
                justify-content: center;
            }
            
            .profile-section { flex-direction: column; align-items: center; text-align: center; margin-top: -80px; }
            .avatar { width: 160px; height: 160px; }
            .content-section { padding: 25px; }
            .hero-header { height: 250px; margin-top: 80px; /* 手机上导航栏变高了，下移背景图 */ }
            p, ul { max-width: 100%; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="nav-content">
            <div class="nav-brand">Lishan Li</div>
            <div class="nav-links">
                <a href="#about">About</a>
                <a href="#news">News</a>
                <a href="#research">Research</a>
                <a href="#publications">Publications</a>
            </div>
        </div>
    </nav>

    <div class="hero-header">
        <div class="hero-overlay"></div>
    </div>

    <div class="container">
        <div class="profile-section">
            <img src="./profile.jpg" alt="Lishan Li" class="avatar">
            
            <div class="profile-info">
                <h1 class="profile-name">Lishan Li (李丽珊)</h1>
                <div class="profile-title">
                    <strong>Research Assistant</strong> @ School of Chinese Language and Literature, BNU<br>
                    M.A. in Chinese Linguistics | B.A. in Chinese Lit
                </div>
                <div class="social-links">
                    <a href="mailto:lilishan0121@gmail.com" class="social-btn">📧 Email</a>
                    <a href="./Lishan_Li_CV_2025.pdf" class="social-btn">📄 CV</a>
                    <a href="https://www.researchgate.net/profile/Lishan-Li-3?ev=hdr_xprf" class="social-btn" target="_blank">🔬 ResearchGate</a>
                </div>
            </div>
        </div>

        <div class="content-section" id="about">
            <h2>👋 Introduction</h2>
            <p>
                Hello! I am a linguistics researcher passionate about <strong>Phonetics</strong>, <strong>Dialectology</strong>, and <strong>Language Acquisition</strong>.
            </p>
            <p>
                My research interests lie in the evolution of tones in Chinese dialects, specifically how they merge over time and how they interact with musical melodies. I combine traditional <strong>fieldwork</strong> (recording 180+ children; documenting endangered dialects) with <strong>computational modeling</strong> (Python/R) to decode the mechanism of sound change.
            </p>
            <p>
                I obtained my M.A. from <strong>Beijing Normal University</strong> (Outstanding Graduate) and B.A. from <strong>Shandong University</strong> (GPA: 4.03/5.0, Rank: 6/102).
            </p>
        </div>

        <div class="content-section" id="news">
            <h2>🔥 News</h2>
            <ul class="news-list">
                <li><strong>[Sep 2025]</strong> Started full-time position as Research Assistant at BNU.</li>
                <li><strong>[Aug 2025]</strong> Presented our work on <em>Cantonese Tone Merging</em> orally at <strong>Interspeech 2025</strong>! 🎤</li>
                <li><strong>[Jun 2025]</strong> Graduated from BNU as an <strong>Outstanding Graduate of Beijing</strong>.</li>
                <li><strong>[2024]</strong> Paper on dialect loss and tone perception published in <strong>JASA</strong> (Vol. 156).</li>
            </ul>
        </div>

        <div class="content-section" id="research">
            <h2>🧪 Research Overview</h2>
            <p>
                My research program focuses on understanding how sound systems evolve, how listeners adapt to complex acoustic signals, and how these processes unfold across different populations. I integrate experimental phonetics, speech perception, developmental linguistics, and comparative tonology to build a unified account of how tonal categories emerge, change, and are represented in the mind.
            </p>

            <h3>1. Mechanisms of Sound Change</h3>
            <p>
                I investigate how phonetic variation is transformed into phonological restructuring, with a particular focus on tone languages. A central component of my research concerns <strong>Cantonese tone evolution</strong>, especially the interaction between morphological tone alternation (<em>Pinjam</em>) and ongoing tonal mergers. I explore whether the functional load of morphology can delay or prevent merger, evaluating competing hypotheses such as <strong>Static Storage</strong> vs. <strong>Dynamic Co-activation</strong>.
            </p>

            <h3>2. Bilingualism & Perceptual Plasticity</h3>
            <p>
                A second major line of my work investigates how language experience shapes perceptual sensitivity. I demonstrate that speech perception is not fixed: listeners continually reweight multiple dimensions—such as F0, duration, or voice quality—depending on their linguistic background. I focus especially on bilinguals and bi-dialectal speakers (e.g., Changsha Mandarin) to test how merger patterns influence perceptual categories.
            </p>

            <h3>3. Language Acquisition: Typical & Atypical</h3>
            <p>
                I extend my expertise in prosody and acoustic analysis to developmental populations. My current project focuses on children with <strong>Autism Spectrum Disorder (ASD)</strong>. I examine how ASD affects the production and perception of suprasegmental features—including intonation, lexical tone, and voice quality—aiming to identify reliable acoustic markers of atypical prosodic development.
            </p>

            <h3>4. Multidimensional Cue Dynamics</h3>
            <p>
                Across all areas of my research lies a unifying methodological interest: how listeners integrate multiple acoustic cues (pitch, duration, spectral tilt, voice quality) and how these strategies shift in different environments, such as tonal mergers or noisy signals.
            </p>
        </div>

        <div class="content-section" id="publications">
            <h2>📝 Selected Publications</h2>
            
            <div class="pub-item">
                <span class="pub-title">The influence of dialect loss on tone perception: Diminishing voice quality cues in preserved tone contrast</span>
                <div class="pub-meta">Zhang, Y., <strong>Li, L.</strong>, Lai, W., & Xu, X. (2024). <em>Journal of the Acoustical Society of America (JASA)</em>, 156(6):3707-3722.</div>
                <div class="pub-links">[<a href="#">Paper Link</a>]</div>
            </div>

            <div class="pub-item">
                <span class="pub-title">Lexical competition in the process of Cantonese tone merging: Diverse Impact Mechanisms Across Different Individuals and Tone Pairs</span>
                <div class="pub-meta"><strong>Li, L.</strong>, Zhou, Y., & Xu, X. (2025). <em>In Proc. of Interspeech 2025</em>. (<strong>Oral Presentation</strong>)</div>
                <div class="pub-links">[<a href="#">PDF</a>] [<a href="#">Slides</a>]</div>
            </div>

             <div class="pub-item">
                <span class="pub-title">Level-Tone Merger in Production and Perception: Study in two Chinese Min Dialects</span>
                <div class="pub-meta">Wu, Y., <strong>Li, L.</strong>, & Xu, X. (2025). <em>In Proc. of International Conference on Asian Language Processing (IALP)</em>. (*Equal Contribution)</div>
            </div>
            
            <div class="pub-item">
                <span class="pub-title">Multiple Patterns of Merging Guangzhou Cantonese Tones in Production and Perception: Study on Youth Groups</span>
                <div class="pub-meta"><strong>Li, L.</strong> & Xu, X. (2024). <em>In Proc. of ISCSLP 2024</em>. (<strong>Oral Presentation</strong>)</div>
            </div>
        </div>

        <div style="text-align: center; color: #999; font-size: 0.85rem; margin-bottom: 50px;">
            &copy; 2025 Lishan Li. Hosted on GitHub Pages.
        </div>

    </div>

</body>
</html>
