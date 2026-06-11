<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Pretty Girl, Mia ❤️</title>
    <style>
        :root {
            --primary-pink: #ff4b6e;
            --soft-pink: #ffe3e8;
            --dark-pink: #d63354;
            --bg-color: #fff5f6;
            --cream: #fffdf9;
            --butterfly-color: #ff9ebb;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            overflow-x: hidden;
        }

        header {
            text-align: center;
            padding: 40px 20px 10px 20px;
        }

        h1 {
            color: var(--primary-pink);
            font-size: 2.6rem;
            margin-bottom: 5px;
            text-shadow: 0 2px 4px rgba(255, 75, 110, 0.1);
        }

        .subtitle {
            color: #777;
            font-size: 1.1rem;
            margin-top: 0;
        }

        .container {
            width: 90%;
            max-width: 700px;
            margin-bottom: 60px;
        }

        /* Polaroid Photo Scrapbook Section */
        .gallery-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 20px 0 40px 0;
        }

        .polaroid {
            background: white;
            padding: 12px 12px 25px 12px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.08);
            border-radius: 4px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            width: 180px;
            text-align: center;
            position: relative;
        }

        .polaroid img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-radius: 2px;
        }

        /* Scrapbook angled look */
        .polaroid:nth-child(1) { transform: rotate(-5deg); }
        .polaroid:nth-child(2) { transform: rotate(3deg); }
        .polaroid:nth-child(3) { transform: rotate(-3deg); }

        .polaroid:hover {
            transform: scale(1.08) rotate(0deg);
            z-index: 10;
            box-shadow: 0 15px 30px rgba(255, 75, 110, 0.25);
        }

        /* Interactive Elements Container & Cards */
        .card {
            background: var(--cream);
            padding: 35px;
            border-radius: 24px;
            box-shadow: 0 10px 25px rgba(255, 75, 110, 0.06);
            margin-bottom: 35px;
            border: 1px solid rgba(255, 75, 110, 0.15);
            position: relative;
        }

        /* Message Box Styling */
        .essay-text {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #444;
            white-space: pre-line;
            text-align: left;
        }

        .essay-title {
            color: var(--dark-pink);
            font-size: 1.9rem;
            margin-top: 0;
            margin-bottom: 25px;
            text-align: center;
        }

        /* Button Layout Styles */
        .button-group {
            display: flex;
            flex-direction: column;
            gap: 15px;
            align-items: center;
            margin-top: 15px;
        }

        .btn {
            background-color: var(--primary-pink);
            color: white;
            border: none;
            padding: 14px 28px;
            font-size: 1rem;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: background 0.2s, transform 0.1s, box-shadow 0.2s;
            box-shadow: 0 4px 10px rgba(255, 75, 110, 0.2);
            outline: none;
        }

        .btn:hover {
            background-color: var(--dark-pink);
            box-shadow: 0 6px 15px rgba(255, 75, 110, 0.35);
        }

        .btn:active {
            transform: scale(0.96);
        }

        /* Special interactive trick buttons */
        .btn-flex-container {
            display: flex;
            gap: 20px;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
            position: relative;
            min-height: 60px;
        }

        #runawayBtn {
            position: absolute;
            transition: all 0.2s ease;
        }

        /* Love Meter styling */
        .meter-container {
            background-color: #f0f0f0;
            border-radius: 15px;
            height: 25px;
            width: 100%;
            margin-top: 20px;
            overflow: hidden;
            display: none;
            position: relative;
            box-shadow: inset 0 2px 5px rgba(0,0,0,0.05);
        }

        .meter-fill {
            background: linear-gradient(90deg, var(--primary-pink), #ff8ea4);
            height: 100%;
            width: 0%;
            transition: width 2s cubic-bezier(0.1, 0.8, 0.3, 1);
        }

        .meter-text {
            position: absolute;
            width: 100%;
            text-align: center;
            top: 3px;
            font-weight: bold;
            color: #333;
            font-size: 0.9rem;
        }

        /* Interactive popup box for dynamic buttons */
        #complimentDisplay {
            margin-top: 20px;
            font-size: 1.1rem;
            font-style: italic;
            color: var(--dark-pink);
            font-weight: 600;
            min-height: 25px;
            transition: opacity 0.3s ease;
        }

        /* Flying Elements System (Hearts & Butterflies) */
        .floating-heart {
            position: fixed;
            color: var(--primary-pink);
            font-size: 1.5rem;
            animation: floatUp linear infinite;
            bottom: -50px;
            opacity: 0;
            z-index: -1;
            pointer-events: none;
        }

        .butterfly {
            position: fixed;
            font-size: 1.8rem;
            animation: flyAround linear infinite;
            bottom: -50px;
            opacity: 0;
            z-index: -1;
            pointer-events: none;
        }

        @keyframes floatUp {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-105vh) rotate(360deg); opacity: 0; }
        }

        @keyframes flyAround {
            0% {
                transform: translateY(0) translateX(0) rotate(0deg);
                opacity: 1;
            }
            25% {
                transform: translateY(-25vh) translateX(30px) rotate(15deg);
            }
            50% {
                transform: translateY(-50vh) translateX(-30px) rotate(-15deg);
            }
            75% {
                transform: translateY(-75vh) translateX(20px) rotate(10deg);
            }
            100% {
                transform: translateY(-105vh) translateX(-10px) rotate(0deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>For My Pretty Girl ✨</h1>
        <p class="subtitle">Mia, I made a special interactive space just for us.</p>
    </header>

    <div class="container">

        <!-- PHOTO SCRAPBOOK SECTION -->
        <div class="gallery-container">
            <div class="polaroid">
                <img src="IMG-20260607-WA0015.jpg" alt="Mia and Me 1">
                <p style="margin: 8px 0 0 0; font-family: 'Courier New', monospace; color: #555; font-size: 0.9rem;">🤪 Always laughing</p>
            </div>
            <div class="polaroid">
                <img src="IMG-20250505-WA0009.jpg" alt="Mia and Me 2">
                <p style="margin: 8px 0 0 0; font-family: 'Courier New', monospace; color: #555; font-size: 0.9rem;">❤️ My favorite view</p>
            </div>
            <div class="polaroid">
                <img src="IMG-20260305-WA0223.jpg" alt="Mia and Me 3">
                <p style="margin: 8px 0 0 0; font-family: 'Courier New', monospace; color: #555; font-size: 0.9rem;">👩‍❤️‍💋‍👨 Forever yours.</p>
            </div>
        </div>

        <!-- MAIN ESSAY MESSAGE CARD -->
        <div class="card">
            <h2 class="essay-title">Mia ❤️</h2>
            <div class="essay-text">I don’t even know where to start, because every time I try to explain what you mean to me, normal words feel too small. They don’t carry enough weight. They don’t hold enough feeling. But I’ll still try, because you deserve to know — even if I can never fully express it the way I feel it inside me.

You are not just someone I love. You are someone who changed the way I see love completely. Before you, I thought love was just a word people used easily. But now I understand it differently. I understand it in quiet moments, in small thoughts, in the way my mind always finds its way back to you no matter what I’m doing.

You became my peace without even trying. My comfort without even knowing. My favourite part of days that feel ordinary. Even when life gets stressful, even when things don’t go right, even when I feel tired or overwhelmed — the thought of you somehow makes everything feel lighter.

I love you in ways that are not loud or dramatic. I love you in the quiet consistency of my heart choosing you again and again. I love you in the way I miss you randomly. In the way I imagine you smiling and it makes me feel calm. In the way I find myself caring about your happiness more than anything else around me.

You are my pretty girl, Mia. And when I say that, I don’t mean it in a shallow way. I mean it in a deep, permanent way — like something my heart decided and never questioned again.

There are so many things I wish I could tell you in person. Like how you’ve become part of my thoughts without effort. How I find myself thinking about your voice, your smile, your presence when I’m alone. How even silence feels less empty when I think of you.

If I had to describe what you mean to me in one sentence, I couldn’t. Because you are not a sentence. You are a feeling. You are a chapter in my life that I never want to end. You are the kind of person I don’t just like in the moment — I care about in a long-term, deep, real way.

And maybe I’m not perfect. Maybe I don’t always say things the right way or show everything exactly how I feel it. But one thing will always stay true — my feelings for you are real, and they don’t fade when things get quiet or when life gets busy. They stay. They grow. They stay yours.

I don’t know what the future holds, but I know that in every version of it I imagine, you are there in some way. Not because I need you to complete me, but because you already mean something to me that I don’t want to lose.

So if you ever doubt yourself, or ever wonder how much you matter to me, I hope you come back to this and remember:

You are deeply loved, consistently chosen, and genuinely important to me — more than you might ever fully realise. ❤️</div>
        </div>

        <!-- NEW BUTTON CONTAINER: REASON GENERATOR -->
        <div class="card" style="text-align: center;">
            <h3 style="color: var(--dark-pink); margin-top: 0;">✨ Reminders For Mia ✨</h3>
            <p style="color: #666;">Press this button whenever you need a reminder of what you mean to me.</p>
            <div class="button-group">
                <button class="btn" onclick="generateCompliment()">Click For a Surprise</button>
                <div id="complimentDisplay"></div>
            </div>
        </div>

        <!-- LOVE METER CARD -->
        <div class="card" style="text-align: center;">
            <h3 style="color: var(--dark-pink); margin-top: 0;">The Official Love Meter</h3>
            <p style="color: #666;">Click below to measure exactly how much I love you right now.</p>
            <button class="btn" onclick="startLoveMeter()">Calculate Love Force</button>
            
            <div class="meter-container" id="meterBg">
                <div class="meter-fill" id="meterFill"></div>
                <div class="meter-text" id="meterText">0%</div>
            </div>
            <p id="loveMessage" style="margin-top: 15px; font-weight: bold; color: var(--dark-pink); line-height: 1.4;"></p>
        </div>

        <!-- NEW BUTTON CONTAINER: GAME BUTTON -->
        <div class="card" style="text-align: center;">
            <h3 style="color: var(--dark-pink); margin-top: 0;">A Quick Question... 🤔</h3>
            <p style="color: #666;">Do you know how completely amazing you are?</p>
            <div class="btn-flex-container">
                <button class="btn" onclick="answeredYes()">Yes, completely! 🥰</button>
                <button class="btn" id="runawayBtn" onmouseover="dodgeButton()" onclick="dodgeButton()">No 😤</button>
            </div>
            <p id="gameResponse" style="margin-top: 15px; font-weight: bold; color: var(--dark-pink);"></p>
        </div>

    </div>

    <script>
        // Custom Reminders List
        const compliments = [
            "You became my peace without even trying. 🌸",
            "You are deeply loved, consistently chosen, and genuinely important. ❤️",
            "You are my pretty girl, Mia. Always and forever.",
            "Even when life gets stressful, the thought of you makes everything feel lighter. ✨",
            "You are a chapter in my life that I never want to end. 📖",
            "My mind always finds its way back to you no matter what I’m doing. 🥰",
            "My feelings for you are real, and they stay. They grow. They stay yours."
        ];

        function generateCompliment() {
            const display = document.getElementById('complimentDisplay');
            const randomPhrase = compliments[Math.floor(Math.random() * compliments.length)];
            display.style.opacity = 0;
            setTimeout(() => {
                display.innerText = randomPhrase;
                display.style.opacity = 1;
            }, 200);

            // Pop a mini group of butterflies and hearts when clicked
            for(let i=0; i<3; i++) {
                spawnElement('💗', 'floating-heart');
                spawnElement('🦋', 'butterfly');
            }
        }

        // Love Meter Logic
        function startLoveMeter() {
            const meterBg = document.getElementById('meterBg');
            const meterFill = document.getElementById('meterFill');
            const meterText = document.getElementById('meterText');
            const loveMessage = document.getElementById('loveMessage');

            meterBg.style.display = 'block';
            meterFill.style.width = '0%';
            meterText.innerText = '0%';
            loveMessage.innerText = 'Calculating...';

            setTimeout(() => {
                meterFill.style.width = '100%';
                meterText.innerText = '9999999%';
                loveMessage.innerText = 'Error: System overload! My love for you cannot be measured by standard mathematics. It broke the system! 📈❤️';
                
                // Massive burst of flying butterflies and hearts
                for(let i=0; i<20; i++) {
                    setTimeout(() => spawnElement('💗', 'floating-heart'), i * 80);
                    setTimeout(() => spawnElement('🦋', 'butterfly'), i * 110);
                }
            }, 150);
        }

        // Interactive Trick Button Logic
        function dodgeButton() {
            const btn = document.getElementById('runawayBtn');
            // Move the "No" button randomly so she can't easily click it
            const randomX = Math.random() * 140 - 70; // boundaries inside container
            const randomY = Math.random() * 50 - 25;
            btn.style.transform = `translate(${randomX}px, ${randomY}px)`;
            document.getElementById('gameResponse').innerText = "Hey, no picking that choice! Try the other one. 😉";
        }

        function answeredYes() {
            document.getElementById('gameResponse').innerText = "Good! Because you deserve to know it every single day. 😘❤️";
            const btn = document.getElementById('runawayBtn');
            btn.style.transform = `translate(0px, 0px)`; // reset position
            
            for(let i=0; i<10; i++) {
                spawnElement('🦋', 'butterfly');
                spawnElement('💗', 'floating-heart');
            }
        }

        // Dynamic Elements Generator Function
        function spawnElement(character, className) {
            const el = document.createElement('div');
            el.classList.add(className);
            el.innerHTML = character;
            
            el.style.left = Math.random() * 100 + 'vw';
            el.style.animationDuration = (Math.random() * 2 + 3) + 's'; // 3-5 seconds duration
            el.style.fontSize = (Math.random() * 15 + 15) + 'px'; // size between 15px and 30px
            
            document.body.appendChild(el);

            setTimeout(() => {
                el.remove();
            }, 5000);
        }

        // Keep a steady ambient stream of flying hearts and butterflies in the background
        setInterval(() => spawnElement('💗', 'floating-heart'), 2000);
        setInterval(() => spawnElement('🦋', 'butterfly'), 2800);
    </script>

</body>
                  </html>
                  
