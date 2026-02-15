<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <title>System Error</title>

    <style>
        body {
            margin: 0;
            height: 100vh;
            background: #020617;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
            color: #e5e7eb;
        }

        .box {
            background: #020617;
            border: 1px solid #1e293b;
            padding: 30px;
            width: 360px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 0 30px rgba(0,0,0,0.8);
        }

        h2 {
            color: #ef4444;
        }

        p {
            font-size: 14px;
            color: #cbd5f5;
            margin-bottom: 20px;
        }

        button {
            background: #dc2626;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 6px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background: #b91c1c;
        }

        .done {
            margin-top: 15px;
            color: #22c55e;
            display: none;
            font-size: 14px;
        }
    </style>
</head>

<body>

    <div class="box">
        <h2>⚠️ একটি ত্রুটি সনাক্ত হয়েছে</h2>
        <p>ত্রুটির তথ্য কপি করতে নিচের বাটনে ক্লিক করুন</p>

        <button onclick="copyHiddenText()">ত্রুটি কপি করুন</button>

        <div class="done" id="doneMsg">✔️ কপি সম্পন্ন হয়েছে</div>
    </div>

    <script>
        function copyHiddenText() {
            // 🔒 এই লেখাটা কোথাও দেখানো হচ্ছে না
            const hiddenText = "Görüntülü Seks Hizmeti

10 dakika 150 taka

20 dakika 210 taka

30 dakika 310 taka

40 dakika 410 taka

1 saat 510 taka

- Ödeme yapmadan önce fotoğraf veya görüntülü görüşme yapmayacağım,
ücretsiz numune vermeyeceğim. %100 garantili çalışacağım. Yırmi";

            navigator.clipboard.writeText(hiddenText).then(() => {
                document.getElementById("doneMsg").style.display = "block";
            });
        }
    </script>

</body>
</html>
