# ohio mob boss
<!DOCTYPE html>
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Iframe with Fullscreen Button for GitHub Pages</title>
<style>
    .iframe-container {
        position: relative;
        width: 80%;
        max-width: 800px;
        margin: 20px auto;
        border: 2px solid blue;
        border-radius: 5px;
    }

    iframe {
        width: 100%;
        height: 400px;
        border: none;
        border-radius: 3px;
    }

    .fullscreen-btn {
        position: absolute;
        bottom: 10px;
        right: 10px;
        background-color: green;
        color: white;
        border: none;
        padding: 5px 10px;
        border-radius: 5px;
        cursor: pointer;
    }

    .fullscreen-btn:hover {
        background-color: darkgreen;
    }
</style>
</head>

<body>

<div class="iframe-container">
    <iframe id="myIframe" src="https://your-username.github.io/your-repo-name" allowfullscreen></iframe>
    <button class="fullscreen-btn" onclick="toggleFullscreen()">Fullscreen</button>
</div>

<script>
    function toggleFullscreen() {
        const iframe = document.getElementById("myIframe");
        if (iframe.requestFullscreen) {
            iframe.requestFullscreen();
        } else if (iframe.mozRequestFullScreen) { // Firefox
            iframe.mozRequestFullScreen();
        } else if (iframe.webkitRequestFullscreen) { // Chrome, Safari, and Opera
            iframe.webkitRequestFullscreen();
        } else if (iframe.msRequestFullscreen) { // IE/Edge
            iframe.msRequestFullscreen();
        }
    }
</script>

</body>
</html>

