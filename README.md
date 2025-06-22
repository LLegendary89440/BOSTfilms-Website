<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BOSTfilms - Cinematic Production</title>
    <style>
        /* --- Global Resets & Apple-inspired Base Styles --- */
        :root {
            /* Light Theme Base with Blue/Green Prominence */
            --base-bg-color: #f5f5f7;       /* Apple's light grey / off-white */
            --content-bg-color: #ffffff;     /* White for cards */
            --primary-text-color: #1d1d1f;   /* Dark grey for headings */
            --secondary-text-color: #6e6e73; /* Medium grey for paragraphs */
            
            --accent-blue: #007aff; 
            --accent-blue-hover: #0071e3;
            --accent-green: #34c759; 
            --accent-green-hover: #2dbd52;

            /* Text on dark/vibrant backgrounds (e.g., hero) */
            --text-on-accent-bg: #ffffff; 

            --font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            --container-width: 1024px;
            --border-radius-large: 18px;
            --border-radius-medium: 12px;
            --border-radius-small: 8px;

            --section-alt-bg-color: #eef2f7; /* Optional subtle alternate bg for sections */
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-family);
            background-color: var(--base-bg-color);
            color: var(--primary-text-color); /* Default text color */
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        /* --- Typography --- */
        h1, h2, h3, h4 {
            font-weight: 600;
            margin-bottom: 1.5rem;
            color: var(--primary-text-color);
            letter-spacing: -0.01em;
        }

        h1 {
            font-size: clamp(2.5rem, 5vw + 1rem, 4.5rem);
            line-height: 1.1;
        }

        h2 {
            font-size: clamp(2rem, 4vw, 3rem);
            text-align: center;
            padding-top: 3rem;
            margin-bottom: 3rem;
        }

        h3 { /* Used for section sub-titles or group titles, less prominent */
            font-size: 1.75rem;
        }
        
        h4 { /* Used for item titles within cards */
            font-size: 1.25rem;
            font-weight: 500;
            margin-bottom: 0.75rem;
        }

        p {
            margin-bottom: 1.25rem;
            font-size: 1.05rem;
            color: var(--secondary-text-color);
            max-width: 680px;
        }
        section p.section-intro-text, section > div > p:first-of-type { /* For centered section text */
             margin-left: auto;
             margin-right: auto;
        }


        a {
            color: var(--accent-blue);
            text-decoration: none;
            transition: color 0.2s ease-in-out;
        }

        a:hover {
            color: var(--accent-blue-hover);
        }

        /* --- Layout & Structure --- */
        .container {
            width: 90%;
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 2rem 0;
        }

        section {
            padding: 5rem 0;
            text-align: center;
            overflow: hidden; /* For animations */
        }
        section#services { /* Example of using an alternate subtle bg */
            background-color: var(--section-alt-bg-color);
        }
        
        .section-intro-text {
            font-size: 1.2rem;
            color: var(--secondary-text-color);
            margin-bottom: 3rem;
            max-width: 720px;
        }


        /* --- Header & Navigation --- */
        .main-header {
            background-color: rgba(245, 245, 247, 0.82); /* Light translucent */
            backdrop-filter: saturate(180%) blur(20px);
            -webkit-backdrop-filter: saturate(180%) blur(20px);
            padding: 0.75rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            width: 100%;
            border-bottom: 1px solid rgba(0,0,0,0.07);
        }

        .main-header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 0.5rem;
            padding-bottom: 0.5rem;
        }

        .logo {
            font-size: 1.7rem;
            font-weight: 700;
            color: var(--primary-text-color); /* Dark text on light header */
            letter-spacing: -0.02em;
        }
        .logo span { color: var(--accent-green); } 

        .main-nav ul {
            list-style: none;
            display: flex;
        }

        .main-nav ul li {
            margin-left: 25px;
        }

        .main-nav ul li a {
            color: var(--primary-text-color); /* Dark text on light header */
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.2s ease-in-out;
        }
        .main-nav ul li a:hover {
            color: var(--accent-green); 
        }

        /* --- Hero Section --- */
        #hero {
            min-height: 85vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding-top: 0;
            background: linear-gradient(135deg, var(--accent-blue) 0%, var(--accent-green) 100%);
            color: var(--text-on-accent-bg); /* White text on vibrant bg */
        }

        #hero h1 {
            color: var(--text-on-accent-bg);
            margin-bottom: 1rem;
        }
        #hero p.tagline {
            font-size: 1.5rem;
            font-weight: 400;
            margin-bottom: 2.5rem;
            color: rgba(255, 255, 255, 0.9); /* Slightly softer white */
            max-width: 650px;
        }
        .cta-button {
            display: inline-block;
            background-color: var(--content-bg-color); /* White button on hero */
            color: var(--accent-blue); /* Blue text on white button */
            padding: 14px 30px;
            border-radius: var(--border-radius-medium);
            font-weight: 600;
            font-size: 1rem;
            transition: background-color 0.2s ease-in-out, transform 0.2s ease-in-out, color 0.2s ease-in-out;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        .cta-button:hover {
            background-color: #f0f0f0; /* Slightly darker white */
            color: var(--accent-blue-hover);
            transform: scale(1.03);
        }
        /* For CTAs outside hero (on light backgrounds) */
        .cta-button.accent-bg {
            background-color: var(--accent-blue);
            color: var(--text-on-accent-bg);
        }
         .cta-button.accent-bg:hover {
            background-color: var(--accent-blue-hover);
            color: var(--text-on-accent-bg);
        }
        .cta-button.green-accent {
            background-color: var(--accent-green);
            color: var(--text-on-accent-bg);
        }
        .cta-button.green-accent:hover {
            background-color: var(--accent-green-hover);
            color: var(--text-on-accent-bg);
        }


        /* --- Services Section --- */
        #services .service-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            text-align: left;
            margin-top: 3rem;
        }
        .service-item {
            background-color: var(--content-bg-color); /* White cards */
            padding: 2rem 1.5rem;
            border-radius: var(--border-radius-large);
            transition: transform 0.3s ease-out, box-shadow 0.3s ease-out;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }
        .service-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.08);
        }
        .service-item h4 { 
            color: var(--accent-green); /* Green for service titles */
            margin-bottom: 0.5rem;
        }
        .service-item p {
            font-size: 0.95rem;
            color: var(--secondary-text-color);
        }


        /* --- Portfolio Section --- */
        #portfolio .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            margin-top: 1rem; 
        }
        .portfolio-item {
            background-color: var(--content-bg-color); /* White cards */
            border-radius: var(--border-radius-large);
            overflow: hidden;
            text-align: left;
            transition: transform 0.3s ease-out, box-shadow 0.3s ease-out;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }
         .portfolio-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.08);
        }
        .portfolio-item img {
            width: 100%;
            height: 220px; 
            object-fit: cover;
            display: block;
            transition: transform 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        .portfolio-item:hover img {
            transform: scale(1.08);
        }
        .portfolio-item-content {
            padding: 1.5rem;
        }
        .portfolio-item-content h4 { 
            margin-top: 0;
            font-size: 1.4rem;
            color: var(--primary-text-color); 
        }
        .portfolio-item-content p {
            font-size: 0.95rem;
            color: var(--secondary-text-color);
        }

        /* --- Contact Section --- */
        #contact .container > p:first-of-type { /* Target direct child p for intro text */
            max-width: 600px;
            margin-bottom: 2.5rem;
            font-size: 1.1rem;
        }
        .contact-info a {
            display: inline-block; 
            margin: 0.5rem 1rem 0.5rem 0;
            font-size: 1.2rem;
            font-weight: 500;
            color: var(--accent-green); /* Green for contact email */
        }
        .contact-info a:hover {
            color: var(--accent-green-hover);
        }
        .contact-info p {
            margin-bottom: 0.5rem; 
            color: var(--primary-text-color); /* Make "Email:" label darker */
        }


        /* --- Footer --- */
        .main-footer {
            text-align: center;
            padding: 3rem 0;
            background-color: var(--base-bg-color); 
            border-top: 1px solid #d2d2d7; 
            font-size: 0.9rem;
        }
        .main-footer p {
            color: var(--secondary-text-color);
            margin-bottom: 0.5rem;
            font-size: 0.85rem;
        }
        .main-footer .container {
            padding-top: 0;
            padding-bottom: 0;
        }

        /* --- Animations --- */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .animate-on-scroll.is-visible {
            opacity: 1;
            transform: translateY(0);
        }
        .service-grid > .animate-on-scroll,
        .portfolio-grid > .animate-on-scroll {
            transition-delay: calc(0.1s * var(--animation-order, 0));
        }


        /* --- Responsive --- */
        @media (max-width: 768px) {
            h1 { font-size: 2.8rem; }
            #hero h1 { font-size: 3rem; }
            #hero p.tagline { font-size: 1.3rem; }

            .main-header .container {
                flex-direction: column;
                padding-top: 0.25rem;
                padding-bottom: 0.25rem;
            }
            .main-nav ul {
                margin-top: 1rem;
                padding-left: 0;
                justify-content: center;
            }
            .main-nav ul li {
                margin: 0 12px;
            }

            #services .service-grid,
            #portfolio .portfolio-grid {
                grid-template-columns: 1fr; 
            }
            .service-item, .portfolio-item {
                padding: 1.5rem;
            }
            .portfolio-item img {
                height: 200px;
            }
            section {
                padding: 3.5rem 0;
            }
            h2 {
                font-size: 2.2rem;
                margin-bottom: 2rem;
            }
        }

    </style>
