html
Copy
<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>پر کردن صفحه با رنگ قرمز</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
        }
        #red-screen {
            width: 100%;
            height: 100%;
            background-color: white;
            transition: background-color 0.5s;
        }
    </style>
</head>
<body>
    <div id="red-screen"></div>

    <script>
        // تابع برای تغییر رنگ صفحه به قرمز
        function turnRed() {
            const redScreen = document.getElementById('red-screen');
            redScreen.style.backgroundColor = 'red';
        }

        // تغییر رنگ صفحه به قرمز بعد از 3 ثانیه
        setTimeout(turnRed, 3000);

        // تغییر رنگ صفحه به قرمز با کلیک
        document.getElementById('red-screen').addEventListener('click', turnRed);
    </script>
</body>
</html>
