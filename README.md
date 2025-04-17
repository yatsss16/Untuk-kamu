<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Untuk Kartika</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: radial-gradient(ellipse at bottom, #1b2735 0%, #090a0f 100%);
      color: white;
      font-family: 'Comic Sans MS', cursive;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
    }

    .stars {
      position: absolute;
      width: 100%;
      height: 100%;
      background: transparent;
      box-shadow: 0 0 1px #fff;
      animation: twinkle 2s infinite;
    }

    @keyframes twinkle {
      0%, 100% { opacity: 0.3; }
      50% { opacity: 1; }
    }

    .text {
      font-size: 1.5rem;
      max-width: 600px;
      padding: 20px;
      animation: fadeIn 2s ease-in-out forwards;
      opacity: 0;
    }

    @keyframes fadeIn {
      to { opacity: 1; }
    }

    .btn {
      background-color: pink;
      color: #fff;
      padding: 15px 25px;
      margin-top: 30px;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      font-size: 1.2rem;
      transition: transform 0.3s;
    }

    .btn:hover {
      transform: scale(1.1);
    }

    .heart {
      font-size: 2rem;
      animation: pulse 1s infinite;
      color: red;
      margin-top: 10px;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }

    audio {
      position: absolute;
      bottom: 10px;
      left: 10px;
    }
  </style>
</head>
<body>
  <div class="stars"></div>

  <div class="text" id="message">Hei Kartika, boleh curhat sebentar?</div>
  <button class="btn" onclick="showNextMessage()">Klik lagi ya</button>
  <div class="heart" id="heart">♥</div>

  <!-- Musik Komang (pastikan file mp3 tersimpan di folder yang sama, atau pakai link jika host online) -->
  <audio controls autoplay loop>
    <source src="komang.mp3" type="audio/mpeg">
    Maaf, browser kamu tidak mendukung audio.
  </audio>

  <script>
    const messages = [
      "Sejak aku kenal kamu, dunia rasanya lebih indah.",
      "Ada damai tiap kali denger namamu... Kartika.",
      "Kalau kamu senyum, hatiku ikut hangat.",
      "Kamu itu kayak lagu Komang... nggak pernah bosen didengar.",
      "Maukah kamu jadi bagian dari hariku... setiap hari?"
    ];

    let i = 0;
    function showNextMessage() {
      if (i < messages.length) {
        document.getElementById('message').textContent = messages[i];
        i++;
      } else {
        document.getElementById('message').textContent = "Jawaban kamu adalah musik terbaik buatku, Kartika.";
      }
    }
  </script>
</body>
</html>
