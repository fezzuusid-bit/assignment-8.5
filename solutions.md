HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DevPortfolio Gallery — CSS Grid Mini-Project</title>
    <meta name="description" content="A modern, fully responsive photo and project gallery website built using CSS Grid layout systems.">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="site-layout">
        <!-- Header -->
        <header class="site-header">
            <div class="logo">
                <a href="#">GridGallery</a>
            </div>
            <nav class="site-nav">
                <ul>
                    <li><a href="#" class="active">All Projects</a></li>
                    <li><a href="#">UI/UX Design</a></li>
                    <li><a href="#">Web Apps</a></li>
                    <li><a href="#">Photography</a></li>
                </ul>
            </nav>
        </header>

        <!-- Main Content Area -->
        <main class="site-main">
            <section class="gallery-hero">
                <h1>Featured Work & Photography</h1>
                <p>Exploring responsive CSS Grid systems with named areas, implicit auto-fit flows, and explicit card placement.</p>
            </section>

            <!-- Grid Layout -->
            <section class="gallery-grid">
                <!-- Featured Card (Explicit Grid Placement / Spans 2 Columns & Rows) -->
                <article class="card card-featured">
                    <div class="card-image-wrapper">
                        <img src="images/project-hero.jpg" alt="Featured Developer Workstation Setup" class="card-img">
                        <span class="card-tag">Featured</span>
                    </div>
                    <div class="card-body">
                        <h3>Full-Stack Developer Workstation</h3>
                        <p>High-performance setup designed for modern web engineering, multi-monitor debugging, and UI design.</p>
                    </div>
                </article>

                <!-- Standard Cards -->
                <article class="card">
                    <div class="card-image-wrapper">
                        <img src="images/project-1.jpg" alt="Responsive Web Application Dashboard" class="card-img">
                        <span class="card-tag">Web App</span>
                    </div>
                    <div class="card-body">
                        <h3>Analytics Dashboard</h3>
                        <p>Real-time data visualization built with semantic HTML5 and CSS Grid components.</p>
                    </div>
                </article>

                <article class="card">
                    <div class="card-image-wrapper">
                        <img src="images/project-2.jpg" alt="Mobile App UI Wireframing" class="card-img">
                        <span class="card-tag">UI/UX</span>
                    </div>
                    <div class="card-body">
                        <h3>Mobile Interface System</h3>
                        <p>Clean design tokens and modular UI components engineered for cross-platform apps.</p>
                    </div>
                </article>

                <article class="card">
                    <div class="card-image-wrapper">
                        <img src="images/project-3.jpg" alt="Mechanical Keyboard Architecture" class="card-img">
                        <span class="card-tag">Hardware</span>
                    </div>
                    <div class="card-body">
                        <h3>Custom Ergonomic Keyboard</h3>
                        <p>Hot-swappable custom build engineered for high-speed programming workflows.</p>
                    </div>
                </article>

                <article class="card">
                    <div class="card-image-wrapper">
                        <img src="images/project-4.jpg" alt="Cloud Infrastructure Server Rack" class="card-img">
                        <span class="card-tag">DevOps</span>
                    </div>
                    <div class="card-body">
                        <h3>Cloud Server Deployment</h3>
                        <p>Scalable container architecture configured for automated continuous integration.</p>
                    </div>
                </article>

                <article class="card">
                    <div class="card-image-wrapper">
                        <img src="images/project-5.jpg" alt="Code IDE Interface Screen" class="card-img">
                        <span class="card-tag">Frontend</span>
                    </div>
                    <div class="card-body">
                        <h3>Dark Syntax Theme</h3>
                        <p>Custom developer environment color scheme optimized for long coding sessions.</p>
                    </div>
                </article>
            </section>
        </main>

        <!-- Footer -->
        <footer class="site-footer">
            <div class="footer-content">
                <p>&copy; 2026 Atim Akhtar. Invertis University. All rights reserved.</p>
                <div class="footer-links">
                    <a href="https://github.com/AtimAkhtar" target="_blank" rel="noopener">GitHub</a>
                    <a href="https://www.linkedin.com/in/atim-akhtar-68b409430" target="_blank" rel="noopener">LinkedIn</a>
                </div>
            </div>
        </footer>
    </div>
