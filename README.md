# Kaitns-home
birthday nawami-birthday my-gift
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>هدية عيد ميلاد ناوامي</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>من فضلك ادخل اسمك أو لقبك الذي تناديك به ناوامي (أنا)</h1>
        <input type="text" id="nameInput" placeholder="ادخل الاسم هنا">
        <button onclick="checkName()">التالي</button>
        <p id="message"></p>
    </div>

    <script src="script.js"></script>
</body>
</html>![7830b98076aa6752ee5f36ba3a0abf3f](https://github.com/user-attachments/assets/684b9823-4194-43e6-a88d-22ece567bc95)
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
![7830b98076aa6752ee5f36ba3a0abf3f](https://github.com/user-attachments/assets/74eeae27-3326-4435-bde3-4cd999f891f8)
