<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <title>Be My Valentine 💘</title>  
  <style>  
    body {  
      height: 100vh;  
      margin: 0;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);  
      font-family: 'Arial', sans-serif;  
      overflow: hidden;  
    }  
  
    .container {  
      text-align: center;  
    }  
  
    h1 {  
      font-size: 2.5rem;  
      color: #fff;  
      margin-bottom: 30px;  
    }  
  
    button {  
      padding: 15px 35px;  
      font-size: 1.2rem;  
      border: none;  
      border-radius: 40px;  
      cursor: pointer;  
      position: relative;  
    }  
  
    #yes {  
      background: #ff4d6d;  
      color: white;  
      margin-right: 20px;  
    }  
  
    #no {  
      background: #444;  
      color: white;  
      position: absolute;  
    }  
  
    .wow {  
      display: none;  
      font-size: 3rem;  
      color: #fff;  
      margin-top: 20px;  
      animation: pop 0.8s ease infinite alternate;  
    }  
  
    @keyframes pop {  
      from { transform: scale(1); }  
      to { transform: scale(1.15); }  
    }  
  
    .heart {  
      position: fixed;  
      font-size: 30px;  
      animation: float 4s linear infinite;  
    }  
  
    @keyframes float {  
      from {  
        transform: translateY(100vh);  
        opacity: 1;  
      }  
      to {  
        transform: translateY(-10vh);  
        opacity: 0;  
      }  
    }  
  </style>  
</head>  
<body>  
  
  <div class="container">  
    <h1>Will you be my Valentine? 💖</h1>  
    <button id="yes">Yes ❤️</button>  
    <button id="no">No 😒</button>  
    <div class="wow">WOW 😍💥</div>  
  </div>  
  
  <script>  
    const noBtn = document.getElementById("no");  
    const yesBtn = document.getElementById("yes");  
    const wowText = document.querySelector(".wow");  
  
    noBtn.addEventListener("mouseover", () => {  
      const x = Math.random() * (window.innerWidth - 100);  
      const y = Math.random() * (window.innerHeight - 50);  
      noBtn.style.left = x + "px";  
      noBtn.style.top = y + "px";  
    });  
  
    yesBtn.addEventListener("click", () => {  
      wowText.style.display = "block";  
  
      for (let i = 0; i < 25; i++) {  
        const heart = document.createElement("div");  
        heart.classList.add("heart");  
        heart.innerHTML = "❤️";  
        heart.style.left = Math.random() * 100 + "vw";  
        heart.style.animationDuration = (Math.random() * 2 + 3) + "s";  
        document.body.appendChild(heart);  
  
        setTimeout(() => {  
          heart.remove();  
        }, 4000);  
      }  
    });  
  </script>  
  
</body>  
</html>  
