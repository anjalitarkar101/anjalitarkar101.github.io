/* ========================================== */
/* RESET & BASE STYLES */
/* ========================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    line-height: 1.6;
    color: #2D3748;
    background: #F8F9FE;
}

/* ========================================== */
/* HEADER / NAVIGATION */
/* ========================================== */

header {
    background: rgba(26, 26, 46, 0.95);
    backdrop-filter: blur(10px);
    box-shadow: 0 2px 30px rgba(108, 99, 255, 0.15);
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
    padding: 1rem 0;
    border-bottom: 1px solid rgba(108, 99, 255, 0.2);
}

nav {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2rem;
}

.logo {
    font-size: 1.3rem;
    font-weight: bold;
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    letter-spacing: 1px;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 2rem;
}

nav ul li a {
    text-decoration: none;
    color: #E2E8F0;
    font-weight: 500;
    transition: color 0.3s;
}

nav ul li a:hover {
    color: #FF6B9D;
}

/* ========================================== */
/* HERO SECTION */
/* ========================================== */

#hero {
    background: linear-gradient(135deg, #1A1A2E 0%, #2D1B4E 50%, #1A1A2E 100%);
    color: white;
    padding: 8rem 2rem 4rem;
    text-align: center;
    min-height: 60vh;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
}

#hero::before {
    content: '';
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle at 30% 50%, rgba(108, 99, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 70% 50%, rgba(255, 107, 157, 0.08) 0%, transparent 50%);
    animation: heroGlow 10s ease-in-out infinite alternate;
}

@keyframes heroGlow {
    0% { transform: translate(0, 0); }
    100% { transform: translate(2%, 2%); }
}

.hero-content {
    position: relative;
    z-index: 1;
}

.hero-content h1 {
    font-size: 4rem;
    margin-bottom: 1rem;
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-shadow: none;
}

.hero-content p {
    font-size: 1.3rem;
    opacity: 0.9;
    max-width: 600px;
    margin: 0 auto 2rem;
    color: #CBD5E0;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
}

.btn-primary {
    padding: 0.8rem 2.5rem;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    display: inline-block;
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    color: #FFFFFF;
    box-shadow: 0 4px 25px rgba(108, 99, 255, 0.3);
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 35px rgba(108, 99, 255, 0.4);
}

.btn-secondary {
    padding: 0.8rem 2.5rem;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    display: inline-block;
    background: rgba(255, 255, 255, 0.08);
    color: #E2E8F0;
    border: 1px solid rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px);
}

.btn-secondary:hover {
    transform: translateY(-3px);
    background: rgba(255, 255, 255, 0.15);
    border-color: #6C63FF;
}

/* ========================================== */
/* SECTION STYLES */
/* ========================================== */

section {
    padding: 4rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

section h2 {
    font-size: 2.5rem;
    text-align: center;
    margin-bottom: 3rem;
    color: #1A1A2E;
    position: relative;
}

section h2::after {
    content: '';
    display: block;
    width: 80px;
    height: 4px;
    background: linear-gradient(90deg, #6C63FF, #FF6B9D);
    margin: 10px auto 0;
    border-radius: 2px;
}

/* ========================================== */
/* ABOUT SECTION */
/* ========================================== */

#about {
    background: #FFFFFF;
}

.about-content {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 3rem;
    align-items: start;
}

.about-text p {
    margin-bottom: 1rem;
    color: #2D3748;
}

.about-text ul {
    list-style: none;
    margin: 1rem 0;
}

.about-text ul li {
    padding: 0.5rem 0;
    border-bottom: 1px solid #EDF2F7;
    color: #2D3748;
}

.about-text ul li::before {
    content: '✦ ';
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.about-stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
}

.stat {
    background: linear-gradient(135deg, #F8F9FE, #EDF0FF);
    padding: 1.5rem;
    border-radius: 16px;
    text-align: center;
    border: 1px solid rgba(108, 99, 255, 0.1);
    transition: transform 0.3s;
}

.stat:hover {
    transform: translateY(-3px);
}

.stat h3 {
    font-size: 2.5rem;
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.stat p {
    color: #4A5568;
    font-size: 0.9rem;
}

/* ========================================== */
/* PROJECTS SECTION */
/* ========================================== */

#projects {
    background: #F8F9FE;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 2rem;
}

.project-card {
    background: rgba(255, 255, 255, 0.8);
    backdrop-filter: blur(20px);
    border-radius: 20px;
    padding: 1.8rem;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.06);
    transition: all 0.4s ease;
    display: flex;
    flex-direction: column;
    border: 1px solid rgba(255, 255, 255, 0.2);
}

.project-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 50px rgba(108, 99, 255, 0.12);
    border-color: rgba(108, 99, 255, 0.2);
}

