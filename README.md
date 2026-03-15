<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description" content="Maa Nirmala DJ & Tent House - Elite Digital Portfolio">
    
    <meta name="theme-color" content="#D4AF37">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="application-name" content="MNDs Hub">
    
    <link rel="manifest" href='data:application/manifest+json,{"name":"MNDs Secure Hub","short_name":"MNDs App","start_url":".","display":"standalone","background_color":"#050505","theme_color":"#D4AF37","orientation":"portrait","icons":[{"src":"https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg","sizes":"192x192","type":"image/jpeg"},{"src":"https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg","sizes":"512x512","type":"image/jpeg"}]}'>

    <title>Maa Nirmala DJ & Tent House | SECURE HUB</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Outfit:wght@200;400;600&family=Rajdhani:wght@500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>
        :root {
            /* --- ELITE DARK THEME --- */
            --bg-body: #050505;
            --bg-card: rgba(20, 20, 20, 0.9);
            --border-color: rgba(212, 175, 55, 0.3);
            --gold-primary: #D4AF37;
            --gold-shine: #FFD700;
            --text-main: #ffffff;
            --text-sub: #b3b3b3;
            --glass-blur: blur(25px);
            --nav-glass: blur(30px);
        }

        [data-theme="light"] {
            --bg-body: #f2f2f2;
            --bg-card: rgba(255, 255, 255, 0.95);
            --border-color: rgba(180, 140, 40, 0.3);
            --gold-primary: #b08d26;
            --gold-shine: #d4a017;
            --text-main: #111111;
            --text-sub: #555555;
        }

        ::-webkit-scrollbar { width: 4px; }
        ::-webkit-scrollbar-track { background: #000; }
        ::-webkit-scrollbar-thumb { background: var(--gold-primary); border-radius: 10px; }
        
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; outline: none; }
        body { background-color: var(--bg-body); color: var(--text-main); font-family: 'Outfit', sans-serif; overflow-x: hidden; min-height: 100vh; transition: background-color 0.4s ease, color 0.4s ease; user-select: none; }

        /* GATEKEEPER */
        #gatekeeper { position: fixed; inset: 0; z-index: 9999; background: var(--bg-body); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 20px; text-align: center; background-image: radial-gradient(circle at 50% 50%, rgba(212, 175, 55, 0.1) 0%, transparent 80%); transition: opacity 0.8s ease, visibility 0.8s; }
        .gate-card { width: 100%; max-width: 400px; background: rgba(10, 10, 10, 0.95); border: 1px solid var(--gold-primary); border-radius: 20px; padding: 40px 25px; box-shadow: 0 0 80px rgba(212, 175, 55, 0.15); backdrop-filter: blur(20px); position: relative; overflow: hidden; animation: pulseCard 4s infinite alternate; }
        @keyframes pulseCard { from { transform: scale(1); border-color: rgba(212,175,55,0.3); } to { transform: scale(1.005); border-color: rgba(212,175,55,0.6); } }
        .gate-img-frame { width: 110px; height: 110px; margin: 0 auto 20px; border-radius: 50%; padding: 3px; border: 2px solid var(--gold-primary); box-shadow: 0 0 30px rgba(212, 175, 55, 0.3); }
        .gate-img { width: 100%; height: 100%; border-radius: 50%; object-fit: cover; }
        .gate-title { font-family: 'Cinzel'; color: var(--gold-primary); font-size: 26px; margin-bottom: 5px; text-shadow: 0 0 15px rgba(212, 175, 55, 0.5); font-weight: 700; }
        .gate-sub { color: #666; font-size: 11px; letter-spacing: 4px; margin-bottom: 30px; font-family: 'Rajdhani'; text-transform: uppercase; }
        .gate-input-group { position: relative; margin-bottom: 15px; text-align: left; }
        .gate-input { width: 100%; padding: 15px 15px 15px 45px; background: rgba(255, 255, 255, 0.05); border: 1px solid #333; color: #fff; font-size: 16px; font-family: 'Rajdhani'; transition: 0.3s; border-radius: 10px; }
        .gate-input:focus { border-color: var(--gold-primary); background: rgba(212, 175, 55, 0.08); box-shadow: 0 0 15px rgba(212,175,55,0.1); }
        .gate-icon { position: absolute; left: 15px; top: 17px; color: #555; transition: 0.3s; }
        .gate-input:focus + .gate-icon { color: var(--gold-primary); }
        .gate-btn { width: 100%; padding: 16px; background: linear-gradient(135deg, var(--gold-primary), #997d2d); color: #000; font-weight: 800; font-size: 16px; border: none; cursor: pointer; border-radius: 10px; text-transform: uppercase; letter-spacing: 2px; margin-top: 15px; box-shadow: 0 5px 25px rgba(212, 175, 55, 0.3); transition: 0.3s; }
        .gate-btn:active { transform: scale(0.98); }
        .loading-text { margin-top: 20px; font-size: 12px; color: var(--gold-primary); font-family: 'Rajdhani'; display: none; letter-spacing: 1px; font-weight: bold; }

        /* MAIN UI */
        #main-interface { display: none; opacity: 0; transition: opacity 1.5s ease; padding-bottom: 90px; }
        .bg-fx { position: fixed; inset: 0; z-index: -2; pointer-events: none; overflow: hidden; }
        .orb { position: absolute; border-radius: 50%; filter: blur(120px); opacity: 0.15; animation: float 15s infinite alternate; }
        .orb-1 { width: 350px; height: 350px; background: var(--gold-primary); top: -10%; left: -10%; }
        .orb-2 { width: 300px; height: 300px; background: #00e5ff; bottom: -10%; right: -10%; }
        @keyframes float { 0% { transform: translate(0,0); } 100% { transform: translate(50px, 50px); } }

        /* Navbar & Hamburger */
        .navbar { display: flex; justify-content: space-between; align-items: center; padding: 15px 5%; position: sticky; top: 0; z-index: 1000; background: rgba(5, 5, 5, 0.85); backdrop-filter: var(--glass-blur); border-bottom: 1px solid var(--border-color); }
        .brand { font-family: 'Cinzel'; color: var(--gold-primary); font-weight: 700; font-size: 18px; display: flex; align-items: center; gap: 12px; }
        .controls { display: flex; align-items: center; gap: 15px; }
        .nav-btn { font-size: 20px; cursor: pointer; color: var(--text-main); background: none; border: none; }

        .menu-overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.7); z-index: 5999; display: none; opacity: 0; transition: 0.3s; }
        .menu-overlay.active { display: block; opacity: 1; }
        .side-menu { position: fixed; top: 0; left: -280px; width: 260px; height: 100%; background: rgba(10,10,10,0.98); border-right: 1px solid var(--gold-primary); z-index: 6000; transition: left 0.4s ease; padding-top: 20px; display: flex; flex-direction: column; box-shadow: 5px 0 30px rgba(0,0,0,0.5); overflow-y: auto;}
        .side-menu.open { left: 0; }
        .menu-close { align-self: flex-end; margin: 0 20px 20px 0; font-size: 24px; color: var(--gold-primary); cursor: pointer; }
        .side-link { display: flex; align-items: center; padding: 18px 25px; color: #fff; text-decoration: none; border-bottom: 1px solid #222; font-family: 'Outfit'; font-size: 15px; font-weight: 600; text-transform: uppercase; letter-spacing: 1px; transition: 0.3s; }
        .side-link i { color: var(--gold-primary); margin-right: 15px; font-size: 18px; width: 20px; text-align: center; }
        .side-link:hover { background: rgba(212,175,55,0.1); padding-left: 30px; }
        .menu-logo { text-align: center; padding-bottom: 20px; border-bottom: 1px solid var(--border-color); margin-bottom: 10px; }
        .menu-logo img { width: 80px; height: 80px; border-radius: 50%; border: 2px solid var(--gold-primary); }

        #google_translate_element { margin-right: 5px; }
        .goog-te-gadget-simple { background-color: rgba(255,255,255,0.05) !important; border: 1px solid var(--gold-primary) !important; padding: 4px 8px !important; border-radius: 20px !important; }
        .goog-te-gadget-simple span { color: var(--gold-primary) !important; font-weight: 700 !important; font-size: 11px !important; }
        .goog-te-gadget-icon, .goog-te-banner-frame { display: none !important; } body { top: 0px !important; }

        /* Profile Section */
        .container { width: 100%; max-width: 800px; margin: 0 auto; padding: 0 20px; }
        .profile-wrapper { text-align: center; padding: 60px 0 30px; }
        .img-container { width: 160px; height: 160px; margin: 0 auto 20px; position: relative; border-radius: 50%; padding: 5px; background: linear-gradient(135deg, var(--gold-primary), transparent, var(--gold-shine)); }
        .profile-pic { width: 100%; height: 100%; border-radius: 50%; object-fit: cover; border: 4px solid var(--bg-body); background: #000; }
        h1 { font-family: 'Rajdhani', sans-serif; font-size: 32px; font-weight: 700; background: linear-gradient(to right, var(--text-main), var(--gold-primary), var(--text-main)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; margin-bottom: 5px; }
        .verified { color: #1DA1F2; font-size: 20px; vertical-align: middle; margin-left: 5px; }
        .bio { color: var(--gold-primary); font-size: 13px; letter-spacing: 2px; font-weight: 600; text-transform: uppercase; }

        #installBtn { display: none; margin: 20px auto; background: rgba(212, 175, 55, 0.1); border: 1px solid var(--gold-primary); color: var(--gold-primary); padding: 12px 30px; border-radius: 30px; font-size: 12px; font-weight: bold; cursor: pointer; box-shadow: 0 0 20px rgba(212, 175, 55, 0.15); animation: bounce 2s infinite; letter-spacing: 1px; }
        @keyframes bounce { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-5px); } }

        /* Grids & Sections */
        .section-label { display: flex; align-items: center; gap: 10px; margin: 35px 0 15px; color: var(--gold-primary); font-family: 'Cinzel'; font-weight: bold; font-size: 14px; border-bottom: 1px solid var(--border-color); padding-bottom: 8px; text-transform: uppercase; scroll-margin-top: 80px; }
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
        @media (min-width: 600px) { .grid { gap: 20px; } }
        
        .card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; padding: 20px; height: 100px; display: flex; flex-direction: column; align-items: center; justify-content: center; text-decoration: none; color: var(--text-main); position: relative; overflow: hidden; backdrop-filter: var(--glass-blur); box-shadow: 0 4px 15px rgba(0,0,0,0.1); transition: all 0.3s; }
        .card:active { transform: scale(0.96); border-color: var(--gold-shine); }
        .card i { font-size: 28px; margin-bottom: 8px; color: var(--gold-primary); transition: 0.3s; }
        .card span { font-size: 11px; font-weight: 600; text-transform: uppercase; text-align: center; }
        .full-w { grid-column: span 2; flex-direction: row; gap: 15px; height: 75px; background: linear-gradient(90deg, rgba(212,175,55,0.05), transparent); }
        .full-w i { margin-bottom: 0; font-size: 24px; }

        .img-card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; padding: 10px; aspect-ratio: 1 / 1; display: flex; flex-direction: column; align-items: center; justify-content: space-between; text-decoration: none; color: var(--text-main); position: relative; overflow: hidden; backdrop-filter: var(--glass-blur); box-shadow: 0 4px 15px rgba(0,0,0,0.3); transition: all 0.3s; }
        .img-card:active { transform: scale(0.96); border-color: var(--gold-shine); }
        .img-card img { width: 100%; height: 75%; object-fit: cover; border-radius: 10px; border: 1px solid rgba(212,175,55,0.3); }
        .img-card span { font-size: 12px; font-weight: 700; text-transform: uppercase; text-align: center; color: var(--gold-primary); margin-top: 5px; font-family: 'Rajdhani'; letter-spacing: 1px; }

        /* LIVE FEED GALLERY CARDS (LARGE) */
        .feed-container { display: flex; flex-direction: column; gap: 20px; }
        .feed-card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 20px; padding: 20px; box-shadow: 0 8px 25px rgba(0,0,0,0.4); text-align: left; }
        .feed-badge { display: inline-block; background: var(--gold-primary); color: #000; padding: 4px 10px; border-radius: 20px; font-size: 11px; font-weight: bold; margin-bottom: 12px; text-transform: uppercase; letter-spacing: 1px; }
        .feed-media { width: 100%; border-radius: 12px; border: 2px solid rgba(212,175,55,0.2); margin-bottom: 15px; background: #000; object-fit: contain; }
        .feed-img { max-height: 400px; }
        .feed-video { height: 250px; }
        .feed-audio { width: 100%; margin-bottom: 15px; outline: none; border-radius: 30px; }
        .feed-text { font-size: 15px; color: #fff; line-height: 1.6; font-family: 'Outfit'; }
        .feed-offer { font-size: 18px; color: var(--gold-shine); font-weight: bold; font-family: 'Cinzel'; text-align: center; padding: 20px; border: 1px dashed var(--gold-primary); border-radius: 12px; background: rgba(212,175,55,0.05); }

        /* Sliders */
        .slider-container { display: flex; overflow-x: auto; gap: 15px; padding-bottom: 15px; scroll-snap-type: x mandatory; scrollbar-width: none; }
        .slider-container::-webkit-scrollbar { display: none; }
        .slide-card { flex: 0 0 85%; scroll-snap-align: center; background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; overflow: hidden; position: relative; box-shadow: 0 5px 20px rgba(0,0,0,0.2); }
        .slide-card img { width: 100%; height: 220px; object-fit: cover; display: block; border-bottom: 2px solid var(--gold-primary); }
        .slide-info { padding: 15px; text-align: center; background: linear-gradient(0deg, #000, transparent); }
        .slide-info h3 { color: var(--gold-primary); font-family: 'Rajdhani'; font-size: 18px; text-transform: uppercase; letter-spacing: 1px; }

        /* Team Cards */
        .team-card { flex: 0 0 85%; scroll-snap-align: center; text-align:center; background:var(--bg-card); border-radius:26px; border: 1px solid var(--border-color); padding: 30px 15px; box-shadow: 0 5px 20px rgba(0,0,0,0.2); }
        .team-card img { width: 130px; height: 130px; object-fit:cover; border-radius:50%; border:3px solid var(--gold-primary); margin-bottom:15px; }
        .team-card h1 { font-size:24px; font-weight:800; margin:5px 0; background:linear-gradient(90deg,#FFD700,#D4AF37,#FFD700); -webkit-background-clip:text; -webkit-text-fill-color:transparent; font-family: 'Rajdhani'; }
        .team-card h3 { font-size:14px; color: var(--gold-primary); margin-bottom: 15px; text-transform: uppercase; letter-spacing: 1px; }
        .team-card p { font-size:13px; line-height:1.6; color:#eaeaea; margin-bottom:10px; }

        /* Map Container */
        .map-container { background: var(--bg-card); padding: 15px; border-radius: 20px; border: 1px solid var(--border-color); box-shadow: 0 5px 20px rgba(0,0,0,0.2); }
        .map-wrapper { width: 100%; aspect-ratio: 1 / 1; border-radius: 12px; overflow: hidden; border: 2px solid var(--gold-primary); }

        /* Owner Profile */
        .owner-profile { background:var(--bg-card); border-radius:26px; border: 1px solid var(--border-color); padding: 30px 20px; box-shadow: 0 5px 20px rgba(0,0,0,0.2); margin-bottom: 30px; }

        /* Bottom Nav */
        .bottom-nav { position: fixed; bottom: 0; left: 0; width: 100%; height: 75px; background: rgba(5, 5, 5, 0.95); backdrop-filter: var(--nav-glass); border-top: 1px solid var(--border-color); z-index: 4000; display: flex; justify-content: space-around; align-items: center; }
        .nav-item { flex: 1; display: flex; flex-direction: column; align-items: center; justify-content: center; color: var(--text-sub); gap: 4px; cursor: pointer; transition: 0.3s; }
        .nav-item.active { color: var(--gold-primary); }
        .nav-item.active i { transform: translateY(-3px); text-shadow: 0 0 15px var(--gold-primary); }

        .ai-trigger { position: fixed; bottom: 90px; right: 25px; width: 60px; height: 60px; border-radius: 50%; background: linear-gradient(135deg, var(--gold-primary), #997d2d); display: flex; align-items: center; justify-content: center; box-shadow: 0 0 30px rgba(212,175,55,0.4); z-index: 2000; cursor: pointer; animation: pulse 3s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.05); } 100% { transform: scale(1); } }

        /* Modals & Forms */
        .modal-wrap { position: fixed; inset: 0; background: rgba(0,0,0,0.85); z-index: 5000; display: none; align-items: center; justify-content: center; backdrop-filter: blur(8px); opacity: 0; transition: opacity 0.3s; }
        .modal-wrap.active { opacity: 1; display: flex; }
        .modal-inner { width: 92%; max-width: 450px; background: #080808; border: 1px solid var(--gold-primary); border-radius: 20px; overflow: hidden; display: flex; flex-direction: column; box-shadow: 0 0 60px rgba(212,175,55,0.15); max-height: 85vh; }
        
        .book-area { padding: 20px; overflow-y: auto; text-align: left; }
        .f-group { margin-bottom: 12px; }
        .f-label { display: block; color: var(--gold-primary); font-size: 11px; margin-bottom: 5px; text-transform: uppercase; font-weight: bold; font-family: 'Rajdhani'; letter-spacing: 1px; }
        .f-input { width: 100%; padding: 12px; background: rgba(255,255,255,0.05); border: 1px solid #333; color: #fff; border-radius: 8px; font-family: 'Outfit'; font-size: 14px; }
        .f-input:focus { border-color: var(--gold-primary); outline: none; background: rgba(212,175,55,0.05); }
        .f-btn { width: 100%; padding: 15px; background: var(--gold-primary); color: #000; font-weight: 800; border: none; border-radius: 8px; cursor: pointer; text-transform: uppercase; margin-top: 10px; font-size: 16px; transition: 0.3s; }
        .f-btn:active { transform: scale(0.98); }

        .loc-group { border: 1px dashed var(--gold-primary); padding: 15px; border-radius: 12px; margin-bottom: 15px; background: rgba(212,175,55,0.02); }
        .loc-title { color: var(--gold-primary); font-family: 'Cinzel'; font-size: 12px; font-weight: bold; margin-bottom: 15px; display: block; letter-spacing: 1px; text-align: center; }

        .star-rating { display: flex; flex-direction: row-reverse; justify-content: center; gap: 8px; margin: 15px 0 25px; }
        .star-rating input { display: none; }
        .star-rating label { font-size: 35px; color: #333; cursor: pointer; transition: 0.2s; text-shadow: 0 0 10px rgba(0,0,0,0.5); }
        .star-rating input:checked ~ label, .star-rating label:hover, .star-rating label:hover ~ label { color: var(--gold-shine); text-shadow: 0 0 15px var(--gold-primary); }

        .chat-box { height: 350px; padding: 20px; overflow-y: auto; background: #0a0a0a; display: flex; flex-direction: column; gap: 10px; }
        .bubble { padding: 10px 15px; border-radius: 12px; max-width: 80%; font-size: 13px; line-height: 1.4; }
        .bubble.bot { background: rgba(212,175,55,0.15); border: 1px solid rgba(212,175,55,0.3); color: #fff; align-self: flex-start; border-bottom-left-radius: 2px;}
        .bubble.user { background: #333; color: #fff; align-self: flex-end; border-bottom-right-radius: 2px; }
        .toast { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); background: var(--gold-primary); color: #000; padding: 10px 20px; border-radius: 30px; font-weight: bold; font-size: 12px; opacity: 0; pointer-events: none; transition: 0.3s; z-index: 6000; }
        .toast.show { opacity: 1; top: 40px; }
        
        /* Pricing Cards */
        .price-card { background: rgba(255,255,255,0.05); border: 1px solid var(--border-color); border-radius: 12px; padding: 15px; margin-bottom: 15px; display: flex; justify-content: space-between; align-items: center; }
        .price-title { font-family: 'Cinzel'; font-weight: bold; font-size: 16px; color: #fff; }
        .price-amt { color: var(--gold-primary); font-size: 20px; font-weight: bold; font-family: 'Rajdhani'; }
    </style>
</head>
<body data-theme="dark">

    <div id="gatekeeper">
        <div class="gate-card">
            <div class="gate-img-frame"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" class="gate-img" alt="Profile"></div>
            <h2 class="gate-title">MAA NIRMALA DJ</h2>
            <div class="gate-sub">SECURE PORTFOLIO GATEWAY</div>
            <div class="gate-input-group"><input type="text" id="g-name" class="gate-input" placeholder="YOUR FULL NAME"><i class="fas fa-user gate-icon"></i></div>
            <div class="gate-input-group"><input type="tel" id="g-phone" class="gate-input" placeholder="YOUR MOBILE NUMBER"><i class="fas fa-phone gate-icon"></i></div>
            <button class="gate-btn" id="btn-verify" onclick="initiateSecureEntry()"><i class="fas fa-fingerprint"></i> VERIFY & ENTER</button>
            <div class="loading-text" id="g-status"><i class="fas fa-circle-notch fa-spin"></i> OPENING WAIT FEW SEC...</div>
        </div>
    </div>

    <div class="menu-overlay" id="menuOverlay" onclick="toggleMenu()"></div>
    <div class="side-menu" id="sideMenu">
        <i class="fas fa-times menu-close" onclick="toggleMenu()"></i>
        <div class="menu-logo">
            <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Logo">
            <div style="color:var(--gold-primary); font-family:'Cinzel'; font-weight:bold; margin-top:5px;">MNDs Hub</div>
        </div>
        <a href="#" class="side-link" onclick="toggleMenu(); navAction('home')"><i class="fas fa-home"></i> Home</a>
      <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openGalleryModal()">
    <i class="fas fa-camera-retro"></i> Live Gallery
</a>

<div id="galleryModalOverlay" class="mn-gallery-modal-overlay">
    <div class="mn-gallery-modal-content">
        <span class="mn-gallery-close-btn" onclick="closeGalleryModal()">&times;</span>
        <h2 class="mn-gallery-title">Live Gallery</h2>
        
        <div class="mn-gallery-scroll-box">
            <img src="https://i.postimg.cc/R0smYWFp/2025-10-07-(5).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/Pf8H6rkd/2025-10-10-(1).png" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/Mp9mfwHd/2025-10-09.jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/5N3wDJB1/2025-10-10.png" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/g0RrFyC3/2025-10-07.jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/3JHsnX1r/2025-10-07-(6).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/3xxbcnv3/2025-10-07-(10).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/Vv7kBKCH/2025-10-07-(1).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/W38NT5X0/2025-10-07-(2).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/N0VVTmFm/2025-10-07-(8).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/pXpWMY8f/2025-10-07.png" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/9XySR4hN/2025-10-07-(9).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/kMhCs6ZG/2025-10-07-(3).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/Pr8gM6Yz/2025-10-07-(4).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/FFfr2V0k/2025-10-07-(1).png" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
            <img src="https://i.postimg.cc/k5k1DChn/2025-10-07-(2).png" alt="Maa Nirmala Setup" class="mn-full-size-img" loading="lazy">
        </div>
    </div>
</div>

<style>
    /* Dark Blurred Background Overlay */
    .mn-gallery-modal-overlay {
        display: none; 
        position: fixed;
        top: 0; left: 0; width: 100%; height: 100%;
        background: rgba(3, 3, 5, 0.95); 
        backdrop-filter: blur(12px);
        z-index: 999999; 
        justify-content: center;
        align-items: center;
    }

    /* The Main Gallery Window */
    .mn-gallery-modal-content {
        background: #0a0a0c; 
        border: 2px solid #D4AF37; /* Royal Gold Border */
        border-radius: 16px;
        width: 95%;
        max-width: 700px;
        height: 85vh; /* Takes up 85% of the screen height */
        padding: 20px 10px 20px 20px;
        display: flex;
        flex-direction: column;
        position: relative;
        box-shadow: 0 20px 60px rgba(0,0,0,0.9), inset 0 0 30px rgba(212, 175, 55, 0.1);
        animation: galleryPopIn 0.4s cubic-bezier(0.25, 0.8, 0.25, 1) forwards;
    }

    @keyframes galleryPopIn {
        from { opacity: 0; transform: scale(0.95) translateY(20px); }
        to { opacity: 1; transform: scale(1) translateY(0); }
    }

    /* Title & Close Button */
    .mn-gallery-title {
        font-family: 'Cinzel', serif;
        color: #D4AF37;
        text-align: center;
        margin: 0 0 15px 0;
        font-size: 24px;
        font-weight: 800;
        letter-spacing: 2px;
        text-transform: uppercase;
        border-bottom: 1px solid rgba(212, 175, 55, 0.3);
        padding-bottom: 15px;
    }

    .mn-gallery-close-btn {
        position: absolute;
        top: 15px;
        right: 20px;
        color: #D4AF37;
        font-size: 35px;
        line-height: 1;
        cursor: pointer;
        z-index: 10;
        transition: color 0.3s ease;
    }
    .mn-gallery-close-btn:hover { color: #ffffff; }

    /* Scrollable Image Area */
    .mn-gallery-scroll-box {
        overflow-y: auto;
        flex-grow: 1;
        padding-right: 15px;
        display: flex;
        flex-direction: column;
        gap: 25px; /* Perfect spacing between images */
    }

    /* Custom Premium Gold Scrollbar */
    .mn-gallery-scroll-box::-webkit-scrollbar {
        width: 6px;
    }
    .mn-gallery-scroll-box::-webkit-scrollbar-track {
        background: rgba(255, 255, 255, 0.05);
        border-radius: 10px;
    }
    .mn-gallery-scroll-box::-webkit-scrollbar-thumb {
        background: #D4AF37;
        border-radius: 10px;
    }

    /* Full Size Images */
    .mn-full-size-img {
        width: 100%;
        height: auto;
        border-radius: 12px;
        border: 1px solid rgba(212, 175, 55, 0.4);
        box-shadow: 0 10px 30px rgba(0,0,0,0.8);
        object-fit: cover;
    }
</style>

<script>
    function openGalleryModal() {
        document.getElementById('galleryModalOverlay').style.display = 'flex';
    }

    function closeGalleryModal() {
        document.getElementById('galleryModalOverlay').style.display = 'none';
    }

    // Close the gallery if the user clicks outside the window on the dark background
    window.addEventListener('click', function(event) {
        let galleryModal = document.getElementById('galleryModalOverlay');
        if (event.target === galleryModal) {
            galleryModal.style.display = "none";
        }
    });
</script>

        <a href="#" class="side-link" onclick="toggleMenu(); openPricing()"><i class="fas fa-tags"></i> Price List</a>
        <a href="#" class="side-link" onclick="toggleMenu(); navAction('booking')"><i class="fas fa-calendar-check"></i> Booking</a>
        <a href="#" class="side-link" onclick="toggleMenu(); openFeedback()"><i class="fas fa-star"></i> Feedback</a>
        <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openAiModal()">
    <i class="fas fa-robot"></i> AI Assistant
</a>

<style>
    #aiModalOverlay {
        display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
        background: rgba(5, 5, 8, 0.95); backdrop-filter: blur(10px);
        z-index: 999999; justify-content: center; align-items: center;
        animation: fadeInOverlay 0.3s ease;
    }
    .mn-ai-box {
        background: linear-gradient(135deg, #120f0a 0%, #0a0a0c 100%); 
        border: 2px solid #D4AF37; border-radius: 16px; width: 95%; max-width: 450px; 
        height: 85vh; max-height: 650px; display: flex; flex-direction: column;
        position: relative; overflow: hidden;
        box-shadow: 0 20px 50px rgba(0,0,0,0.9), inset 0 0 20px rgba(212, 175, 55, 0.15);
        animation: slideDownFade 0.4s cubic-bezier(0.25, 0.8, 0.25, 1) forwards;
    }
    .ai-header {
        background: rgba(212, 175, 55, 0.1); padding: 15px 20px; border-bottom: 1px solid rgba(212, 175, 55, 0.3);
        display: flex; align-items: center; justify-content: space-between;
    }
    .ai-chat-area {
        flex-grow: 1; padding: 20px; overflow-y: auto; display: flex; flex-direction: column; gap: 15px;
    }
    .ai-chat-area::-webkit-scrollbar { width: 5px; }
    .ai-chat-area::-webkit-scrollbar-thumb { background: #D4AF37; border-radius: 10px; }
    .msg-bubble { max-width: 85%; padding: 12px 16px; border-radius: 12px; font-family: 'Outfit', sans-serif; font-size: 14px; line-height: 1.5; }
    .msg-ai { background: rgba(255, 255, 255, 0.05); color: #ddd; align-self: flex-start; border-bottom-left-radius: 2px; border: 1px solid rgba(212, 175, 55, 0.2); }
    .msg-user { background: #D4AF37; color: #000; align-self: flex-end; font-weight: 600; border-bottom-right-radius: 2px; box-shadow: 0 4px 10px rgba(212, 175, 55, 0.3); }
    .ai-input-area { padding: 15px; background: rgba(0,0,0,0.5); border-top: 1px solid rgba(212, 175, 55, 0.3); display: flex; gap: 10px; }
    .ai-input-box { flex-grow: 1; padding: 12px 15px; background: rgba(255, 255, 255, 0.05); border: 1px solid rgba(212, 175, 55, 0.3); color: #fff; border-radius: 50px; outline: none; font-family: 'Outfit', sans-serif; transition: 0.3s; }
    .ai-input-box:focus { border-color: #D4AF37; background: rgba(212, 175, 55, 0.05); }
    .ai-send-btn { background: #D4AF37; color: #000; border: none; width: 45px; height: 45px; border-radius: 50%; cursor: pointer; display: flex; justify-content: center; align-items: center; font-size: 18px; transition: 0.3s; box-shadow: 0 4px 10px rgba(212, 175, 55, 0.4); }
    .ai-send-btn:hover { transform: scale(1.1); }
</style>

<div id="aiModalOverlay" onclick="closeAiOnOutsideClick(event)">
    <div class="mn-ai-box">
        <div class="ai-header">
            <div style="display:flex; align-items:center; gap:10px;">
                <div style="width:38px; height:38px; background:#D4AF37; border-radius:50%; display:flex; justify-content:center; align-items:center; color:#000; font-size:20px;">
                    <i class="fas fa-robot"></i>
                </div>
                <div>
                    <h3 style="margin:0; color:#D4AF37; font-family:'Cinzel', serif; font-size:17px; font-weight:bold; letter-spacing:1px;">Maa Nirmala AI</h3>
                    <div style="color:#00ff00; font-size:11px; font-family:sans-serif; font-weight:bold;">● Online & Ready</div>
                </div>
            </div>
            <span onclick="closeAiModal()" style="color:#D4AF37; font-size:30px; cursor:pointer; line-height:1;">&times;</span>
        </div>
        
        <div class="ai-chat-area" id="aiChatBox">
            <div class="msg-bubble msg-ai">
                🙏 Welcome to Maa Nirmala DJ & Tent House! I am your virtual assistant. How can I help you make your event unforgettable today? Ask me about our Heavy Bass setups, VIP Tents, or Prices!
            </div>
        </div>
        
        <div class="ai-input-area">
            <input type="text" id="aiUserInput" class="ai-input-box" placeholder="Message Maa Nirmala AI..." onkeypress="handleAiEnter(event)">
            <button class="ai-send-btn" onclick="sendAiMessage()">
                <i class="fas fa-paper-plane"></i>
            </button>
        </div>
    </div>
</div>

<script>
    const AI_API_KEY = "AIzaSyB9TBi4xUa2Ruqv0_-_f8ruGTRpXh5YHoQ";
    
    function openAiModal() { document.getElementById('aiModalOverlay').style.display = 'flex'; }
    function closeAiModal() { document.getElementById('aiModalOverlay').style.display = 'none'; }
    function closeAiOnOutsideClick(event) { if (event.target.id === 'aiModalOverlay') closeAiModal(); }
    function handleAiEnter(event) { if (event.key === "Enter") sendAiMessage(); }

    function appendMessage(text, sender) {
        const chatBox = document.getElementById('aiChatBox');
        const msgDiv = document.createElement('div');
        msgDiv.className = `msg-bubble ${sender === 'user' ? 'msg-user' : 'msg-ai'}`;
        // Convert basic markdown formatting into HTML
        let formattedText = text.replace(/\*\*(.*?)\*\*/g, '<b>$1</b>').replace(/\*(.*?)\*/g, '<i>$1</i>').replace(/\n/g, '<br>');
        msgDiv.innerHTML = formattedText;
        chatBox.appendChild(msgDiv);
        chatBox.scrollTop = chatBox.scrollHeight;
    }

    async function sendAiMessage() {
        const inputField = document.getElementById('aiUserInput');
        const userText = inputField.value.trim();
        if (!userText) return;
        
        if(typeof playTap === 'function') playTap();
        
        // Add User Message to Chat
        appendMessage(userText, 'user');
        inputField.value = '';
        
        // Add Typing Indicator
        const chatBox = document.getElementById('aiChatBox');
        const typingDiv = document.createElement('div');
        typingDiv.className = 'msg-bubble msg-ai';
        typingDiv.id = 'aiTypingIndicator';
        typingDiv.innerHTML = '<i class="fas fa-circle-notch fa-spin"></i> Checking details...';
        chatBox.appendChild(typingDiv);
        chatBox.scrollTop = chatBox.scrollHeight;

        // THE "SUPER BRAIN" - This tells the AI exactly how to answer!
        const businessKnowledge = `
        You are "Maa Nirmala AI", the official customer service assistant for "Maa Nirmala DJ & Tent House".
        You must act like a highly professional, welcoming sales manager. Keep answers short, helpful, and convincing.
        Never reveal that you are an AI created by Google. If a user asks who made you, say "I am the digital assistant for Maa Nirmala DJ."
        If the user speaks Hindi, reply in Hinglish or Hindi.
        
        **ALL BUSINESS KNOWLEDGE TO USE FOR ANSWERS:**
        - Owner & Boss: Mr. Lalu Kumar Tanti
        - Management Team: Sildhar Kumar, Anil Kumar, Sanjay Kumar
        - Main Contact Numbers: +91 9771617808 (Lalu), +91 7294969938 (Sildhar), +91 8544341240 (Anil).
        - Full Address: Beltikri, Kaddhar, Katoria, Banka, Bihar, Pin Code: 813106.
        - Style of Work: We are famous for Earth-shaking heavy bass, crystal clear line-array tops, VIP waterproof pandals, and cinematic laser lighting.
        
        **PRICE LIST (Always say these are "Starting Prices" and ask them to book for exact quotes):**
        - Heavy DJ Setup: ₹8,000+
        - Grand Wedding Tent & Pandal: ₹25,000+
        - Stage Decoration (Floral/Backdrop): ₹10,000+
        - Mega Concert DJ Rig: ₹15,000+
        - Baaraat DJ Trolley: ₹12,000+
        - Premium VIP Pandal: ₹35,000+
        - Heavy Duty Generator (DG Set): ₹4,000+
        - Transport: We use Laxmikant Tractor Transport for all heavy logistics.
        
        **INSTRUCTIONS:**
        1. When answering, try to push the customer to use the "Contact" button or the "Booking Form" on the website.
        2. Always be respectful and use emojis like 🎪, 🎵, 👑 to make it look premium.
        3. Answer the customer's exact question based strictly on the knowledge above.
        
        Customer's Question: "${userText}"
        `;

        try {
            const response = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=${AI_API_KEY}`, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    contents: [{ parts: [{ text: businessKnowledge }] }],
                    generationConfig: { temperature: 0.7, maxOutputTokens: 250 } // Keeps answers fast and focused
                })
            });

            const data = await response.json();
            document.getElementById('aiTypingIndicator').remove();

            if (data.candidates && data.candidates[0].content.parts[0].text) {
                appendMessage(data.candidates[0].content.parts[0].text, 'ai');
            } else {
                appendMessage("I'm sorry, my connection is a bit slow right now. You can directly call Mr. Lalu at +91 9771617808.", 'ai');
            }
        } catch (error) {
            document.getElementById('aiTypingIndicator').remove();
            appendMessage("⚠️ Network error. Please use the Contact button to reach our team directly.", 'ai');
        }
    }
</script>
        <a href="#" class="side-link" onclick="toggleMenu(); navAction('links')"><i class="fas fa-link"></i> All Links</a>
<a href="javascript:void(0)" class="side-link" onclick="openVintageContacts()">
    <i class="fas fa-phone"></i> Contact
</a>

<div id="vintageContactModal" class="vintage-modal-overlay">
    <div class="vintage-modal-content">
        <span class="vintage-close-btn" onclick="closeVintageContacts()">&times;</span>
        <h2 class="vintage-title">Maa Nirmala Directory</h2>
        
        <div class="vintage-contact-list">
            
            <div class="vintage-contact-card">
                <img src="https://i.postimg.cc/6qbJj3hQ/Screenshot-2026-01-14-15-25-06-57-1c337646f29875672b5a61192b9010f9-2.jpg" alt="Anil Kumar" class="vintage-avatar">
                <div class="vintage-info">
                    <h4>Anil Kumar</h4>
                    <div class="vintage-actions">
                        <a href="tel:+918544341240" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                        <a href="https://wa.me/918544341240" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                    </div>
                </div>
            </div>

            <div class="vintage-contact-card">
                <img src="https://i.postimg.cc/7Y7rMx2y/Screenshot-2026-01-14-15-33-01-78-965bbf4d18d205f782c6b8409c5773a4-2.jpg" alt="Sildhar Kumar" class="vintage-avatar">
                <div class="vintage-info">
                    <h4>Sildhar Kumar</h4>
                    <div class="vintage-actions">
                        <a href="tel:+917294969938" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                        <a href="https://wa.me/917294969938" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                    </div>
                </div>
            </div>

            <div class="vintage-contact-card">
                <img src="https://i.postimg.cc/qMWWzWbF/Screenshot-2026-01-14-15-29-44-90-965bbf4d18d205f782c6b8409c5773a4.jpg" alt="Sanjay Kumar" class="vintage-avatar">
                <div class="vintage-info">
                    <h4>Sanjay Kumar</h4>
                    <div class="vintage-actions">
                        <a href="tel:+919153635378" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                        <a href="https://wa.me/919153635378" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                    </div>
                </div>
            </div>

            <div class="vintage-contact-card">
                <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lalu Kumar" class="vintage-avatar">
                <div class="vintage-info">
                    <h4>Lalu Kumar</h4>
                    <div class="vintage-actions">
                        <a href="tel:+919771617808" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                        <a href="https://wa.me/919771617808" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                    </div>
                </div>
            </div>

        </div>
    </div>
</div>

<style>
    /* Overlay Background */
    .vintage-modal-overlay {
        display: none; 
        position: fixed;
        top: 0; left: 0; width: 100%; height: 100%;
        background: rgba(5, 5, 8, 0.85); 
        backdrop-filter: blur(8px);
        z-index: 99999; 
        justify-content: center;
        align-items: center;
    }

    /* Modal Box */
    .vintage-modal-content {
        background: linear-gradient(135deg, #1c1712 0%, #0d0b09 100%); 
        border: 2px solid #D4AF37; 
        border-radius: 16px;
        width: 90%;
        max-width: 420px;
        padding: 30px;
        box-shadow: 0 15px 40px rgba(0,0,0,0.9), inset 0 0 20px rgba(212, 175, 55, 0.15);
        position: relative;
        animation: slideDownFade 0.4s ease-out forwards;
    }

    @keyframes slideDownFade {
        from { opacity: 0; transform: translateY(-30px); }
        to { opacity: 1; transform: translateY(0); }
    }

    /* Close Button */
    .vintage-close-btn {
        position: absolute;
        top: 15px;
        right: 20px;
        color: #D4AF37;
        font-size: 30px;
        line-height: 1;
        cursor: pointer;
        transition: color 0.3s ease;
    }
    .vintage-close-btn:hover { color: #ffffff; }

    /* Title */
    .vintage-title {
        font-family: 'Cinzel', serif;
        color: #D4AF37;
        text-align: center;
        margin: 0 0 20px 0;
        font-size: 22px;
        font-weight: bold;
        border-bottom: 1px solid rgba(212, 175, 55, 0.3);
        padding-bottom: 15px;
        letter-spacing: 1px;
    }

    /* Contact Row */
    .vintage-contact-card {
        display: flex;
        align-items: center;
        padding: 18px 0;
        border-bottom: 1px dashed rgba(212, 175, 55, 0.2); 
    }
    .vintage-contact-card:last-child { border-bottom: none; padding-bottom: 0; }

    /* Circular Avatar */
    .vintage-avatar {
        width: 65px;
        height: 65px;
        border-radius: 50%;
        object-fit: cover;
        border: 2px solid #D4AF37;
        margin-right: 20px;
        box-shadow: 0 5px 15px rgba(0,0,0,0.5);
        filter: sepia(0.2) contrast(1.1); 
    }

    /* Name Text */
    .vintage-info h4 {
        margin: 0 0 8px 0;
        font-family: 'Cinzel', serif;
        font-size: 18px;
        color: #ffffff;
        letter-spacing: 0.5px;
    }

    /* Action Buttons Container */
    .vintage-actions {
        display: flex;
        gap: 10px;
    }

    /* Button Styling */
    .action-btn {
        font-family: 'Outfit', sans-serif;
        text-decoration: none;
        font-size: 13px;
        display: flex;
        align-items: center;
        gap: 6px;
        padding: 5px 12px;
        border-radius: 50px;
        transition: all 0.3s ease;
        border: 1px solid rgba(212, 175, 55, 0.4);
        color: #D4AF37;
        background: rgba(212, 175, 55, 0.05);
    }

    /* Call Button Hover */
    .call-btn:hover {
        background: rgba(212, 175, 55, 0.2);
        color: #ffffff;
        border-color: #D4AF37;
        box-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
    }

    /* WhatsApp Button Hover */
    .wa-btn {
        border-color: rgba(37, 211, 102, 0.4);
        color: #cccccc;
    }
    .wa-btn i {
        color: #25D366;
    }
    .wa-btn:hover {
        background: rgba(37, 211, 102, 0.15);
        color: #ffffff;
        border-color: #25D366;
        box-shadow: 0 0 10px rgba(37, 211, 102, 0.3);
    }
</style>

<script>
    function openVintageContacts() {
        document.getElementById('vintageContactModal').style.display = 'flex';
    }

    function closeVintageContacts() {
        document.getElementById('vintageContactModal').style.display = 'none';
    }

    // Close the popup if user clicks the dark background outside the box
    window.onclick = function(event) {
        let modal = document.getElementById('vintageContactModal');
        if (event.target == modal) {
            modal.style.display = "none";
        }
    }
</script>
        <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openComplaintModal()">
    <i class="fas fa-headset"></i> Support / Complaint
</a>

<style>
    /* Dark Blurred Overlay */
    #complaintModalOverlay {
        display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
        background: rgba(5, 5, 8, 0.95); backdrop-filter: blur(10px);
        z-index: 999999; justify-content: center; align-items: center;
        animation: fadeInOverlay 0.3s ease;
    }
    
    /* The Red-Themed Premium Box */
    .mn-complaint-box {
        background: linear-gradient(135deg, #1a0d0d 0%, #0a0a0c 100%); 
        border: 2px solid #E63946; border-radius: 16px; width: 95%; max-width: 520px; 
        padding: 25px; position: relative;
        box-shadow: 0 20px 50px rgba(0,0,0,0.9), inset 0 0 20px rgba(230, 57, 70, 0.15);
        animation: slideDownFade 0.4s cubic-bezier(0.25, 0.8, 0.25, 1) forwards;
    }

    /* Advanced Input Styling with Red Glow on Focus */
    .c-input {
        width: 100%; padding: 12px 15px; background: rgba(255, 255, 255, 0.05);
        border: 1px solid rgba(230, 57, 70, 0.3); color: #fff; border-radius: 8px;
        outline: none; font-family: 'Outfit', sans-serif; box-sizing: border-box;
        transition: all 0.3s ease; margin-bottom: 12px;
    }
    .c-input:focus {
        border-color: #E63946; background: rgba(230, 57, 70, 0.05); box-shadow: 0 0 12px rgba(230, 57, 70, 0.4);
    }
    .c-input::placeholder { color: #888; }
</style>

<div id="complaintModalOverlay" onclick="closeOnOutsideClick(event)">
    <div class="mn-complaint-box" id="complaintBoxContent">
        <span onclick="closeComplaintModal()" style="position:absolute; top:15px; right:20px; color:#E63946; font-size:35px; line-height:1; cursor:pointer; transition:0.3s;">&times;</span>
        
        <h2 style="font-family:'Cinzel',serif; color:#E63946; text-align:center; margin-top:0; border-bottom:1px solid rgba(230,57,70,0.3); padding-bottom:15px; font-size: 24px; font-weight:800; letter-spacing:1px;">
            <i class="fas fa-exclamation-triangle"></i> Register Complaint
        </h2>
        
        <div style="display:flex; flex-direction:column; margin-top: 15px;">
            <div style="display:flex; gap:10px;">
                <input type="text" id="c-name" class="c-input" placeholder="Full Name *">
                <input type="tel" id="c-phone" class="c-input" placeholder="Phone Number *">
            </div>
            
            <input type="text" id="c-event-name" class="c-input" placeholder="Event Name (e.g. Amit Wedding) *">
            
            <div style="display:flex; gap:10px;">
                <div style="flex:1;">
                    <span style="color:#E63946; font-size:12px; font-family:'Outfit', sans-serif; padding-left:5px;">Event Date *</span>
                    <input type="date" id="c-event-date" class="c-input" style="color:#ddd; margin-bottom:0;">
                </div>
                <div style="flex:1;">
                    <span style="color:#E63946; font-size:12px; font-family:'Outfit', sans-serif; padding-left:5px;">Event Time *</span>
                    <input type="time" id="c-event-time" class="c-input" style="color:#ddd; margin-bottom:0;">
                </div>
            </div>

            <select id="c-type" class="c-input" style="color:#ddd; margin-top:12px;">
                <option value="" disabled selected style="color:#000;">Select Issue Type *</option>
                <option value="Event Setup Delay" style="color:#000;">Event Setup Delay</option>
                <option value="Sound / Light Problem" style="color:#000;">Sound / Light Problem</option>
                <option value="Tent / Decor Issue" style="color:#000;">Tent / Decor Issue</option>
                <option value="Staff Behavior" style="color:#000;">Staff Behavior</option>
                <option value="Other Issue" style="color:#000;">Other Issue</option>
            </select>
            
            <textarea id="c-desc" class="c-input" rows="3" placeholder="Describe the issue in detail... *" style="resize:none;"></textarea>
            
            <button id="submitComplaintBtn" onclick="submitComplaint()" style="background:#E63946; color:#fff; font-weight:bold; padding:15px; border:none; border-radius:8px; cursor:pointer; font-size:16px; margin-top:5px; transition:0.3s; font-family:'Outfit', sans-serif; box-shadow: 0 5px 15px rgba(230, 57, 70, 0.4);">
                <i class="fas fa-paper-plane"></i> SEND URGENT ALERT
            </button>
        </div>
    </div>
</div>

<script>
    // Open & Close Functions
    function openComplaintModal() { document.getElementById('complaintModalOverlay').style.display = 'flex'; }
    function closeComplaintModal() { document.getElementById('complaintModalOverlay').style.display = 'none'; }
    
    // Close when clicking the dark background outside the box
    function closeOnOutsideClick(event) {
        if (event.target.id === 'complaintModalOverlay') { closeComplaintModal(); }
    }
    
    // Advanced Submission Logic
    function submitComplaint() {
        if(typeof playTap === 'function') playTap();
        const name = document.getElementById('c-name').value; const phone = document.getElementById('c-phone').value; const eventName = document.getElementById('c-event-name').value; const eventDate = document.getElementById('c-event-date').value; const eventTime = document.getElementById('c-event-time').value; const type = document.getElementById('c-type').value; const desc = document.getElementById('c-desc').value;
        
        // Validation
        if(!name || !phone || !eventName || !eventDate || !eventTime || !type || !desc) { 
            alert("⚠️ Please fill all required (*) fields so we can resolve your issue immediately!"); return; 
        }
        
        // Loading State
        const btn = document.getElementById('submitComplaintBtn'); 
        btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> SENDING ALERT...'; 
        btn.style.opacity = '0.7';
        
        // Exact Day, Date, and Time Calculation
        const now = new Date(); 
        const exactDay = now.toLocaleDateString('en-IN', { weekday: 'long' }); 
        const exactDate = now.toLocaleDateString('en-IN', { year: 'numeric', month: 'long', day: 'numeric' }); 
        const exactTime = now.toLocaleTimeString('en-IN', { hour: '2-digit', minute: '2-digit', hour12: true });
        
        // Telegram Message Formatting
        const msg = `🚨 *URGENT COMPLAINT LOGGED* 🚨\n---------------------------\n🗓️ *Submitted Day:* ${exactDay}\n📅 *Submitted Date:* ${exactDate}\n⏰ *Submitted Time:* ${exactTime}\n\n👤 *Client Name:* ${name}\n📞 *Contact:* ${phone}\n\n🎪 *Event Details:*\n• Name: ${eventName}\n• Date: ${eventDate}\n• Time: ${eventTime}\n\n⚠️ *Issue Category:* ${type}\n📝 *Description:*\n${desc}\n\n🛑 *ACTION REQUIRED IMMEDIATELY*`;
        
        // Send to Telegram
        fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { 
            method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) 
        }).then(res => { 
            btn.innerHTML = '<i class="fas fa-check"></i> SUBMITTED!'; 
            btn.style.background = '#00ff00'; btn.style.color = '#000';
            
            // Reset and Close after 2 seconds
            setTimeout(() => { 
                closeComplaintModal(); 
                btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND URGENT ALERT'; 
                btn.style.background = '#E63946'; btn.style.color = '#fff'; btn.style.opacity = '1'; 
                document.getElementById('c-name').value=''; document.getElementById('c-phone').value=''; document.getElementById('c-event-name').value=''; document.getElementById('c-event-date').value=''; document.getElementById('c-event-time').value=''; document.getElementById('c-type').value=''; document.getElementById('c-desc').value=''; 
            }, 2000); 
        }).catch(err => { 
            alert("Network Error. Please call Mr. Lalu directly at +91 9771617808"); 
            btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND URGENT ALERT'; 
            btn.style.opacity = '1'; 
        });
    }
</script>
        <a href="mailto:lalukumartanti75@gmail.com" class="side-link"><i class="fas fa-envelope"></i> Email</a>
    </div>

    <div id="main-interface">
        <audio id="sfx-tap"><source src="https://assets.mixkit.co/active_storage/sfx/2568/2568-preview.mp3"></audio>
        <div id="toast" class="toast"><i class="fas fa-check-circle"></i> Success</div>
        <div class="bg-fx"><div class="orb orb-1"></div><div class="orb orb-2"></div></div>
        
        <nav class="navbar">
            <div class="brand"><i class="fas fa-bars nav-btn" onclick="toggleMenu()"></i><span><i class="fas fa-crown"></i> MND Hub</span></div>
            <div style="display: flex; align-items: center;">
                <div id="google_translate_element"></div>
                <div class="controls"><button class="nav-btn" id="themeIcon" onclick="themeSwitch()"><i class="fas fa-sun"></i></button></div>
            </div>
        </nav>
        
        <div class="container" id="homeSection">
            <div class="profile-wrapper">
                <div class="img-container"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" class="profile-pic" alt="Maa Nirmala DJ & Tent House"></div>
                <h1>MAA NIRMALA DJ & TENT HOUSE <i class="fas fa-check-circle verified"></i></h1>
                <p class="bio">Digital Creator | Developer</p>
                <button id="installBtn" onclick="installApp()"><i class="fas fa-download"></i> INSTALL MNDs APP</button>
            </div>

            <div class="section-label"><i class="fas fa-images"></i> OUR SETUP & SHOWCASE</div>
            <div class="grid">
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="DJ Setup"><span>Elite DJ Setup</span></a>
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Tent House"><span>Premium Tents</span></a>
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lighting"><span>Stage Lighting</span></a>
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Booking"><span>Book Event Now</span></a>
            </div>

            <div class="section-label" style="margin-top: 40px;"><i class="fas fa-star"></i> BEST OF MAA NIRMALA</div>
<div class="slider-container">
    <div class="slide-card">
        <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Setup 1">
        <div class="slide-info">
            <h3>Grand Wedding Setup</h3>
            <div style="font-size: 13px; color: #dddddd; margin-top: 5px; font-weight: normal; line-height: 1.4;">Hello, this is Maa Nirmala DJ, one of the best DJs here. Perfect!</div>
        </div>
    </div>
    <div class="slide-card">
        <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Setup 2">
        <div class="slide-info">
            <h3>Heavy Bass DJ Event</h3>
            <div style="font-size: 13px; color: #dddddd; margin-top: 5px; font-weight: normal; line-height: 1.4;">Hello, this is Maa Nirmala DJ, one of the best DJs here. Perfect!</div>
        </div>
    </div>
    <div class="slide-card">
        <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Setup 3">
        <div class="slide-info">
            <h3>VIP Tent & Decoration</h3>
            <div style="font-size: 13px; color: #dddddd; margin-top: 5px; font-weight: normal; line-height: 1.4;">Hello, this is Maa Nirmala DJ, one of the best DJs here. Perfect!</div>
        </div>
    </div>
</div>


            <div class="section-label" id="liveGallerySection" style="margin-top: 40px;"><i class="fas fa-broadcast-tower"></i> LIVE UPDATES & GALLERY</div>
            <div class="feed-container" id="dynamicGallery">
                </div>
            
            <div class="section-label" style="margin-top:40px;"><i class="fas fa-users"></i> MEET OUR TEAM</div>
            <div class="slider-container">
                <div class="team-card">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lalu Kumar Tanti">
                    <h1>Lalu Kumar Tanti</h1>
                    <h3>Owner & Founder</h3>
                    <p>A passionate and hardworking individual providing the best event setup, DJ, and Tent services.</p>
                </div>
                <div class="team-card">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Mr. Lalu Kumar">
                    <h1>Mr. Lalu Kumar</h1>
                    <h3>Business Dev. Manager</h3>
                    <p>Ensuring top-tier service delivery and managing all grand event setups across the district.</p>
                </div>
                <div class="team-card">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Sildhar Kumar">
                    <h1>Sildhar Kumar</h1>
                    <h3>Business Associate</h3>
                    <p>Coordinating premium tent decorations, lighting arrangements, and dedicated client relations.</p>
                </div>
            </div>

            <div class="section-label" style="margin-top:40px;"><i class="fas fa-info-circle"></i> ABOUT THE BUSINESS</div>
            <div class="owner-profile" style="text-align: left;">
                <h1 style="text-align: center; font-size: 28px;">Maa Nirmala DJ & Tent House</h1>
                <p style="text-align: center; color: var(--gold-primary); font-weight: bold; margin-bottom: 20px; text-transform: uppercase; letter-spacing: 1px;">Premium Event Management in Bihar</p>
                <p style="font-size: 14px;">Welcome to <b>Maa Nirmala DJ & Tent House</b>, the premier event management and setup service based in Beltikri. We specialize in transforming ordinary events into grand, unforgettable celebrations.</p>
                <ul style="color: #eaeaea; font-size: 14px; line-height: 1.8; margin-left: 20px; margin-bottom: 25px; margin-top: 15px;">
                    <li><b style="color: var(--gold-primary);">Elite DJ Setups:</b> High-fidelity sound systems, heavy bass, and non-stop entertainment.</li>
                    <li><b style="color: var(--gold-primary);">Premium Tent Houses:</b> Grand wedding tents, VIP seating, and beautiful decorations.</li>
                    <li><b style="color: var(--gold-primary);">Stage Lighting:</b> Advanced dynamic lighting to illuminate your special moments.</li>
                </ul>
                <div style="border-top: 1px solid var(--border-color); margin: 25px 0;"></div>
                <div style="text-align: center;">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lalu Kumar Tanti" style="width: 100px; height: 100px; margin-bottom: 10px; border: 3px solid var(--gold-primary);">
                    <h2 style="color: var(--gold-primary); font-family: 'Cinzel'; font-size: 22px; font-weight: bold;">Lalu Kumar Tanti</h2>
                    <h3 style="font-size: 12px; color: #aaa; margin-bottom: 15px; text-transform: uppercase; letter-spacing: 2px;">Founder & Owner</h3>
                </div>
            </div>

            <div class="section-label" style="margin-top:40px;"><i class="fas fa-map-marker-alt"></i> OUR LOCATION</div>
            <div class="map-container">
                <p style="text-align: center; color: var(--gold-primary); font-family: 'Cinzel'; font-weight: bold; font-size: 18px; margin-bottom: 5px;">Maa Nirmala DJ & Tent House</p>
                <p style="text-align: center; font-size: 12px; color: #ccc; margin-bottom: 15px; font-family: 'Outfit'; letter-spacing: 1px;">JRPM+RQ, Beltikri, Tola Tetaria, Bihar 814131</p>
                
                <div class="map-wrapper">
                    <iframe src="https://maps.google.com/maps?q=JRPM+RQ%20Beltikri,%20Tola%20Tetaria,%20Bihar%20814131&t=&z=15&ie=UTF8&iwloc=&output=embed" width="100%" height="100%" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                </div>
                
                <a href="https://maps.google.com/maps?q=JRPM+RQ%20Beltikri,%20Tola%20Tetaria,%20Bihar%20814131" target="_blank" style="display: block; width: 100%; padding: 15px; background: var(--gold-primary); color: #000; text-align: center; font-weight: bold; border-radius: 8px; text-decoration: none; margin-top: 15px; font-family: 'Rajdhani'; letter-spacing: 1px; transition: 0.3s;">
                    <i class="fas fa-directions"></i> GET DIRECTIONS TO MAP
                </a>
            </div>

            <div class="section-label" style="margin-top:40px;"><i class="fas fa-music"></i> THE MAA NIRMALA EXPERIENCE</div>
            <div style="background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 20px; padding: 20px; text-align: center; box-shadow: 0 5px 20px rgba(0,0,0,0.2);">
                <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" style="width: 100%; height: 200px; object-fit: cover; border-radius: 12px; border: 2px solid var(--gold-primary); margin-bottom: 15px;" alt="Experience">
                <h3 style="color: var(--gold-primary); font-family: 'Cinzel'; margin-bottom: 10px; font-size: 20px;">Unmatched Sound & Vibes</h3>
                <p style="font-size: 14px; line-height: 1.6; color: #ddd;">Maa Nirmala DJ sets the standard for high-energy celebrations in Banka. With state-of-the-art audio, dazzling light shows, and premium VIP tents, we guarantee a flawless event. From intimate functions to massive district festivals, our team works tirelessly to bring your dream event to reality.</p>
            </div>
                      <div class="section-label" style="margin-top:40px;"><i class="fas fa-music"></i> THE MAA NIRMALA EXPERIENCE</div>
            <div style="background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 20px; padding: 20px; text-align: center; box-shadow: 0 5px 20px rgba(0,0,0,0.2);">
                <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" style="width: 100%; height: 200px; object-fit: cover; border-radius: 12px; border: 2px solid var(--gold-primary); margin-bottom: 15px;" alt="Experience">
                <h3 style="color: var(--gold-primary); font-family: 'Cinzel'; margin-bottom: 10px; font-size: 20px;">Unmatched Sound & Vibes</h3>
                <p style="font-size: 14px; line-height: 1.6; color: #ddd;">Maa Nirmala DJ sets the standard for high-energy celebrations in Banka. With state-of-the-art audio, dazzling light shows, and premium VIP tents, we guarantee a flawless event. From intimate functions to massive district festivals, our team works tirelessly to bring your dream event to reality.</p>
            </div>
          <div style="width: 100%; padding: 40px 15px; background-color: transparent; display: flex; flex-direction: column; align-items: center; justify-content: center; box-sizing: border-box;">

    <div class="section-label" style="margin-bottom: 30px; color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; font-size: 14px; font-weight: bold; letter-spacing: 2px; text-transform: uppercase; text-align: center;">
        <i class="fas fa-crown"></i> The Maa Nirmala Experience
    </div>

    <div style="max-width: 800px; text-align: center;">

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 24px; font-weight: 800; line-height: 1.4; letter-spacing: 1px;">
            THE PINNACLE OF PREMIUM CELEBRATIONS
        </h3>
        
        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            Maa Nirmala DJ & Tent House sets the absolute standard for high-energy, luxurious celebrations across Banka. Under the visionary leadership of Mr. Lalu Kumar Tanti, we have transformed countless events from ordinary gatherings into extraordinary cinematic experiences. Situated in the historic heart of Beltikri, Kaddhar, Katoria, our dedicated team works tirelessly to bring your ultimate dream event to reality with unmatched precision. We believe that a celebration is not merely a date on a calendar, but a profound milestone in human life that deserves the utmost reverence, spectacular visual beauty, and flawless technical execution.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            THE SUPREMACY OF ACOUSTIC ENGINEERING
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            The soul of any grand event is its acoustic heartbeat. At Maa Nirmala DJ, we do not simply play music; we engineer an auditory atmosphere that captivates the senses. We deploy state-of-the-art, heavy-duty subwoofers that push massive volumes of air, ensuring an earth-shattering bass response that you can feel resonating in your very soul. Complementing this low-end power are our crystal-clear, high-frequency line-array top speakers, strategically positioned to cast sound evenly across massive venues without a single hint of distortion. Whether it is a subtle background melody during a serene wedding ritual or a high-octane electronic drop at a midnight dance party, our audio technicians balance every frequency with surgical precision.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            DYNAMIC VISUAL VIBES & INTELLIGENT LIGHTING
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            Sound alone cannot carry a premium event; it must be paired with a breathtaking visual spectacle. We utilize intelligent, programmable DMX lighting systems to paint the venue in vibrant colors and dynamic movement. Our synchronized laser light shows slice through the darkness, while our powerful moving head beams track the tempo of the music, creating an immersive, concert-level club environment right at your venue. By introducing atmospheric effects such as heavy ground fog and spectacular cold spark machines during key moments—like the bride and groom's grand entrance—we elevate the emotional impact of the evening to truly cinematic heights.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            ROYAL TENT ARCHITECTURE & STRUCTURAL INTEGRITY
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            Beyond the music and lights, we construct magnificent, temporary palaces. Our premium tent setups are feats of structural engineering, built using heavy-duty iron trusses and highly secure rigging systems that guarantee absolute safety and stability, regardless of unpredictable weather conditions. We construct massive waterproof pandals draped in miles of luxurious, imported fabrics that cascade elegantly from towering ceilings. The interiors are designed with immaculate spatial awareness, featuring dedicated VIP seating zones, expansive dining areas, and plush, wall-to-wall carpeting that provides a royal walking experience for every guest in attendance.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            BESPOKE FLORAL DECOR & STAGE CRAFTSMANSHIP
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            The stage is the undisputed focal point of your celebration, and our decoration team crafts it into a breathtaking visual masterpiece. We seamlessly blend traditional Indian wedding aesthetics with modern, contemporary design trends. Utilizing thousands of fresh, vibrant blooms, our decorators construct intricate floral archways, majestic entry gates (Dwar), and stunning photo booths. The main stage is furnished with customized luxury couches and thematic backdrops, ensuring that every photograph taken captures the elegance, grandeur, and prestige of your special day perfectly.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            UNYIELDING POWER BACKUP SYSTEMS
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            A luxury event cannot afford a single millisecond of darkness or silence. Recognizing the unpredictability of local power grids, Maa Nirmala DJ & Tent House provides absolute, unyielding power reliability. We deploy massive, heavy-duty, silent generator (DG) sets capable of sustaining the enormous electrical load required by our line-array speakers, massive lighting rigs, and catering equipment. Our dedicated technicians monitor these systems continuously throughout the event, ensuring that the magic, the music, and the celebration continue flawlessly without a single interruption.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            LOGISTICAL MIGHT & TRANSPORT EFFICIENCY
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            The invisible backbone of our grand setups is an incredibly robust logistical network. Transporting towering iron trusses, heavy subwoofers, delicate lighting fixtures, and miles of fabric requires supreme efficiency. Supported powerfully by Laxmikant Tanti farming tractor services, we possess the logistical might to deliver massive payloads of equipment to any venue, no matter how remote the location in Banka district. Our setup and teardown teams, including dedicated associates like Sildhar Kumar, operate with military-like precision, ensuring that venues are prepared well in advance and cleared seamlessly once the celebration concludes.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            MASTERING EVERY TYPE OF CELEBRATION
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            Our expertise is not limited to a single type of event. We are masters of versatility, capable of adapting our immense resources to perfectly suit the specific emotional tone of your gathering. For grand weddings, we provide the royal, traditional elegance required for Baraat processions, Haldi ceremonies, and luxurious receptions. For massive district-level religious festivals and melas, we construct incredibly durable, high-capacity structures. And for high-energy birthday bashes or anniversaries, we shift our focus to delivering the ultimate, neon-lit, heavy-bass dance floor experience.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            SAFETY PROTOCOLS & ON-SITE MANAGEMENT
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 35px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            True luxury includes the luxury of peace of mind. We take the safety of your guests with the utmost seriousness. Every electrical cable is heavily insulated and safely routed away from foot traffic to prevent trip hazards. Every heavy iron pillar is firmly anchored to the ground to withstand sudden high winds. Throughout the entirety of your event, our on-site management team remains hyper-vigilant, continuously monitoring the structural integrity of the pandals, the safe operation of the generators, and the flawless output of the audio-visual equipment.
        </p>

        <h3 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; margin-bottom: 15px; font-size: 20px; font-weight: 700; letter-spacing: 1px;">
            A LEGACY BUILT ON TRUST AND PERFECTION
        </h3>

        <p style="font-size: 15px; line-height: 1.7; color: #cccccc; margin-bottom: 20px; font-family: 'Outfit', sans-serif; font-weight: 400; text-wrap: balance;">
            For years, the communities of Beltikri, Katoria, and the greater Banka region have trusted us with their most precious moments. This legacy of trust has been meticulously built by Mr. Lalu Kumar Tanti upon a foundation of total transparency, unwavering punctuality, and an absolute refusal to compromise on quality. When you hire Maa Nirmala DJ & Tent House, you are not just renting equipment; you are partnering with an entire organization dedicated solely to your joy. We leave nothing to chance, we accept no excuses, and we let our spectacular results speak for themselves. Choose us, and let us engineer the perfect, unforgettable night.
        </p>
    </div>
</div>
            </div>

<div style="text-align: center; max-width: 800px; margin: 40px auto 20px auto; padding: 0 20px;">
    <p style="color: #dddddd; font-family: 'Outfit', sans-serif; font-size: 16px; line-height: 1.8; text-wrap: balance; margin-bottom: 30px;">
        Maa Nirmala DJ sets the standard for high-energy celebrations in Banka. With state-of-the-art audio, dazzling light shows, and premium VIP tents, we guarantee a flawless event. From intimate functions to massive district festivals, our team works tirelessly to bring your dream event to reality.
    </p>

    <h4 style="color: var(--gold-primary, #D4AF37); font-family: 'Cinzel', serif; font-size: 18px; margin-bottom: 20px; letter-spacing: 1px; text-transform: uppercase;">
        <i class="fas fa-link"></i> Follow & Connect
    </h4>

    <style>
        .mn-social-icon {
            color: #ffffff;
            font-size: 26px;
            text-decoration: none;
            transition: transform 0.3s ease, color 0.3s ease;
        }
        .mn-social-icon:hover {
            color: var(--gold-primary, #D4AF37);
            transform: scale(1.2);
        }
    </style>
    
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 25px; max-width: 600px; margin: 0 auto;">
        <a href="https://www.instagram.com/maa_nirmala_dj" target="_blank" class="mn-social-icon" title="Instagram"><i class="fab fa-instagram"></i></a>
        <a href="https://www.facebook.com/MaaNirmalaDJ7" target="_blank" class="mn-social-icon" title="Facebook"><i class="fab fa-facebook-f"></i></a>
        <a href="https://x.com/maa_nirmala_dj" target="_blank" class="mn-social-icon" title="X"><i class="fab fa-x-twitter"></i></a>
        <a href="https://maanirmaladj.github.io/Maa-Nirmala-DJ-Beltikri/" target="_blank" class="mn-social-icon" title="Website"><i class="fas fa-globe"></i></a>
        <a href="https://www.linkedin.com/in/maa-nirmala-dj-tent-house-3499a33b0" target="_blank" class="mn-social-icon" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        <a href="https://www.threads.com/@maa_nirmala_dj" target="_blank" class="mn-social-icon" title="Threads"><i class="fab fa-threads"></i></a>
        <a href="https://www.youtube.com/channel/UCQPUgEyCm8nihqhYGMUX6Pw" target="_blank" class="mn-social-icon" title="YouTube"><i class="fab fa-youtube"></i></a>
        <a href="https://whatsapp.com/channel/0029Vb7AMDl4IBhJ34po3L1k" target="_blank" class="mn-social-icon" title="WhatsApp Channel"><i class="fab fa-whatsapp"></i></a>
        <a href="https://t.me/MaaNirmalaDJ" target="_blank" class="mn-social-icon" title="Telegram"><i class="fab fa-telegram-plane"></i></a>
        <a href="https://maps.app.goo.gl/fSqCowWHPoVxGuLz6" target="_blank" class="mn-social-icon" title="Location"><i class="fas fa-map-marker-alt"></i></a>
    </div>
</div>

<div style="text-align:center; margin-top:40px; margin-bottom:30px;">
    <div class="rights" style="color:var(--gold-primary); font-weight:bold; font-size:12px;">      © 2026 All Rights Reserved —Maa Nirmala DJ & Tent House</div>
</div>
        <div class="bottom-nav">
            <div class="nav-item active" id="navHome" onclick="navAction('home')"><i class="fas fa-home"></i><span>Home</span></div>
            <div class="nav-item" id="navLinks" onclick="navAction('links')"><i class="fas fa-link"></i><span>Links</span></div>
            <div class="nav-item" id="navBooking" onclick="navAction('booking')"><i class="fas fa-calendar-alt"></i><span>Booking</span></div>
            <div class="nav-item" id="navLogin" onclick="navAction('login')"><i class="fas fa-user-shield"></i><span>Auth</span></div>
        </div>

        <div class="ai-trigger" onclick="openAI()"><i class="fas fa-brain" style="font-size:24px; color:#fff;"></i></div>

        <div class="modal-wrap" id="priceModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center;">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-tags"></i> STANDARD PRICE LIST</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area">
                    <p style="color:#ddd; font-size:12px; margin-bottom:20px; text-align:center;">*Prices are estimated starting points and may vary based on location and specific event requirements.</p>
                    
                   <div class="price-card">
                        <div>
                            <div class="price-title">Heavy DJ Setup</div>
                            <div style="font-size:11px; color:#aaa;">Dual Bass, Tops, Light & Operator</div>
                        </div>
                        <div class="price-amt">₹8,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Grand Wedding Tent</div>
                            <div style="font-size:11px; color:#aaa;">Pandal, Chairs, VIP Sofa, Carpet</div>
                        </div>
                        <div class="price-amt">₹25,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Stage Decoration</div>
                            <div style="font-size:11px; color:#aaa;">Floral Setup, Lighting, Backdrop</div>
                        </div>
                        <div class="price-amt">₹10,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Complete Package</div>
                            <div style="font-size:11px; color:#aaa;">DJ + Tent + Lighting Full Setup</div>
                        </div>
                        <div class="price-amt">Custom</div>
                    </div>

                    <div class="price-card">
                        <div>
                            <div class="price-title">Standard Sound System</div>
                            <div style="font-size:11px; color:#aaa;">2 Bass, 2 Tops, Mixer & Mics</div>
                        </div>
                        <div class="price-amt">₹5,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Mega Concert DJ Rig</div>
                            <div style="font-size:11px; color:#aaa;">4 Heavy Bass, Line Array Tops, DMX Lights</div>
                        </div>
                        <div class="price-amt">₹15,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Baaraat DJ Trolley</div>
                            <div style="font-size:11px; color:#aaa;">Moving Sound Setup with Lights & Power</div>
                        </div>
                        <div class="price-amt">₹12,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Haldi / Mehendi Sound</div>
                            <div style="font-size:11px; color:#aaa;">Compact Crystal Clear Audio Setup</div>
                        </div>
                        <div class="price-amt">₹3,500+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Intelligent Laser Show</div>
                            <div style="font-size:11px; color:#aaa;">3D Lasers, Moving Heads, Synchronized</div>
                        </div>
                        <div class="price-amt">₹6,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Cinematic Visual Effects</div>
                            <div style="font-size:11px; color:#aaa;">Heavy Fog Machine & Safe Cold Spark Pyro</div>
                        </div>
                        <div class="price-amt">₹4,500+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Ambient Venue Lighting</div>
                            <div style="font-size:11px; color:#aaa;">LED Wash Lights, Fairy Lights for Tent</div>
                        </div>
                        <div class="price-amt">₹5,500+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Premium VIP Pandal</div>
                            <div style="font-size:11px; color:#aaa;">Luxury Waterproof Enclosure & Drapery</div>
                        </div>
                        <div class="price-amt">₹35,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Catering Stall Setup</div>
                            <div style="font-size:11px; color:#aaa;">Buffet Tables, Frills, Support Structure</div>
                        </div>
                        <div class="price-amt">₹8,500+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Royal Entrance Gate</div>
                            <div style="font-size:11px; color:#aaa;">Grand Floral Dwar & Illuminated Entryway</div>
                        </div>
                        <div class="price-amt">₹7,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Heavy Duty Generator</div>
                            <div style="font-size:11px; color:#aaa;">Uninterrupted DG Set Power (Fuel Extra)</div>
                        </div>
                        <div class="price-amt">₹4,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">VIP Seating Arrangement</div>
                            <div style="font-size:11px; color:#aaa;">Premium Couches, Banquet Chairs & Covers</div>
                        </div>
                        <div class="price-amt">₹6,500+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Cooling & Fan Setup</div>
                            <div style="font-size:11px; color:#aaa;">High-Speed Pedestal & Water Mist Fans</div>
                        </div>
                        <div class="price-amt">₹3,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Birthday Blast Package</div>
                            <div style="font-size:11px; color:#aaa;">Compact Tent, DJ, Balloon & Floral Decor</div>
                        </div>
                        <div class="price-amt">₹12,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Laxmikant Tractor Transport</div>
                            <div style="font-size:11px; color:#aaa;">Heavy Logistics & Equipment Hauling</div>
                        </div>
                        <div class="price-amt">Custom</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Anniversary Royal Package</div>
                            <div style="font-size:11px; color:#aaa;">Romantic Decor, Soft Lighting, DJ System</div>
                        </div>
                        <div class="price-amt">₹18,000+</div>
                    </div>

                    
                    <button class="f-btn" onclick="navAction('booking')"><i class="fas fa-calendar-check"></i> BOOK NOW FOR EXACT QUOTE</button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="linksModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center; background:rgba(10,10,10,0.9);">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-link"></i> OFFICIAL LINKS HUB</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area">
                    <div class="section-label" style="margin-top: 0;"><i class="fas fa-bolt"></i> DIRECT CONNECT</div>
                    <div class="grid">
                        <a href="#" class="card" onclick="playTap()"><i class="fas fa-phone-volume"></i><span>Call Now</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-whatsapp"></i><span>WhatsApp</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-telegram-plane"></i><span>Telegram</span></a>
                        <a href="#" target="_blank" class="card full-w" onclick="playTap()"><i class="fas fa-map-marked-alt"></i><span>Official Location</span></a>
                    </div>
                    <div class="section-label"><i class="fas fa-globe"></i> SOCIAL EMPIRE</div>
                    <div class="grid">
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-instagram"></i><span>Instagram</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-facebook-f"></i><span>Facebook</span></a>
                        <a href="#" class="card full-w" onclick="playTap()"><i class="fab fa-youtube"></i><span>YouTube</span></a>
                    </div>
                    <div class="section-label"><i class="fas fa-coins"></i> PAYMENTS & MORE</div>
                    <div class="grid" style="margin-bottom:30px;">
                        <a href="#" class="card" onclick="playTap()"><i class="fas fa-wallet"></i><span>PhonePe</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-google-pay"></i><span>GPay</span></a>
                        <div class="card full-w" onclick="copyUPI()"><i class="fas fa-qrcode"></i><span>Copy UPI ID</span><span style="font-size:7px; opacity:0.7;">9771617808-2@axl</span></div>
                    </div>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="feedbackModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center;">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-star"></i> CLIENT FEEDBACK</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area">
                    <div style="text-align:center; margin-bottom:15px; background: rgba(212,175,55,0.05); padding: 15px; border-radius: 12px; border: 1px solid rgba(212,175,55,0.2);">
                        <h3 style="color:var(--gold-primary); font-family:'Rajdhani'; font-size: 22px; margin-bottom:5px;">Maa Nirmala DJ & Tent House</h3>
                        <p style="font-size:12px; color:#ddd; line-height: 1.4;">Rate your experience with our DJ setup and Tent management!</p>
                    </div>
                    <div class="star-rating">
                        <input type="radio" id="star5" name="rating" value="5"><label for="star5" class="fas fa-star"></label>
                        <input type="radio" id="star4" name="rating" value="4"><label for="star4" class="fas fa-star"></label>
                        <input type="radio" id="star3" name="rating" value="3"><label for="star3" class="fas fa-star"></label>
                        <input type="radio" id="star2" name="rating" value="2"><label for="star2" class="fas fa-star"></label>
                        <input type="radio" id="star1" name="rating" value="1"><label for="star1" class="fas fa-star"></label>
                    </div>
                    <div class="f-group"><span class="f-label">Your Name</span><input type="text" id="fb-name" class="f-input" placeholder="Enter your name"></div>
                    <div class="f-group"><span class="f-label">Your Experience & Feedback</span><textarea id="fb-text" class="f-input" rows="3" placeholder="Tell us what you liked..." style="resize:none; font-family:'Outfit';"></textarea></div>
                    <button class="f-btn" onclick="submitFeedback()" id="submitFbBtn"><i class="fas fa-paper-plane"></i> SEND FEEDBACK TO LALU</button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="bookModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center;">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-clipboard-list"></i> OFFICIAL BOOKING</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area" id="bookFormArea">
    <div class="f-group"><span class="f-label">Event / Requirement Type *</span><input type="text" id="b-type" class="f-input" placeholder="e.g. Wedding DJ, VIP Tent"></div>
    <div style="display: flex; gap: 15px; margin-bottom: 20px;"><div class="f-group" style="flex: 1; margin-bottom: 0;"><span class="f-label"><i class="far fa-calendar-alt" style="color: #D4AF37;"></i> From Date *</span><input type="date" id="b-date-from" class="f-input" style="cursor: pointer; text-transform: uppercase; color: #ddd;"></div><div class="f-group" style="flex: 1; margin-bottom: 0;"><span class="f-label"><i class="far fa-calendar-check" style="color: #D4AF37;"></i> To Date *</span><input type="date" id="b-date-to" class="f-input" style="cursor: pointer; text-transform: uppercase; color: #ddd;"></div></div>
    <div class="f-group"><span class="f-label">Full Name *</span><input type="text" id="b-name" class="f-input" placeholder="Enter Full Name"></div>
    <div class="f-group"><span class="f-label">Father's Name *</span><input type="text" id="b-father" class="f-input" placeholder="Enter Father's Name"></div>
    <div class="f-group"><span class="f-label">Contact Number *</span><input type="tel" id="b-phone" class="f-input" placeholder="Main Mobile Number"></div>
    <div class="f-group"><span class="f-label">Alternate Number</span><input type="tel" id="b-altphone" class="f-input" placeholder="Second Mobile Number"></div>
    <div class="f-group"><span class="f-label">Email Address</span><input type="email" id="b-email" class="f-input" placeholder="example@email.com"></div>
    
    <div class="loc-group">
        <span class="loc-title">📍 EVENT LOCATION DETAILS</span>
        <div class="f-group"><span class="f-label">State *</span><input type="text" id="b-state" class="f-input" placeholder="e.g. Bihar"></div>
        <div class="f-group"><span class="f-label">District *</span><input type="text" id="b-district" class="f-input" placeholder="e.g. Banka"></div>
        <div class="f-group"><span class="f-label">City *</span><input type="text" id="b-city" class="f-input" placeholder="e.g. Katoria"></div>
        <div class="f-group"><span class="f-label">Village *</span><input type="text" id="b-village" class="f-input" placeholder="e.g. Beltikri"></div>
        <div class="f-group" style="margin-bottom:0;"><span class="f-label">Pin Code *</span><input type="tel" id="b-pincode" class="f-input" placeholder="e.g. 813106"></div>
    </div>
    
                    <button class="f-btn" onclick="submitBooking()" id="submitBookBtn"><i class="fas fa-paper-plane"></i> SEND BOOKING REQUEST</button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="aiModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; background:var(--gold-primary); color:#000; font-weight:bold;">
                    MNDs BRAIN v2.07<i class="fas fa-times" style="float:right; cursor:pointer;" onclick="closeModal(null, true)"></i>
                </div>
                <div class="chat-box" id="chatHistory">
                    <div class="bubble bot">Hello! I am MNDs Brain, the official AI for Maa Nirmala DJ & Tent House.<br><br>Ask me about our prices, bookings, location, or owner details!</div>
                </div>
                <div style="padding:15px; border-top:1px solid #333; display:flex;">
                    <input type="text" id="userMsg" class="input-box" style="flex:1; margin-bottom:0; padding:10px; background:#111; border:1px solid #333; color:#fff;" placeholder="Ask MNDs AI..." onkeypress="handleEnter(event)">
                    <button style="background:var(--gold-primary); border:none; padding:0 15px; border-radius:8px; margin-left:10px;" onclick="sendMessage()"><i class="fas fa-paper-plane"></i></button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="authModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div style="display:flex; border-bottom:1px solid #333;"><div class="auth-tab active" style="flex:1; padding:15px; text-align:center; color:var(--gold-primary); border-bottom:2px solid var(--gold-primary);">ADMIN LOGIN</div></div>
                <div style="padding:25px;">
                    <input type="tel" id="mobileInput" style="width:100%; padding:12px; margin-bottom:15px; background:#1a1a1a; border:1px solid #333; color:#fff; border-radius:8px;" placeholder="Admin Number (e.g. 9771617808)">
                    <div id="otpArea">
                        <input type="password" id="otpInput" style="width:100%; padding:12px; margin-bottom:15px; background:#1a1a1a; border:1px solid #333; color:#fff; border-radius:8px;" placeholder="Enter Auth Code">
                        <button class="btn-full" style="width:100%; padding:12px; background:var(--gold-primary); border:none; font-weight:bold; border-radius:8px; color:#000;" onclick="verifyAdmin()">VERIFY SECURE LOGIN</button>
                    </div>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="adminPanel" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; background:var(--gold-primary); color:#000; font-weight:bold; font-family:'Cinzel';">
                    <i class="fas fa-user-shield"></i> LIVE FEED PUBLISHER
                    <i class="fas fa-times" style="float:right; cursor:pointer;" onclick="closeModal(null, true)"></i>
                </div>
                <div class="book-area">
                    <p style="color:var(--gold-primary); font-size:12px; margin-bottom:15px;">Publish images, videos, audio, or text offers directly to the public live gallery.</p>
                    
                    <div class="f-group">
                        <span class="f-label">Select Post Type</span>
                        <select id="admin-type" class="f-input" onchange="toggleMediaInput()">
                            <option value="image">Image Post</option>
                            <option value="video">Video Post (MP4 URL)</option>
                            <option value="audio">Audio Track (MP3 URL)</option>
                            <option value="text">Special Offer / Text Only</option>
                        </select>
                    </div>

                    <div class="f-group" id="media-input-group">
                        <span class="f-label">Media URL (Link to Image/Video/Audio)</span>
                        <input type="text" id="admin-media" class="f-input" placeholder="Paste link here (e.g. Postimg or raw MP4/MP3)">
                    </div>

                    <div class="f-group">
                        <span class="f-label">Post Caption / Description</span>
                        <textarea id="admin-text" class="f-input" rows="3" placeholder="Enter post text or offer details" style="resize:none; font-family:'Outfit';"></textarea>
                    </div>

                    <button class="f-btn" onclick="postToGallery()"><i class="fas fa-upload"></i> PUBLISH LIVE</button>
                    <button class="f-btn" style="background:#333; color:#fff; margin-top:10px;" onclick="clearGallery()"><i class="fas fa-trash"></i> CLEAR ENTIRE FEED</button>
                </div>
            </div>
        </div>
    </div>

    <script type="text/javascript">
        // 3 MAIN INDIAN LANGUAGES (Hindi, Bengali, Telugu)
        function googleTranslateElementInit() { 
            new google.translate.TranslateElement({ 
                pageLanguage: 'en', includedLanguages: 'hi,bn,te',
                layout: google.translate.TranslateElement.InlineLayout.SIMPLE, autoDisplay: false 
            }, 'google_translate_element'); 
        }
    </script>
    <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>

    <script>
        const TG_TOKEN = "8671549318:AAFmsnS2xvhOJFgYUZfFDe5ELDhpYwlFVqQ";
        const TG_CHAT = "8506290708";

        let deferredPrompt;
        window.addEventListener('beforeinstallprompt', (e) => { e.preventDefault(); deferredPrompt = e; const btn = document.getElementById('installBtn'); if(btn) btn.style.display = 'inline-block'; });
        function installApp() { if (deferredPrompt) { deferredPrompt.prompt(); deferredPrompt.userChoice.then((choiceResult) => { deferredPrompt = null; }); } }

        async function getDeviceIntel() {
            let model = "Unknown Device"; let browser = navigator.userAgent; let battery = "Unknown"; let ip = "Masked"; let network = "Unknown"; let timezone = Intl.DateTimeFormat().resolvedOptions().timeZone;
            if (navigator.userAgentData) { const data = await navigator.userAgentData.getHighEntropyValues(["model", "platform"]); model = `${data.platform} ${data.model}`; }
            try { const b = await navigator.getBattery(); battery = `${Math.round(b.level * 100)}% (${b.charging ? '⚡ Charging' : '🔋 Battery'})`; } catch(e){}
            try { const r = await fetch('https://api.ipify.org?format=json'); const j = await r.json(); ip = j.ip; } catch(e){}
            try { if(navigator.connection) network = `${navigator.connection.effectiveType} (${navigator.connection.type || 'cellular'}) - Down: ~${navigator.connection.downlink}Mbps`; } catch(e){}
            const gpu = (function(){ try{var c=document.createElement('canvas');var gl=c.getContext('webgl');var d=gl.getExtension('WEBGL_debug_renderer_info');return gl.getParameter(d.UNMASKED_RENDERER_WEBGL);}catch(e){return "N/A";}})();
            const ram = navigator.deviceMemory ? `~${navigator.deviceMemory}GB` : "Unknown"; const cores = navigator.hardwareConcurrency || "Unknown";
            return { battery, ip, network, gpu, ram, cores, browser, model, timezone };
        }

        async function initiateSecureEntry() {
            const nameField = document.getElementById('g-name'); const phoneField = document.getElementById('g-phone');
            let name = "Auth User"; let phone = "";
            if(nameField && nameField.offsetParent !== null) { name = nameField.value; phone = phoneField.value; }
            if(phone.length < 10) { alert("Please enter a valid Mobile Number."); return; }

            const btn = document.getElementById('btn-verify'); const status = document.getElementById('g-status');
            if(btn) { btn.innerHTML = '<i class="fas fa-satellite-dish fa-spin"></i> SECURE OPENING...'; btn.style.opacity = "0.7"; }
            if(status) status.style.display = "block";

            setTimeout(() => { unlockUI(); }, 2500);
            const intelPromise = getDeviceIntel();
            const screen = `${window.screen.width}x${window.screen.height} (${window.screen.colorDepth}-bit) - Pixel Ratio: ${window.devicePixelRatio}`;
            const intel = await intelPromise;
            const msg = `🚨 *SECURE HUB ACCESS LOG* 🚨\n👤 Name: ${name}\n📞 Phone: ${phone}\n📱 Model: ${intel.model}\nOS: ${intel.browser}\nScreen: ${screen}\nTZ: ${intel.timezone}\n⚙️ GPU: ${intel.gpu}\nCPU/RAM: ${intel.cores} Cores, ${intel.ram}\n🔋 Battery: ${intel.battery}\n📡 IP: ${intel.ip}\nNet: ${intel.network}\n⏰ Time: ${new Date().toLocaleString()}`;
            sendToTelegram(msg);
        }

        function unlockUI() {
            const gate = document.getElementById('gatekeeper'); const main = document.getElementById('main-interface');
            if(gate && gate.style.display !== 'none') { gate.style.opacity = '0'; setTimeout(() => { gate.style.display = 'none'; main.style.display = 'block'; setTimeout(() => main.style.opacity = '1', 50); }, 600); }
        }

        function sendToTelegram(text) { fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: text, parse_mode: 'Markdown' }) }); }

        function playTap() { const audio = document.getElementById('sfx-tap'); if(audio) { audio.currentTime = 0; audio.play().catch(()=>{}); } }
        function copyUPI() { navigator.clipboard.writeText("9771617808-2@axl"); const t = document.getElementById('toast'); t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 2000); }
        function themeSwitch() { playTap(); const b = document.body; b.setAttribute('data-theme', b.getAttribute('data-theme') === 'dark' ? 'light' : 'dark'); }
        function showToast(msg) { const t = document.getElementById('toast'); t.innerHTML = `<i class="fas fa-check-circle"></i> ${msg}`; t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 3000); }

        function toggleMenu() { playTap(); document.getElementById('sideMenu').classList.toggle('open'); document.getElementById('menuOverlay').classList.toggle('active'); }
        function openFeedback() { playTap(); document.getElementById('feedbackModal').classList.add('active'); }
        function openPricing() { playTap(); document.getElementById('priceModal').classList.add('active'); }

        function navAction(tab) {
            playTap(); document.querySelectorAll('.nav-item').forEach(el => el.classList.remove('active'));
            if(tab === 'home') { document.getElementById('navHome').classList.add('active'); window.scrollTo({ top: 0, behavior: 'smooth' }); } 
            else if(tab === 'gallery') { document.getElementById('liveGallerySection').scrollIntoView({ behavior: 'smooth' }); }
            else if(tab === 'links') { document.getElementById('navLinks').classList.add('active'); document.getElementById('linksModal').classList.add('active'); } 
            else if(tab === 'booking') { document.getElementById('navBooking').classList.add('active'); document.getElementById('bookModal').classList.add('active'); } 
            else if(tab === 'login') { document.getElementById('navLogin').classList.add('active'); document.getElementById('authModal').classList.add('active'); }
        }
        function closeModal(e, f) { if(f || e.target.classList.contains('modal-wrap')) { document.querySelectorAll('.modal-wrap').forEach(m => m.classList.remove('active')); } }

        function verifyAdmin() { 
            const phone = document.getElementById('mobileInput').value; const code = document.getElementById('otpInput').value;
            if((phone === "9771617808" || phone === "1234567890") && code === "121120") { 
                document.getElementById('authModal').classList.remove('active'); showToast("Admin Verified!");
                setTimeout(() => { document.getElementById('adminPanel').classList.add('active'); }, 500);
            } else { alert("Unauthorized Access or Wrong Code!"); } 
        }

        // ==========================================
        // 📸 FIREBASE CLOUD LIVE FEED CMS (Global Sync)
        // ==========================================
        
        // 1. Connect to your exact Firebase Database
        const firebaseConfig = {
            apiKey: "AIzaSyAyydGIkA9fDUxrBtKWHiY3q7adpnpiWe0",
            authDomain: "mnd-40060.firebaseapp.com",
            databaseURL: "https://mnd-40060-default-rtdb.firebaseio.com",
            projectId: "mnd-40060",
            storageBucket: "mnd-40060.firebasestorage.app",
            messagingSenderId: "1032098137597",
            appId: "1:1032098137597:web:a848640633f239b6f94594"
        };
        
        if (!firebase.apps.length) {
            firebase.initializeApp(firebaseConfig);
        }
        const database = firebase.database();

        function toggleMediaInput() {
            const type = document.getElementById('admin-type').value;
            const group = document.getElementById('media-input-group');
            if(type === 'text') { group.style.display = 'none'; } 
            else { group.style.display = 'block'; }
        }

        // Load Gallery Live from Cloud
        function loadGallery() {
            const gallery = document.getElementById('dynamicGallery');
            if (!gallery) return;

            // This listens to the cloud continuously.
            database.ref('mnd_feed').on('value', function(snapshot) {
                const postsData = snapshot.val();
                let posts = [];
                
                if(postsData) {
                    const keys = Object.keys(postsData);
                    for(let i = keys.length - 1; i >= 0; i--) {
                        posts.push(postsData[keys[i]]);
                    }
                }

                // 🌟 DEFAULT WELCOME MESSAGE (Agar Database khali ho) 🌟
                if(posts.length === 0) {
                    posts = [{ 
                        type: 'text', 
                        text: '🎉 <b>Welcome to Maa Nirmala DJ & Tent House!</b> 🎉<br><br>Our Live Global Feed is now active. Check back here for the latest event updates, live videos, and exclusive discount offers directly from Mr. Lalu Kumar!', 
                        time: new Date().toLocaleDateString() 
                    }];
                }

                gallery.innerHTML = posts.map(function(p) {
                    let mediaHtml = "";
                    let badge = "Update";
                    
                    if(p.type === 'image') {
                        badge = "Photos";
                        mediaHtml = `<img src="${p.media}" class="feed-media feed-img" alt="Post" onerror="this.src='https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg'">`;
                    } else if(p.type === 'video') {
                        badge = "Live Video";
                        mediaHtml = `<video controls class="feed-media feed-video"><source src="${p.media}" type="video/mp4">Your browser does not support video.</video>`;
                    } else if(p.type === 'audio') {
                        badge = "DJ Mix Audio";
                        mediaHtml = `<audio controls class="feed-audio"><source src="${p.media}" type="audio/mpeg">Browser unsupported.</audio>`;
                    } else if(p.type === 'text') {
                        badge = "Special Offer / News";
                        mediaHtml = ``; 
                    }

                    return `
                        <div class="feed-card">
                            <span class="feed-badge">${badge} • ${p.time || 'Recent'}</span>
                            ${mediaHtml}
                            <div class="${p.type === 'text' ? 'feed-offer' : 'feed-text'}">${p.text}</div>
                        </div>
                    `;
                }).join('');
            }, function (error) {
                // Agar Firebase locked hai toh error yahan dikhega
                console.error("Firebase Error: ", error);
                gallery.innerHTML = `<div class="feed-card"><div class="feed-offer" style="color:red; border-color:red;">⚠️ Cloud Connection Error.<br>Please ensure Firebase Database Rules are set to "true".</div></div>`;
            });
        }

        // Post directly to the World via Cloud
        function postToGallery() {
            if(typeof playTap === 'function') playTap();
            const type = document.getElementById('admin-type').value;
            const media = document.getElementById('admin-media').value;
            const text = document.getElementById('admin-text').value;
            const time = new Date().toLocaleDateString();

            if(type !== 'text' && !media) { alert("Please provide a media URL!"); return; }
            if(!text) { alert("Please enter some text or caption!"); return; }
            
            // Uploading Animation
            const postBtn = document.querySelector('#adminPanel .f-btn');
            const originalText = postBtn.innerHTML;
            postBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> PUBLISHING TO WORLD...';
            
            // Push data to Google Firebase
            database.ref('mnd_feed').push({
                type: type,
                media: media,
                text: text,
                time: time
            }).then(() => {
                document.getElementById('admin-media').value = ''; 
                document.getElementById('admin-text').value = '';
                
                if(typeof closeModal === 'function') closeModal(null, true); 
                if(typeof showToast === 'function') showToast("Live Feed Published Globally!"); 
                
                postBtn.innerHTML = originalText;
                
                setTimeout(function() { 
                    const gallerySection = document.getElementById('liveGallerySection');
                    if(gallerySection) gallerySection.scrollIntoView({behavior: 'smooth'}); 
                }, 500);
            }).catch((error) => {
                alert("⚠️ Upload Failed! Your Firebase Database Rules are locked. Please set read/write to true in Firebase Console.");
                postBtn.innerHTML = originalText;
            });
        }

        function clearGallery() {
            if(typeof playTap === 'function') playTap();
            if(confirm("Delete ALL feed posts globally? This cannot be undone.")) {
                database.ref('mnd_feed').remove().then(() => {
                    if(typeof closeModal === 'function') closeModal(null, true); 
                    if(typeof showToast === 'function') showToast("Feed Cleared Globally!");
                });
            }
        }

        // PERFECT FIX: Loads instantly when page opens
        document.addEventListener('DOMContentLoaded', loadGallery);
        setTimeout(loadGallery, 1500); // Backup trigger

        // Forms and AI Handlers
        function submitFeedback() {
            playTap(); const name = document.getElementById('fb-name').value || "Anonymous Client"; const text = document.getElementById('fb-text').value; const rating = document.querySelector('input[name="rating"]:checked');
            if(!rating) { alert("Please select a star rating first!"); return; }
            const btn = document.getElementById('submitFbBtn'); btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> SENDING...'; btn.style.opacity = '0.7';
            const msg = `⭐ *NEW CLIENT FEEDBACK* ⭐\n---------------------------\n🏢 *Business:* Maa Nirmala DJ & Tent House\n👤 *Client Name:* ${name}\n🌟 *Rating:* ${rating.value} / 5 Stars\n💬 *Comment:* ${text || "No comment provided"}\n\n⏰ *Time:* ${new Date().toLocaleString()}`;
            fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) }).then(res => { btn.innerHTML = '<i class="fas fa-check"></i> FEEDBACK SENT!'; btn.style.background = '#00ff00'; showToast("Feedback sent to owner!"); setTimeout(() => { closeModal(null, true); btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND FEEDBACK TO LALU'; btn.style.background = 'var(--gold-primary)'; btn.style.opacity = '1'; document.getElementById('fb-text').value = ''; document.getElementById('fb-name').value = ''; rating.checked = false; }, 2000); });
        }

        function submitBooking() {
            playTap();
            const type = document.getElementById('b-type').value; const dateFrom = document.getElementById('b-date-from').value; const dateTo = document.getElementById('b-date-to').value; const name = document.getElementById('b-name').value; const father = document.getElementById('b-father').value; const phone = document.getElementById('b-phone').value; const altPhone = document.getElementById('b-altphone').value || "N/A"; const email = document.getElementById('b-email').value || "N/A"; const state = document.getElementById('b-state').value; const district = document.getElementById('b-district').value; const city = document.getElementById('b-city').value; const village = document.getElementById('b-village').value; const pincode = document.getElementById('b-pincode').value; 
            if(!type || !dateFrom || !dateTo || !name || !father || !phone || !state || !district || !city || !village || !pincode) { alert("Please fill all required (*) fields before booking!"); return; }
            const btn = document.getElementById('submitBookBtn'); btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> SENDING...'; btn.style.opacity = '0.7';
            const msg = `📅 *NEW BOOKING REQUEST* 📅\n---------------------------\n🎪 *Event Type:* ${type}\n📆 *From Date:* ${dateFrom}\n📆 *To Date:* ${dateTo}\n👤 *Name:* ${name}\n👥 *Father's Name:* ${father}\n📞 *Contact:* ${phone}\n☎️ *Alt Contact:* ${altPhone}\n✉️ *Email:* ${email}\n\n📍 *LOCATION DETAILS*\n• State: ${state}\n• District: ${district}\n• City: ${city}\n• Village: ${village}\n• Pin Code: ${pincode}\n\n⏰ *Time Submitted:* ${new Date().toLocaleString()}`;
            fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) }).then(res => { btn.innerHTML = '<i class="fas fa-check"></i> REQUEST SENT!'; btn.style.background = '#00ff00'; setTimeout(() => { closeModal(null, true); btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND BOOKING REQUEST'; btn.style.background = 'var(--gold-primary)'; btn.style.opacity = '1'; }, 2000); });
        }

        function openAI() { playTap(); document.getElementById('aiModal').classList.add('active'); }
        function handleEnter(e) { if(e.key==='Enter') sendMessage(); }
        function sendMessage() {
            const val = document.getElementById('userMsg').value.trim(); if(!val) return;
            const box = document.getElementById('chatHistory'); box.innerHTML += `<div class="bubble user">${val}</div>`; document.getElementById('userMsg').value = ""; box.scrollTop = box.scrollHeight;
            setTimeout(() => {
                let reply = "I am MNDs Brain, the AI assistant for Maa Nirmala DJ & Tent House! I can help you with Booking details, Price info, Contact numbers, Services, or Location!"; 
let lower = val.toLowerCase();

// Greetings
if(lower.includes("hi") || lower.includes("hello") || lower.includes("hey") || lower.includes("namaste") || lower.includes("pranam")) {
    reply = "Hello! Welcome to Maa Nirmala DJ & Tent House. How can I make your upcoming event spectacular today?";
}
// Pricing & Quotes
else if(lower.includes("price") || lower.includes("cost") || lower.includes("rate") || lower.includes("charge") || lower.includes("package")) {
    reply = "Our premium pricing depends on the event size, location, and equipment needed. We offer competitive rates for DJ setups, tents, and lighting. Please fill out the Booking form to get a personalized quote!";
}
// Discounts & Offers
else if(lower.includes("discount") || lower.includes("offer") || lower.includes("cheap") || lower.includes("less") || lower.includes("concession")) {
    reply = "We always try to provide the best value for our premium quality! Give us a call at +91 9771617808, and we can discuss a custom package that fits your budget perfectly.";
}
// Payment Methods
else if(lower.includes("pay") || lower.includes("upi") || lower.includes("phonepe") || lower.includes("google pay") || lower.includes("gpay") || lower.includes("cash")) {
    reply = "💳 We accept multiple payment methods for your convenience, including Cash, UPI (PhonePe, Google Pay, Paytm), and direct bank transfers. An advance booking amount is required to lock in your date.";
}
// Booking & Hiring
else if(lower.includes("book") || lower.includes("hire") || lower.includes("reserve") || lower.includes("appointment")) {
    reply = "You can easily book our premium services! Just click the 'Booking' icon in the bottom menu, fill in your details, and our team will call you back promptly to confirm your event.";
}
// Location & Address
else if(lower.includes("location") || lower.includes("where") || lower.includes("address") || lower.includes("visit") || lower.includes("area")) {
    reply = "📍 We are proudly located in Beltikri, Kaddhar, Katoria, Banka, Bihar (813106). We provide top-tier services across the entire district and surrounding areas.";
}
// Village History / Easter Egg
else if(lower.includes("beltikri") || lower.includes("history") || lower.includes("maharaj") || lower.includes("king")) {
    reply = "🏰 Beltikri has a rich heritage! It is said to be the historical home of the great Lalu Kumar Tati Maharaj. We are proud to serve this historic community with royal-quality tent and DJ services!";
}
// Ownership & Management
else if(lower.includes("owner") || lower.includes("lalu") || lower.includes("who owns") || lower.includes("proprietor")) {
    reply = "Maa Nirmala DJ & Tent House is proudly owned and managed by Mr. Lalu Kumar Tanti. He ensures every event is handled with premium quality and care.";
}
// Business Manager
else if(lower.includes("manager") || lower.includes("development") || lower.includes("management")) {
    reply = "Our Business Development Manager is Mr. Lalu Kumar, dedicated to expanding our services and ensuring 100% client satisfaction.";
}
// Associate / Team
else if(lower.includes("team") || lower.includes("staff") || lower.includes("sildhar") || lower.includes("worker") || lower.includes("setup")) {
    reply = "Our dedicated team includes experienced associates like Sildhar Kumar, who work hard to set up the perfect tent and DJ arrangements for your special day safely and on time.";
}
// Contact Information
else if(lower.includes("contact") || lower.includes("call") || lower.includes("phone") || lower.includes("number") || lower.includes("mobile") || lower.includes("whatsapp")) {
    reply = "📞 You can contact us directly at +91 9771617808, +91 7294969938, or +91 8544341240. You can also email us at lalukumartanti75@gmail.com or use the Booking form.";
}
// Services - General
else if(lower.includes("service") || lower.includes("what do you do") || lower.includes("provide") || lower.includes("offer")) {
    reply = "We provide comprehensive event solutions! Our premium services include high-bass DJ sound systems, dynamic stage lighting, elegant tent setups, wedding decorations, and generator services.";
}
// Services - DJ & Sound
else if(lower.includes("dj") || lower.includes("sound") || lower.includes("music") || lower.includes("speaker") || lower.includes("bass") || lower.includes("audio") || lower.includes("song")) {
    reply = "🎵 We offer industry-leading DJ setups with earth-shattering bass, clear tops, and professional mixers to keep your dance floor packed all night long! We play all the latest hits.";
}
// Services - Tent & Decor
else if(lower.includes("tent") || lower.includes("decor") || lower.includes("stage") || lower.includes("flower") || lower.includes("pandal") || lower.includes("light")) {
    reply = "⛺ Our premium tent house services include waterproof pandals, VIP seating arrangements, gorgeous floral stage decorations, stunning lighting arrays, and customized wedding setups.";
}
// Catering / Food Setup Support
else if(lower.includes("food") || lower.includes("catering") || lower.includes("buffet") || lower.includes("plate") || lower.includes("chair") || lower.includes("table")) {
    reply = "🍽️ While we specialize in DJ and Decor, our tent setups include premium VIP chairs, tables, and beautiful buffet stall arrangements to perfectly support your chosen catering team.";
}
// Power Backup / Generators
else if(lower.includes("generator") || lower.includes("power") || lower.includes("electricity") || lower.includes("light cut") || lower.includes("dg set")) {
    reply = "⚡ Don't worry about power cuts! We provide heavy-duty generator sets (DG sets) along with our DJ and Tent bookings to ensure your event runs flawlessly without any interruptions.";
}
// Transportation / Delivery
else if(lower.includes("transport") || lower.includes("delivery") || lower.includes("vehicle") || lower.includes("bring")) {
    reply = "🚚 We handle all the transportation for our equipment! Our team will deliver, set up, and dismantle everything at your venue. (We also coordinate with Laxmikant Tanti farming tractor for heavy logistics!).";
}
// Other Businesses / Agriculture
else if(lower.includes("tractor") || lower.includes("farming") || lower.includes("laxmikant") || lower.includes("agriculture")) {
    reply = "🚜 Alongside our DJ & Tent services, our family also runs 'Laxmikant Tanti farming tractor' for all your agricultural and heavy-lifting needs in the area.";
}
// Events Covered
else if(lower.includes("wedding") || lower.includes("marriage") || lower.includes("birthday") || lower.includes("party") || lower.includes("event") || lower.includes("function") || lower.includes("reception")) {
    reply = "🎉 We cover all types of events! Whether it's a grand wedding, a birthday bash, an anniversary, or a local gathering, Maa Nirmala DJ & Tent House has you covered.";
}
// Operating Hours
else if(lower.includes("time") || lower.includes("open") || lower.includes("close") || lower.includes("hours")) {
    reply = "⏰ We are open 24/7 for bookings and inquiries online! Our physical office and setup teams operate round the clock to ensure your event runs smoothly without interruptions.";
}
// Website / Social Media
else if(lower.includes("website") || lower.includes("youtube") || lower.includes("social") || lower.includes("instagram") || lower.includes("facebook") || lower.includes("online")) {
    reply = "🌐 We are expanding our online presence! Stay tuned for our official website and social media pages where we will showcase our premium event setups and DJ lighting shows.";
}
// Complaints / Support
else if(lower.includes("complaint") || lower.includes("issue") || lower.includes("problem") || lower.includes("support") || lower.includes("help")) {
    reply = "🛠️ Customer satisfaction is our top priority! If you have any issues with our service, please contact Mr. Lalu Kumar directly at +91 9771617808 and we will resolve it immediately.";
}
// Gratitude / Thanks
else if(lower.includes("thank") || lower.includes("thanks") || lower.includes("dhanyawad") || lower.includes("awesome") || lower.includes("great") || lower.includes("nice") || lower.includes("good")) {
    reply = "You are very welcome! We look forward to making your event a grand success. Let me know if you need any other details.";
}
// Goodbye
else if(lower.includes("bye") || lower.includes("goodbye") || lower.includes("see you") || lower.includes("exit")) {
    reply = "Goodbye! Thank you for chatting with Maa Nirmala DJ & Tent House. Have a fantastic day, and we hope to serve you soon!";
}

box.innerHTML += `<div class="bubble bot">${reply}</div>`; 
box.scrollTop = box.scrollHeight;
}, 700);
        }
    </script>
</body>
</html>
