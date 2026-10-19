
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Quà tặng 20/10 💝</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #ffe0ec, #fff0f5, #ffc2d8);
    min-height: 100vh;
    overflow-x: hidden;
    text-align: center;
    color: #b51e59;
}

.container {
    padding: 35px 15px;
    max-width: 650px;
    margin: auto;
}

h1 {
    font-size: clamp(27px, 6vw, 40px);
    margin-bottom: 15px;
    text-shadow: 1px 2px 5px #ffffff;
}

.subtitle {
    color: #d63384;
    margin-bottom: 25px;
    line-height: 1.7;
}

.gift {
    font-size: 110px;
    cursor: pointer;
    display: inline-block;
    animation: bounce 1.5s infinite;
    transition: transform .3s;
    filter: drop-shadow(0 8px 10px #e88aaa);
}

.gift:hover {
    transform: scale(1.12);
}

@keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-12px); }
}

.card {
    background: rgba(255,255,255,.9);
    border: 2px solid #ff9fc5;
    border-radius: 25px;
    padding: 25px 20px;
    margin-top: 25px;
    box-shadow: 0 10px 30px #e68bab55;
}

#letter {
    display: none;
    animation: appear 1s ease;
}

#letter.show {
    display: block;
}

@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

#letter h2 {
    margin-bottom: 20px;
    color: #e91e63;
    line-height: 1.5;
}

.message {
    font-size: 17px;
    line-height: 1.9;
    color: #7b2448;
    white-space: pre-line;
}

.heart {
    font-size: 45px;
    margin: 15px 0;
    animation: heartbeat 1s infinite;
}

@keyframes heartbeat {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.2); }
}

button {
    border: none;
    border-radius: 30px;
    background: linear-gradient(90deg, #ff4f91, #e91e63);
    color: white;
    padding: 13px 24px;
    margin: 12px 5px;
    font-size: 15px;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 4px 12px #e91e6340;
}

button:hover {
    opacity: .85;
}

.qr-section {
    background: white;
    padding: 22px 15px;
    margin-top: 30px;
    border-radius: 20px;
    box-shadow: 0 8px 25px #e68bab40;
}

.qr-section h2 {
    margin-bottom: 12px;
    font-size: 22px;
}

input {
    width: 100%;
    padding: 13px;
    border: 1px solid #f49abb;
    border-radius: 12px;
    font-size: 15px;
    margin: 12px 0;
}

#qr {
    display: none;
    max-width: 100%;
    margin: 20px auto 5px;
    padding: 10px;
    border: 1px solid #eee;
}

.note {
    font-size: 13px;
    color: #92506a;
    line-height: 1.7;
    margin-top: 12px;
}

.floating {
    position: fixed;
    top: -30px;
    pointer-events: none;
    animation: fall linear forwards;
    z-index: 5;
}

@keyframes fall {
    to {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
    }
}

footer {
    margin-top: 28px;
    font-size: 14px;
    color: #ad4771;
}
</style>
</head>

<body>
<div class="container">

    <h1>🌷 Happy Women's Day 🌷</h1>

    <p class="subtitle">
        Gửi đến cô gái đặc biệt một món quà nhỏ<br>
        Nhấn vào hộp quà để khám phá nhé! 💗
    </p>

    <div class="gift" onclick="openGift()" title="Mở quà">
        🎁
    </div>

    <p>💌 Một món quà nhỏ, ngàn lời yêu thương 💌</p>

    <div class="card" id="letter">
        <h2>🌸 Chúc mừng ngày 20/10 🌸</h2>

        <div class="heart">💖</div>

        <p class="message" id="message">
Gửi cô gái đáng yêu!

Chúc bạn ngày 20/10 thật vui vẻ,
luôn xinh đẹp, hạnh phúc và bình an.

Mong mọi điều tốt đẹp nhất sẽ đến với bạn.
Luôn mỉm cười và tự tin với chính mình nhé!

Cảm ơn vì đã xuất hiện
và làm cho cuộc sống này thêm nhiều màu sắc.

Chúc bạn có một ngày thật đáng nhớ! 🌷
        </p>

        <div class="heart">❤️</div>
        <p>With love, 💕</p>
    </div>

    <button onclick="openGift()">🎁 Mở món quà</button>

    <div class="qr-section">
        <h2>💝 Tạo mã QR tặng quà</h2>

        <p class="note">
            Dán đường dẫn website quà tặng đã đăng lên Internet
            vào ô dưới đây để tạo mã QR cho người nhận quét.
        </p>

        <input
            type="url"
            id="url"
            placeholder="https://ten-website-cua-ban..."
        >

        <button onclick="createQR()">✨ Tạo mã QR</button>

        <div>
            <img id="qr" alt="Mã QR quà tặng 20/10">

            <br>

            <button id="download"
                    onclick="downloadQR()"
                    style="display:none">
                📥 Tải mã QR
            </button>
        </div>

        <p class="note">
            Lưu ý: Phải sử dụng đường dẫn công khai của website.
            Đường dẫn localhost hoặc file trên máy tính
            sẽ không mở được trên điện thoại người nhận.
        </p>
    </div>

    <footer>
        Made with ❤️ for October 20th
    </footer>
</div>

<script>
function openGift() {
    const letter = document.getElementById("letter");

    letter.classList.add("show");

    letter.scrollIntoView({
        behavior: "smooth",
        block: "center"
    });

    for (let i = 0; i < 25; i++) {
        setTimeout(createHeart, i * 80);
    }
}

function createHeart() {
    const heart = document.createElement("div");

    heart.className = "floating";

    const icons = ["💗", "💖", "💕", "🌸", "🌷", "❤️"];

    heart.textContent =
        icons[Math.floor(Math.random() * icons.length)];

    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (18 + Math.random() * 20) + "px";
    heart.style.animationDuration = (3 + Math.random() * 4) + "s";

    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 7000);
}

function createQR() {
    const url = document.getElementById("url").value.trim();
    const qr = document.getElementById("qr");
    const download = document.getElementById("download");

    if (!url) {
        alert("Bạn hãy nhập đường dẫn website quà tặng nhé!");
        return;
    }

    try {
        const parsed = new URL(url);

        if (parsed.protocol !== "https:" &&
            parsed.protocol !== "http:") {
            throw new Error("Invalid URL");
        }

        qr.src =
            "https://api.qrserver.com/v1/create-qr-code/" +
            "?size=300x300&data=" + encodeURIComponent(url);

        qr.onload = function() {
            qr.style.display = "block";
            download.style.display = "inline-block";
        };

        qr.onerror = function() {
            alert("Không tạo được mã QR. Hãy kiểm tra kết nối Internet.");
        };
    } catch (error) {
        alert("Đường dẫn chưa hợp lệ. Hãy nhập URL đầy đủ nhé!");
    }
}

function downloadQR() {
    const qr = document.getElementById("qr");

    if (!qr.src || qr.style.display === "none") return;

    const link = document.createElement("a");
    link.href = qr.src;
    link.download = "qua-tang-20-10-QR.png";
    link.target = "_blank";
    link.click();
}
</script>
</body>
</html>

