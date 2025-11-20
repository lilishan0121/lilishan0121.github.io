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
            --primary-color: #0056b3;
            --bg-color: #f8f9fa;
            --text-color: #212529;
            --header-height: 350px;
            --container-width: 1100px;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            line-height: 1.7;
            scroll-behavior: smooth;
        }

        h1, h2, h3 { font-family: 'Newsreader', serif; color: #000; }
        a { color: var(--primary-color); text-decoration: none; transition: 0.2s; }
        a:hover { text-decoration: underline; color: #003d82; }

        /* Navbar */
        .navbar {
            position: fixed;
            top: 0; left: 0; width: 100%;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #ddd;
            z-index: 9999;
            padding: 12px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        .nav-content {
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .nav-brand { font-weight: 700; font-size: 1.3rem; color: #222; font-family: 'Newsreader', serif; }
        .nav-links { display: flex; gap: 25px; }
        .nav-links a { font-size: 0.95rem; color: #555; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px; }
        .nav-links a:hover { color: var(--primary-color); text-decoration: none; }

        /* Hero Header */
        .hero-header {
            height: var(--header-height);
            background-image: url('./bg.jpg');
            background-size: cover;
            background-position: center;
            position: relative;
            margin-top: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }
        .hero-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(to bottom, rgba(0,0,0,0.2), rgba(0,0,0,0.5));
            z-index: 1;
        }
        .hero-text {
            position: relative;
            z-index: 2;
            color: #fff;
        }
        .hero-text h1 { font-size: 3rem; margin-bottom: 10px; text-shadow: 2px 2px 8px rgba(0,0,0,0.5); }
        .hero-text p { font-size: 1.2rem; font-weight: 500; text-shadow: 1px 1px 5px rgba(0,0,0,0.5); }

        /* Container */
        .container { max-width: var(--container-width); margin: 0 auto; padding: 0 20px; position: relative; }

        /* Profile */
        .profile-section {
            margin-top: -100px;
            margin-bottom: 50px;
            position: relative;
            z-index: 10;
            display: flex;
            align-items: flex-end;
            gap: 35px;
        }
        .avatar { width: 210px; height: 210px; border-radius: 12px; border: 5px solid #fff; box-shadow: 0 10px 25px rgba(0,0,0,0.15); object-fit: cover; background: #fff; flex-shrink: 0; transition: transform 0.3s; }
        .avatar:hover { transform: scale(1.05); }
        .profile-info { padding-bottom: 5px; }
        .profile-name { font-size: 2.8rem; font-weight: 700; margin: 0; line-height: 1.1; color: #222; text-shadow: 2px 2px 4px rgba(255,255,255,0.8); }
        .profile-title { font-size: 1.15rem; color: #444; margin-top: 12px; margin-bottom: 18px; line-height: 1.4; }
        .social-links { margin-top: 10px; }
        .social-btn { display: inline-block; padding: 6px 16px; border: 1px solid #ddd; border-radius: 20px; font-size: 0.9rem; margin-right: 10px; color: #555; background: #fff; box-shadow: 0 2px 5px rgba(0,0,0,0.05); margin-bottom: 5px; transition: all 0.2s; }
        .social-btn:hover { background: #f0f0f0; text-decoration: none; color: #0056b3; transform: translateY(-2px); }

        /* Content Sections */
        .content-section {
            background: #fff;
            padding: 50px;
            margin-bottom: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.04);
            border: 1px solid #f0f0f0;
            scroll-margin-top: 80px;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.8s ease-out;
        }
        .content-section.visible { opacity: 1; transform: translateY(0); }

        h2 { border-bottom: 2px solid #f0f0f0; padding-bottom: 15px; margin-top: 0; margin-bottom: 25px; font-size: 1.6rem; color: #111; }
        h3 { font-size: 1.25rem; margin-top: 35px; margin-bottom: 15px; color: #333; }

        p { margin-bottom: 15px; text-align: justify; color: #444; max-width: 850px; }
        ul { padding-left: 20px; color: #444; max-width: 850px; }
        li { margin-bottom: 8px; }

        .news-list li::before { content: "•"; color: #0056b3; font-weight: bold; position: absolute; left: 5px; font-size: 1.2em; line-height: 1; }

        /* Publications */
        .pub-item { margin-bottom: 30px; }
        .pub-title { font-weight: 700; color: #000; display: block; margin-bottom: 6px; font-size: 1.05rem; }
        .pub-meta { font-size: 0.95rem; color: #555; font-family: 'Newsreader', serif; }
        .pub-links { margin-top: 5px; }
        .pub-links a { font-size: 0.85rem; margin-right: 10px; font-weight: 600; }

        /* Research Card Style */
        .research-cards { display: grid; grid-template-columns: repeat(auto-fit,minmax(280px,1fr)); gap: 25px; margin-top: 20px; }
        .research-card { background: #fdfdfd; padding: 25px; border-radius: 12px; box-shadow: 0 4px 20px rgba(0,0,0,0.05); transition: transform 0.3s, box-shadow 0.3s; }
        .research-card:hover { transform: translateY(-5px); box-shadow: 0 10px 30px rgba(0,0,0,0.1); }
        .research-card h4 { margin-top: 0; color: var(--primary-color); font-size: 1.2rem; margin-bottom: 10px; }

        /* Footer */
        .footer { text-align: center; color: #999; font-size: 0.85rem; margin-bottom: 50px; }

        /* Media Queries */
        @media (max-width: 768px) {
            .nav-content { flex-direction: column; gap: 10px; }
            .nav-links { gap: 15px; font-size: 0.85rem; flex-wrap: wrap; justify-content: center; }
            .profile-section { flex-direction: column; align-items: center; text-align: center; margin-top: -80px; }
            .avatar { width: 160px; height: 160px; }
            .content-section { padding: 25px; }
            .hero-header { height: 250px; margin-top: 80px; }
            p, ul { max-width: 100%; }
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
        <p>Exploring the evolution of Chinese tones | Phonetics & Computational Modeling</p>
    </div>
</div>

<div class="container">
    <!-- Profile Section -->
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

    <!-- About Section -->
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

    <!-- News Section -->
    <div class="content-section" id="news">
        <h2>🔥 News</h2>
        <ul class="news-list">
            <li><strong>[Aug 2025]</strong> Presented our work on <em>Cantonese Tone Merging</em> orally at <strong>Interspeech 2025</strong>! 🎤</li>
            <li><strong>[2024]</strong> Paper on dialect loss and tone perception published in <strong>JASA</strong> (Vol. 156).</li>
        </ul>
    </div>

    <!-- Research Section -->
    <div class="content-section" id="research">
        <h2>🧪 Research Overview</h2>
        <p>
            My research program focuses on understanding how sound systems evolve, how listeners adapt to complex acoustic signals, and how these processes unfold across different populations. I integrate experimental phonetics, speech perception, developmental linguistics, and comparative tonology to build a unified account of how tonal categories emerge, change, and are represented in the mind.
        </p>

        <div class="research-cards">
            <div class="research-card">
                <h4>1. Mechanisms of Sound Change</h4>
                <p>
                    I investigate how phonetic variation is transformed into phonological restructuring, with a particular focus on tone languages. A central component of my research concerns <strong>Cantonese tone evolution</strong>, especially the interaction between morphological tone alternation (<em>Pinjam</em>) and ongoing tonal mergers. I explore whether the functional load of morphology can delay or prevent merger, evaluating competing hypotheses such as <strong>Static Storage</strong> vs. <strong>Dynamic Co-activation</strong>.
                </p>
            </div>
            <div class="research-card">
                <h4>2. Bilingualism & Perceptual Plasticity</h4>
                <p>
                    A second major line of my work investigates how language experience shapes perceptual sensitivity. I demonstrate that speech perception is not fixed: listeners continually reweight multiple dimensions—such as F0, duration, or voice quality—depending on their linguistic background. I focus especially on bilinguals and bi-dialectal speakers (e.g., Changsha Mandarin) to test how merger patterns influence perceptual categories.
                </p>
            </div>
            <div class="research-card">
                <h4>3. Language Acquisition: Typical & Atypical</h4>
                <p>
                    I extend my expertise in prosody and acoustic analysis to developmental populations. My current project focuses on children with <strong>Autism Spectrum Disorder (ASD)</strong>. I examine how ASD affects the production and perception of suprasegmental features—including intonation, lexical tone, and voice quality—aiming to identify reliable acoustic markers of atypical prosodic development.
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

    <!-- Publications Section -->
    <div class="content-section" id="publications">
        <h2>📝 Selected Publications</h2>
        <div class="pub-item">
            <span class="pub-title">The influence of dialect loss on tone perception: Diminishing voice quality cues in preserved tone contrast</span>
            <div class="pub-meta">Zhang, Y., <strong>Li, L.</strong>, Lai, W., & Xu, X. (2024). <em>JASA</em>, 156(6):3707-3722.</div>
            <div class="pub-links">[<a href="#">Paper Link</a>]</div>
        </div>
        <div class="pub-item">
            <span class="pub-title">Lexical competition in the process of Cantonese tone merging: Diverse Impact Mechanisms Across Different Individuals and Tone Pairs</span>
            <div class="pub-meta"><strong>Li, L.</strong>, Zhou, Y., & Xu, X. (2025). <em>Interspeech 2025</em>. (Oral Presentation)</div>
            <div class="pub-links">[<a href="#">PDF</a>] [<a href="#">Slides</a>]</div>
        </div>
        <div class="pub-item">
            <span class="pub-title">Level-Tone Merger in Production and Perception: Study in two Chinese Min Dialects</span>
            <div class="pub-meta">Wu, Y., <strong>Li, L.</strong>, & Xu, X. (2025). <em>IALP</em>. (*Equal Contribution)</div>
        </div>
       
