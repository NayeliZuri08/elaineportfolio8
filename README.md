<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ma. Elaine Gay Viason — Data Operations Specialist & VA</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0a1628;
    --navy-mid: #0f2444;
    --navy-light: #1a3a5c;
    --emerald: #10b981;
    --emerald-bright: #34d399;
    --emerald-dim: #065f46;
    --white: #f8fafc;
    --off-white: #e2e8f0;
    --muted: #94a3b8;
    --accent-gold: #f59e0b;
    --glass: rgba(255,255,255,0.04);
    --glass-border: rgba(255,255,255,0.08);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--navy);
    color: var(--white);
    overflow-x: hidden;
    cursor: default;
  }

  /* ===== GRID BACKGROUND ===== */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(16,185,129,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(16,185,129,0.04) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
    z-index: 0;
  }

  /* ===== NAV ===== */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.25rem 5%;
    background: rgba(10,22,40,0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--glass-border);
  }

  .nav-logo {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 1.1rem;
    letter-spacing: -0.02em;
    color: var(--white);
  }

  .nav-logo span { color: var(--emerald); }

  .nav-links {
    display: flex;
    gap: 2.5rem;
    list-style: none;
  }

  .nav-links a {
    font-family: 'DM Mono', monospace;
    font-size: 0.75rem;
    color: var(--muted);
    text-decoration: none;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    transition: color 0.25s;
  }

  .nav-links a:hover { color: var(--emerald); }

  .nav-cta {
    background: var(--emerald);
    color: var(--navy) !important;
    font-weight: 600 !important;
    padding: 0.5rem 1.25rem;
    border-radius: 4px;
    transition: background 0.25s !important;
  }

  .nav-cta:hover { background: var(--emerald-bright) !important; color: var(--navy) !important; }

  /* ===== HERO ===== */
  #hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 8rem 5% 4rem;
    position: relative;
    overflow: hidden;
    gap: 4rem;
  }

  .hero-orb {
    position: absolute;
    border-radius: 50%;
    filter: blur(120px);
    pointer-events: none;
  }

  .hero-orb-1 {
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(16,185,129,0.15), transparent 70%);
    top: -100px; right: -100px;
  }

  .hero-orb-2 {
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(16,185,129,0.08), transparent 70%);
    bottom: 0; left: 10%;
  }

  .hero-content { position: relative; z-index: 1; }

  .hero-tag {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--emerald);
    border: 1px solid rgba(16,185,129,0.3);
    padding: 0.35rem 0.9rem;
    border-radius: 100px;
    margin-bottom: 1.75rem;
    background: rgba(16,185,129,0.05);
  }

  .hero-tag::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--emerald);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  .hero-h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2.4rem, 4.5vw, 3.8rem);
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -0.03em;
    margin-bottom: 1.5rem;
  }

  .hero-h1 em {
    font-style: normal;
    color: var(--emerald);
    position: relative;
  }

  .hero-h1 em::after {
    content: '';
    position: absolute;
    bottom: 2px; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--emerald), transparent);
    border-radius: 2px;
  }

  .hero-sub {
    font-size: 1.05rem;
    color: var(--muted);
    line-height: 1.75;
    max-width: 480px;
    margin-bottom: 2.5rem;
    font-weight: 300;
  }

  .hero-ctas {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--emerald);
    color: var(--navy);
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 0.9rem;
    padding: 0.85rem 2rem;
    border-radius: 6px;
    text-decoration: none;
    transition: all 0.3s;
    letter-spacing: 0.02em;
  }

  .btn-primary:hover {
    background: var(--emerald-bright);
    transform: translateY(-2px);
    box-shadow: 0 12px 40px rgba(16,185,129,0.3);
  }

  .btn-secondary {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: transparent;
    color: var(--white);
    font-family: 'Syne', sans-serif;
    font-weight: 600;
    font-size: 0.9rem;
    padding: 0.85rem 2rem;
    border-radius: 6px;
    border: 1px solid var(--glass-border);
    text-decoration: none;
    transition: all 0.3s;
  }

  .btn-secondary:hover {
    border-color: rgba(16,185,129,0.5);
    color: var(--emerald);
    background: rgba(16,185,129,0.05);
  }

  .hero-stats {
    display: flex;
    gap: 2.5rem;
    margin-top: 3rem;
    padding-top: 2rem;
    border-top: 1px solid var(--glass-border);
  }

  .stat-item { }

  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    color: var(--white);
    line-height: 1;
  }

  .stat-num span { color: var(--emerald); }

  .stat-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: 0.3rem;
  }

  /* Hero Image Side */
  .hero-visual {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.5rem;
  }

  .hero-photo-wrap {
    position: relative;
    width: 340px;
    height: 420px;
  }

  .hero-photo-bg {
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, var(--navy-mid) 0%, var(--emerald-dim) 100%);
    border-radius: 20px;
    border: 1px solid rgba(16,185,129,0.2);
  }

  .hero-photo-bg::before {
    content: '';
    position: absolute;
    inset: 1px;
    border-radius: 19px;
    background: linear-gradient(135deg, rgba(16,185,129,0.1), transparent);
  }

  .hero-photo-placeholder {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    border-radius: 20px;
    overflow: hidden;
  }

  .hero-initials {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--emerald-dim), var(--emerald));
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 2.5rem;
    font-weight: 800;
    color: var(--white);
    border: 3px solid rgba(255,255,255,0.15);
  }

  .hero-name-card {
    text-align: center;
  }

  .hero-name-card h3 {
    font-family: 'Syne', sans-serif;
    font-size: 1.1rem;
    font-weight: 700;
  }

  .hero-name-card p {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--emerald);
    letter-spacing: 0.08em;
    margin-top: 0.25rem;
  }

  .hero-badge {
    position: absolute;
    bottom: -16px;
    right: -20px;
    background: var(--emerald);
    color: var(--navy);
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 0.75rem;
    padding: 0.6rem 1rem;
    border-radius: 8px;
    display: flex;
    align-items: center;
    gap: 0.4rem;
    box-shadow: 0 8px 30px rgba(16,185,129,0.4);
  }

  .hero-data-card {
    background: var(--glass);
    border: 1px solid var(--glass-border);
    border-radius: 12px;
    padding: 1rem 1.5rem;
    width: 340px;
    display: flex;
    align-items: center;
    gap: 1rem;
    backdrop-filter: blur(10px);
  }

  .data-card-icon {
    width: 40px; height: 40px;
    background: rgba(16,185,129,0.15);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.1rem;
    flex-shrink: 0;
  }

  .data-card-text p { font-size: 0.8rem; color: var(--muted); }
  .data-card-text strong {
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    display: block;
    color: var(--white);
  }

  /* ===== SECTIONS COMMON ===== */
  section { position: relative; z-index: 1; }

  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--emerald);
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .section-label::before {
    content: '';
    width: 24px; height: 1px;
    background: var(--emerald);
  }

  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    font-weight: 800;
    letter-spacing: -0.03em;
    line-height: 1.1;
    margin-bottom: 1rem;
  }

  .section-subtitle {
    font-size: 1rem;
    color: var(--muted);
    max-width: 560px;
    line-height: 1.7;
    font-weight: 300;
    margin-bottom: 3rem;
  }

  /* ===== EXPERTISE ===== */
  #expertise {
    padding: 6rem 5%;
    background: linear-gradient(to bottom, transparent, rgba(15,36,68,0.5), transparent);
  }

  .expertise-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5px;
    background: var(--glass-border);
    border: 1px solid var(--glass-border);
    border-radius: 16px;
    overflow: hidden;
    margin-top: 3rem;
  }

  .expertise-card {
    background: var(--navy);
    padding: 2.5rem 2rem;
    position: relative;
    transition: background 0.3s;
    overflow: hidden;
  }

  .expertise-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--emerald), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }

  .expertise-card:hover { background: var(--navy-mid); }
  .expertise-card:hover::before { opacity: 1; }

  .expertise-icon {
    font-size: 2rem;
    margin-bottom: 1.25rem;
    display: block;
  }

  .expertise-name {
    font-family: 'Syne', sans-serif;
    font-size: 1.15rem;
    font-weight: 700;
    margin-bottom: 0.75rem;
  }

  .expertise-desc {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.65;
  }

  .expertise-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-top: 1.25rem;
  }

  .etag {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.06em;
    padding: 0.25rem 0.6rem;
    border-radius: 4px;
    border: 1px solid rgba(16,185,129,0.25);
    color: var(--emerald);
    background: rgba(16,185,129,0.05);
  }

  /* ===== PORTFOLIO ===== */
  #portfolio {
    padding: 6rem 5%;
  }

  .portfolio-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.25rem;
    margin-top: 3rem;
  }

  .portfolio-card {
    position: relative;
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid var(--glass-border);
    background: var(--navy-mid);
    aspect-ratio: 4/3;
    cursor: pointer;
    group: true;
  }

  .portfolio-card-inner {
    width: 100%; height: 100%;
    position: relative;
    overflow: hidden;
  }

  .portfolio-thumb {
    width: 100%; height: 100%;
    object-fit: cover;
    display: block;
    transition: transform 0.5s ease, filter 0.5s ease;
  }

  .portfolio-card:hover .portfolio-thumb {
    transform: scale(1.06);
    filter: brightness(0.35);
  }

  .portfolio-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(to top, rgba(10,22,40,0.95), rgba(10,22,40,0.3));
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 1.5rem;
    transition: background 0.4s;
  }

  .portfolio-card:hover .portfolio-overlay {
    background: rgba(10,22,40,0.92);
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .portfolio-cat {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--emerald);
    margin-bottom: 0.4rem;
  }

  .portfolio-title {
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    color: var(--white);
    line-height: 1.2;
  }

  .portfolio-cta {
    display: none;
    align-items: center;
    gap: 0.5rem;
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 0.85rem;
    color: var(--emerald);
    border: 1px solid var(--emerald);
    padding: 0.6rem 1.25rem;
    border-radius: 6px;
    margin-top: 1rem;
    transition: all 0.3s;
    background: rgba(16,185,129,0.1);
  }

  .portfolio-card:hover .portfolio-cat,
  .portfolio-card:hover .portfolio-title {
    transform: translateY(-8px);
  }

  .portfolio-card:hover .portfolio-cta {
    display: inline-flex;
    animation: fadeUp 0.3s ease forwards;
  }

  .portfolio-card:hover .portfolio-cat { margin-bottom: 0.6rem; }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Portfolio placeholder visuals */
  .port-visual {
    width: 100%; height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3.5rem;
    position: absolute;
    top: 0;
  }

  .port-kpi { background: linear-gradient(135deg, #0f2444, #0d3320); }
  .port-util { background: linear-gradient(135deg, #0f2444, #1a2a0f); }
  .port-lead { background: linear-gradient(135deg, #0f1f3d, #1a1a3d); }
  .port-brand { background: linear-gradient(135deg, #2d0a08, #1a0f00); }
  .port-digital { background: linear-gradient(135deg, #1a1a0f, #0f1a2a); }
  .port-ops { background: linear-gradient(135deg, #0a1628, #0f2444); }

  /* Fake chart visual inside KPI card */
  .mini-chart {
    position: absolute;
    bottom: 60px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    align-items: flex-end;
    gap: 4px;
    opacity: 0.5;
  }

  .mini-bar {
    width: 8px;
    border-radius: 2px 2px 0 0;
    background: var(--emerald);
    animation: barGrow 1.5s ease infinite alternate;
  }

  @keyframes barGrow {
    from { opacity: 0.3; }
    to { opacity: 0.8; }
  }

  /* ===== WHY ME ===== */
  #why {
    padding: 6rem 5%;
    background: linear-gradient(to bottom, transparent, rgba(15,36,68,0.4), transparent);
  }

  .why-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: center;
    margin-top: 3rem;
  }

  .why-content { }

  .why-points {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    margin-top: 2rem;
  }

  .why-point {
    display: flex;
    gap: 1.25rem;
    align-items: flex-start;
    padding: 1.5rem;
    border: 1px solid var(--glass-border);
    border-radius: 12px;
    background: var(--glass);
    transition: border-color 0.3s, background 0.3s;
  }

  .why-point:hover {
    border-color: rgba(16,185,129,0.3);
    background: rgba(16,185,129,0.04);
  }

  .why-point-icon {
    width: 44px; height: 44px;
    flex-shrink: 0;
    background: rgba(16,185,129,0.12);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2rem;
    border: 1px solid rgba(16,185,129,0.2);
  }

  .why-point-text h4 {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 0.95rem;
    margin-bottom: 0.4rem;
  }

  .why-point-text p {
    font-size: 0.85rem;
    color: var(--muted);
    line-height: 1.6;
  }

  /* Timeline / experience side */
  .why-timeline {
    position: relative;
    padding-left: 2rem;
  }

  .why-timeline::before {
    content: '';
    position: absolute;
    left: 0; top: 10px; bottom: 10px;
    width: 1px;
    background: linear-gradient(to bottom, var(--emerald), rgba(16,185,129,0.1));
  }

  .timeline-item {
    position: relative;
    margin-bottom: 2.5rem;
    padding: 1.5rem;
    border: 1px solid var(--glass-border);
    border-radius: 12px;
    background: var(--glass);
  }

  .timeline-item::before {
    content: '';
    position: absolute;
    left: -2.5rem;
    top: 1.75rem;
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--emerald);
    border: 2px solid var(--navy);
    box-shadow: 0 0 0 3px rgba(16,185,129,0.2);
  }

  .timeline-date {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    color: var(--emerald);
    letter-spacing: 0.08em;
    margin-bottom: 0.4rem;
  }

  .timeline-role {
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    margin-bottom: 0.25rem;
  }

  .timeline-company {
    font-size: 0.8rem;
    color: var(--muted);
    margin-bottom: 0.75rem;
  }

  .timeline-bullets {
    display: flex;
    flex-direction: column;
    gap: 0.35rem;
  }

  .timeline-bullets li {
    font-size: 0.8rem;
    color: var(--muted);
    list-style: none;
    display: flex;
    gap: 0.5rem;
    line-height: 1.5;
  }

  .timeline-bullets li::before {
    content: '▸';
    color: var(--emerald);
    font-size: 0.75rem;
    flex-shrink: 0;
    margin-top: 0.05rem;
  }

  /* ===== CONTACT ===== */
  #contact {
    padding: 6rem 5% 4rem;
  }

  .contact-layout {
    display: grid;
    grid-template-columns: 1fr 1.6fr;
    gap: 4rem;
    margin-top: 3rem;
    align-items: start;
  }

  .contact-info { }

  .contact-detail {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 1.25rem;
    border: 1px solid var(--glass-border);
    border-radius: 10px;
    margin-bottom: 1rem;
    transition: border-color 0.3s;
  }

  .contact-detail:hover { border-color: rgba(16,185,129,0.3); }

  .contact-detail-icon {
    font-size: 1.1rem;
    width: 36px; height: 36px;
    background: rgba(16,185,129,0.1);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  .contact-detail-text p { font-size: 0.75rem; color: var(--muted); }
  .contact-detail-text a, .contact-detail-text span {
    font-size: 0.88rem;
    color: var(--white);
    text-decoration: none;
    font-weight: 500;
    transition: color 0.2s;
  }

  .contact-detail-text a:hover { color: var(--emerald); }

  .contact-form {
    background: var(--glass);
    border: 1px solid var(--glass-border);
    border-radius: 16px;
    padding: 2.5rem;
    backdrop-filter: blur(10px);
  }

  .contact-form h3 {
    font-family: 'Syne', sans-serif;
    font-size: 1.3rem;
    font-weight: 700;
    margin-bottom: 1.75rem;
  }

  .form-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-bottom: 1rem;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
    margin-bottom: 1rem;
  }

  .form-group label {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .form-group input,
  .form-group textarea,
  .form-group select {
    background: rgba(255,255,255,0.04);
    border: 1px solid var(--glass-border);
    border-radius: 8px;
    color: var(--white);
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    padding: 0.75rem 1rem;
    outline: none;
    transition: border-color 0.25s;
    width: 100%;
    resize: vertical;
  }

  .form-group input:focus,
  .form-group textarea:focus,
  .form-group select:focus {
    border-color: rgba(16,185,129,0.5);
    background: rgba(16,185,129,0.03);
  }

  .form-group input::placeholder,
  .form-group textarea::placeholder { color: rgba(148,163,184,0.5); }

  .form-group select option { background: var(--navy-mid); color: var(--white); }

  .form-group textarea { min-height: 110px; }

  .form-submit {
    width: 100%;
    background: var(--emerald);
    color: var(--navy);
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 0.95rem;
    padding: 0.9rem;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s;
    letter-spacing: 0.02em;
    margin-top: 0.5rem;
  }

  .form-submit:hover {
    background: var(--emerald-bright);
    transform: translateY(-2px);
    box-shadow: 0 8px 30px rgba(16,185,129,0.25);
  }

  /* ===== FOOTER ===== */
  footer {
    padding: 2rem 5%;
    border-top: 1px solid var(--glass-border);
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .footer-left {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  .footer-links {
    display: flex;
    gap: 1.5rem;
    list-style: none;
  }

  .footer-links a {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    text-decoration: none;
    letter-spacing: 0.05em;
    transition: color 0.2s;
  }

  .footer-links a:hover { color: var(--emerald); }

  /* ===== TOAST ===== */
  .toast {
    position: fixed;
    bottom: 2rem;
    right: 2rem;
    background: var(--emerald);
    color: var(--navy);
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    padding: 1rem 1.5rem;
    border-radius: 10px;
    font-size: 0.9rem;
    z-index: 999;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    transform: translateY(100px);
    opacity: 0;
    transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    pointer-events: none;
  }

  .toast.show {
    transform: translateY(0);
    opacity: 1;
  }

  /* ===== SCROLL ANIMATIONS ===== */
  .fade-up {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .fade-up.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* Stagger children */
  .stagger-children > * {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }

  .stagger-children.visible > *:nth-child(1) { opacity: 1; transform: none; transition-delay: 0s; }
  .stagger-children.visible > *:nth-child(2) { opacity: 1; transform: none; transition-delay: 0.1s; }
  .stagger-children.visible > *:nth-child(3) { opacity: 1; transform: none; transition-delay: 0.2s; }
  .stagger-children.visible > *:nth-child(4) { opacity: 1; transform: none; transition-delay: 0.3s; }
  .stagger-children.visible > *:nth-child(5) { opacity: 1; transform: none; transition-delay: 0.4s; }
  .stagger-children.visible > *:nth-child(6) { opacity: 1; transform: none; transition-delay: 0.5s; }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 900px) {
    #hero { grid-template-columns: 1fr; text-align: center; }
    .hero-visual { display: none; }
    .hero-sub { max-width: 100%; }
    .hero-ctas { justify-content: center; }
    .hero-stats { justify-content: center; }
    .expertise-grid { grid-template-columns: 1fr; }
    .portfolio-grid { grid-template-columns: 1fr 1fr; }
    .why-layout { grid-template-columns: 1fr; }
    .contact-layout { grid-template-columns: 1fr; }
    .nav-links { display: none; }
    .form-row { grid-template-columns: 1fr; }
  }

  @media (max-width: 580px) {
    .portfolio-grid { grid-template-columns: 1fr; }
  }

  /* ===== MODAL ===== */
  .modal-overlay {
    position: fixed;
    inset: 0;
    background: rgba(10,22,40,0.95);
    z-index: 200;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2rem;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s;
    backdrop-filter: blur(10px);
  }

  .modal-overlay.open {
    opacity: 1;
    pointer-events: all;
  }

  .modal-box {
    background: var(--navy-mid);
    border: 1px solid var(--glass-border);
    border-radius: 20px;
    padding: 2.5rem;
    max-width: 560px;
    width: 100%;
    position: relative;
    transform: scale(0.95) translateY(20px);
    transition: transform 0.3s;
  }

  .modal-overlay.open .modal-box {
    transform: scale(1) translateY(0);
  }

  .modal-close {
    position: absolute;
    top: 1.25rem; right: 1.25rem;
    width: 32px; height: 32px;
    background: var(--glass);
    border: 1px solid var(--glass-border);
    border-radius: 6px;
    color: var(--muted);
    font-size: 1rem;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.2s;
  }

  .modal-close:hover { color: var(--white); border-color: rgba(255,255,255,0.2); }

  .modal-cat {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--emerald);
    margin-bottom: 0.5rem;
  }

  .modal-title {
    font-family: 'Syne', sans-serif;
    font-size: 1.6rem;
    font-weight: 800;
    margin-bottom: 1rem;
  }

  .modal-body {
    font-size: 0.9rem;
    color: var(--muted);
    line-height: 1.7;
    margin-bottom: 1.5rem;
  }

  .modal-skills {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .modal-skill-tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.06em;
    padding: 0.3rem 0.7rem;
    border-radius: 4px;
    background: rgba(16,185,129,0.1);
    border: 1px solid rgba(16,185,129,0.25);
    color: var(--emerald);
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">EV<span>.</span>Data</div>
  <ul class="nav-links">
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#why">About</a></li>
    <li><a href="#contact" class="nav-cta">Hire Me</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-orb hero-orb-1"></div>
  <div class="hero-orb hero-orb-2"></div>

  <div class="hero-content">
    <div class="hero-tag">Available for Projects</div>
    <h1 class="hero-h1">Turning Raw Data into <em>Actionable Business</em> Intelligence</h1>
    <p class="hero-sub">Data Operations Specialist & Virtual Assistant with 6+ years transforming complex operational data into clarity. From KPI dashboards to brand assets — precision meets creativity.</p>
    <div class="hero-ctas">
      <a href="#portfolio" class="btn-primary">↗ View Data Portfolios</a>
      <a href="#contact" class="btn-secondary">📩 Start a Project</a>
    </div>
    <div class="hero-stats">
      <div class="stat-item">
        <div class="stat-num">6<span>+</span></div>
        <div class="stat-label">Years Experience</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">3<span>+</span></div>
        <div class="stat-label">Industries Served</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">BS<span>IT</span></div>
        <div class="stat-label">Degree Holder</div>
      </div>
    </div>
  </div>

  <div class="hero-visual">
    <div class="hero-photo-wrap">
      <div class="hero-photo-bg"></div>
      <div class="hero-photo-placeholder">
        <div class="ELAINE.jpg">EV</div>
        <div class="hero-name-card">
          <h3>Ma. Elaine Gay Viason</h3>
          <p>Data Ops · VA · Analytics</p>
        </div>
      </div>
      <div class="hero-badge">✦ BS Information Technology</div>
    </div>
    <div class="hero-data-card">
      <div class="data-card-icon">📊</div>
      <div class="data-card-text">
        <strong>KPI Dashboards & OPP Reports</strong>
        <p>Fleet · Finance · Operations</p>
      </div>
    </div>
    <div class="hero-data-card">
      <div class="data-card-icon">🎯</div>
      <div class="data-card-text">
        <strong>Lead Generation & CRM</strong>
        <p>B2B Prospecting · Email Marketing</p>
      </div>
    </div>
  </div>
</section>

<!-- EXPERTISE -->
<section id="expertise">
  <div class="section-label">Core Capabilities</div>
  <h2 class="section-title">What I Deliver</h2>
  <p class="section-subtitle">Specialized skills across data operations, marketing, and administrative support—built for businesses that need results, not just effort.</p>

  <div class="expertise-grid stagger-children">
    <div class="expertise-card">
      <span class="expertise-icon">📈</span>
      <div class="expertise-name">Data Operations & Analytics</div>
      <p class="expertise-desc">Automated dashboards, KPI tracking, and Target vs. Actual variance analysis. Transforming raw operational data into decision-ready intelligence.</p>
      <div class="expertise-tags">
        <span class="etag">Excel Advanced</span>
        <span class="etag">KPI Reports</span>
        <span class="etag">Data Visualization</span>
        <span class="etag">OPP Reports</span>
      </div>
    </div>
    <div class="expertise-card">
      <span class="expertise-icon">🎯</span>
      <div class="expertise-name">Lead Generation & CRM</div>
      <p class="expertise-desc">Targeted B2B prospecting with verified contact lists. CRM management, email marketing campaigns, and appointment setting workflows.</p>
      <div class="expertise-tags">
        <span class="etag">B2B Prospecting</span>
        <span class="etag">Email Marketing</span>
        <span class="etag">Appointment Setting</span>
        <span class="etag">CRM Management</span>
      </div>
    </div>
    <div class="expertise-card">
      <span class="expertise-icon">⚙️</span>
      <div class="expertise-name">Administrative Support</div>
      <p class="expertise-desc">Email and calendar management, workflow coordination via Trello & Notion, document management, and reliable day-to-day virtual support.</p>
      <div class="expertise-tags">
        <span class="etag">Google Workspace</span>
        <span class="etag">Trello / Notion</span>
        <span class="etag">Calendar Mgmt</span>
        <span class="etag">MS Office</span>
      </div>
    </div>
    <div class="expertise-card">
      <span class="expertise-icon">🎨</span>
      <div class="expertise-name">Brand & Graphic Design</div>
      <p class="expertise-desc">Professional marketing materials using Canva—restaurant menus, product flyers, business brochures, and promotional banners that convert.</p>
      <div class="expertise-tags">
        <span class="etag">Canva</span>
        <span class="etag">Flyer Design</span>
        <span class="etag">Menus & Brochures</span>
        <span class="etag">Brand Assets</span>
      </div>
    </div>
    <div class="expertise-card">
      <span class="expertise-icon">📱</span>
      <div class="expertise-name">Social Media Management</div>
      <p class="expertise-desc">Content scheduling, engagement monitoring, and post creation. Building brand presence across platforms aligned with business goals.</p>
      <div class="expertise-tags">
        <span class="etag">Content Strategy</span>
        <span class="etag">Scheduling</span>
        <span class="etag">Engagement</span>
        <span class="etag">Brand Voice</span>
      </div>
    </div>
    <div class="expertise-card">
      <span class="expertise-icon">🖥️</span>
      <div class="expertise-name">I.T. Support & Systems</div>
      <p class="expertise-desc">Technical troubleshooting, system maintenance, user access management, data backups, and equipment database accuracy to keep operations running.</p>
      <div class="expertise-tags">
        <span class="etag">IT Support</span>
        <span class="etag">Data Backups</span>
        <span class="etag">Systems Admin</span>
        <span class="etag">QuickBooks</span>
      </div>
    </div>
  </div>
</section>

<!-- PORTFOLIO -->
<section id="portfolio">
  <div class="section-label fade-up">Selected Work</div>
  <h2 class="section-title fade-up">Portfolio Gallery</h2>
  <p class="section-subtitle fade-up">Six samples showcasing the breadth of my capabilities — from enterprise analytics to creative brand assets.</p>

  <div class="portfolio-grid stagger-children">

    <!-- 1: KPI Reporting -->
    <div class="portfolio-card" onclick="openModal('kpi')">
      <div class="portfolio-card-inner">
        <div class="port-visual port-kpi">
          <div style="text-align:center; padding:1rem;">
            <div style="font-family:'DM Mono',monospace; font-size:0.65rem; letter-spacing:0.1em; color:var(--emerald); margin-bottom:1rem; text-transform:uppercase;">KPI Dashboard</div>
            <div style="display:flex; align-items:flex-end; justify-content:center; gap:5px; margin-bottom:0.75rem;">
              <div style="width:14px; height:40px; background:var(--emerald); border-radius:3px; opacity:0.7;"></div>
              <div style="width:14px; height:65px; background:var(--emerald); border-radius:3px; opacity:0.8;"></div>
              <div style="width:14px; height:50px; background:var(--emerald); border-radius:3px; opacity:0.6;"></div>
              <div style="width:14px; height:80px; background:var(--emerald); border-radius:3px; opacity:0.9;"></div>
              <div style="width:14px; height:55px; background:var(--emerald); border-radius:3px; opacity:0.7;"></div>
              <div style="width:14px; height:90px; background:var(--emerald); border-radius:3px;"></div>
              <div style="width:14px; height:70px; background:var(--emerald); border-radius:3px; opacity:0.75;"></div>
            </div>
            <div style="font-family:'Syne',sans-serif; font-size:1.8rem; font-weight:800; color:var(--white);">141%</div>
            <div style="font-size:0.72rem; color:var(--muted);">YTD Utilization</div>
          </div>
        </div>
        <div class="portfolio-overlay">
          <div class="portfolio-cat">KPI Reporting</div>
          <div class="portfolio-title">Objective Performance Progress Report</div>
          <div class="portfolio-cta">↗ View Project Details</div>
        </div>
      </div>
    </div>

    <!-- 2: Utilization Analytics -->
    <div class="portfolio-card" onclick="openModal('util')">
      <div class="portfolio-card-inner">
        <div class="port-visual port-util">
          <div style="text-align:center; padding:1rem; width:100%;">
            <div style="font-family:'DM Mono',monospace; font-size:0.65rem; letter-spacing:0.1em; color:#34d399; margin-bottom:1rem; text-transform:uppercase;">Fleet Analytics</div>
            <div style="display:flex; justify-content:center; gap:1.5rem; margin-bottom:1rem;">
              <div style="text-align:center;">
                <div style="font-family:'Syne',sans-serif; font-size:1.5rem; font-weight:800; color:var(--white);">80%</div>
                <div style="font-size:0.65rem; color:var(--muted);">Target</div>
              </div>
              <div style="text-align:center;">
                <div style="font-family:'Syne',sans-serif; font-size:1.5rem; font-weight:800; color:#34d399;">100%</div>
                <div style="font-size:0.65rem; color:var(--muted);">Actual</div>
              </div>
            </div>
            <div style="background:rgba(255,255,255,0.06); border-radius:6px; padding:0.5rem; width:160px; margin:0 auto;">
              <div style="height:6px; background:rgba(255,255,255,0.1); border-radius:3px; margin-bottom:4px;">
                <div style="height:100%; width:80%; background:#34d399; border-radius:3px;"></div>
              </div>
              <div style="height:6px; background:rgba(255,255,255,0.1); border-radius:3px;">
                <div style="height:100%; width:100%; background:var(--emerald); border-radius:3px;"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="portfolio-overlay">
          <div class="portfolio-cat">Utilization Analytics</div>
          <div class="portfolio-title">Fleet & Equipment Utilization Tracker — Target vs. Actual</div>
          <div class="portfolio-cta">↗ View Project Details</div>
        </div>
      </div>
    </div>

    <!-- 3: Lead Generation -->
    <div class="portfolio-card" onclick="openModal('lead')">
      <div class="portfolio-card-inner">
        <div class="port-visual port-lead">
          <div style="padding:1rem; width:90%;">
            <div style="font-family:'DM Mono',monospace; font-size:0.6rem; letter-spacing:0.1em; color:#818cf8; margin-bottom:0.75rem; text-transform:uppercase;">B2B Contact List</div>
            <div style="border:1px solid rgba(255,255,255,0.1); border-radius:6px; overflow:hidden; font-size:0.6rem;">
              <div style="background:rgba(99,102,241,0.2); padding:0.4rem 0.6rem; display:grid; grid-template-columns:1fr 1fr 1fr; color:var(--muted); font-family:'DM Mono',monospace; letter-spacing:0.06em;">
                <span>NAME</span><span>TITLE</span><span>COMPANY</span>
              </div>
              <div style="background:rgba(255,255,255,0.03); padding:0.35rem 0.6rem; display:grid; grid-template-columns:1fr 1fr 1fr; color:var(--off-white); border-top:1px solid rgba(255,255,255,0.05);">
                <span>Sarah M.</span><span>CEO</span><span>Abbey Acad.</span>
              </div>
              <div style="background:rgba(255,255,255,0.01); padding:0.35rem 0.6rem; display:grid; grid-template-columns:1fr 1fr 1fr; color:var(--off-white); border-top:1px solid rgba(255,255,255,0.05);">
                <span>Fiona H.</span><span>CEO</span><span>Abingdon</span>
              </div>
              <div style="background:rgba(255,255,255,0.03); padding:0.35rem 0.6rem; display:grid; grid-template-columns:1fr 1fr 1fr; color:var(--off-white); border-top:1px solid rgba(255,255,255,0.05);">
                <span>Alan W.</span><span>CEO</span><span>Accord</span>
              </div>
              <div style="background:rgba(255,255,255,0.01); padding:0.35rem 0.6rem; display:grid; grid-template-columns:1fr 1fr 1fr; color:var(--muted); border-top:1px solid rgba(255,255,255,0.05);">
                <span>+200 more...</span><span></span><span></span>
              </div>
            </div>
          </div>
        </div>
        <div class="portfolio-overlay">
          <div class="portfolio-cat">Lead Generation</div>
          <div class="portfolio-title">Verified B2B Contact Lists — CEO & Executive Prospects</div>
          <div class="portfolio-cta">↗ View Project Details</div>
        </div>
      </div>
    </div>

    <!-- 4: Brand Marketing -->
    <div class="portfolio-card" onclick="openModal('brand')">
      <div class="portfolio-card-inner">
        <div class="port-visual port-brand">
          <div style="text-align:center; padding:1rem;">
            <div style="font-size:0.6rem; font-family:'DM Mono',monospace; letter-spacing:0.1em; color:#fb923c; text-transform:uppercase; margin-bottom:0.75rem;">Brand Marketing</div>
            <div style="display:flex; justify-content:center; gap:0.5rem; flex-wrap:wrap;">
              <div style="background:linear-gradient(135deg,#ea580c,#78350f); border-radius:6px; padding:0.4rem 0.6rem; font-family:'Syne',sans-serif; font-size:0.65rem; font-weight:700; color:white; border:1px solid rgba(255,255,255,0.1);">FOOD MENU</div>
              <div style="background:linear-gradient(135deg,#be185d,#831843); border-radius:6px; padding:0.4rem 0.6rem; font-family:'Syne',sans-serif; font-size:0.65rem; font-weight:700; color:white; border:1px solid rgba(255,255,255,0.1);">ICE CREAM</div>
              <div style="background:linear-gradient(135deg,#7c2d12,#292524); border-radius:6px; padding:0.4rem 0.6rem; font-family:'Syne',sans-serif; font-size:0.65rem; font-weight:700; color:white; border:1px solid rgba(255,255,255,0.1);">COFFEE</div>
            </div>
            <div style="margin-top:0.75rem; font-family:'Syne',sans-serif; font-size:2rem; font-weight:800; color:white; opacity:0.9;">🍔 🍦 ☕</div>
          </div>
        </div>
        <div class="portfolio-overlay">
          <div class="portfolio-cat">Brand Marketing</div>
          <div class="portfolio-title">Restaurant Menus, Café Promos & F&B Flyers</div>
          <div class="portfolio-cta">↗ View Project Details</div>
        </div>
      </div>
    </div>

    <!-- 5: Digital Products -->
    <div class="portfolio-card" onclick="openModal('digital')">
      <div class="portfolio-card-inner">
        <div class="port-visual port-digital">
          <div style="text-align:center; padding:1rem;">
            <div style="font-size:0.6rem; font-family:'DM Mono',monospace; letter-spacing:0.1em; color:#d4b483; text-transform:uppercase; margin-bottom:0.75rem;">Digital Retail</div>
            <div style="font-size:3rem;">👟</div>
            <div style="font-family:'Syne',sans-serif; font-size:0.9rem; font-weight:700; color:white; margin-top:0.5rem;">PICK YOUR BEST</div>
            <div style="font-family:'Georgia',serif; font-style:italic; font-size:1.1rem; color:#d4b483; margin-top:0.15rem;">wear</div>
            <div style="font-family:'Syne',sans-serif; font-size:1.3rem; font-weight:800; color:rgba(255,255,255,0.15); letter-spacing:0.1em; margin-top:0.5rem;">SHOES</div>
          </div>
        </div>
        <div class="portfolio-overlay">
          <div class="portfolio-cat">Digital Products</div>
          <div class="portfolio-title">Product Showcase — Footwear & Retail Visual Assets</div>
          <div class="portfolio-cta">↗ View Project Details</div>
        </div>
      </div>
    </div>

    <!-- 6: Operational Docs -->
    <div class="portfolio-card" onclick="openModal('ops')">
      <div class="portfolio-card-inner">
        <div class="port-visual port-ops">
          <div style="text-align:center; padding:1rem; width:90%;">
            <div style="font-size:0.6rem; font-family:'DM Mono',monospace; letter-spacing:0.1em; color:var(--emerald); text-transform:uppercase; margin-bottom:0.75rem;">Business Docs</div>
            <div style="background:rgba(255,255,255,0.04); border:1px solid rgba(255,255,255,0.08); border-radius:8px; padding:1rem; text-align:left;">
              <div style="font-family:'Syne',sans-serif; font-size:0.75rem; font-weight:800; color:white; margin-bottom:0.4rem;">MODERN BUSINESS</div>
              <div style="font-family:'Syne',sans-serif; font-size:0.75rem; font-weight:800; color:white; margin-bottom:0.5rem;">SOLUTIONS</div>
              <div style="font-size:0.65rem; color:var(--muted); line-height:1.5; margin-bottom:0.4rem;">Delivering high-quality creative solutions for business growth...</div>
              <div style="font-family:'DM Mono',monospace; font-size:0.6rem; color:var(--emerald);">About Us · Get in Touch · Strategy</div>
            </div>
          </div>
        </div>
        <div class="portfolio-overlay">
          <div class="portfolio-cat">Operational Documentation</div>
          <div class="portfolio-title">Business Solutions Brochure & SOP Documentation</div>
          <div class="portfolio-cta">↗ View Project Details</div>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- WHY ME -->
<section id="why">
  <div class="section-label fade-up">Why Work With Me</div>
  <h2 class="section-title fade-up">The Edge You're Looking For</h2>

  <div class="why-layout">
    <div class="why-content">
      <p class="section-subtitle">A BS in Information Technology combined with 6+ years of hands-on analytics experience means I bridge the gap between technical precision and practical business outcomes.</p>
      <div class="why-points stagger-children">
        <div class="why-point">
          <div class="why-point-icon">🎓</div>
          <div class="why-point-text">
            <h4>BS Information Technology Graduate</h4>
            <p>Strong technical foundation with practical skills in data management, programming, and systems support from IBAC Mindanao.</p>
          </div>
        </div>
        <div class="why-point">
          <div class="why-point-icon">📊</div>
          <div class="why-point-text">
            <h4>Proven KPI & Analytics Track Record</h4>
            <p>Developed OPP Reports and variance analysis frameworks that improved decision-making at the management level — measurable, documented results.</p>
          </div>
        </div>
        <div class="why-point">
          <div class="why-point-icon">⚡</div>
          <div class="why-point-text">
            <h4>Multi-Domain Expertise</h4>
            <p>From IT support to accounting data entry to fleet analytics and brand design — a rare combination of depth across operations, tech, and creative work.</p>
          </div>
        </div>
        <div class="why-point">
          <div class="why-point-icon">🏆</div>
          <div class="why-point-text">
            <h4>Award-Winning & Certified</h4>
            <p>Best in Capstone Project, Outstanding Intern Award, and certified in Excel, Goal Setting, Social Media Management, and more.</p>
          </div>
        </div>
      </div>
    </div>

    <div class="why-timeline">
      <div class="timeline-item">
        <div class="timeline-date">Feb 2020 – Apr 2026</div>
        <div class="timeline-role">Utilization Analyst</div>
        <div class="timeline-company">M. Montesclaros Enterprises Inc. · Valencia City, Bukidnon</div>
        <ul class="timeline-bullets">
          <li>Collected and analyzed light vehicle data — usage patterns, mileage, downtime</li>
          <li>Developed OPP Reports tracking departmental KPIs with Target vs. Actual variance</li>
          <li>Created management dashboards for fleet status monitoring</li>
        </ul>
      </div>
      <div class="timeline-item">
        <div class="timeline-date">Mar 2018 – Jan 2020</div>
        <div class="timeline-role">I.T. Support Specialist</div>
        <div class="timeline-company">M. Montesclaros Enterprises Inc. · Valencia City, Bukidnon</div>
        <ul class="timeline-bullets">
          <li>Daily technical support, troubleshooting, and system updates across departments</li>
          <li>Managed user access and performed regular data backups</li>
          <li>Maintained accurate equipment databases for reliable reporting</li>
        </ul>
      </div>
      <div class="timeline-item">
        <div class="timeline-date">Oct 2017 – Feb 2018</div>
        <div class="timeline-role">Accounting Data Entry Specialist</div>
        <div class="timeline-company">Centro Supersales Inc. · Valencia City, Bukidnon</div>
        <ul class="timeline-bullets">
          <li>Processed POs, sales invoices, and delivery receipts with high accuracy</li>
          <li>Maintained organized financial records for audits and monthly reporting</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label fade-up">Get in Touch</div>
  <h2 class="section-title fade-up">Let's Build Something Together</h2>
  <p class="section-subtitle fade-up">Have a project in mind? I'd love to hear about it. Fill out the form or reach out directly.</p>

  <div class="contact-layout">
    <div class="contact-info">
      <div class="contact-detail">
        <div class="contact-detail-icon">📧</div>
        <div class="contact-detail-text">
          <p>Email</p>
          <a href="mailto:elaineviason08.va@gmail.com">elaineviason08.va@gmail.com</a>
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-detail-icon">📞</div>
        <div class="contact-detail-text">
          <p>Phone / WhatsApp</p>
          <a href="tel:+639481680177">+63 948 168 0177</a>
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-detail-icon">📍</div>
        <div class="contact-detail-text">
          <p>Location</p>
          <span>Valencia City, Bukidnon, Philippines</span>
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-detail-icon">🌐</div>
        <div class="contact-detail-text">
          <p>Portfolio Site</p>
          <a href="https://elaineviason.my.canva.site/portfolio-data-operations-specialist" target="_blank">View Canva Portfolio ↗</a>
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-detail-icon">💼</div>
        <div class="contact-detail-text">
          <p>LinkedIn</p>
          <a href="#" target="_blank">Connect on LinkedIn ↗</a>
        </div>
      </div>

      <div style="margin-top:2rem; padding:1.5rem; border:1px solid rgba(16,185,129,0.2); border-radius:12px; background:rgba(16,185,129,0.04);">
        <div style="font-family:'DM Mono',monospace; font-size:0.68rem; letter-spacing:0.1em; color:var(--emerald); text-transform:uppercase; margin-bottom:0.75rem;">Services I offer</div>
        <div style="display:flex; flex-direction:column; gap:0.4rem;">
          <div style="font-size:0.85rem; color:var(--muted);">✦ KPI Dashboards & Data Reports</div>
          <div style="font-size:0.85rem; color:var(--muted);">✦ B2B Lead Generation Lists</div>
          <div style="font-size:0.85rem; color:var(--muted);">✦ Virtual Assistant Support</div>
          <div style="font-size:0.85rem; color:var(--muted);">✦ Graphic Design (Canva)</div>
          <div style="font-size:0.85rem; color:var(--muted);">✦ Social Media Management</div>
        </div>
      </div>
    </div>

    <div class="contact-form">
      <h3>Send a Project Inquiry</h3>
      <div class="form-row">
        <div class="form-group">
          <label>Your Name</label>
          <input type="text" placeholder="Jane Smith" id="fname">
        </div>
        <div class="form-group">
          <label>Your Email</label>
          <input type="email" placeholder="jane@company.com" id="femail">
        </div>
      </div>
      <div class="form-group">
        <label>Service Needed</label>
        <select id="fservice">
          <option value="">Select a service...</option>
          <option>Data Operations & KPI Reporting</option>
          <option>Lead Generation & CRM</option>
          <option>Virtual Assistant Support</option>
          <option>Graphic Design & Brand Assets</option>
          <option>Social Media Management</option>
          <option>Other / Multiple Services</option>
        </select>
      </div>
      <div class="form-group">
        <label>Budget Range</label>
        <select id="fbudget">
          <option value="">Select budget range...</option>
          <option>Under $200</option>
          <option>$200 – $500</option>
          <option>$500 – $1,000</option>
          <option>$1,000+</option>
          <option>Open to discussion</option>
        </select>
      </div>
      <div class="form-group">
        <label>Project Details</label>
        <textarea placeholder="Tell me about your project, timeline, and goals..." id="fmsg"></textarea>
      </div>
      <button class="form-submit" onclick="handleSubmit()">✦ Send Inquiry</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-left">© 2025 Ma. Elaine Gay Viason · Data Ops Specialist & VA · Valencia City, PH</div>
  <ul class="footer-links">
    <li><a href="#hero">Top</a></li>
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="https://elaineviason.my.canva.site/portfolio-data-operations-specialist" target="_blank">Canva Site ↗</a></li>
  </ul>
</footer>

<!-- TOAST -->
<div class="toast" id="toast">✓ Message sent! I'll be in touch soon.</div>

<!-- MODAL -->
<div class="modal-overlay" id="modal">
  <div class="modal-box">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-cat" id="modal-cat"></div>
    <div class="modal-title" id="modal-title"></div>
    <div class="modal-body" id="modal-body"></div>
    <div class="modal-skills" id="modal-skills"></div>
  </div>
</div>

<script>
// Modal data
const projects = {
  kpi: {
    cat: 'KPI Reporting',
    title: 'Objective Performance Progress Report',
    body: 'Designed and maintained the OPP Report system for M. Montesclaros Enterprises tracking dump truck utilization against monthly and annual KPI targets. Built in Excel with advanced formulas, conditional formatting, variance analysis, and dynamic charts comparing Actual vs. Previous Year vs. Target. Covered Jan–Dec 2025 across South, North, and Central clusters.',
    skills: ['Microsoft Excel', 'KPI Frameworks', 'Target vs. Actual', 'Data Visualization', 'Cluster Analytics', 'YTD Reporting']
  },
  util: {
    cat: 'Utilization Analytics',
    title: 'Fleet & Equipment Utilization Tracker',
    body: 'Comprehensive fleet tracking spreadsheet covering 200+ equipment units (MM series). Columns include mileage, hours run, breakdowns, working conditions, and % utilization. Includes weekly summary dashboards, pie charts for downtime categories, and bar charts for YTD utilization performance per machine. Enables management to identify underperforming units and operational bottlenecks.',
    skills: ['Fleet Management', 'Excel Dashboards', 'Equipment Analytics', 'Variance Analysis', 'Downtime Tracking', 'Operations Reporting']
  },
  lead: {
    cat: 'Lead Generation',
    title: 'Verified B2B Contact Lists — CEO & Executive Prospects',
    body: 'Curated and verified B2B contact spreadsheet with 200+ executive leads including First Name, Last Name, Full Name, Title, Phone Number, Company, Email, Address, City, State, Zip, Country, and Source URL. All contacts researched and validated with direct links to company websites and executive profiles. Ideal for targeted outreach campaigns.',
    skills: ['B2B Prospecting', 'Data Verification', 'Lead Qualification', 'Google Sheets', 'CRM Data Entry', 'LinkedIn Research']
  },
  brand: {
    cat: 'Brand Marketing',
    title: 'Restaurant Menus, Café Promos & F&B Flyers',
    body: 'Professional marketing collateral created in Canva for the food and beverage sector. Includes a vibrant orange restaurant food menu with diagonal diamond photo layouts, a bold pink strawberry ice cream promotional flyer with 50% off badges, and a premium brewed coffee poster with a split cream-and-brown color scheme. Each piece balances visual appeal with clear call-to-action messaging.',
    skills: ['Canva Design', 'Menu Design', 'Promotional Flyers', 'F&B Marketing', 'Color Theory', 'Typography']
  },
  digital: {
    cat: 'Digital Products',
    title: 'Footwear & Retail Visual Product Showcase',
    body: 'Minimalist product showcase design for a footwear brand featuring a clean split diagonal layout — white and warm gold — with bold editorial typography. Features Kayanas brand loafers in a lifestyle-oriented flat-lay composition. Designed for use on e-commerce platforms, Instagram, and product landing pages to drive purchase intent.',
    skills: ['Product Photography Layout', 'Canva', 'E-commerce Visuals', 'Retail Design', 'Typography Pairing', 'Brand Aesthetics']
  },
  ops: {
    cat: 'Operational Documentation',
    title: 'Business Solutions Brochure & SOP Documentation',
    body: 'Two-panel business brochure created for "Modern Business Solutions" featuring a bold red-black-white corporate aesthetic. Left panel contains brand identity with logo and mission statement. Right panel features cityscape photography, strategic headline, About Us copy, and Get in Touch section with contact details. Demonstrates SOP-level documentation and brand communication standards.',
    skills: ['Canva Design', 'Corporate Branding', 'Brochure Layout', 'Copywriting', 'SOP Documentation', 'Business Communication']
  }
};

function openModal(key) {
  const p = projects[key];
  document.getElementById('modal-cat').textContent = p.cat;
  document.getElementById('modal-title').textContent = p.title;
  document.getElementById('modal-body').textContent = p.body;
  const skillsEl = document.getElementById('modal-skills');
  skillsEl.innerHTML = p.skills.map(s => `<span class="modal-skill-tag">${s}</span>`).join('');
  document.getElementById('modal').classList.add('open');
  document.body.style.overflow = 'hidden';
}

function closeModal() {
  document.getElementById('modal').classList.remove('open');
  document.body.style.overflow = '';
}

document.getElementById('modal').addEventListener('click', function(e) {
  if (e.target === this) closeModal();
});

document.addEventListener('keydown', e => { if (e.key === 'Escape') closeModal(); });

function handleSubmit() {
  const name = document.getElementById('fname').value.trim();
  const email = document.getElementById('femail').value.trim();
  const msg = document.getElementById('fmsg').value.trim();
  if (!name || !email) {
    alert('Please fill in your name and email.');
    return;
  }
  const toast = document.getElementById('toast');
  toast.classList.add('show');
  setTimeout(() => toast.classList.remove('show'), 4000);
  ['fname','femail','fservice','fbudget','fmsg'].forEach(id => {
    const el = document.getElementById(id);
    el.value = '';
  });
}

// Scroll animations
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
    }
  });
}, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });

document.querySelectorAll('.fade-up, .stagger-children').forEach(el => observer.observe(el));
</script>
</body>
</html>
