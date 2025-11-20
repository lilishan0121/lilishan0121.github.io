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
            background-color: #f4f7f6;
            color: #333;
            margin: 0;
            line-height: 1.7; /* 增加行高，阅读体验更好 */
            padding-top: 60px;
        }
        a { color: #0056b3; text-decoration: none; transition: color 0.2s;}
        a:hover { color: #003d82; text-decoration: underline; }

        /* === 顶部导航栏 === */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
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
        .avatar:hover { transform: scale(1.05); }
        
        .name { font-size: 1.6em; font-weight: 700; margin-bottom: 5px; color: #222; }
        
        .education-box {
            margin-bottom: 20px;
            color: #666;
            font-size: 0.9em;
        }
        .edu-item { margin-bottom: 8px; }
        .edu-degree { font-weight: 600; color: #444; display: block; }
        .edu-school { font-weight: 400; }

        .contact-box {
            text-align: left;
            font-size: 0.9em;
            color: #555;
            background: #fff;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }
        .contact-item { margin-bottom: 12px; display: flex; align-items: center; overflow: hidden;}
        .contact-item a { color: #333; }
        .contact-item a:hover { color: #0056b3; }
        .icon { margin-right: 10px; width: 20px; text-align: center; flex-shrink: 0;}
        
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
        
        section { margin-bottom: 60px; scroll-margin-top: 80px; }
        
        /* 标题样式 */
        h2 { 
            font-size: 1.6em; 
            margin-bottom: 25px; 
            color: #111; 
            border-bottom: 2px solid #f0f0f0; 
            padding-bottom: 10px;
        }
        h3 {
            font-size: 1.25em;
            color: #2c3e50;
            margin-top: 35px;
            margin-bottom: 15px;
            font-weight: 600;
        }
        
        /* 段落与列表样式 */
        p { margin-bottom: 15px; color: #444; text-align: justify; }
        
        /* 针对 Research 部分的列表优化 */
        .research-list {
            margin-top: 10px;
            margin-bottom: 20px;
            padding-left: 20px;
        }
        .research-list li {
            margin-bottom: 8px;
            color: #555;
        }

        /* News 列表样式 */
        .news-list { list-style: none; padding: 0; }
        .news-list li { margin-bottom: 12px; padding-left: 20px; position: relative; color: #444; }
        .news-list li::before { content: "•"; color: #0056b3; font-weight: bold; position: absolute; left: 0; }
        
        /* Publications 样式 */
        .paper-item { margin-bottom: 25px; }
        .paper-title { font-weight: 700; color: #222; font-size: 1.05em; }
        .paper-authors { color: #555; font-size: 0.95em; margin: 4px 0; }
        .paper-venue { font-style: italic; color: #0056b3; font-size: 0.9em; }
        
        @media (max-width: 768px) {
            .container { flex-direction: column; gap: 30px; margin-top: 20px; }
            .sidebar { width: 100%; }
            .navbar .nav-links { display: none; }
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
        
        <div class="education-box">
            <div class="edu-item">
                <span class="edu-degree">M.A. in Chinese Linguistics</span>
                <span class="edu-school">Beijing Normal University</span>
            </div>
            <div class="edu-item" style="margin-top: 10px;">
                <span class="edu-degree">B.A. in Chinese Lit</span>
                <span class="edu-school">Shandong University</span>
            </div>
        </div>
        
        <div class="contact-box">
            <div class="contact-item"><span class="icon">📍</span> Beijing, China</div>
            <div class="contact-item"><span class="icon">📧</span> <a href="mailto:lilishan0121@gmail.com">lilishan0121@gmail.com</a></div>
            
            <div class="contact-item">
                <span class="icon">🔬</span> 
                <a href="https://www.researchgate.net/profile/Lishan-Li-3?ev=hdr_xprf" target="_blank">ResearchGate Profile</a>
            </div>
            
            <a href="./Lishan_Li_CV_2025.pdf" class="btn-cv">Download CV</a>
        </div>
    </aside>

    <main class="main-content">
        
        <section id="about">
            <h2>👋 Introduction</h2>
            <p>
                Hello! I am a linguistics researcher passionate about <strong>Phonetics</strong>, <strong>Dialectology</strong>, and <strong>Language Acquisition</strong>.
            </p>
            <p>
                My research interests lie in the evolution of tones in Chinese dialects, specifically how they merge over time and how they interact with musical melodies. I combine traditional <strong>fieldwork</strong> with <strong>computational modeling</strong> (Python/R) to decode the mechanism of sound change.
            </p>
            <p>
                I obtained my M.A. from <strong>Beijing Normal University</strong> (Outstanding Graduate) and B.A. from <strong>Shandong University</strong> (GPA: 4.03/5.0, Rank: 6/102).
            </p>
        </section>

        <section id="news">
            <h2>🔥 News</h2>
            <ul class="news-list">
                <li><strong>[Aug 2025]</strong> Presented our work on <em>Cantonese Tone Merging</em> orally at <strong>Interspeech 2025</strong>.</li>
                <li><strong>[Jun 2025]</strong> Graduated from Beijing Normal University.</li>
                <li><strong>[2024]</strong> Paper on dialect loss published in <strong>JASA</strong>.</li>
            </ul>
        </section>

        <section id="research">
            <h2>🧪 Research Overview</h2>
            <p>
                My research program focuses on understanding how sound systems evolve, how listeners adapt to complex acoustic signals, and how these processes unfold across different populations—including bilingual speakers and children with atypical language development. I integrate experimental phonetics, speech perception, developmental linguistics, and comparative tonology to build a unified account of how tonal categories emerge, change, and are represented in the mind.
            </p>

            <h3>1. Mechanisms of Sound Change</h3>
            <p>
                I investigate how phonetic variation is transformed into phonological restructuring, with a particular focus on tone languages. My work examines how cognitive, morphological, and acoustic factors jointly shape pathways of sound change.
            </p>
            <p>
                A central component of my research concerns Cantonese tone evolution, especially the interaction between morphological tone alternation (<em>Pinjam</em>) and ongoing tonal mergers. I explore whether the functional load of morphology can delay or prevent merger, evaluating competing hypotheses such as <strong>Static Storage</strong> vs. <strong>Dynamic Co-activation</strong> of tonal categories.
            </p>
            <p>Beyond Cantonese, I adopt a comparative approach to identify cross-linguistic regularities. Current projects include:</p>
            <ul class="research-list">
                <li><strong>Khmer:</strong> Tonogenesis and the emergence of new prosodic contrasts.</li>
                <li><strong>Thai:</strong> Tonal evolution under contact-induced phonetic pressures.</li>
                <li><strong>Wulian Mandarin:</strong> Segmental change illustrating how tonal and segmental systems co-evolve.</li>
            </ul>

            <h3>2. Bilingualism & Perceptual Plasticity</h3>
            <p>
                A second major line of my work investigates how language experience shapes perceptual sensitivity. I demonstrate that speech perception is not fixed: listeners continually reweight multiple dimensions—such as F0, duration, or voice quality—depending on their linguistic background.
            </p>
            <p>
                I focus especially on bilinguals and bi-dialectal speakers. For example, I compare speakers of Changsha Mandarin (a tone-merging variety) with speakers of conservative varieties to test how merger patterns influence perceptual categories. Key questions include:
            </p>
            <ul class="research-list">
                <li>How does bilingualism recalibrate perceptual attention to pitch vs. voice quality?</li>
                <li>Do speakers from tone-merging dialects show reduced sensitivity to contrastive cues?</li>
                <li>What kinds of perceptual “plasticity windows” exist in adulthood?</li>
            </ul>
            <p>
                Using controlled AX/ABX perception tasks and mixed-effects modeling, I map how listeners dynamically adjust their weighting strategies in response to signal instability.
            </p>

            <h3>3. Language Acquisition: Typical & Atypical</h3>
            <p>
                I extend my expertise in prosody and acoustic analysis to developmental populations. My research investigates how children acquire tonal categories and how these processes differ in clinical contexts.
            </p>
            <p>
                My current project focuses on children with <strong>Autism Spectrum Disorder (ASD)</strong>. I examine how ASD affects the production and perception of suprasegmental features—including intonation, lexical tone, and voice quality—aiming to identify reliable acoustic markers of atypical prosodic development. This work contributes to both theory and practice by:
            </p>
            <ul class="research-list">
                <li>Revealing how prosodic categories emerge in the developing mind.</li>
                <li>Identifying which acoustic dimensions are most vulnerable in atypical populations.</li>
                <li>Providing quantitative tools for assessing prosodic development.</li>
            </ul>

            <h3>4. Multidimensional Cue Dynamics</h3>
            <p>
                Across all areas of my research lies a unifying methodological interest: how listeners integrate multiple acoustic cues and how these strategies shift in different environments. I examine how pitch, duration, spectral tilt, and voice quality interact, compete, or reinforce each other—especially under conditions of instability such as:
            </p>
            <ul class="research-list">
                <li>Tonal mergers</li>
                <li>Bilingual input</li>
                <li>Atypical prosodic development</li>
                <li>Noisy or ambiguous signals</li>
            </ul>
            <p>
                Using fine-grained acoustic modeling, my work demonstrates that cue weighting is an adaptive, experience-driven process. This framework explains why populations diverge in their perception of contrasts and why certain sound changes accelerate while others stabilize.
            </p>
        </section>

        <section id="publications">
            <h2>📝 Publications</h2>

            <div class="paper-item">
                <div class="paper-title">The influence of dialect loss on tone perception: Diminishing voice quality cues in preserved tone contrast</div>
                <div class="paper-authors">Zhang, Y., <strong>Li, L.</strong>, Lai, W., & Xu, X. (2024)</div>
                <div class="paper-venue">Journal of the Acoustical Society of America (JASA), 156(6):3707-3722.</div>
                <div>[<a href="#">PDF</a>]</div>
            </div>

            <div class="paper-item">
                <div class="paper-title">Lexical competition in the process of Cantonese tone merging: Diverse Impact Mechanisms Across Different Individuals and Tone Pairs</div>
                <div class="paper-authors"><strong>Li, L.</strong>, Zhou, Y., & Xu, X. (2025)</div>
                <div class="paper-venue">In Proc. of Interspeech 2025 (Oral Presentation).</div>
            </div>

            <div class="paper-item">
                <div class="paper-title">Level-Tone Merger in Production and Perception: Study in two Chinese Min Dialects</div>
                <div class="paper-authors">Wu, Y., <strong>Li, L.</strong>, & Xu, X. (2025)</div>
                <div class="paper-venue">In Proc. of International Conference on Asian Language Processing (IALP).</div>
            </div>
            
            <div class="paper-item">
                <div class="paper-title">Multiple Patterns of Merging Guangzhou Cantonese Tones in Production and Perception: Study on Youth Groups</div>
                <div class="paper-authors"><strong>Li, L.</strong> & Xu, X. (2024)</div>
                <div class="paper-venue">In Proc. of ISCSLP 2024 (Oral Presentation).</div>
            </div>

        </section>

    </main>
</div>

</body>
</html>
