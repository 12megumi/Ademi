<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hey Sweetie - Fun Quiz</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to bottom right, #cce3f0, #fef6ff);
      color: #333;
      padding: 20px;
      max-width: 600px;
      margin: auto;
    }
    .slide {
      display: none;
      background-color: #ffffffcc;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }
    .slide.active {
      display: block;
    }
    h1, h2 {
      text-align: center;
      color: #4d6faf;
    }
    label {
      display: block;
      margin-top: 10px;
    }
    button {
      margin-top: 20px;
      background-color: #4d6faf;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
      font-weight: 600;
    }
    button:hover {
      background-color: #3d5e99;
    }
    .result, .message-box {
      display: none;
      background-color: #f0f9ff;
      padding: 20px;
      border-radius: 10px;
      margin-top: 20px;
    }
    textarea {
      width: 100%;
      font-family: 'Poppins', sans-serif;
      font-size: 14px;
      padding: 8px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>

<audio id="bgMusic" loop>
  <source src="https://www.bensound.com/bensound-music/bensound-ukulele.mp3" type="audio/mpeg">
</audio>

<h1>💌 Hey sweetie, let's play a fun quiz!<br>How well do you know me?</h1>

<form id="quizForm">
  <div class="slide active">
    <strong>🌤 But before we start... how are you today?</strong><br>
    <label><input type="radio" name="mood" value="good"> 😊 I'm good</label>
    <label><input type="radio" name="mood" value="not_good"> 🙁 Not so good</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <!-- Questions Start Here -->
  <!-- Repeat this format for all questions -->

  <div class="slide">
    <strong>1. What month was I born?</strong><br>
    <label><input type="radio" name="q0" value="february"> ❄️ February</label>
    <label><input type="radio" name="q0" value="december"> 🎄 December</label>
    <label><input type="radio" name="q0" value="june"> ☀️ June</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>2. What's my favorite color?</strong><br>
    <label><input type="radio" name="q1" value="blue"> 💙 Blue</label>
    <label><input type="radio" name="q1" value="pink"> 💖 Pink</label>
    <label><input type="radio" name="q1" value="yellow"> 💛 Yellow</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>3. What food do I love the most?</strong><br>
    <label><input type="radio" name="q2" value="burger"> 🍔 Burger</label>
    <label><input type="radio" name="q2" value="rice"> 🍚 Rice</label>
    <label><input type="radio" name="q2" value="noodles"> 🍜 Instant Noodles</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>4. What do I prefer on weekends?</strong><br>
    <label><input type="radio" name="q3" value="sleep"> 🛏 Sleep all day</label>
    <label><input type="radio" name="q3" value="movie"> 🎬 Watching Movie</label>
    <label><input type="radio" name="q3" value="walk"> 🏞 Go out for a walk</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>5. My favorite animal is:</strong><br>
    <label><input type="radio" name="q4" value="cat"> 🐱 Cat</label>
    <label><input type="radio" name="q4" value="fish"> 🐟 Fish</label>
    <label><input type="radio" name="q4" value="dog"> 🐶 Dog</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>6. If I were a fruit, I would be:</strong><br>
    <label><input type="radio" name="q5" value="pineapple"> 🍍 Pineapple (sweet but spiky)</label>
    <label><input type="radio" name="q5" value="strawberry"> 🍓 Strawberry (tiny and cute)</label>
    <label><input type="radio" name="q5" value="avocado"> 🥑 Avocado (extra and mysterious)</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>7. What's my hidden superpower?</strong><br>
    <label><input type="radio" name="q6" value="sleeping"> 😴 Sleeping anytime, anywhere</label>
    <label><input type="radio" name="q6" value="easygoing"> 🫂 Easy to get along with</label>
    <label><input type="radio" name="q6" value="singing"> 🎤 Singing badly but confidently</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>8. If I were an animal in a past life, I’d be:</strong><br>
    <label><input type="radio" name="q7" value="koala"> 🐨 Koala(lazy and always sleeping)</label>
    <label><input type="radio" name="q7" value="cat"> 🐈 Cat(atractive and cute)</label>
    <label><input type="radio" name="q7" value="turtle"> 🐢 Turtle(slow but stedy)</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>9. My reaction to sudden plans:</strong><br>
    <label><input type="radio" name="q8" value="panic"> 😱 Panic first</label>
    <label><input type="radio" name="q8" value="im_in"> 🤔 Say "I'm in" then regret</label>
    <label><input type="radio" name="q8" value="no"> 🙅 Say "No" but secretly want to join</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>10. Favorite confused phrase:</strong><br>
    <label><input type="radio" name="q9" value="hah"> 😱 "HAH?"</label>
    <label><input type="radio" name="q9" value="what"> 😲 "Wait... what?"</label>
    <label><input type="radio" name="q9" value="nothing"> 🙂 "Nothing"</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>11. Midnight crisis activity:</strong><br>
    <label><input type="radio" name="q10" value="food"> 🍕 Ordering food</label>
    <label><input type="radio" name="q10" value="shopping"> 🛒 Adding stuff to cart</label>
    <label><input type="radio" name="q10" value="stalking"> 🤳 Stalking my old photos</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>12. My weirdest habit:</strong><br>
    <label><input type="radio" name="q11" value="talking"> 🗣️ Talking to myself</label>
    <label><input type="radio" name="q11" value="laughing"> 🤣 Laughing at my own jokes</label>
    <label><input type="radio" name="q11" value="overreacting"> 😶‍🌫️ Overreacting</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>13. My life’s background music:</strong><br>
    <label><input type="radio" name="q12" value="dramatic"> 🎻 Dramatic violin</label>
    <label><input type="radio" name="q12" value="rock"> 🤘 Rock</label>
    <label><input type="radio" name="q12" value="cartoon"> 🔉 Cartoon boing effect</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>14. Something I believe but can’t prove:</strong><br>
    <label><input type="radio" name="q13" value="bed"> 🛌 My bed loves me</label>
    <label><input type="radio" name="q13" value="brain"> 🧠 My brain works better when doing nothing</label>
    <label><input type="radio" name="q13" value="justin"> 👩‍🎤 My voice is like Justin Bieber</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>15. When I’m stressed, I usually...</strong><br>
    <label><input type="radio" name="q14" value="music"> 🎧 Listen to music</label>
    <label><input type="radio" name="q14" value="crying"> 😭 Cry</label>
    <label><input type="radio" name="q14" value="sleep"> 💤 Sleep</label>
    <button type="button" onclick="showResult()">See Result</button>
  </div>
</form>

<div class="result" id="resultBox">
  <h2>✨ Your Quiz Result ✨</h2>
  <p id="moodResult"></p>
  <p id="scoreResult"></p>
  <p><strong><div class
  <h2>Just one more thing...</h2>
  <p style="font-size: 1.1em; line-height: 1.6; text-align: center; padding: 0 20px;">
    Thank you for playing this silly little quiz.<br>
    I hope it made you smile, even just a little.<br><br>
    Life can be confusing, loud, and overwhelming...  
    but I want you to know that you're not alone.<br>
    You're smart, beautiful, and honestly — one of my favorite humans.<br><br>
    Goodluck for your last Exam, i know you will gonna make it couse you always do the best.. you got here, and that means the world to me.<br><br>
    <strong>I love you. Please keep going.</strong>
  </p>

<div class="message-box" id="messageBox">
  <h3>📩 Send Me a Message!</h3>
  <textarea id="messageText" rows="5" placeholder="Write your message here..."></textarea><br>
  <button onclick="sendMessage()">Send via WhatsApp</button>
</div>

<script>
  let currentSlide = 0;
  const slides = document.querySelectorAll(".slide");

  function nextSlide() {
    if (currentSlide === 0) {
      const bgMusic = document.getElementById("bgMusic");
      bgMusic.volume = 0.3;
      bgMusic.play().catch(e => console.log("Autoplay failed:", e));
    }
    slides[currentSlide].classList.remove("active");
    currentSlide++;
    slides[currentSlide].classList.add("active");
  }

  function showResult() {
    slides[currentSlide].classList.remove("active");

    const answers = {
      q0: "february",
      q1: "blue",
      q2: "noodles",
      q3: "sleep",
      q4: "cat",
      q5: "strawberry",
      q6: "singing",
      q7: "cat",
      q8: "im_in",
      q9: "hah",
      q10: "stalking",
      q11: "laughing",
      q12: "cartoon",
      q13: "bed",
      q14: "sleep"
    };

    let score = 0;
    for (let i = 0; i < 15; i++) {
      const qKey = `q${i}`;
      const selected = document.querySelector(`input[name="${qKey}"]:checked`);
      if (selected && selected.value === answers[qKey]) {
        score++;
      }
    }

    const mood = document.querySelector('input[name="mood"]:checked');
    let moodMessage = "";
    if (mood) {
      moodMessage = mood.value === "good"
        ? "Yay! I'm so glad you're feeling good today! 😊"
        : "Hope this quiz helped cheer you up a little! 💛";
    } else {
      moodMessage = "You didn’t answer how you’re feeling... but I hope you’re okay~";
    }

    let resultMsg = "";
    if (score === 15) resultMsg = "15/15! You totally know me! 💯✨";
    else if (score >= 10) resultMsg = `${score}/15! You know me pretty well! 🤗`;
    else resultMsg = `${score}/15! We need more cozy chats! ☕`;

    document.getElementById("moodResult").textContent = moodMessage;
    document.getElementById("scoreResult").textContent = resultMsg;

    document.getElementById("resultBox").style.display = "block";
    document.getElementById("messageBox").style.display = "block";
  }

  function sendMessage() {
    const text = document.getElementById("messageText").value;
    const phone = '6285369261133'; // Format international
    const waUrl = `https://wa.me/${phone}?text=${encodeURIComponent(text)}`;
    window.open(waUrl, '_blank');
  }
</script>

</body>
</html>
