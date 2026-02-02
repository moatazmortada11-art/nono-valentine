<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>From Toty</title>
    <style>
        body { 
            height: 100vh; 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            background: #ffe6eb; 
            font-family: Arial, sans-serif; 
            overflow: hidden; 
            margin: 0; 
        }
        .box { text-align: center; padding: 20px; width: 100%; }
        h1 { color: #e6005c; font-size: 2.2rem; }
        
        button { 
            padding: 15px 35px; 
            font-size: 18px; 
            margin: 10px; 
            border: none; 
            border-radius: 50px; 
            cursor: pointer; 
            font-weight: bold; 
        }
        
        #yes { background-color: #ff4d79; color: white; }
        
        #no { 
            background-color: #999; 
            color: white; 
            position: absolute; 
            transition: 0.1s;
            left: 50%;
            top: 60%;
            transform: translate(-50%, -50%);
        }
        
        #content { display: none; margin-top: 10px; }
        
        video { 
            width: 90%; 
            max-width: 320px; 
            border-radius: 20px; 
            box-shadow: 0 10px 25px rgba(0,0,0,0.1); 
        }
    </style>
</head>
<body>

    <div class="box">
        <h1 id="question">Will you be my Valentine? 😔</h1>
        <button id="yes">Yes</button>
        <button id="no">No</button>

        <div id="content">
            <h2 style="color: #e6005c;">From Toty 😜</h2>
            <video id="valVideo" playsinline>
                <source src="V14044g50000d4a5tp7og65nalcc65ag.mov" type="video/quicktime">
                Your browser does not support the video tag.
            </video>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById("no");
        const yesBtn = document.getElementById("yes");
        const video = document.getElementById("valVideo");
        const question = document.getElementById("question");
        const content = document.getElementById("content");

        const moveButton = () => {
            const maxX = window.innerWidth - noBtn.offsetWidth;
            const maxY = window.innerHeight - noBtn.offsetHeight;
            const randomX = Math.floor(Math.random() * maxX);
            const randomY = Math.floor(Math.random() * maxY);
            noBtn.style.left = randomX + "px";
            noBtn.style.top = randomY + "px";
        };

        noBtn.addEventListener("mouseover", moveButton);
        noBtn.addEventListener("touchstart", (e) => {
            e.preventDefault();
            moveButton();
        });

        yesBtn.addEventListener("click", () => {
            question.style.display = "none";
            yesBtn.style.display = "none";
            noBtn.style.display = "none";
            content.style.display = "block";
            video.play(); // Starts video and sound
        });
    </script>
</body>
</html>
