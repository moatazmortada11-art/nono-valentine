<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine?</title>
    <style>
        body { 
            height: 100vh; 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            background: #ffe6eb; 
            font-family: 'Arial', sans-serif; 
            overflow: hidden; 
            margin: 0; 
        }
        .box { text-align: center; padding: 20px; width: 100%; }
        h1 { color: #e6005c; font-size: 2.2rem; margin-bottom: 20px; }
        h2 { color: #e6005c; margin-bottom: 15px; display: none; }
        
        button { 
            padding: 15px 35px; 
            font-size: 18px; 
            margin: 10px; 
            border: none; 
            border-radius: 50px; 
            cursor: pointer; 
            font-weight: bold; 
            transition: 0.2s; 
        }
        #yes { background-color: #ff4d79; color: white; }
        #no { 
            background-color: #999; 
            color: white; 
            position: absolute; 
            left: 55%;
            top: 60%;
        }
        
        #video-container { display: none; margin-top: 10px; }
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

        <div id="video-container">
            <h2>you have no choice😜</h2>
            <video id="valVideo" playsinline>
                <source src="V14044g50000d4a5tp7og65nalcc65ag.mov" type="video/quicktime">
            </video>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById("no");
        const yesBtn = document.getElementById("yes");
        const question = document.getElementById("question");
        const videoContainer = document.getElementById("video-container");
        const videoText = document.querySelector("h2");
        const video = document.getElementById("valVideo");

        // Running No Button
        noBtn.addEventListener("mouseover", () => {
            const x = Math.random() * (window.innerWidth - 100);
            const y = Math.random() * (window.innerHeight - 50);
            noBtn.style.left = x + "px";
            noBtn.style.top = y + "px";
        });

        // Yes Button Action
        yesBtn.addEventListener("click", () => {
            question.style.display = "none";
            yesBtn.style.display = "none";
            noBtn.style.display = "none";
            
            videoContainer.style.display = "block";
            videoText.style.display = "block";
            
            video.play();
        });
    </script>
</body>
</html>
