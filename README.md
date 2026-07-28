<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chandan Angad Vishwakarma | Digital Portal</title>
    <style>
        :root {
            --primary: #FF9933;
            --secondary: #138808;
            --dark: #0a0d1a;
            --surface: #131722;
            --surface-hover: #1c2130;
            --text: #ffffff;
            --text-muted: #8f9cae;
            --accent: #2979ff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            scroll-behavior: smooth;
        }

        body {
            font-family: '-apple-system', BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--dark);
            color: var(--text);
            line-height: 1.6;
        }

        /* Hero Banner */
        header {
            position: relative;
            background: linear-gradient(145deg, #111424, #060814);
            padding: 100px 20px 80px;
            text-align: center;
            overflow: hidden;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,153,51,0.05) 0%, rgba(19,136,8,0.03) 50%, transparent 100%);
            z-index: 0;
        }

        .header-container {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }

        .badge {
            background: rgba(255, 153, 51, 0.1);
            color: var(--primary);
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            letter-spacing: 1px;
            text-transform: uppercase;
            display: inline-block;
            margin-bottom: 20px;
            border: 1px solid rgba(255, 153, 51, 0.2);
        }

        h1 {
            font-size: 3rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            margin-bottom: 15px;
            background: linear-gradient(to right, #ffffff, #b0c4de);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .subtitle {
            font-size: 1.25rem;
            color: var(--text-muted);
            max-width: 600px;
            margin: 0 auto 30px;
        }

        /* Navigation Bar */
        nav {
            position: sticky;
            top: 0;
            background: rgba(10, 13, 26, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            z-index: 100;
            text-align: center;
            padding: 15px 0;
        }

        nav a {
            color: var(--text-muted);
            text-decoration: none;
            font-size: 0.95rem;
            font-weight: 500;
            margin: 0 15px;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--primary);
        }

        /* Content Layout */
        .container {
            max-width: 1050px;
            margin: 50px auto;
            padding: 0 20px;
        }

        section {
            scroll-margin-top: 80px;
            margin-bottom: 60px;
        }

        .section-title {
            font-size: 1.75rem;
            font-weight: 700;
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title::after {
            content: '';
            flex: 1;
            height: 1px;
            background: rgba(255, 255, 255, 0.1);
        }

        /* Grid Framework */
        .grid-2 {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 25px;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        /* Cards Design */
        .card {
            background-color: var(--surface);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 12px;
            padding: 30px;
            transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1), border-color 0.3s ease, background-color 0.3s ease;
        }

        .card:hover {
            transform: translateY(-4px);
            background-color: var(--surface-hover);
            border-color: rgba(255, 153, 51, 0.2);
        }

        .card h3 {
            font-size: 1.2rem;
            margin-bottom: 12px;
            color: var(--text);
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Timeline / Key List elements */
        .role-item {
            display: flex;
            gap: 20px;
            padding: 20px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .role-item:last-child {
            border-bottom: none;
        }

        .icon-indicator {
            color: var(--primary);
            font-size: 1.2rem;
            line-height: 1;
        }

        .role-details h4 {
            font-size: 1.1rem;
            margin-bottom: 4px;
        }

        .role-details span {
            font-size: 0.85rem;
            color: var(--secondary);
            font-weight: 600;
        }

        /* Contact Details & Links */
        .contact-wrapper {
            background: linear-gradient(135deg, #131722 0%, #0d1017 100%);
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .btn {
            display: inline-block;
            background: rgba(255, 255, 255, 0.05);
            color: var(--text);
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 6px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: background 0.2s, color 0.2s;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .btn:hover {
            background: var(--primary);
            color: var(--dark);
            font-weight: 600;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px 20px;
            color: var(--text-muted);
            font-size: 0.85rem;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            background-color: #060811;
        }

        /* Responsive Breakpoints */
        @media (max-width: 900px) {
            .grid-3 { grid-template-columns: 1fr; }
            h1 { font-size: 2.25rem; }
        }

        @media (max-width: 700px) {
            .grid-2 { grid-template-columns: 1fr; }
            header { padding: 60px 20px 50px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-container">
            <span class="badge">Official Public Profile</span>
            <h1>Chandan Angad Vishwakarma</h1>
            <p class="subtitle">BJP IT Cell Co-Convenor (Thane City District) & Strategic Leader</p>
        </div>
    </header>

    <nav>
        <a href="#about">Overview</a>
        <a href="#portfolio">Responsibilities</a>
        <a href="#connect">Connect</a>
    </nav>

    <div class="container">
        
        <!-- Profile Overview Section -->
        <section id="about">
            <h2 class="section-title">Overview</h2>
            <div class="grid-2">
                <div class="card">
                    <h3>Strategic Governance</h3>
                    <p>Driving digital transformation, youth coordination, and technology architecture frameworks across political communication landscapes within Thane district operations.</p>
                </div>
                <div class="card">
                    <h3>Professional Core</h3>
                    <p>Holds a Master of Business Administration (MBA). Actively managing extensive operations within the high-stakes Corporate and Shipping enterprise sectors.</p>
                </div>
            </div>
        </section>

        <!-- Responsibilities Framework -->
        <section id="portfolio">
            <h2 class="section-title">Leadership & Key Areas</h2>
            <div class="card">
                <div class="role-item">
                    <div class="icon-indicator">✦</div>
                    <div class="role-details">
                        <h4>Co-Convenor</h4>
                        <span>BJP IT Cell, Thane City District</span>
                    </div>
                </div>
                <div class="role-item">
                    <div class="icon-indicator">✦</div>
                    <div class="role-details">
                        <h4>Former Vice President</h4>
                        <span>BJYM (Bharatiya Janata Party Yuva Morcha), Thane</span>
                    </div>
                </div>
                <div class="role-item">
                    <div class="icon-indicator">✦</div>
                    <div class="role-details">
                        <h4>State Secretary</h4>
                        <span>Rashtriya Vidyarthi Manch</span>
                    </div>
                </div>
                <div class="role-item">
                    <div class="icon-indicator">✦</div>
                    <div class="role-details">
                        <h4>Executive Board Member</h4>
                        <span>Namo Group Foundation, Maharashtra State</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Connectivity Portal -->
        <section id="connect">
            <h2 class="section-title">Communication Portal</h2>
