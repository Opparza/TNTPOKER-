<!DOCTYPE html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirect</title>
    <script>
        function redirectToBrowser() {
            const userAgent = navigator.userAgent || navigator.vendor || window.opera;
            const targetUrl = "https://linktr.ee/tntpoker";
            if (/android/i.test(userAgent)) {
                window.location.href = "googlechrome://navigate?url=" + targetUrl;
            } else if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
                window.location.href = "googlechrome://navigate?url=" + targetUrl;
            } else {
                alert("Please open this link in your browser for a better experience.");
            }
        }
        window.onload = redirectToBrowser;
    </script>
</head>
<body>
    <p>If you are not redirected, <a href="https://linktr.ee/tntpoker">click here</a>.</p>
</body>
</html>
