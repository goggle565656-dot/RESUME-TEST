<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mohit.M — Content Creator & Digital Strategist</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;900&family=Open+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --white: #ffffff;
    --bg: #f8f7ff;
    --purple: #7c3aed;
    --purple-light: #a78bfa;
    --pink: #ec4899;
    --blue: #3b82f6;
    --blue-light: #93c5fd;
    --dark: #1a1a2e;
    --grey: #4b5563;
    --grey-light: #9ca3af;
    --card-bg: rgba(255,255,255,0.85);
    --gradient: linear-gradient(135deg, #7c3aed, #3b82f6, #ec4899);
    --gradient-soft: linear-gradient(135deg, #ede9fe, #dbeafe, #fce7f3);
    --shadow: 0 8px 32px rgba(124,58,237,0.12);
    --shadow-hover: 0 16px 48px rgba(124,58,237,0.22);
    --radius: 20px;
    --radius-sm: 12px;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Open Sans', sans-serif;
    background: var(--bg);
    color: var(--dark);
    overflow-x: hidden;
    line-height: 1.7;
  }

  /* ─── NOISE TEXTURE OVERLAY ─── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.025'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 0;
    opacity: 0.4;
  }

  /* ─── NAVBAR ─── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 1.2rem 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    backdrop-filter: blur(16px);
    background: rgba(248,247,255,0.85);
    border-bottom: 1px solid rgba(124,58,237,0.08);
    transition: box-shadow 0.3s;
  }
  nav.scrolled { box-shadow: 0 4px 24px rgba(124,58,237,0.1); }

  .nav-logo {
    font-family: 'Montserrat', sans-serif;
    font-weight: 900;
    font-size: 1.4rem;
    background: var(--gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    letter-spacing: -0.5px;
  }

  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    font-family: 'Montserrat', sans-serif;
    font-weight: 600;
    font-size: 0.85rem;
    color: var(--grey);
    text-decoration: none;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    transition: color 0.2s;
    position: relative;
  }
  .nav-links a::after {
    content: '';
    position: absolute;
    bottom: -4px; left: 0; right: 0;
    height: 2px;
    background: var(--gradient);
    border-radius: 2px;
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s;
  }
  .nav-links a:hover { color: var(--purple); }
  .nav-links a:hover::after { transform: scaleX(1); }

  .nav-cta {
    padding: 0.55rem 1.4rem;
    background: var(--gradient);
    color: white !important;
    border-radius: 50px;
    font-size: 0.82rem !important;
    font-weight: 700 !important;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    transition: opacity 0.2s, transform 0.2s, box-shadow 0.2s !important;
    box-shadow: 0 4px 16px rgba(124,58,237,0.3);
    -webkit-text-fill-color: white !important;
  }
  .nav-cta:hover { opacity: 0.9; transform: translateY(-1px); box-shadow: 0 8px 24px rgba(124,58,237,0.4) !important; }
  .nav-cta::after { display: none !important; }

  /* ─── HERO ─── */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 8rem 5% 5rem;
    position: relative;
    overflow: hidden;
  }

  .hero-blob {
    position: absolute;
    border-radius: 50%;
    filter: blur(80px);
    opacity: 0.25;
    pointer-events: none;
  }
  .blob1 { width: 500px; height: 500px; backgrou
