# Kaitns-home
birthday nawami-birthday my-gift
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>هدية عيد ميلاد ناوامي</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #fff;
            background-image: url('pudding-chibi.png'); /* خلي الصورة عندك بنفس الاسم */
            background-size: cover;
            background-repeat: no-repeat;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            background-color: rgba(255, 255, 255, 0.9);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            text-align: center;
            max-width: 400px;
        }

        input {
            width: 80%;
            padding: 10px;
            margin: 15px 0;
            border-radius: 8px;
            border: 1px solid #ccc;
            background-color: #9b59b6;
            color: rgba(255,255,255,0.9);
            font-size: 16px;
        }

        button {
            padding: 10px 20px;
            border: none;
            border-radius: 8px;
            background-color: #8e44ad;
            color: #fff;
            cursor: pointer;
        }

        button:hover {
            background-color: #732d91;
        }

        #message {
            margin-top: 15px;
            font-size: 16px;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>من فضلك ادخل اسمك أو لقبك الذي تناديك به ناوامي (أنا)</h1>
        <input type="text" id="nameInput" placeholder="ادخل الاسم هنا">
        <button onclick="checkName()">التالي</button>
        <p id="message"></p>
    </div>

    <script>
        let attempts = 0; // عداد المحاولات

        function checkName() {
            const input = document.getElementById("nameInput").value.trim();
            const messageEl = document.getElementById("message");
            const validNames = ["تشانغبيني", "نونتي", "سلمى", "يونا"]; // لاحقًا تضيفي باقي الصحاب

            if (validNames.includes(input)) {
                messageEl.innerHTML = "اسمك صحيح! جاري الانتقال للصفحة الخاصة…"; // لاحقًا نعمل الصفحة الخاصة
            } else {
                attempts++;
                if (attempts === 1) {
                    messageEl.innerHTML = "من الممكن انك كتبت اسم اخر انا لا اناديك به، جرب مرة اخرى";
                } else {
                    messageEl.innerHTML = "يبدو أن هناك مشكلة، عليك أن ترجع إلى ناوامي (أنا) وتسألها عن مشكلتك!";
                }
            }
        }
    </script>
</body>
</html>
