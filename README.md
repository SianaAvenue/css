/* Base Styles */
:root {
    --primary-color: #8b5cf6;
    --secondary-color: #3b82f6;
    --background-dark: #1a1a1a;
    --text-light: #ffffff;
    --text-gray: #9ca3af;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: system-ui, -apple-system, sans-serif;
    line-height: 1.5;
    color: var(--text-light);
    background: var(--background-dark);
}

.bg-gradient {
    background: linear-gradient(to bottom, #1e1b4b, #3b2465, #1e1b4b);
    min-height: 100vh;
}

.container {
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 1rem;
}

/* Navigation */
.main-nav {
    background: rgba(0, 0, 0, 0.2);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    position: sticky;
    top: 0;
    z-index: 100;
}

.nav-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 4rem;
}

.nav-links {
    display: flex;
    gap: 2rem;
}

.nav-link {
    color: var(--text-light);
    text-decoration: none;
    opacity: 0.8;
    transition: opacity 0.2s;
}

.nav-link:hover {
    opacity: 1;
}

.nav-link.active {
    opacity: 1;
    font-weight: 500;
}

/* Buttons */
.btn {
    padding: 0.5rem 1rem;
    border-radius: 0.5rem;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.2s;
}

.btn-primary {
    background: var(--primary-color);
    color: var(--text-light);
    border: none;
}

.btn-outline {
    background: transparent;
    border: 1px solid var(--text-light);
    color: var(--text-light);
}

.btn-lg {
    padding: 0.75rem 1.5rem;
    font-size: 1.1rem;
}

/* Cards */
.card {
    background: rgba(255, 255, 255, 0.05);
    border-radius: 1rem;
    padding: 1.5rem;
    border: 1px solid rgba(255, 255, 255, 0.1);
    transition: transform 0.2s;
}

.card:hover {
    transform: translateY(-2px);
}

/* Grid Layouts */
.category-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

/* Sections */
section {
    padding: 4rem 0;
}

section h2 {
    font-size: 2rem;
    margin-bottom: 2rem;
    text-align: center;
}

/* Hero Section */
.hero {
    padding: 6rem 0;
    text-align: center;
}

.hero h1 {
    font-size: 3.5rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.25rem;
    color: var(--text-gray);
    margin-bottom: 2rem;
}

/* Responsive Design */
@media (max-width: 768px) {
    .nav-links {
        display: none;
    }

    .hero h1 {
        font-size: 2.5rem;
    }

    .category-grid,
    .features-grid {
        grid-template-columns: 1fr;
    }
}
