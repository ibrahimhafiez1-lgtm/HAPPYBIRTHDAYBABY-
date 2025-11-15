
<html lang="ms">
<head>
    <meta charset="UTF-8" />
    <title>Happy Birthday Shuraya 🎀🎉</title>

    <!-- Cute Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet">

    <style>
        body {
            margin: 0;
            font-family: 'Quicksand', sans-serif;
            background: #ffd9ec; /* Soft Pink */
            text-align: center;
            overflow-x: hidden;
        }

        h1, h2, h3 {
            color: #ff5fa2;
        }

        /* Navigation */
        .nav {
            background: white;
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 3px solid #ffb3d9;
        }
        .nav button {
            background: #ff5fa2;
            border: none;
            padding: 10px 18px;
            margin: 5px;
            color: white;
            border-radius: 10px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
        }
        .nav button:hover {
            transform: scale(1.05);
        }

        /* Soft Pink Card Sections */
        .section {
            background: white;
            margin: 30px auto;
            width: 90%;
            max-width: 800px;
            padding: 30px;
            border-radius: 18px;
            box-shadow: 0 4px 14px rgba(255, 105, 180, 0.25);
            border: 3px solid #ffb3d9;
        }

        /* Slideshow */
        .slideshow img {
            width: 100%;
            max-width: 350px;
            border-radius: 15px;
            border: 4px solid #ffb3d9;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }

        /* Floating Love Animation */
        .love {
            position: fixed;
            top: -10px;
            color: #ff5fa2;
            font-size: 24px;
            animation: fall 4s linear infinite;
        }
        @keyframes fall {
            to { transform: translateY(110vh); opacity: 0; }
        }

        /* Confetti */
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: pink;
            top: -10px;
            animation: confettiFall 3s linear infinite;
        }
        @keyframes confettiFall {
            to { transform: translateY(120vh) rotate(720deg); opacity: 0; }
        }

        /* Balloon */
        .balloon {
            position: fixed;
            bottom: -150px;
            font-size: 40px;
            animation: balloonUp 6s ease-in infinite;
        }
        @keyframes balloonUp {
            to { transform: translateY(-120vh); }
        }

        /* Glowing Name */
        .glow {
            font-size: 32px;
            font-weight: bold;
            color: #ff2e7e;
            text-shadow: 0 0 10px #ff5fa2, 0 0 20px #ff7fbf;
        }

        audio {
            margin-top: 10px;
        }

        /* LOCK SCREEN */
        #lockScreen{
          position:fixed;inset:0;background:linear-gradient(180deg,#fff6fb,#fff);display:flex;align-items:center;justify-content:center;z-index:10000;flex-direction:column;padding:20px;text-align:center
        }
        #lockScreen h2{font-family:'Quicksand',sans-serif;color:#ff5fa2;font-size:34px;margin:6px 0}
        .btn{background:#ff5fa2;color:#fff;border:none;padding:10px 16px;border-radius:12px;cursor:pointer;font-weight:700}

        /* overlay modal */
        .overlay{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,0.6);z-index:10001}
        .overlay.open{display:flex}
        .modal{background:#fff;border-radius:12px;padding:16px;max-width:420px;width:90%;position:relative}
        .closeBtn{position:absolute;right:12px;top:8px;border:none;background:none;font-size:20px;cursor:pointer}

    </style>
</head>

<body>

  <!-- LOCK SCREEN -->
  <div id="lockScreen">
    <h2>Happy Birthday, Shuraya 🎀</h2>
    <p style="color:#666">Website ini ada perlindungan kata laluan. Tekan butang di bawah untuk masukkan password.</p>
    <div style="height:12px"></div>
    <button class="btn" id="enterBtn">MASUK</button>
  </div>

  <!-- PASSWORD MODAL -->
  <div id="pwdModal" class="overlay">
    <div class="modal">
      <button class="closeBtn" onclick="closePwd()">✕</button>
      <h3>Masukkan Password</h3>
      <input id="pwdInput" type="password" placeholder="Password" style="width:100%;padding:10px;border-radius:8px;border:1px solid #ddd;margin-top:8px">
      <div style="height:12px"></div>
      <button class="btn" id="pwdCheck">Buka</button>
      <p style="color:#999;margin-top:8px">Password default: <strong>sayangsangat</strong> (boleh diubah dalam kod)</p>
    </div>
  </div>

    <!-- NAVIGATION -->
    <div class="nav">
        <button onclick="go('home')">Home</button>
        <button onclick="go('slideshow')">Gambar</button>
        <button onclick="go('video')">Video</button>
        <button onclick="go('surat')">Surat</button>
        <button onclick="go('memory')">Memori</button>
        <button onclick="go('why')">Why You’re Special</button>
        <button onclick="go('wish')">Ucapan Panjang</button>
    </div>

    <!-- CONFETTI -->
    <script>
        for (let i = 0; i < 35; i++) {
            let c = document.createElement("div");
            c.className = "confetti";
            c.style.left = Math.random() * 100 + "vw";
            c.style.animationDuration = 2 + Math.random() * 3 + "s";
            c.style.background = ["#ff5fa2", "#ffb3d9", "#ffcce6"][Math.floor(Math.random() * 3)];
            document.body.appendChild(c);
        }
    </script>

    <!-- HOME -->
    <section id="home" class="section">
        <h1 class="glow">Happy Birthday, NURUL SHURAYA 🎀💗</h1>
        <h3>23 November 2005</h3>
        <p>Hari ni hari istimewa untuk seorang yang sangat bermakna… iaitu awak 💗</p>

        <h2>🎀 Countdown Ke Birthday Shuraya</h2>
        <h1 id="countdown"></h1>

        <h3>🎶 Background Music</h3>
        <audio controls id="bgAudio" preload="none">
            <source src="YOUR-SONG.mp3">
        </audio>
        <p style="opacity:0.6;">*Masukkan link/audio file awak sendiri nanti*</p>
    </section>

    <!-- SLIDESHOW -->
    <section id="slideshow" class="section" style="display:none">
        <h2>📸 Gambar Cantik Shuraya</h2>
        <img id="slide" src="<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/f215eba8-4895-42dc-ae15-356d02ac7d07" />
" class="slideshow">
        <p style="opacity:0.6;">*Masukkan gambar di folder sama & tukar nama file*</p>
    </section>

    <!-- VIDEO -->
    <section id="video" class="section" style="display:none">
        <h2>🎥 Video Untuk Shuraya</h2>
        <video width="300" controls>
            <source src="video_shuraya.mp4">
        </video>
        <p style="opacity:0.6;">*Letak video file dalam folder sama*</p>
    </section>

    <!-- SURAT -->
    <section id="surat" class="section" style="display:none">
        <h2>💌 Surat Untuk Shuraya</h2>
        <p style="font-size:19px; width:85%; margin:auto;">
            Shuraya… 
            Pada hari lahir awak ni, saya nak awak tahu satu perkara. 
            Awak seorang yang sangat istimewa, sangat lembut hati, kuat,
            dan sangat berharga. Dunia jadi lebih indah sebab ada awak. 
            Semoga setiap langkah awak tahun ni penuh rezeki, senyuman,
            kebahagiaan dan perlindungan. 💗
        </p>
    </section>

    <!-- MEMORY PAGE -->
    <section id="memory" class="section" style="display:none">
        <h2>📚 Memory Page</h2>
        <p style="font-size:18px;">Letak gambar & kenangan awak dengan dia nanti 💗</p>
    </section>

    <!-- WHY SPECIAL -->
    <section id="why" class="section" style="display:none">
        <h2>🌸 Kenapa Shuraya Istimewa</h2>
        <ul style="list-style:none; padding:0; font-size:19px; line-height:2;">
            <li>• Awak baik hati 💗</li>
            <li>• Awak penyayang sangat 🎀</li>
            <li>• Awak cantik luar & dalam 💞</li>
            <li>• Awak kuat walaupun banyak pendam 💗</li>
            <li>• Awak buat orang lain rasa dihargai 🎀</li>
        </ul>
    </section>

    <!-- LONG WISH -->
    <section id="wish" class="section" style="display:none">
        <h2>🎂 Ucapan Panjang Untuk Shuraya</h2>
        <p style="font-size:20px; width:90%; margin:auto;">
            Selamat Hari Lahir, Shuraya 🎀💗
            Saya doakan hidup awak sentiasa dipenuhi kegembiraan,
            ketenangan, rezeki yang melimpah, dan orang-orang yang sayang
            awak dengan ikhlas. Awak layak dapat semuanya 💕
        </p>
    </section>

    <!-- Balloons -->
    <script>
        for (let i = 0; i < 6; i++) {
            let b = document.createElement("div");
            b.className = "balloon";
            b.style.left = Math.random() * 100 + "vw";
            b.style.animationDuration = 4 + Math.random() * 4 + "s";
            b.innerHTML = "🎈";
            document.body.appendChild(b);
        }

        // Password logic
        const DEFAULT_PASSWORD = 'sayangsangat'; // <-- change if you want
        const enterBtn = document.getElementById('enterBtn');
        const pwdModal = document.getElementById('pwdModal');
        const pwdInput = document.getElementById('pwdInput');
        const pwdCheck = document.getElementById('pwdCheck');
        const lockScreen = document.getElementById('lockScreen');

        enterBtn.addEventListener('click', ()=>{
            pwdModal.classList.add('open');
        });
        function closePwd(){ pwdModal.classList.remove('open'); pwdInput.value=''; }
        pwdCheck.addEventListener('click', ()=>{
            const val = pwdInput.value.trim();
            if(val === DEFAULT_PASSWORD){
                // unlock: hide lock screen and show home
                lockScreen.style.display = 'none';
                pwdModal.classList.remove('open');
                // show home section and make nav functional
                showSection('home');
                // autoplay music if possible
                const a = document.getElementById('bgAudio');
                if(a){ a.play().catch(()=>{}); }
            } else {
                alert('Password salah! Sila cuba lagi.');
                pwdInput.value = '';
            }
        });

        // Simple section show/hide navigation
        function showSection(id){
            const sections = ['home','slideshow','video','surat','memory','why','wish'];
            sections.forEach(s=>{
                const el = document.getElementById(s);
                if(el) el.style.display = (s===id? 'block' : 'none');
            });
            window.scrollTo({top:0, behavior:'smooth'});
        }

        // nav buttons
        document.querySelectorAll('.nav button').forEach((btn,i)=>{
            btn.addEventListener('click', ()=>{
                const ids = ['home','slideshow','video','surat','memory','why','wish'];
                showSection(ids[i]);
            });
        });

        // Countdown
        function countdown(){
            const target = new Date('Nov 23, 2025 00:00:00').getTime();
            setInterval(()=>{
                const now = new Date().getTime();
                const diff = target - now;
                const d = Math.max(0, Math.floor(diff / (1000*60*60*24)));
                const h = Math.floor((diff % (1000*60*60*24)) / (1000*60*60));
                const m = Math.floor((diff % (1000*60*60)) / (1000*60));
                const s = Math.floor((diff % (1000*60)) / 1000);
                document.getElementById('countdown').textContent = `${d} hari ${h} jam ${m} minit ${s} saat`;
            },1000);
        }
        countdown();

    </script>

</body>
</html>
