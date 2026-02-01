# nono-valentine
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
            font-family: Arial, sans-serif; 
            overflow: hidden; 
            margin: 0; 
        }

        .box { 
            text-align: center; 
            padding: 20px; 
        }

        h1 { 
            color: #e6005c; 
            font-size: 2rem; 
        }

        button { 
            padding: 15px 30px; 
            font-size: 18px; 
            margin: 10px; 
            border: none; 
            border-radius: 50px; 
            cursor: pointer; 
            font-weight: bold; 
            transition: transform 0.2s; 
        }

        #yes { 
            background-color: #ff4d79; 
            color: white; 
            box-shadow: 0 4px 15px rgba(255, 77, 121, 0.4); 
        }

        #no { 
            background-color: #999; 
            color: white; 
            position: absolute; 
            transition: 0.1s;
            left: 55%;
            top: 50%;
        }

        #content { 
            display: none; 
            margin-top: 20px; 
        }

        video { 
            width: 100%; 
            max-width: 320px; 
            border-radius: 20px; 
            box-shadow: 0 10px 30px rgba(0,0,0,0.2); 
        }

        h2 {
            color: #e6005c;
            margin-bottom: 15px;
        }
    </style>
</head>
<body>

    <div class="box" id="main-box">
        <h1>Will you be my Valentine? 😔</h1>
        <button id="yes">Yes</button>
        <button id="no">No</button>

        <div id="content">
            <h2>you have no choice😜</h2>
            <video id="valVideo" playsinline>
                <source src="V14044g50000d4a5tp7og65nalcc65ag.mov" type="video/quicktime">
                Your browser does not support the video tag.
            </video>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById("no");
        const yesBtn = document.getElementById("yes");
        const content = document.getElementById("content");
        const video = document.getElementById("valVideo");
        const mainTitle = document.querySelector("h1");

        // Logic to make the 'No' button run away
        noBtn.addEventListener("mouseover", () => {
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            
            noBtn.style.left = x + "px";
            noBtn.style.top = y + "px";
        });

        // Trigger video and sound on 'Yes' click
        yesBtn.addEventListener("click", () => {
            content.style.display = "block";
            noBtn.style.display = "none";
            yesBtn.style.display = "none";
            mainTitle.style.display = "none";
            
            // Starts the .mov file with sound enabled
            video.play(); 
        });
    </script>

</body>
</html>
