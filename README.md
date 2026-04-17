<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sri Hardyanti – Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Inter:wght@400;500;600&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --navy: #0D2137;
            --navy-light: #2A5482;
            --gold: #C4993A;
            --cream: #F8F7F4;
            --white: #FFFFFF;
            --muted: #5A6B7C;
            --border: #D0DAE4;
            --surface: #EEF3F8;
        }

        * { margin:0; padding:0; box-sizing:border-box; }

        body {
            background: var(--cream);
            color: var(--navy);
            font-family: 'Inter', sans-serif;
            font-size: 18px;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* MULTI-PAGE SYSTEM */
        .page {
            display: none; /* Hidden by default */
            min-height: 100vh;
            padding: 120px 8vw 80px;
            animation: fadeIn 0.4s ease-out;
        }

        .page.active { display: block; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* NAVIGATION */
        nav {
            position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
            background: rgba(13, 33, 55, 0.98);
            backdrop-filter: blur(10px);
            padding: 0 8vw;
            display: flex; align-items: center; justify-content: space-between;
            height: 80px;
        }

        .nav-brand {
            font-family: 'Playfair Display', serif;
            font-size: 24px; font-weight: 600;
            color: var(--gold); text-decoration: none;
        }

        .nav-links { display: flex; gap: 32px; list-style: none; }
        .nav-links a {
            font-size: 14px; font-weight: 600;
            letter-spacing: 0.1em; text-transform: uppercase;
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none; cursor: pointer;
            transition: color 0.2s;
        }
        .nav-links a:hover, .nav-links a.active { color: var(--gold); }

        /* TYPOGRAPHY & LAYOUT UTILITIES */
        .section-eyebrow {
            font-family: 'Space Mono', monospace;
            font-size: 14px; letter-spacing: 0.2em;
            text-transform: uppercase; color: var(--gold);
            margin-bottom: 12px;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(32px, 4vw, 48px);
            margin-bottom: 40px; color: var(--navy);
        }

        /* PROFILE PAGE */
        .profile-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 6vw; align-items: center; }
        .profile-name { font-family: 'Playfair Display', serif; font-size: 80px; line-height: 1; margin-bottom: 24px; }
        .about-text { font-size: 20px; color: var(--muted); border-left: 3px solid var(--gold); padding-left: 24px; margin-bottom: 30px; }

        /* EXPERIENCE PAGE */
        .exp-item { padding: 30px 0; border-bottom: 1px solid var(--border); }
        .exp-header { display: flex; justify-content: space-between; align-items: baseline; }
        .exp-org { font-weight: 700; font-size: 22px; }
        .exp-role { color: var(--gold); font-weight: 600; margin-bottom: 10px; }

        /* FEATURED WORK (TYPOGRAPHY REFINEMENT) */
        .expertise-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 30px; }
        .expertise-card {
            background: var(--white);
            border: 1px solid var(--border);
            padding: 32px; border-radius: 8px;
            display: flex; flex-direction: column; gap: 20px;
        }
        .exp-section-title {
            font-family: 'Space Mono', monospace;
            font-size: 12px; font-weight: 700;
            text-transform: uppercase; color: var(--gold);
            margin-bottom: 4px;
        }
        .exp-content { font-size: 17px; line-height: 1.7; color: var(--muted); }

        @media (max-width: 768px) {
            .profile-grid { grid-template-columns: 1fr; }
            .nav-links { display: none; } /* Consider adding a hamburger menu for mobile */
        }
    </style>
</head>
<body>

<nav>
    <a onclick="showPage('home')" class="nav-brand">Sri Hardyanti</a>
    <ul class="nav-links">
        <li><a onclick="showPage('home')" id="link-home">Profile</a></li>
        <li><a onclick="showPage('experience')" id="link-experience">Experience</a></li>
        <li><a onclick="showPage('work')" id="link-work">Expertise</a></li>
        <li><a onclick="showPage('contact')" id="link-contact">Contact</a></li>
    </ul>
</nav>

<div id="home" class="page active">
    <div class="profile-grid">
        <div>
            <div class="section-eyebrow">Instructional Designer</div>
            <h1 class="profile-name">Sri<br>Hardyanti</h1>
            <p class="about-text">Instructional Design professional with 4+ years of experience specializing in psychology-based learning content. Proficient in structured course design and quality assurance.</p>
            <button onclick="showPage('work')" style="padding: 15px 30px; background: var(--navy); color: white; border: none; cursor: pointer; font-weight: 600;">VIEW MY WORK</button>
        </div>
        <div>
            </div>
    </div>
</div>

<div id="experience" class="page">
    <div class="section-eyebrow">Career Journey</div>
    <h2 class="section-title">Professional Experience</h2>
    
    <div class="exp-item">
        <div class="exp-header">
            <div class="exp-org">Company Name / Organization</div>
            <div style="font-family: 'Space Mono'; font-size: 14px;">2020 — Present</div>
        </div>
        <div class="exp-role">Lead Instructional Designer</div>
        <p class="exp-content">Managed end-to-end development of psychology-based learning modules and coordinated with cross-functional SMEs.</p>
    </div>
    </div>

<div id="work" class="page">
    <div class="section-eyebrow">Showcase</div>
    <h2 class="section-title">Expertise & Analytical Approach</h2>
    
    <div class="expertise-grid">
        <div class="expertise-card">
            <h3 style="font-family: 'Playfair Display'; margin-bottom: 10px;">Quality Assurance</h3>
            
            <div>
                <div class="exp-section-title">Process</div>
                <p class="exp-content">Comprehensive review of self-paced content using standardized rubrics to ensure pedagogical alignment.</p>
            </div>
            
            <div>
                <div class="exp-section-title">Analytical Approach</div>
                <p class="exp-content">Data-driven feedback loops that identify recurring content gaps and structural inconsistencies.</p>
            </div>

            <div>
                <div class="exp-section-title">Output</div>
                <p class="exp-content">Refined curriculum maps and high-engagement learning modules.</p>
            </div>
        </div>

        </div>
</div>

<div id="contact" class="page" style="text-align: center;">
    <div class="section-eyebrow">Get in Touch</div>
    <h2 class="section-title">Let's Collaborate</h2>
    <p style="margin-bottom: 40px; font-size: 20px;">Open to discussions on instructional design, AI in education, and research translation.</p>
    <a href="mailto:your-email@example.com" style="font-size: 24px; color: var(--navy); font-weight: 700;">email@srihardyanti.com</a>
</div>

<script>
    function showPage(pageId) {
        // Hide all pages
        const pages = document.querySelectorAll('.page');
        pages.forEach(page => page.classList.remove('active'));
        
        // Show the selected page
        document.getElementById(pageId).classList.add('active');
        
        // Update Nav Links
        const links = document.querySelectorAll('.nav-links a');
        links.forEach(link => link.classList.remove('active'));
        document.getElementById('link-' + pageId).classList.add('active');
        
        // Scroll to top of the new page
        window.scrollTo(0, 0);
    }
</script>

</body>
</html>
