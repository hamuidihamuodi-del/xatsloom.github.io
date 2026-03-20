<html lang="es"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Maria</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
    <script src="https://unpkg.com/@phosphor-icons/web"></script><link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.2/src/regular/style.css"><link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.2/src/thin/style.css"><link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.2/src/light/style.css"><link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.2/src/bold/style.css"><link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.2/src/fill/style.css"><link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.2/src/duotone/style.css">
    
    <style>
        :root {
            --rose-gold: #E5A999;
            --rose-gold-light: #F4C7BB;
            --rose-gold-dark: #C2806E;
            --bg-dark: rgba(18, 9, 12, 0.85);
            --text-light: #FFFFFF;
            --text-muted: #BDBDBD;
            --gold-1: #BF953F;
            --gold-2: #FCF6BA;
            --gold-3: #B38728;
            --gold-4: #FBF5B7;
            --gold-5: #AA771C;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
        }

        img {
            -webkit-user-drag: none;
            -khtml-user-drag: none;
            -moz-user-drag: none;
            -o-user-drag: none;
            user-drag: none;
        }

        ::-webkit-scrollbar {
            width: 10px;
            height: 10px;
        }
        ::-webkit-scrollbar-track {
            background: rgba(18, 9, 12, 0.9);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--rose-gold-dark);
            border-radius: 5px;
            border: 2px solid rgba(18, 9, 12, 0.9);
        }
        ::-webkit-scrollbar-thumb:hover {
            background: var(--rose-gold-light);
        }

        body {
            background: linear-gradient(135deg, #fbc2eb 0%, #a6c1ee 0%, #fbc2eb 50%, #e198b4 100%);
            background-size: 200% 200%;
            animation: gradientBG 15s ease infinite;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
            position: relative;
            overflow-x: hidden;
            overflow-y: auto;
        }

        body.intro-active {
            overflow: hidden;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        #intro-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(251, 194, 235, 0.6);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            z-index: 9999;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: opacity 0.8s ease, visibility 0.8s ease;
        }

        #intro-screen.hidden {
            opacity: 0;
            visibility: hidden;
        }

        .access-card {
            background: rgba(18, 9, 12, 0.95);
            border: 2px solid rgba(212, 175, 55, 0.4);
            border-radius: 20px;
            padding: 40px;
            width: 90%;
            max-width: 420px;
            display: flex;
            flex-direction: column;
            align-items: center;
            box-shadow: 0 30px 60px rgba(0,0,0,0.4), inset 0 0 20px rgba(212, 175, 55, 0.1);
            position: relative;
            transform: translateY(0) scale(1);
            transition: transform 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }

        #intro-screen.hidden .access-card {
            transform: translateY(-50px) scale(0.95);
        }

        .card-hole {
            width: 60px;
            height: 12px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            margin-top: -20px;
            margin-bottom: 30px;
            box-shadow: inset 0 3px 6px rgba(0,0,0,0.8);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .access-profile {
            display: flex;
            align-items: center;
            gap: 25px;
            margin-bottom: 40px;
            width: 100%;
            justify-content: center;
        }

        .access-photo {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--gold-1);
            box-shadow: 0 0 25px rgba(212, 175, 55, 0.4);
        }

        .access-name {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--gold-1), var(--gold-2), var(--gold-3), var(--gold-4), var(--gold-5));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 2px;
            filter: drop-shadow(0 2px 4px rgba(0,0,0,0.5));
        }

        .access-btn {
            background: linear-gradient(135deg, var(--gold-2) 0%, var(--gold-1) 50%, var(--gold-3) 100%);
            color: #111;
            border: none;
            padding: 14px 40px;
            border-radius: 30px;
            font-size: 1.1rem;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 3px;
            box-shadow: 0 5px 20px rgba(179, 135, 40, 0.5);
            width: 100%;
            justify-content: center;
        }

        .access-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 30px rgba(179, 135, 40, 0.7);
            filter: brightness(1.1);
        }

        .main-card {
            background: var(--bg-dark);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(229, 169, 153, 0.3);
            border-radius: 40px;
            width: 100%;
            max-width: 1200px;
            min-height: 700px;
            display: flex;
            position: relative;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
        }

        .card-bg-graphics {
            position: absolute;
            top: 0;
            right: 15%;
            height: 100%;
            width: 50%;
            background-image: 
                radial-gradient(circle at 50% -20%, transparent 60%, rgba(229, 169, 153, 0.1) 61%, rgba(229, 169, 153, 0.1) 65%, transparent 66%),
                radial-gradient(circle at 70% -10%, transparent 60%, rgba(229, 169, 153, 0.05) 61%, rgba(229, 169, 153, 0.05) 65%, transparent 66%);
            pointer-events: none;
            z-index: 0;
        }

        .content-left {
            flex: 1;
            padding: 5rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            z-index: 2;
        }

        .site-title {
            font-family: 'Montserrat', sans-serif;
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, var(--rose-gold-light) 0%, var(--rose-gold-dark) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
            letter-spacing: -1px;
            text-shadow: 0 4px 15px rgba(229, 169, 153, 0.2);
        }

        .about-wrapper {
            margin-top: 1.5rem;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            width: 100%;
        }

        .about-btn {
            background: linear-gradient(135deg, rgba(229, 169, 153, 0.15) 0%, rgba(229, 169, 153, 0.05) 100%);
            border: 1px solid rgba(229, 169, 153, 0.4);
            color: var(--rose-gold-light);
            padding: 0 25px;
            height: 45px;
            line-height: 43px;
            border-radius: 30px;
            font-size: 0.85rem;
            font-weight: 600;
            letter-spacing: 2px;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            overflow: hidden;
            opacity: 1;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .about-btn:hover {
            background: rgba(229, 169, 153, 0.25);
            border-color: var(--rose-gold);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(229, 169, 153, 0.2);
        }

        .about-btn.hide {
            height: 0;
            opacity: 0;
            border-width: 0;
            margin: 0;
            transform: translateY(-10px);
            pointer-events: none;
        }

        .about-content-wrapper {
            display: grid;
            grid-template-rows: 0fr;
            transition: grid-template-rows 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            width: 100%;
            max-width: 450px;
        }

        .about-content-wrapper.show {
            grid-template-rows: 1fr;
        }

        .about-card {
            overflow: hidden;
            background: rgba(18, 9, 12, 0.5);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(229, 169, 153, 0.2);
            border-radius: 20px;
            opacity: 0;
            transform: translateY(-15px);
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 15px 35px rgba(0,0,0,0.3);
        }

        .about-content-wrapper.show .about-card {
            opacity: 1;
            transform: translateY(0);
        }

        .about-card-inner {
            padding: 22px 25px;
            position: relative;
        }

        .about-close {
            position: absolute;
            top: 15px;
            right: 18px;
            background: transparent;
            border: none;
            color: var(--text-muted);
            font-size: 1.2rem;
            cursor: pointer;
            transition: color 0.3s ease, transform 0.3s ease;
            padding: 5px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .about-close:hover {
            color: var(--rose-gold-light);
            transform: scale(1.1) rotate(90deg);
        }

        .about-row {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .about-icon {
            height: 24px;
            width: auto;
            border-radius: 4px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.4);
        }

        .about-text {
            font-size: 1.2rem;
            color: #fff;
            font-weight: 500;
            letter-spacing: 1px;
        }

        .about-quote-box {
            border-left: 3px solid var(--rose-gold);
            padding-left: 15px;
            margin-bottom: 18px;
        }

        .about-quote-box p {
            font-size: 1.05rem;
            font-style: italic;
            color: var(--rose-gold-light);
            line-height: 1.6;
            font-weight: 300;
            margin: 0;
        }

        .content-right {
            flex: 1;
            position: relative;
            z-index: 1;
        }

        .hero-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top center;
            mask-image: linear-gradient(to right, transparent 0%, black 30%), linear-gradient(to top, transparent 0%, black 20%);
            -webkit-mask-image: 
                linear-gradient(to right, transparent 0%, black 25%), 
                linear-gradient(to top, transparent 0%, black 30%);
            -webkit-mask-composite: source-in;
            mask-composite: intersect;
        }

        .player-placeholder {
            display: none;
            width: 100%;
            max-width: 550px;
            margin-top: 3rem;
            height: 95px;
        }

        .music-player {
            margin-top: 3rem;
            background: rgba(18, 9, 12, 0.7);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid rgba(229, 169, 153, 0.3);
            border-radius: 24px;
            padding: 15px 45px 15px 25px;
            display: flex;
            align-items: center;
            gap: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.4), inset 0 0 0 1px rgba(255,255,255,0.05);
            width: 100%;
            max-width: 550px;
            position: relative;
            transition: all 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            transform-origin: center;
        }

        .music-player:hover:not(.minimized) {
            background: rgba(18, 9, 12, 0.85);
            transform: translateY(-5px);
        }

        .minimize-btn {
            position: absolute;
            top: 15px;
            right: 20px;
            background: transparent;
            border: none;
            color: var(--text-muted);
            font-size: 1.2rem;
            cursor: pointer;
            transition: color 0.3s ease, transform 0.3s ease;
            z-index: 10;
        }

        .minimize-btn:hover {
            color: var(--rose-gold-light);
            transform: scale(1.2);
        }

        .music-player.is-fixed {
            position: fixed;
            margin-top: 0 !important;
            z-index: 9000;
        }

        .music-player.minimized {
            width: 75px !important;
            max-width: 75px !important;
            height: 75px !important;
            padding: 0 !important;
            border-radius: 50% !important;
            bottom: 30px !important;
            left: 30px !important;
            top: auto !important;
            cursor: pointer;
            box-shadow: 0 15px 35px rgba(0,0,0,0.6), 0 0 0 2px var(--rose-gold) !important;
        }

        .music-player.minimized .player-info,
        .music-player.minimized .player-controls,
        .music-player.minimized .minimize-btn,
        .music-player.minimized audio {
            opacity: 0 !important;
            visibility: hidden !important;
            pointer-events: none;
            position: absolute;
        }

        .player-cover {
            width: 65px;
            height: 65px;
            border-radius: 14px;
            object-fit: cover;
            box-shadow: 0 5px 15px rgba(0,0,0,0.4);
            transition: all 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            position: relative;
        }

        .music-player.minimized .player-cover {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            margin: 0;
            box-shadow: none;
            animation: spinDisc 5s linear infinite;
        }

        .music-player.minimized.paused .player-cover {
            animation-play-state: paused;
        }

        @keyframes spinDisc {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .player-info {
            display: flex;
            flex-direction: column;
            justify-content: center;
            gap: 6px;
            flex: 1;
            overflow: hidden;
            transition: opacity 0.3s;
        }

        .song-title {
            color: #fff;
            font-size: 1rem;
            font-weight: 600;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            letter-spacing: 0.5px;
        }

        .song-artist {
            color: var(--rose-gold-light);
            font-size: 0.8rem;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            opacity: 0.8;
        }

        .player-progress {
            width: 100%;
            height: 6px;
            background: rgba(255, 255, 255, 0.15);
            border-radius: 3px;
            margin-top: 6px;
            position: relative;
            cursor: pointer;
            overflow: visible;
        }

        .progress-bar {
            width: 0%;
            height: 100%;
            background: var(--rose-gold);
            border-radius: 3px;
            position: absolute;
            left: 0;
            top: 0;
        }

        .progress-bar::after {
            content: '';
            position: absolute;
            right: -6px;
            top: 50%;
            transform: translateY(-50%);
            width: 12px;
            height: 12px;
            background: #fff;
            border-radius: 50%;
            box-shadow: 0 0 8px rgba(0,0,0,0.8);
            pointer-events: none;
        }

        .player-controls {
            display: flex;
            align-items: center;
            gap: 12px;
            transition: opacity 0.3s;
        }

        .control-btn {
            background: transparent;
            border: none;
            color: var(--text-muted);
            font-size: 1.5rem;
            cursor: pointer;
            transition: color 0.2s ease, transform 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .control-btn:hover {
            color: var(--text-light);
            transform: scale(1.1);
        }

        .play-btn {
            background: linear-gradient(135deg, var(--rose-gold-light) 0%, var(--rose-gold) 100%);
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            color: #111;
            font-size: 1.4rem;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(229, 169, 153, 0.4);
        }

        .play-btn:hover {
            transform: scale(1.08);
            box-shadow: 0 8px 20px rgba(229, 169, 153, 0.6);
        }

        @media (max-width: 968px) {
            body { padding: 1rem; }
            .main-card {
                flex-direction: column-reverse;
                min-height: auto;
            }
            .content-left {
                padding: 3rem 1.5rem;
                text-align: center;
                align-items: center;
            }
            .site-title { font-size: 2.8rem; }
            
            .about-wrapper {
                align-items: center;
                margin-top: 1.5rem;
            }

            .content-right { height: 350px; }
            .hero-image {
                -webkit-mask-image: linear-gradient(to top, transparent 0%, black 40%);
                mask-image: linear-gradient(to top, transparent 0%, black 40%);
            }
            
            .music-player {
                margin-top: 2.5rem;
                margin-left: auto;
                margin-right: auto;
                padding: 12px 35px 12px 15px;
                gap: 12px;
                border-radius: 20px;
            }
            .player-placeholder { margin-top: 2.5rem; height: 85px; }
            
            .player-cover { width: 50px; height: 50px; border-radius: 10px; }
            .play-btn { width: 42px; height: 42px; font-size: 1.2rem; }
            .control-btn { font-size: 1.3rem; }
            
            .access-profile { flex-direction: column; gap: 15px; }
            .access-name { font-size: 2.5rem; }

            .music-player.minimized {
                bottom: 20px !important;
                left: 20px !important;
                width: 60px !important;
                max-width: 60px !important;
                height: 60px !important;
            }
        }
    </style>
</head>
<body class="intro-active">

    <div id="intro-screen">
        <div class="access-card">
            <div class="card-hole"></div>

            <div class="access-profile">
                <img src="https://xatimg.com/image/NGM49XVloYG1.jpg " alt="LION" class="access-photo" draggable="false">
                <div class="access-name">LION</div>
            </div>

            <button id="accessEnterBtn" class="access-btn">
                ENTER <i class="ph-bold ph-sign-in"></i>
            </button>
        </div>
    </div>

    <div class="main-card">
        <div class="card-bg-graphics"></div>
        
        <div class="content-left">
            <div class="site-title">ليون-LION</div>

            <div class="about-wrapper">
                <button class="about-btn" id="aboutBtn">
                    ABOUT ME <i class="ph-bold ph-caret-down"></i>
                </button>
                
                <div class="about-content-wrapper" id="aboutContent">
                    <div class="about-card">
                        <div class="about-card-inner">
                            <button class="about-close" id="aboutClose" title="Cerrar">
                                <i class="ph ph-x"></i>
                            </button>
                            
                            <div class="about-quote-box">
              <p>"كــن لنفســـك كل شــــئ"</p>
                            </div>


                            <div class="about-row">
                                <img src="https://xatimg.com/image/aVikypimltA3.jpg" alt="IRAQ Flag" class="about-icon" draggable="false">
                                <span class="about-text">ابن العراق </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="player-placeholder" id="playerPlaceholder"></div>

            <div class="music-player" id="musicPlayer">
                <button class="minimize-btn" id="minimizeBtn" title="Minimizar">
                    <i class="ph ph-x"></i>
                </button>

                <img src="https://xatimg.com/image/wPs8DmU8ohvO.jpg" alt="Die With A Smile" class="player-cover" draggable="false">
                
                <div class="player-info">
                    <span class="song-title">Die With A Smile</span>
                    <span class="song-artist">Lady Gaga, Bruno Mars</span>
                    <div class="player-progress" id="progressContainer">
                        <div class="progress-bar" id="progressBar"></div>
                    </div>
                </div>

                <div class="player-controls">
                    <button class="control-btn"><i class="ph-fill ph-skip-back"></i></button>
                    <button class="play-btn" id="playPauseBtn">
                        <i class="ph-fill ph-play" id="playIcon"></i>
                    </button>
                    <button class="control-btn"><i class="ph-fill ph-skip-forward"></i></button>
                </div>
                
                <audio id="audioPlayer" loop="">
                    <source src="smile.mp3" type="audio/mpeg">
                </audio>
            </div>
        </div>

        <div class="content-right">
            <img src="https://xatimg.com/image/2TOGqhK0LlpM.png" alt="LION" class="hero-image" draggable="false">
        </div>
    </div>

    <script>
        document.addEventListener('contextmenu', e => e.preventDefault());
        document.addEventListener('selectstart', e => e.preventDefault());
        document.addEventListener('dragstart', e => e.preventDefault());
        document.addEventListener('keydown', e => {
            if(e.keyCode === 123 || 
              (e.ctrlKey && e.shiftKey && (e.keyCode === 73 || e.keyCode === 74 || e.keyCode === 67)) ||
              (e.ctrlKey && (e.keyCode === 85 || e.keyCode === 83 || e.keyCode === 80 || e.keyCode === 67 || e.keyCode === 86))) {
                e.preventDefault();
                return false;
            }
        });

        const introScreen = document.getElementById('intro-screen');
        const accessEnterBtn = document.getElementById('accessEnterBtn');
        const playPauseBtn = document.getElementById('playPauseBtn');
        const playIcon = document.getElementById('playIcon');
        const audioPlayer = document.getElementById('audioPlayer');
        const progressBar = document.getElementById('progressBar');
        const progressContainer = document.getElementById('progressContainer');
        const musicPlayer = document.getElementById('musicPlayer');
        const minimizeBtn = document.getElementById('minimizeBtn');
        const playerPlaceholder = document.getElementById('playerPlaceholder');
        const aboutBtn = document.getElementById('aboutBtn');
        const aboutContent = document.getElementById('aboutContent');
        const aboutClose = document.getElementById('aboutClose');

        let isPlaying = false;
        let animationFrameId;

        aboutBtn.addEventListener('click', () => {
            aboutBtn.classList.add('hide');
            aboutContent.classList.add('show');
        });

        aboutClose.addEventListener('click', () => {
            aboutContent.classList.remove('show');
            aboutBtn.classList.remove('hide');
        });

        accessEnterBtn.addEventListener('click', () => {
            introScreen.classList.add('hidden');
            document.body.classList.remove('intro-active');

            audioPlayer.play().then(() => {
                isPlaying = true;
                playIcon.classList.remove('ph-play');
                playIcon.classList.add('ph-pause');
                musicPlayer.classList.remove('paused');
                startProgressAnimation();
            }).catch(e => {
                console.log(e);
            });
        });

        playPauseBtn.addEventListener('click', (e) => {
            e.stopPropagation();
            togglePlay();
        });

        function togglePlay() {
            if (isPlaying) {
                audioPlayer.pause();
                playIcon.classList.remove('ph-pause');
                playIcon.classList.add('ph-play');
                musicPlayer.classList.add('paused');
                cancelAnimationFrame(animationFrameId);
            } else {
                audioPlayer.play();
                playIcon.classList.remove('ph-play');
                playIcon.classList.add('ph-pause');
                musicPlayer.classList.remove('paused');
                startProgressAnimation();
            }
            isPlaying = !isPlaying;
        }

        function updateProgress() {
            if (audioPlayer.duration > 0) {
                const progressPercent = (audioPlayer.currentTime / audioPlayer.duration) * 100;
                progressBar.style.width = progressPercent + '%';
            }
            if (isPlaying) {
                animationFrameId = requestAnimationFrame(updateProgress);
            }
        }

        function startProgressAnimation() {
            cancelAnimationFrame(animationFrameId);
            animationFrameId = requestAnimationFrame(updateProgress);
        }

        progressContainer.addEventListener('click', (e) => {
            e.stopPropagation();
            const width = progressContainer.clientWidth;
            const clickX = e.offsetX;
            const duration = audioPlayer.duration;
            if (duration) {
                audioPlayer.currentTime = (clickX / width) * duration;
                if(!isPlaying) {
                    progressBar.style.width = ((clickX / width) * 100) + '%';
                }
            }
        });

        minimizeBtn.addEventListener('click', (e) => {
            e.stopPropagation();
            const rect = musicPlayer.getBoundingClientRect();
            
            playerPlaceholder.style.display = 'block';
            playerPlaceholder.style.width = rect.width + 'px';
            playerPlaceholder.style.height = rect.height + 'px';
            
            musicPlayer.classList.add('is-fixed');
            musicPlayer.style.top = rect.top + 'px';
            musicPlayer.style.left = rect.left + 'px';
            musicPlayer.style.width = rect.width + 'px';
            musicPlayer.style.height = rect.height + 'px';

            musicPlayer.offsetHeight; 
            musicPlayer.classList.add('minimized');
        });

        musicPlayer.addEventListener('click', () => {
            if (musicPlayer.classList.contains('minimized')) {
                const targetRect = playerPlaceholder.getBoundingClientRect();
                
                musicPlayer.classList.remove('minimized');

                musicPlayer.style.top = targetRect.top + 'px';
                musicPlayer.style.left = targetRect.left + 'px';
                musicPlayer.style.width = targetRect.width + 'px';
                musicPlayer.style.height = targetRect.height + 'px';

                setTimeout(() => {
                    if (!musicPlayer.classList.contains('minimized')) {
                        musicPlayer.classList.remove('is-fixed');
                        musicPlayer.style.top = '';
                        musicPlayer.style.left = '';
                        musicPlayer.style.width = '';
                        musicPlayer.style.height = '';
                        playerPlaceholder.style.display = 'none';
                    }
                }, 600);
            }
        });

        const innerControls = document.querySelectorAll('.player-controls .control-btn, .player-progress, .player-info');
        innerControls.forEach(ctrl => ctrl.addEventListener('click', (e) => {
            if(!musicPlayer.classList.contains('minimized')) {
                e.stopPropagation();
            }
        }));
    </script>

</body></html>
