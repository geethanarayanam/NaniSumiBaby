<html lang="te">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golden Baby Reveal</title>
    <style>
        body, html { margin: 0; padding: 0; height: 100%; overflow: hidden; background-color: #000; font-family: 'Arial', sans-serif; }

        /* Golden Silk Curtains */
        .curtain-container {
            position: fixed;
            width: 100%;
            height: 100%;
            display: flex;
            z-index: 10;
        }

        .curtain {
            width: 50%;
            height: 100%;
            /* Golden Silk Texture Gradient */
            background: linear-gradient(90deg, #b8860b 0%, #ffd700 25%, #fff8dc 50%, #ffd700 75%, #b8860b 100%);
            background-size: 200% 100%;
            box-shadow: inset 0 0 100px rgba(0,0,0,0.3);
            transition: transform 2s cubic-bezier(0.7, 0, 0.3, 1);
        }

        /* Gold Round Button */
        #revealBtn {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 140px;
            height: 140px;
            border-radius: 50%;
            border: 6px solid #fff;
            background: radial-gradient(circle at 30% 30%, #fff9c4, #fbc02d, #f57f17);
            color: #5d4037;
            font-weight: 900;
            font-size: 18px;
            cursor: pointer;
            z-index: 20;
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.8), 0 15px 40px rgba(0,0,0,0.6);
            transition: all 0.4s ease;
            text-transform: uppercase;
        }

        #revealBtn:hover { transform: translate(-50%, -50%) scale(1.15); box-shadow: 0 0 50px #fffb00; }

        /* Reveal Page with Catchy Background */
        .reveal-page {
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            /* Catchy sky blue background */
            background: linear-gradient(to bottom, #87ceeb, #ffffff);
            text-align: center;
            position: relative;
        }

        .baby-announcement {
            opacity: 0;
            transform: scale(0.5);
            transition: 1.5s cubic-bezier(0.175, 0.885, 0.32, 1.275) 1.2s;
        }

        .baby-img {
            width: 85%;
            max-width: 500px;
            border: 10px solid white;
            border-radius: 30px;
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
        }

        .telugu-text {
            font-size: 3.5rem;
            color: #0d47a1;
            margin-top: 30px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        /* Animation Helpers */
        .open-left { transform: translateX(-100%); }
        .open-right { transform: translateX(100%); }
        .show-reveal { opacity: 1; transform: scale(1); }
        .btn-hide { opacity: 0; pointer-events: none; transform: translate(-50%, -50%) scale(0); }

    </style>
</head>
<body>

    <button id="revealBtn">TAP TO<br>OPEN</button>

    <div class="curtain-container">
        <div class="curtain" id="lCurtain"></div>
        <div class="curtain" id="rCurtain"></div>
    </div>

    <div class="reveal-page">
        <div class="baby-announcement" id="revealBox">
            <img src="https://via.placeholder.com/500x500.png?text=Baby+Boy+<img width="480" height="480" alt="image" src="https://github.com/user-attachments/assets/40da3469-edee-4a6f-b315-a3b3491866e4" />+Here" class="baby-img" id="<img width="480" height="480" alt="image" src="https://github.com/user-attachments/assets/8911c37b-330c-4a4a-8e5d-b5e1657819de" />"><h1 class="telugu-text">మా కన్నయ్య కి స్వాగతం</h1>
        </div><script>
        const btn = document.getElementById('revealBtn');
        const lCurtain = document.getElementById('lCurtain');
        const rCurtain = document.getElementById('rCurtain');
        const revealBox = document.getElementById('revealBox');

        btn.addEventListener('click', () => {
            btn.classList.add('btn-hide');
            lCurtain.classList.add('open-left');
            rCurtain.classList.add('open-right');
            revealBox.classList.add('show-reveal');
        });
    </script>
</body>
</html>