</head>
<body>

    <header class="main-header">
        <div class="container">
            <a href="#hero" class="logo">BOST<span>films</span></a>
            <nav class="main-nav">
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Work</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section id="hero">
            <div class="container animate-on-scroll">
                <h1>BOSTfilms</h1>
                <p class="tagline">Crafting Cinematic Narratives, Frame by Frame.</p>
                <a href="#contact" class="cta-button">Start Your Project</a>
            </div>
        </section>

        <section id="about">
            <div class="container">
                <h2 class="animate-on-scroll">About BOSTfilms</h2>
                <p style="max-width: 700px; margin: 0 auto 1rem auto;" class="animate-on-scroll">
                    BOSTfilms is a modern production house dedicated to bringing powerful stories to life.
                    We believe in the art of visual storytelling, combining innovative techniques with a passion
                    for cinematic excellence to create films that resonate and inspire.
                </p>
                <p style="max-width: 700px; margin: 0 auto;" class="animate-on-scroll">
                    From concept development to final cut, our team is committed to a collaborative and creative process,
                    ensuring your vision is realized with professionalism and artistry.
                </p>
            </div>
        </section>

        <section id="services"> <!-- This section has a subtle alternate background -->
            <div class="container">
                <h2 class="animate-on-scroll">Our Services</h2>
                <p class="section-intro-text animate-on-scroll">
                    We offer a comprehensive suite of film production services, tailored to your creative vision and project goals.
                </p>
                <div class="service-grid">
                    <div class="service-item animate-on-scroll" style="--animation-order: 1;">
                        <h4>Pre-Production</h4>
                        <p>Concept development, scriptwriting, storyboarding, casting, location scouting, and budgeting. We lay the groundwork for a successful shoot.</p>
                    </div>
                    <div class="service-item animate-on-scroll" style="--animation-order: 2;">
                        <h4>Production</h4>
                        <p>High-quality filming with professional crews, state-of-the-art equipment, direction, cinematography, and sound recording.</p>
                    </div>
                    <div class="service-item animate-on-scroll" style="--animation-order: 3;">
                        <h4>Post-Production</h4>
                        <p>Editing, color grading, visual effects (VFX), sound design, mixing, and final mastering for delivery across all platforms.</p>
                    </div>
                     <div class="service-item animate-on-scroll" style="--animation-order: 4;">
                        <h4>Documentary Filmmaking</h4>
                        <p>Capturing reality with compelling narratives, in-depth research, and sensitive storytelling for impactful documentary features and shorts.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="portfolio">
            <div class="container">
                <h2 class="animate-on-scroll">Our Work</h2>
                <p class="section-intro-text animate-on-scroll">A selection of projects that showcase our dedication to quality and creativity.</p>
                <div class="portfolio-grid">
                    <div class="portfolio-item animate-on-scroll" style="--animation-order: 1;">
                        <img src="https://via.placeholder.com/600x400.png?text=The+Agents+1+Still" alt="The Agents 1 Film Still">
                        <div class="portfolio-item-content">
                            <h4>The Agents 1</h4>
                            <p>A thrilling start to an epic espionage saga.</p>
                        </div>
                    </div>
                    <div class="portfolio-item animate-on-scroll" style="--animation-order: 2;">
                        <img src="https://via.placeholder.com/600x400.png?text=The+Agents+2+Scene" alt="The Agents 2 Film Scene">
                        <div class="portfolio-item-content">
                            <h4>The Agents 2</h4>
                            <p>The adventure continues with higher stakes.</p>
                        </div>
                    </div>
                    <div class="portfolio-item animate-on-scroll" style="--animation-order: 3;">
                        <img src="https://via.placeholder.com/600x400.png?text=The+Agents+3+Shot" alt="The Agents 3 Film Shot">
                        <div class="portfolio-item-content">
                            <h4>The Agents 3</h4>
                            <p>The breathtaking conclusion to the trilogy.</p>
                        </div>
                    </div>
                    <!-- Add more portfolio items as needed -->
                </div>
                 <a href="#contact" class="cta-button accent-bg green-accent animate-on-scroll" style="margin-top: 3rem;">Discuss Your Project</a>
            </div>
        </section>

        <section id="contact">
            <div class="container">
                <h2 class="animate-on-scroll">Get In Touch</h2>
                <p class="animate-on-scroll">
                    Ready to bring your vision to the screen? We'd love to hear about your project.
                    Contact us to discuss your ideas and how BOSTfilms can help.
                </p>
                <div class="contact-info animate-on-scroll">
                    <p>Email: <a href="mailto:bostfilmsinfo@gmail.com">bostfilmsinfo@gmail.com</a></p>
                </div>
            </div>
        </section>
    </main>

    <footer class="main-footer">
        <div class="container">
            <p>&copy; <span id="currentYear"></span> BOSTfilms. All Rights Reserved.</p>
            <p>Crafting Cinema with Passion.</p>
            <p style="font-size: 0.8rem; margin-top: 0.75rem;">Website by Mattis.</p>
        </div>
    </footer>

    <script>
        document.getElementById('currentYear').textContent = new Date().getFullYear();

        const animatedElements = document.querySelectorAll('.animate-on-scroll');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('is-visible');
                }
            });
        }, {
            rootMargin: '0px',
            threshold: 0.1
        });
        animatedElements.forEach(el => observer.observe(el));
    </script>

</body>
