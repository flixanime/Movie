<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FyroNex Gaming | Branding & Design</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-color: #0a0a0a;
            --primary-color: #e0e0e0;
            --accent-color-1: #ff4d00; /* Fiery Orange */
            --accent-color-2: #00f2ff; /* Electric Cyan */
            --dark-grey: #1a1a1a;
            --font-heading: 'Orbitron', sans-serif;
            --font-body: 'Poppins', sans-serif;
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
            background-color: var(--bg-color);
            color: var(--primary-color);
            font-family: var(--font-body);
            overflow-x: hidden;
        }

        h1, h2, h3 {
            font-family: var(--font-heading);
            color: var(--accent-color-1);
            text-transform: uppercase;
        }

        p {
            line-height: 1.7;
            color: #b0b0b0;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        section {
            padding: 100px 0;
        }

        .section-title {
            font-size: 3rem;
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-color-1), var(--accent-color-2));
            border-radius: 2px;
        }

        #preloader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--bg-color);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 10000;
            transition: opacity 0.75s ease, visibility 0.75s ease;
        }

        .loader {
            width: 60px;
            height: 60px;
            border: 5px solid var(--dark-grey);
            border-top-color: var(--accent-color-1);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to {
                transform: rotate(360deg);
            }
        }
        
        #preloader.hidden {
            opacity: 0;
            visibility: hidden;
        }
        
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            background: radial-gradient(circle, rgba(26,26,26,0.9) 0%, rgba(10,10,10,0.95) 70%), url('https://source.unsplash.com/1600x900/?futuristic,lava,cyberpunk') no-repeat center center/cover;
            background-attachment: fixed;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(255, 77, 0, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 77, 0, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: moveGrid 5s linear infinite;
            opacity: 0.5;
            z-index: 0;
        }
        
        @keyframes moveGrid {
            from { background-position: 0 0; }
            to { background-position: 50px 50px; }
        }

        .hero-content {
            text-align: center;
            position: relative;
            z-index: 2;
        }

        .hero-text-bg {
            position: absolute;
            font-size: 15vw;
            font-weight: 900;
            color: rgba(255, 255, 255, 0.05);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-family: var(--font-heading);
            user-select: none;
            letter-spacing: 10px;
        }

        .hero h1 {
            font-size: 5rem;
            font-weight: 900;
            color: #fff;
            margin-bottom: 20px;
            position: relative;
            text-shadow: 0 0 10px var(--accent-color-1), 0 0 25px var(--accent-color-1), 0 0 5px var(--accent-color-2);
        }

        .glitch {
            position: relative;
        }

        .glitch::before,
        .glitch::after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--bg-color);
            overflow: hidden;
        }

        .glitch::before {
            left: 2px;
            text-shadow: -2px 0 var(--accent-color-2);
            animation: glitch-anim-1 2.5s infinite linear alternate-reverse;
        }

        .glitch::after {
            left: -2px;
            text-shadow: -2px 0 var(--accent-color-1), 2px 2px var(--accent-color-2);
            animation: glitch-anim-2 1.5s infinite linear alternate-reverse;
        }

        @keyframes glitch-anim-1 {
            0% { clip-path: inset(45% 0 50% 0); }
            100% { clip-path: inset(55% 0 40% 0); }
        }

        @keyframes glitch-anim-2 {
            0% { clip-path: inset(20% 0 75% 0); }
            100% { clip-path: inset(80% 0 5% 0); }
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 30px;
            color: var(--primary-color);
        }

        .cta-button {
            display: inline-block;
            padding: 15px 35px;
            border: 2px solid var(--accent-color-1);
            border-radius: 5px;
            color: var(--accent-color-1);
            text-decoration: none;
            font-family: var(--font-heading);
            font-weight: 700;
            transition: all 0.3s ease;
            box-shadow: 0 0 15px rgba(255, 77, 0, 0.5), inset 0 0 10px rgba(255, 77, 0, 0.3);
        }

        .cta-button:hover {
            background-color: var(--accent-color-1);
            color: var(--bg-color);
            box-shadow: 0 0 25px rgba(255, 77, 0, 0.8), inset 0 0 0 rgba(255, 77, 0, 0.3);
            transform: translateY(-5px);
        }
        
        .hero-top-left {
            position: absolute;
            top: 40px;
            left: 40px;
            writing-mode: vertical-rl;
            text-orientation: mixed;
            font-family: var(--font-heading);
            color: rgba(224, 224, 224, 0.5);
            letter-spacing: 5px;
            z-index: 5;
        }

        .hero-bottom-right {
            position: absolute;
            bottom: 40px;
            right: 40px;
            font-family: var(--font-heading);
            color: rgba(224, 224, 224, 0.5);
            letter-spacing: 2px;
            z-index: 5;
        }

        #services {
            background-color: var(--dark-grey);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .service-card {
            background-color: var(--bg-color);
            padding: 40px 30px;
            border: 1px solid #2a2a2a;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(
                transparent,
                var(--accent-color-1),
                transparent 30%
            );
            animation: rotate 4s linear infinite;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .service-card:hover::before {
            opacity: 1;
        }

        .service-card .card-content {
            background-color: var(--bg-color);
            position: relative;
            z-index: 1;
            padding: 20px;
            border-radius: 8px;
            margin: 2px;
            height: calc(100% - 4px);
        }

        @keyframes rotate {
            100% {
                transform: rotate(1turn);
            }
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .service-card .icon {
            font-size: 3rem;
            color: var(--accent-color-2);
            margin-bottom: 20px;
            display: inline-block;
            transition: all 0.3s ease;
        }
        
        .service-card:hover .icon {
            transform: scale(1.1);
            text-shadow: 0 0 15px var(--accent-color-2);
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .branding-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .branding-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 0 25px rgba(255, 77, 0, 0.2);
            transition: transform 0.3s ease;
        }
        
        .branding-image:hover img {
            transform: scale(1.03);
        }
        
        .branding-content h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        footer {
            background-color: var(--dark-grey);
            padding: 50px 0;
            text-align: center;
        }

        .social-icons a {
            color: var(--primary-color);
            margin: 0 15px;
            display: inline-block;
            transition: all 0.3s ease;
        }
        
        .social-icons a svg {
            width: 24px;
            height: 24px;
            fill: currentColor;
        }

        .social-icons a:hover {
            color: var(--accent-color-1);
            transform: translateY(-5px);
        }
        
        .copyright {
            margin-top: 20px;
            font-size: 0.9rem;
            color: #777;
        }
        
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(50px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        
        .animate-on-scroll.is-visible {
            opacity: 1;
            transform: translateY(0);
        }

        @media (max-width: 992px) {
            .hero h1 {
                font-size: 4rem;
            }
            .hero-text-bg {
                font-size: 18vw;
            }
        }
        
        @media (max-width: 768px) {
            .section-title {
                font-size: 2.5rem;
            }
            .hero h1 {
                font-size: 3rem;
            }
            .hero p {
                font-size: 1rem;
            }
            .hero-top-left, .hero-bottom-right {
                display: none;
            }
            .branding-grid {
                grid-template-columns: 1fr;
            }
            .branding-image {
                order: -1;
                margin-bottom: 40px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            .section-title {
                font-size: 2rem;
            }
            .services-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <div id="preloader">
        <div class="loader"></div>
    </div>
    
    <section class="hero">
        <div class="hero-text-bg">FYRONEX</div>
        <div class="hero-top-left animate-on-scroll">Est. 2024 / Digital Frontier</div>
        <div class="hero-bottom-right animate-on-scroll">Reality is Overrated</div>
        
        <div class="hero-content">
            <h1 class="glitch" data-text="FYRONEX GAMING">FYRONEX GAMING</h1>
            <p class="animate-on-scroll" style="transition-delay: 200ms;">Crafting Legendary Brands & Unforgettable Gaming Experiences</p>
            <a href="#services" class="cta-button animate-on-scroll" style="transition-delay: 400ms;">Explore Our World</a>
        </div>
    </section>

    <section id="services">
        <div class="container">
            <h2 class="section-title animate-on-scroll">Our Arsenal</h2>
            <div class="services-grid">
                
                <div class="service-card animate-on-scroll">
                   <div class="card-content">
                        <div class="icon">🎮</div>
                        <h3>Game Design</h3>
                        <p>From concept to reality, we build immersive worlds and addictive gameplay mechanics that captivate players.</p>
                   </div>
                </div>

                <div class="service-card animate-on-scroll" style="transition-delay: 200ms;">
                    <div class="card-content">
                        <div class="icon">🎨</div>
                        <h3>Branding Identity</h3>
                        <p>We forge powerful, memorable brand identities that resonate with your target audience and stand out in the digital noise.</p>
                    </div>
                </div>

                <div class="service-card animate-on-scroll" style="transition-delay: 400ms;">
                    <div class="card-content">
                        <div class="icon">🌐</div>
                        <h3>Web Development</h3>
                        <p>Creating stunning, high-performance websites that serve as the digital headquarters for your brand or game.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="branding">
        <div class="container">
             <h2 class="section-title animate-on-scroll">Forge Your Legend</h2>
            <div class="branding-grid">
                <div class="branding-content animate-on-scroll">
                    <h2>Beyond The Pixels</h2>
                    <p>A brand is more than a logo; it's a promise, an experience, a universe. We dive deep into your vision to create a strategic brand identity that feels alive. We combine cutting-edge design with market insights to ensure your project not only looks incredible but also achieves its goals.</p>
                    <p>Let's build a legacy together that echoes through the gaming community.</p>
                </div>
                <div class="branding-image animate-on-scroll" style="transition-delay: 200ms;">
                    <img src="https://source.unsplash.com/600x400/?futuristic,esports,arena" alt="Futuristic Esports Arena">
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="social-icons">
                <a href="#" aria-label="Twitter / X">
                    <svg viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
                </a>
                <a href="#" aria-label="Instagram">
                    <svg viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.85s-.011 3.584-.069 4.85c-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07s-3.584-.012-4.85-.07c-3.252-.148-4.771-1.691-4.919-4.919-.058-1.265-.069-1.645-.069-4.85s.011-3.584.069-4.85c.149-3.225 1.664-4.771 4.919-4.919C8.416 2.175 8.796 2.163 12 2.163zm0 1.441c-3.116 0-3.479.012-4.696.068-2.583.118-3.927 1.46-4.045 4.045-.056 1.217-.067 1.58-.067 4.696s.011 3.479.067 4.696c.118 2.583 1.462 3.927 4.045 4.045 1.217.056 1.58.067 4.696.067s3.479-.011 4.696-.067c2.583-.118 3.927-1.462 4.045-4.045.056-1.217.067-1.58.067-4.696s-.011-3.479-.067-4.696c-.118-2.583-1.462-3.927-4.045-4.045-1.217-.056-1.58-.068-4.696-.068zm0 3.196c-2.43 0-4.39 1.96-4.39 4.39s1.96 4.39 4.39 4.39 4.39-1.96 4.39-4.39-1.96-4.39-4.39-4.39zm0 7.332c-1.623 0-2.942-1.32-2.942-2.942s1.32-2.942 2.942-2.942 2.942 1.32 2.942 2.942-1.319 2.942-2.942 2.942zm4.492-6.526c-.767 0-1.39.623-1.39 1.39s.623 1.39 1.39 1.39 1.39-.623 1.39-1.39-.623-1.39-1.39-1.39z"/></svg>
                </a>
                <a href="#" aria-label="Discord">
                    <svg viewBox="0 0 24 24"><path d="M20.317 4.369a1.942 1.942 0 00-1.077-.314H4.76a1.942 1.942 0 00-1.077.314L2.83 5.423A19.421 19.421 0 001 13.61a19.412 19.412 0 003.11 6.446l.06.076c.21.253.47.48.77.683a.936.936 0 00.56.205c.21 0 .4-.085.56-.253.25-.262.43-.578.55-.913a16.273 16.273 0 01-1.23-2.148c.11-.076.22-.152.32-.245 4.22 1.638 8.87 1.638 13.09 0 .11.095.22.18.32.245a16.17 16.17 0 01-1.23 2.148c.12.335.3.65.55.913a.94.94 0 001.12.042c.3-.203.56-.43.77-.683l.06-.076a19.52 19.52 0 003.11-6.446 19.421 19.421 0 00-1.83-8.187zm-11.49 9.875c-1.12 0-2.02-1.02-2.02-2.27s.9-2.27 2.02-2.27c1.12 0 2.02 1.02 2.02 2.27s-.9 2.27-2.02 2.27zm4.99 0c-1.12 0-2.02-1.02-2.02-2.27s.9-2.27 2.02-2.27c1.12 0 2.02 1.02 2.02 2.27s-.9 2.27-2.02 2.27z"/></svg>
                </a>
            </div>
            <p class="copyright">&copy; 2024 FyroNex Gaming & Branding. All Rights Reserved. Created with Max Quality.</p>
        </div>
    </footer>

    <script>
        window.addEventListener('load', () => {
            const preloader = document.getElementById('preloader');
            setTimeout(() => {
                preloader.classList.add('hidden');
            }, 500);
        });

        const animatedElements = document.querySelectorAll('.animate-on-scroll');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('is-visible');
                } else {
                     entry.target.classList.remove('is-visible');
                }
            });
        }, {
            threshold: 0.1
        });

        animatedElements.forEach(element => {
            observer.observe(element);
        });
    </script>

</body>
</html>
