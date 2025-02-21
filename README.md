<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ইমোজি কপি টুল</title>
    <style>
        .emoji-box {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .emoji {
            font-size: 2rem;
            cursor: pointer;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            background: #f9f9f9;
        }
    </style>
</head>
<body>
    <h2>পছন্দের ইমোজি কপি করুন</h2>
    <div class="emoji-box">
        <span class="emoji" onclick="copyEmoji(this)">😀</span>
        <span class="emoji" onclick="copyEmoji(this)">😂</span>
        <span class="emoji" onclick="copyEmoji(this)">😍</span>
        <span class="emoji" onclick="copyEmoji(this)">👍</span>
        <span class="emoji" onclick="copyEmoji(this)">🎉</span>
    </div>

    <script>
        function copyEmoji(element) {
            const text = element.innerText;
            navigator.clipboard.writeText(text).then(() => {
                alert("কপি হয়েছে: " + text);
            });
        }
    </script>
</body>
</html>
