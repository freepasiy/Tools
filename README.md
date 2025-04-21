Img. Comprees.Html<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ToolKit Pro - Online Image & PDF Tools</title>
    <meta name="description" content="Free online tools for images and PDFs. Compress, convert, edit and optimize your files with our easy-to-use web tools.">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #4361ee;
            --secondary: #3f37c9;
            --accent: #4895ef;
            --dark: #1b263b;
            --light: #f8f9fa;
            --success: #4cc9f0;
            --warning: #f72585;
            --gray: #adb5bd;
            --dark-gray: #495057;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            font-size: 2rem;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }

        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
            padding: 0.5rem 0;
            position: relative;
        }

        nav a:hover {
            color: var(--primary);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s;
        }

        nav a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--dark);
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 5rem 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeIn 1s ease-in-out;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }

        .search-bar {
            max-width: 600px;
            margin: 0 auto;
            position: relative;
        }

        .search-bar input {
            width: 100%;
            padding: 1rem 1.5rem;
            border-radius: 50px;
            border: none;
            font-size: 1rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .search-bar button {
            position: absolute;
            right: 5px;
            top: 5px;
            background-color: var(--accent);
            color: white;
            border: none;
            border-radius: 50px;
            padding: 0.7rem 1.5rem;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .search-bar button:hover {
            background-color: var(--secondary);
        }

        /* Categories */
        .categories {
            padding: 4rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2.2rem;
            color: var(--dark);
            margin-bottom: 1rem;
        }

        .section-title p {
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }

        .category-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .category-icon {
            background-color: var(--primary);
            color: white;
            font-size: 2rem;
            padding: 1.5rem;
            text-align: center;
        }

        .category-content {
            padding: 1.5rem;
        }

        .category-content h3 {
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .category-content p {
            color: var(--gray);
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .category-link {
            display: inline-block;
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
            font-size: 0.9rem;
            transition: color 0.3s;
        }

        .category-link:hover {
            color: var(--secondary);
        }

        .category-link i {
            margin-left: 5px;
            transition: transform 0.3s;
        }

        .category-link:hover i {
            transform: translateX(5px);
        }

        /* Popular Tools */
        .popular-tools {
            padding: 4rem 0;
            background-color: #f1f3f5;
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        .tool-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s;
        }

        .tool-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .tool-img {
            height: 180px;
            overflow: hidden;
        }

        .tool-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .tool-card:hover .tool-img img {
            transform: scale(1.05);
        }

        .tool-content {
            padding: 1.5rem;
        }

        .tool-content h3 {
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .tool-content p {
            color: var(--gray);
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .tool-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 1rem;
            font-size: 0.9rem;
        }

        .tool-rating {
            color: #ffc107;
        }

        .tool-usage {
            color: var(--gray);
        }

        /* Features */
        .features {
            padding: 4rem 0;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            align-items: center;
        }

        .feature-img {
            text-align: center;
        }

        .feature-img img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .feature-list {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .feature-item {
            display: flex;
            gap: 1rem;
        }

        .feature-icon {
            background-color: var(--primary);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .feature-text h3 {
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .feature-text p {
            color: var(--gray);
            font-size: 0.95rem;
        }

        /* CTA */
        .cta {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 5rem 0;
            text-align: center;
            margin: 4rem 0;
        }

        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }

        .cta p {
            max-width: 700px;
            margin: 0 auto 2rem;
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            cursor: pointer;
        }

        .btn-primary {
            background-color: white;
            color: var(--primary);
        }

        .btn-primary:hover {
            background-color: #f1f1f1;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .btn-outline {
            border: 2px solid white;
            color: white;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 4rem 0 2rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .footer-col h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.5rem;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--accent);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.8rem;
        }

        .footer-links a {
            color: #adb5bd;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: white;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #adb5bd;
            font-size: 0.9rem;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Responsive */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .cta h2 {
                font-size: 2rem;
            }
        }

        @media (max-width: 768px) {
            .header-container {
                padding: 1rem;
            }
            
            nav {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                background-color: white;
                box-shadow: 0 10px 15px rgba(0,0,0,0.1);
                transition: left 0.3s;
                z-index: 99;
            }
            
            nav.active {
                left: 0;
            }
            
            nav ul {
                flex-direction: column;
                padding: 1rem;
                gap: 0;
            }
            
            nav ul li {
                margin-bottom: 1rem;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero {
                padding: 3rem 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
            
            .cta h2 {
                font-size: 1.8rem;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 250px;
                text-align: center;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .search-bar input {
                padding: 0.8rem 1rem;
            }
            
            .search-bar button {
                padding: 0.5rem 1rem;
                top: 4px;
                right: 4px;
            }
            
            .section-title h2 {
                font-size: 1.6rem;
            }
            
            .feature-item {
                flex-direction: column;
                text-align: center;
            }
            
            .feature-icon {
                margin: 0 auto;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="/" class="logo">
                <i class="fas fa-tools"></i>
                <span>ToolKit Pro</span>
            </a>
            
            <nav id="mainNav">
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/image-tools">Image Tools</a></li>
                    <li><a href="/pdf-tools">PDF Tools</a></li>
                    <li><a href="/features">Features</a></li>
                    <li><a href="/about">About</a></li>
                    <li><a href="/contact">Contact</a></li>
                </ul>
            </nav>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Powerful Online Tools for Images & PDFs</h1>
            <p>Free, fast and easy-to-use tools to compress, convert, edit and optimize your files. No installation required!</p>
            
            <div class="search-bar">
                <input type="text" placeholder="Search for tools...">
                <button type="submit"><i class="fas fa-search"></i> Search</button>
            </div>
        </div>
    </section>

    <!-- Categories -->
    <section class="categories">
        <div class="container">
            <div class="section-title">
                <h2>Browse by Category</h2>
                <p>Discover our collection of specialized tools organized by categories</p>
            </div>
            
            <div class="category-grid">
                <!-- Image Tools -->
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-image"></i>
                    </div>
                    <div class="category-content">
                        <h3>Image Tools</h3>
                        <p>Compress, resize, convert and edit your images with our powerful tools.</p>
                        <a href="/image-tools" class="category-link">Explore Tools <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <!-- PDF Tools -->
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-file-pdf"></i>
                    </div>
                    <div class="category-content">
                        <h3>PDF Tools</h3>
                        <p>Merge, split, compress and convert PDF files with ease.</p>
                        <a href="/pdf-tools" class="category-link">Explore Tools <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <!-- Conversion -->
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-exchange-alt"></i>
                    </div>
                    <div class="category-content">
                        <h3>Conversion</h3>
                        <p>Convert between different file formats quickly and easily.</p>
                        <a href="/conversion-tools" class="category-link">Explore Tools <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <!-- Compression -->
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-compress-alt"></i>
                    </div>
                    <div class="category-content">
                        <h3>Compression</h3>
                        <p>Reduce file sizes without losing quality for faster sharing.</p>
                        <a href="/compression-tools" class="category-link">Explore Tools <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Popular Tools -->
    <section class="popular-tools">
        <div class="container">
            <div class="section-title">
                <h2>Most Popular Tools</h2>
                <p>Our users' favorite tools that save time and simplify workflows</p>
            </div>
            
            <div class="tools-grid">
                <!-- Image Compressor -->
                <div class="tool-card">
                    <div class="tool-img">
                        <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Image Compressor">
                    </div>
                    <div class="tool-content">
                        <h3>Image Compressor</h3>
                        <p>Reduce image file size without noticeable quality loss. Supports JPG, PNG, WebP.</p>
                        <div class="tool-meta">
                            <div class="tool-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                                <span>4.7</span>
                            </div>
                            <div class="tool-usage">
                                <i class="fas fa-users"></i> 250K+/mo
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- PDF Merger -->
                <div class="tool-card">
                    <div class="tool-img">
                        <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="PDF Merger">
                    </div>
                    <div class="tool-content">
                        <h3>PDF Merger</h3>
                        <p>Combine multiple PDF files into a single document in seconds.</p>
                        <div class="tool-meta">
                            <div class="tool-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span>4.9</span>
                            </div>
                            <div class="tool-usage">
                                <i class="fas fa-users"></i> 180K+/mo
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Image Converter -->
                <div class="tool-card">
                    <div class="tool-img">
                        <img src="https://images.unsplash.com/photo-1579820010410-c10411aaaa88?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Image Converter">
                    </div>
                    <div class="tool-content">
                        <h3>Image Converter</h3>
                        <p>Convert between JPG, PNG, WebP, GIF and other image formats.</p>
                        <div class="tool-meta">
                            <div class="tool-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span>4.8</span>
                            </div>
                            <div class="tool-usage">
                                <i class="fas fa-users"></i> 150K+/mo
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- PDF to JPG -->
                <div class="tool-card">
                    <div class="tool-img">
                        <img src="https://images.unsplash.com/photo-1544197150-b99a580bb7a8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="PDF to JPG">
                    </div>
                    <div class="tool-content">
                        <h3>PDF to JPG</h3>
                        <p>Convert PDF pages to high-quality JPG images instantly.</p>
                        <div class="tool-meta">
                            <div class="tool-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                                <span>4.6</span>
                            </div>
                            <div class="tool-usage">
                                <i class="fas fa-users"></i> 120K+/mo
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Image Resizer -->
                <div class="tool-card">
                    <div class="tool-img">
                        <img src="https://images.unsplash.com/photo-1620287341056-49a2fe1a1e8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Image Resizer">
                    </div>
                    <div class="tool-content">
                        <h3>Image Resizer</h3>
                        <p>Resize images to exact dimensions while maintaining quality.</p>
                        <div class="tool-meta">
                            <div class="tool-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span>4.9</span>
                            </div>
                            <div class="tool-usage">
                                <i class="fas fa-users"></i> 200K+/mo
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- PDF Compressor -->
                <div class="tool-card">
                    <div class="tool-img">
                        <img src="https://images.unsplash.com/photo-1608500218866-7860795a6a24?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="PDF Compressor">
                    </div>
                    <div class="tool-content">
                        <h3>PDF Compressor</h3>
                        <p>Reduce PDF file size significantly while preserving quality.</p>
                        <div class="tool-meta">
                            <div class="tool-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                                <span>4.7</span>
                            </div>
                            <div class="tool-usage">
                                <i class="fas fa-users"></i> 160K+/mo
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>Why Choose Our Tools?</h2>
                <p>We provide the best online tools experience with these amazing features</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-img">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Features">
                </div>
                
                <div class="feature-list">
                    <div class="feature-item">
                        <div class="feature-icon">
                            <i class="fas fa-bolt"></i>
                        </div>
                        <div class="feature-text">
                            <h3>Lightning Fast</h3>
                            <p>Our tools process files in seconds using optimized algorithms and cloud computing.</p>
                        </div>
                    </div>
                    
                    <div class="feature-item">
                        <div class="feature-icon">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="feature-text">
                            <h3>Secure & Private</h3>
                            <p>Files are processed in your browser and never stored on our servers for maximum privacy.</p>
                        </div>
                    </div>
                    
                    <div class="feature-item">
                        <div class="feature-icon">
                            <i class="fas fa-desktop"></i>
                        </div>
                        <div class="feature-text">
                            <h3>No Installation</h3>
                            <p>All tools work directly in your browser - no software downloads required.</p>
                        </div>
                    </div>
                    
                    <div class="feature-item">
                        <div class="feature-icon">
                            <i class="fas fa-heart"></i>
                        </div>
                        <div class="feature-text">
                            <h3>100% Free</h3>
                            <p>All our tools are completely free to use with no hidden charges or watermarks.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA -->
    <section class="cta">
        <div class="container">
            <h2>Ready to Boost Your Productivity?</h2>
            <p>Join millions of users who trust our tools for their daily image and PDF needs. No registration required!</p>
            
            <div class="cta-buttons">
                <a href="/image-tools" class="btn btn-primary"><i class="fas fa-image"></i> Try Image Tools</a>
                <a href="/pdf-tools" class="btn btn-outline"><i class="fas fa-file-pdf"></i> Try PDF Tools</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h3>ToolKit Pro</h3>
                    <p>Providing free, high-quality online tools for images and PDFs since 2020.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="/">Home</a></li>
                        <li><a href="/image-tools">Image Tools</a></li>
                        <li><a href="/pdf-tools">PDF Tools</a></li>
                        <li><a href="/features">Features</a></li>
                        <li><a href="/about">About Us</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Popular Tools</h3>
                    <ul class="footer-links">
                        <li><a href="/image-compressor">Image Compressor</a></li>
                        <li><a href="/pdf-merger">PDF Merger</a></li>
                        <li><a href="/image-converter">Image Converter</a></li>
                        <li><a href="/pdf-to-jpg">PDF to JPG</a></li>
                        <li><a href="/image-resizer">Image Resizer</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Support</h3>
                    <ul class="footer-links">
                        <li><a href="/contact">Contact Us</a></li>
                        <li><a href="/faq">FAQs</a></li>
                        <li><a href="/privacy">Privacy Policy</a></li>
                        <li><a href="/terms">Terms of Service</a></li>
                        <li><a href="/blog">Blog</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 ToolKit Pro. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mainNav = document.getElementById('mainNav');
        
        mobileMenuBtn.addEventListener('click', () => {
            mainNav.classList.toggle('active');
            mobileMenuBtn.innerHTML = mainNav.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (mainNav.classList.contains('active')) {
                        mainNav.classList.remove('active');
                        mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                    }
                }
            });
        });
        
        // Animation on scroll
        const animateOnScroll = () => {
            const elements = document.querySelectorAll('.category-card, .tool-card, .feature-item');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (elementPosition < screenPosition) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        };
        
        // Set initial state for animated elements
        document.querySelectorAll('.category-card, .tool-card, .feature-item').forEach(element => {
            element.style.opacity = '0';
            element.style.transform = 'translateY(20px)';
            element.style.transition = 'all 0.5s ease';
        });
        
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>