.project-icon {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

.project-card h3 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
    color: #1A1A2E;
}

.project-card p {
    color: #4A5568;
    font-size: 0.95rem;
    margin-bottom: 1rem;
    flex-grow: 1;
}

.project-card p strong {
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1rem;
}

.project-tech span {
    background: rgba(108, 99, 255, 0.08);
    padding: 0.3rem 0.8rem;
    border-radius: 20px;
    font-size: 0.8rem;
    color: #6C63FF;
    border: 1px solid rgba(108, 99, 255, 0.1);
}

.project-links {
    display: flex;
    gap: 0.5rem;
}

.btn-demo, .btn-code {
    padding: 0.5rem 1.2rem;
    border-radius: 25px;
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 600;
    transition: all 0.3s;
    flex: 1;
    text-align: center;
}

.btn-demo {
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    color: #FFFFFF;
    box-shadow: 0 4px 15px rgba(108, 99, 255, 0.2);
}

.btn-demo:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 25px rgba(108, 99, 255, 0.3);
}

.btn-code {
    background: #EDF2F7;
    color: #1A1A2E;
}

.btn-code:hover {
    background: #E2E8F0;
}

/* ========================================== */
/* SKILLS SECTION */
/* ========================================== */

#skills {
    background: #FFFFFF;
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
}

.skill-category {
    background: #F8F9FE;
    padding: 1.5rem;
    border-radius: 16px;
    border: 1px solid rgba(108, 99, 255, 0.08);
    transition: transform 0.3s;
}

.skill-category:hover {
    transform: translateY(-3px);
}

.skill-category h3 {
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 0.8rem;
    border-bottom: 2px solid rgba(108, 99, 255, 0.15);
    padding-bottom: 0.5rem;
}

.skill-category ul {
    list-style: none;
}

.skill-category ul li {
    padding: 0.4rem 0;
    color: #4A5568;
    border-bottom: 1px solid #EDF2F7;
}

.skill-category ul li:last-child {
    border-bottom: none;
}

/* ========================================== */
/* CONTACT SECTION */
/* ========================================== */

#contact {
    background: linear-gradient(135deg, #1A1A2E 0%, #2D1B4E 100%);
    color: white;
    text-align: center;
    max-width: 100%;
}

#contact h2 {
    color: #FFFFFF;
}

#contact h2::after {
    background: linear-gradient(90deg, #6C63FF, #FF6B9D);
}

.contact-content p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
    opacity: 0.9;
    color: #CBD5E0;
}

.contact-links {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
}

.contact-btn {
    background: linear-gradient(135deg, #6C63FF, #FF6B9D);
    color: #FFFFFF;
    padding: 0.8rem 2rem;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s;
    box-shadow: 0 4px 25px rgba(108, 99, 255, 0.3);
}

.contact-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 35px rgba(108, 99, 255, 0.4);
}

/* ========================================== */
/* FOOTER */
/* ========================================== */

footer {
    background: #0D0D1A;
    color: #718096;
    text-align: center;
    padding: 2rem;
    border-top: 1px solid rgba(108, 99, 255, 0.1);
}

/* ========================================== */
/* RESPONSIVE DESIGN */
/* ========================================== */

@media (max-width: 768px) {
    nav {
        flex-direction: column;
        gap: 1rem;
    }

    nav ul {
        gap: 1rem;
        flex-wrap: wrap;
        justify-content: center;
    }

    .hero-content h1 {
        font-size: 2.5rem;
    }

    .about-content {
        grid-template-columns: 1fr;
    }

    .about-stats {
        grid-template-columns: 1fr 1fr;
    }

    .projects-grid {
        grid-template-columns: 1fr;
    }

    .contact-links {
        flex-direction: column;
        align-items: center;
    }
}

@media (max-width: 480px) {
    .hero-content h1 {
        font-size: 2rem;
    }

    .hero-buttons {
        flex-direction: column;
        align-items: center;
    }

    .btn-primary, .btn-secondary {
        width: 100%;
        text-align: center;
    }

    .project-links {
        flex-direction: column;
    }
}
