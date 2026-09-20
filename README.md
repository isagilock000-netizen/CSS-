/* --- Global Reset & Variables --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

:root {
    --primary-color: #4f46e5;
    --primary-dark: #4338ca;
    --primary-light: #818cf8;
    --bg-color: #f9fafb;
    --text-main: #1f2937;
    --text-muted: #4b5563;
    --white: #ffffff;
    --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    --transition: all 0.3s ease;
}

body {
    background-color: var(--bg-color);
    color: var(--text-main);
    line-height: 1.6;
}

/* --- Navigation Header --- */
header {
    background-color: var(--primary-color);
    color: var(--white);
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: var(--shadow);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 1.5rem;
    font-weight: 700;
    letter-spacing: 0.5px;
    color: var(--white);
}

.nav-links {
    display: flex;
    gap: 1.5rem;
}

.nav-links button {
    background: none;
    border: none;
    color: var(--white);
    font-size: 1rem;
    font-weight: 500;
    cursor: pointer;
    transition: var(--transition);
    padding: 0.5rem 0;
}

.nav-links button:hover {
    color: var(--primary-light);
}

.mobile-menu-btn {
    display: none;
    background: none;
    border: none;
    color: var(--white);
    cursor: pointer;
}

.mobile-menu {
    display: none;
    background-color: var(--primary-dark);
    padding: 1rem 1.5rem;
    flex-direction: column;
    gap: 0.75rem;
}

.mobile-menu button {
    background: none;
    border: none;
    color: var(--white);
    text-align: left;
    font-size: 1rem;
    cursor: pointer;
    padding: 0.25rem 0;
}

/* --- Main Layout & Sections --- */
main {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem 1.5rem;
}

.tab-content {
    display: none;
}

.tab-content.active {
    display: block;
}

/* --- Hero Section --- */
.hero {
    background: linear-gradient(135deg, var(--primary-color), #2563eb);
    color: var(--white);
    border-radius: 1rem;
    padding: 3rem 2rem;
    text-align: center;
    box-shadow: var(--shadow);
    margin-bottom: 2.5rem;
}

.hero h2 {
    font-size: 2.5rem;
    font-weight: 800;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.15rem;
    max-width: 700px;
    margin: 0 auto 1.5rem auto;
    color: #e0e7ff;
}

.hero-btn {
    background-color: var(--white);
    color: var(--primary-color);
    border: none;
    padding: 0.75rem 1.75rem;
    font-size: 1rem;
    font-weight: 600;
    border-radius: 0.5rem;
    cursor: pointer;
    transition: var(--transition);
    box-shadow: var(--shadow);
}

.hero-btn:hover {
    background-color: #f3f4f6;
}

/* --- Card Grids --- */
.grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
}

.card {
    background-color: var(--white);
    border: 1px solid #e5e7eb;
    border-radius: 0.75rem;
    padding: 1.5rem;
    box-shadow: var(--shadow);
    transition: var(--transition);
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}

.card h3 {
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.card-subtitle {
    font-size: 0.9rem;
    font-weight: 600;
    color: var(--primary-dark);
    margin-bottom: 0.75rem;
}

.card p {
    color: var(--text-muted);
    font-size: 0.95rem;
    margin-bottom: 1.25rem;
}

.card-btn {
    background-color: var(--primary-color);
    color: var(--white);
    border: none;
    padding: 0.6rem 1rem;
    border-radius: 0.5rem;
    font-weight: 600;
    cursor: pointer;
    transition: var(--transition);
    width: 100%;
}

.card-btn:hover {
    background-color: var(--primary-dark);
}

/* --- Section Headers ---*/
.section-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 2px solid #e5e7eb;
    padding-bottom: 0.75rem;
    margin-bottom: 1.5rem;
}

.section-header h2 {
    font-size: 1.75rem;
    font-weight: 700;
    color: var(--primary-color);
}

.section-header span {
    font-size: 0.9rem;
    color: var(--text-muted);
    font-weight: 500;
}

/* --- Modal Styles --- */
.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 2000;
    padding: 1rem;
}

.modal-overlay.active {
    display: flex;
}

.modal-box {
    background-color: var(--white);
    border-radius: 0.75rem;
    max-width: 400px;
    width: 100%;
    padding: 2rem;
    position: relative;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
}

.close-modal {
    position: absolute;
    top: 1rem;
    right: 1rem;
    background: none;
    border: none;
    font-size: 1.5rem;
    color: var(--text-muted);
    cursor: pointer;
}

.modal-box h3 {
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.modal-box p {
    font-size: 0.9rem;
    color: var(--text-muted);
    margin-bottom: 1.25rem;
}

.form-group {
    margin-bottom: 1rem;
}

.form-group label {
    display: block;
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--text-main);
    margin-bottom: 0.35rem;
}

.form-group input {
    width: 100%;
    padding: 0.6rem;
    border: 1px solid #d1d5db;
    border-radius: 0.5rem;
    font-size: 0.95rem;
}

.form-group input:focus {
    outline: none;
    border-color: var(--primary-color);
}

.submit-btn {
    background-color: var(--primary-color);
    color: var(--white);
    border: none;
    padding: 0.75rem;
    border-radius: 0.5rem;
    width: 100%;
    font-weight: 600;
    cursor: pointer;
    transition: var(--transition);
}

.submit-btn:hover {
    background-color: var(--primary-dark);
}

/* --- Footer --- */
footer {
    background-color: #1f2937;
    color: var(--white);
    text-align: center;
    padding: 1.5rem;
    margin-top: 3rem;
    font-size: 0.9rem;
    color: #9ca3af;
}

/* --- Responsive Media Queries --- */
@media (max-width: 768px) {
    .nav-links {
        display: none;
    }
    .mobile-menu-btn {
        display: block;
    }
    .mobile-menu.active {
        display: flex;
    }
    .hero h2 {
        font-size: 2rem;
    }
}
# CSS-
