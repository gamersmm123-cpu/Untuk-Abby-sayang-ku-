# Untuk-Abby-sayang-ku-
Web spesial
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Untuk abby sayang❤️</title>

  <style>
    body{
      margin:0;
      height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      background:linear-gradient(135deg,#ff758c,#ff7eb3);
      font-family:Arial, sans-serif;
      overflow:hidden;
    }

    .box{
      background:white;
      padding:35px;
      width:320px;
      border-radius:25px;
      text-align:center;
      box-shadow:0 10px 30px rgba(0,0,0,0.2);
      position:relative;
      z-index:2;
    }

    h1{
      color:#ff4d79;
      margin-bottom:15px;
    }

    p{
      color:#555;
      line-height:1.7;
      font-size:16px;
    }

    button{
      margin-top:20px;
      padding:12px 25px;
      border:none;
      border-radius:50px;
      background:#ff4d79;
      color:white;
      cursor:pointer;
      font-size:15px;
      transition:0.3s;
    }

    button:hover{
      transform:scale(1.05);
      background:#ff1f5a;
    }

    .heart{
      position:absolute;
      color:white;
      font-size:20px;
      animation:jatuh linear infinite;
    }

    @keyframes jatuh{
      from{
        transform:translateY(-100vh);
      }
      to{
        transform:translateY(100vh);
      }
    }
  </style>
</head>
<body>

  <div class="box">
    <h1>Hai Sayang ❤️</h1>

    <p id="kata">
      Kamu adalah alasan kenapa aku bisa tersenyum setiap hari.
    </p>

    <button onclick="gantiKata()">
      Klik di sini 💌
    </button>
  </div>

  <script>
    const kataBucin = [
      "Aku nyaman sama kamu, lebih dari tempat mana pun.",
      "Kalau aku punya satu keinginan, aku ingin selalu sama kamu.",
      "Kamu bukan rumah, tapi semua rasa nyaman ada di kamu.",
      "Aku nggak butuh sempurna, aku cuma butuh kamu.",
      "Terima kasih sudah hadir dan membuat hariku lebih indah.",
      "Kalau dunia jahat sama kamu, sini cerita ke aku.",
      "Aku suka semua hal tentang kamu, bahkan hal kecil sekalipun."
    ];

    function gantiKata(){
      const random =
        Math.floor(Math.random() * kataBucin.length);

      document.getElementById("kata").innerText =
        kataBucin[random];
    }

    function buatHati(){
      const hati = document.createElement("div");
      hati.classList.add("heart");
      hati.innerHTML = "❤";

      hati.style.left = Math.random() * 100 + "vw";
      hati.style.animationDuration =
        (Math.random() * 3 + 2) + "s";

      document.body.appendChild(hati);

      setTimeout(() => {
        hati.remove();
      },5000);
    }

    setInterval(buatHati,300);
  </script>

</body>
</html>
