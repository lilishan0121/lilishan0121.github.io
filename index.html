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
        :root {
            --primary-color: #0056b3; /* 学术蓝 */
            --bg-color: #f8f9fa;
            --text-color: #212529;
            --header-height: 400px; /* 顶部背景图高度加大，更大气 */
            
            /* 【关键修改】宽屏设定：占屏幕宽度的 85% */
            --container-width: 85%; 
        }

        body {
            /* 【关键修改】字体栈：优先使用 Roboto，紧接着是支持 IPA 音标的系统字体 */
            font-family: 'Roboto', "Arial Unicode MS", "Lucida Sans Unicode", "Segoe UI", sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            line-height: 1.7;
            scroll-behavior: smooth;
        }

        h1, h2, h3 { font-family: 'Newsreader', serif; color: #000; }
        a { color: var(--primary-color); text-decoration: none; transition: 0.2s; }
        a:hover { text-decoration: underline; color: #003d82; }

        /* === 导航栏 === */
        .navbar {
            position: fixed;
            top: 0; left: 0; width: 100%;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #ddd;
            z-index: 9999;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        .nav-content {
            width: var(--container-width); /* 跟随全局宽度 */
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .nav-brand { font-weight: 700; font-size: 1.4rem; color: #222; font-family: 'Newsreader', serif; }
        .nav-links { display: flex; gap: 30px; }
        .nav-links a { font-size: 1rem; color: #555; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px; }
        .nav-links a:hover { color: var(--primary-color); text-decoration: none; }

        /* === 顶部大图 (Hero) === */
        .hero-header {
            height: var(--header-height);
            /* 确保你的仓库里有 bg.jpg */
            background-image: url('./bg.jpg');
            background-size: cover;
            background-position: center;
            position: relative;
            margin-top: 65px; 
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }
        .hero-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            /* 加深一点遮罩，让文字更清晰 */
            background: linear-gradient(to bottom, rgba(0,0,0,0.2), rgba(0,0,0,0.6));
            z-index: 1;
        }
        .hero-text {
            position: relative;
            z-index: 2;
            color: #fff;
            padding: 0 20px;
        }
        .hero-text h1 { font-size: 3.5rem; margin-bottom: 15px; text-shadow: 2px 2px 10px rgba(0,0,0,0.6); }
        .hero-text p { font-size: 1.4rem; font-weight: 400; text-shadow: 1px 1px 6px rgba(0,0,0,0.6); }

        /* === 主容器 === */
        .container { 
            width: var(--container-width); /* 关键：宽屏 */
            margin: 0 auto; 
            position: relative; 
        }

        /* === 个人信息区 (Profile) === */
        .profile-section {
            margin-top: -120px; /* 往上提，压住背景图 */
            margin-bottom: 60px;
            position: relative;
            z-index: 10;
            display: flex;
            align-items: flex-end;
            gap: 40px;
        }
        /* 确保你的仓库里有 profile.jpg (全小写) */
        .avatar { 
            width: 230px; height: 230px; 
            border-radius: 12px; 
            border: 6px solid #fff; 
            box-shadow: 0 12px 30px rgba(0,0,0,0.15); 
            object-fit: cover; 
            background: #fff; 
            flex-shrink: 0; 
            transition: transform 0.3s; 
        }
        .avatar:hover { transform: scale(1.05); }
        
        .profile-info { padding-bottom: 5px; }
        .profile-name { 
            font-size: 3.2rem; 
            font-weight: 700; 
            margin: 0; 
            line-height: 1.1; 
            color: #222; 
            text-shadow: 2px 2px 4px rgba(255,255,255,0.9); 
        }
        .profile-title { 
            font-size: 1.2rem; 
            color: #444; 
            margin-top: 15px; 
            margin-bottom: 20px; 
            line-height: 1.5; 
        }
        .social-links { margin-top: 10px; }
        .social-btn { 
            display: inline-block; 
            padding: 8px 20px; 
            border: 1px solid #ddd; 
            border-radius: 30px; 
            font-size: 0.95rem; 
            margin-right: 12px; 
            color: #555; 
            background: #fff; 
            box-shadow: 0 2px 8px rgba(0,0,0,0.05); 
            margin-bottom: 5px; 
            transition: all 0.2s; 
        }
        .social-btn:hover { background: #f0f0f0; text-decoration: none; color: #0056b3; transform: translateY(-2px); }

        /* === 内容板块 (Content) === */
        .content-section {
            background: #fff;
            padding: 60px; /* 内边距加大 */
            margin-bottom: 50px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.04);
            border: 1px solid #f0f0f0;
            scroll-margin-top: 100px;
        }

        h2 { border-bottom: 2px solid #f0f0f0; padding-bottom: 15px; margin-top: 0; margin-bottom: 30px; font-size: 1.8rem; color: #111; }
        h3 { font-size: 1.4rem; margin-top: 40px; margin-bottom: 20px; color: #333; }

        /* 【关键修改】取消了 max-width 限制，让文字铺满宽屏 */
        p { margin-bottom: 15px; text-align: justify; color: #444; max-width: 100%; }
        ul { padding-left: 20px; color: #444; max-width: 100%; }
        
        li { margin-bottom: 10px; }
        .news-list li::before { content: "•"; color: #0056b3; font-weight: bold; position: absolute; left: 5px; font-size: 1.2em; line-height: 1; }

        /* Publications */
        .pub-item { margin-bottom: 35px; }
        .pub-title { font-weight: 700; color: #000; display: block; margin-bottom: 8px; font-size: 1.1rem; }
        .pub-meta { font-size: 1rem; color: #555; font-family: 'Newsreader', serif; }
        .pub-links { margin-top: 8px; }
        .pub-links a { font-size: 0.9rem; margin-right: 15px; font-weight: 600; }

        /* Research Card Style - 自动适应宽屏，四列布局 */
        .research-cards { display: grid; grid-template-columns: repeat(auto-fit,minmax(300px,1fr)); gap: 30px; margin-top: 30px; }
        .research-card { background: #fbfbfb; padding: 30px; border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.03); transition: transform 0.3s, box-shadow 0.3s; border: 1px solid #eee;}
        .research-card:hover { transform: translateY(-5px); box-shadow: 0 12px 30px rgba(0,0,0,0.1); border-color: var(--primary-color); }
        .research-card h4 { margin-top: 0; color: var(--primary-color); font-size: 1.3rem; margin-bottom: 15px; }

        /* Footer */
        .footer { text-align: center; color: #999; font-size: 0.9rem; margin-bottom: 60px; }

        /* === 手机端适配 === */
        @media (max-width: 768px) {
            :root { --container-width: 92%; } /* 手机上保留一点边距 */
            .nav-content { flex-direction: column; gap: 10px; width: 100%; }
            .nav-links { gap: 15px; font-size: 0.85rem; flex-wrap: wrap; justify-content: center; }
            .profile-section { flex-direction: column; align-items: center; text-align: center; margin-top: -80px; gap: 20px;}
            .avatar { width: 160px; height: 160px; }
            .content-section { padding: 25px; }
            .hero-header { height: 280px; margin-top: 80px; }
            .profile-name { font-size: 2.2rem; }
            .research-cards { grid-template-columns: 1fr; }
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
    <div class="hero-text">
        <h1>Lishan Li (李丽珊)</h1>
        <p>Decoding the melody of speech | Phonetics & Computation</p>
    </div>
</div>

<div class="container">
    <div class="profile-section">
        <img src="./profile.jpg" alt="Lishan Li" class="avatar">
        
        <div class="profile-info">
            <h1 class="profile-name">Lishan Li <span style="font-family: 'Arial Unicode MS', 'Lucida Sans Unicode', sans-serif; font-weight: 400; font-size: 0.6em; vertical-align: middle;">[li²¹³ li⁵¹ ʂan⁵⁵]</span></h1>
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

        <div class="research-cards">
            <div class="research-card">
                <h4>1. Mechanisms of Sound Change</h4>
                <p>
                    I investigate how phonetic variation is transformed into phonological restructuring, with a particular focus on tone languages. A central component of my research concerns <strong>Cantonese tone evolution</strong>, especially the interaction between morphological tone alternation (<em>Pinjam</em>) and ongoing tonal mergers. I explore whether the functional load of morphology can delay or prevent merger.
                </p>
            </div>
            <div class="research-card">
                <h4>2. Bilingualism & Perceptual Plasticity</h4>
                <p>
                    A second major line of my work investigates how language experience shapes perceptual sensitivity. I demonstrate that speech perception is not fixed: listeners continually reweight multiple dimensions—such as F0, duration, or voice quality—depending on their linguistic background. I focus especially on bilinguals and bi-dialectal speakers.
                </p>
            </div>
            <div class="research-card">
                <h4>3. Language Acquisition</h4>
                <p>
                    I extend my expertise in prosody and acoustic analysis to developmental populations. My current project focuses on children with <strong>Autism Spectrum Disorder (ASD)</strong>. I examine how ASD affects the production and perception of suprasegmental features—including intonation, lexical tone, and voice quality—aiming to identify reliable acoustic markers.
                </p>
            </div>
            <div class="research-card">
                <h4>4. Multidimensional Cue Dynamics</h4>
                <p>
                    Across all areas of my research lies a unifying methodological interest: how listeners integrate multiple acoustic cues (pitch, duration, spectral tilt, voice quality) and how these strategies shift in different environments, such as tonal mergers or noisy signals.
                </p>
            </div>
        </div>
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

    <div class="footer">
        &copy; 2025 Lishan Li. Hosted on GitHub Pages.
    </div>
</div>

</body>
</html>