</body>
</html>
CSS
/* style.css */
:root {
    --primary-color: #0284c7;
    --primary-hover: #0369a1;
    --secondary-color: #0f172a;
    --bg-color: #f8fafc;
    --surface-color: #ffffff;
    --text-color: #334155;
    --text-muted: #64748b;
    --border-color: #e2e8f0;
    
    --space-sm: 8px;
    --space-md: 16px;
    --space-lg: 24px;
    --space-xl: 32px;
    
    --radius-md: 8px;
    --radius-lg: 12px;
    --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.05);
    --shadow-md: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    line-height: 1.6;
}

/* 1 & 3. Primary Page Layout using Named Grid Areas */
.site-layout {
    display: grid;
    min-height: 100vh;
    grid-template-rows: auto 1fr auto;
    grid-template-columns: 1fr;
    grid-template-areas:
        "header"
        "main"
        "footer";
}

/* Header Area */
.site-header {
    grid-area: header;
    background-color: var(--secondary-color);
    color: var(--surface-color);
    padding: var(--space-md) var(--space-xl);
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: var(--space-md);
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo a {
    font-size: 1.5rem;
    font-weight: bold;
    color: var(--surface-color);
    text-decoration: none;
}

.site-nav ul {
    list-style: none;
    display: flex;
    gap: var(--space-lg);
}

.site-nav a {
    color: #94a3b8;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.2s ease;
}

.site-nav a:hover,
.site-nav a.active {
    color: #38bdf8;
}

/* Main Area */
.site-main {
    grid-area: main;
    max-width: 1300px;
    width: 100%;
    margin: 0 auto;
    padding: 3rem var(--space-xl);
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
}

.gallery-hero h1 {
    font-size: 2.25rem;
    color: var(--secondary-color);
    margin-bottom: 0.5rem;
}

.gallery-hero p {
    color: var(--text-muted);
    font-size: 1.1rem;
}

/* 2. Responsive Cards Grid using repeat(), minmax(), fr units, and gap */
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: var(--space-xl);
    grid-auto-flow: dense;
}

/* Card Styles */
.card {
    background-color: var(--surface-color);
    border: 1px solid var(--border-color);
    border-radius: var(--radius-lg);
    overflow: hidden;
    box-shadow: var(--shadow-sm);
    display: flex;
    flex-direction: column;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
    transform: translateY(-4px);
    box-shadow: var(--shadow-md);
}

/* 3. Explicit Grid Placement for Featured Card on Large Viewports */
@media (min-width: 900px) {
    .card-featured {
        grid-column: span 2;
        grid-row: span 2;
    }
}

.card-image-wrapper {
    position: relative;
    width: 100%;
    height: 220px;
    background-color: #f1f5f9;
    overflow: hidden;
}

.card-featured .card-image-wrapper {
    height: 340px;
}

/* 4. Overflow Prevention for Images */
.card-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    transition: transform 0.3s ease;
}

.card:hover .card-img {
    transform: scale(1.03);
}

.card-tag {
    position: absolute;
    top: 12px;
    right: 12px;
    background-color: var(--secondary-color);
    color: var(--surface-color);
    font-size: 0.75rem;
    font-weight: bold;
    padding: 4px 10px;
    border-radius: 20px;
    text-transform: uppercase;
}

/* 4. Text Content & Ellipsis Overflow Prevention */
.card-body {
    padding: var(--space-lg);
    display: flex;
    flex-direction: column;
    gap: var(--space-sm);
    flex-grow: 1;
}

.card-body h3 {
    font-size: 1.2rem;
    color: var(--secondary-color);
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.card-body p {
    color: var(--text-muted);
    font-size: 0.95rem;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

/* Footer Area */
.site-footer {
    grid-area: footer;
    background-color: var(--secondary-color);
    color: var(--surface-color);
    padding: var(--space-lg) var(--space-xl);
    border-top: 1px solid var(--border-color);
}

.footer-content {
    max-width: 1300px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: var(--space-md);
    font-size: 0.875rem;
    color: #94a3b8;
}

.footer-links {
    display: flex;
    gap: var(--space-md);
}

.footer-links a {
    color: #94a3b8;
    text-decoration: none;
    transition: color 0.2s ease;
}

.footer-links a:hover {
    color: #38bdf8;
}