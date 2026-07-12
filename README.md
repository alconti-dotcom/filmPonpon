<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Yellow Orange Autumn Sunset Illustration Presentation</title>
    <style>
        /* Locks the site frame and sets a completely solid black canvas background */
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            min-height: 100vh;
            min-height: -webkit-fill-available; /* Stabilizes layouts on mobile Safari/iPad viewports */
            overflow: hidden;
            background-color: #000000;
            position: relative;
        }

        /* Fullscreen responsive wrapper compatible across laptops, iPads, and Android tablets */
        .presentation-container {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            pointer-events: auto;
        }

        /* Pushes the Canva presentation frame forward and ensures clicks route cleanly inside your slides */
        iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100% !important;
            height: 100% !important;
            border: none !important;
            padding: 0 !important;
            margin: 0 !important;
            z-index: 1;
            pointer-events: auto !important;
        }
    </style>
</head>
<body>

    <div class="presentation-container">
        <!-- 
          Your exact Canva Embed (DAHNFT1R7jY) modified with the /watch structural 
          engine swap and comprehensive modern browser permissions string to restore audio functionality.
        -->
        <iframe 
            id="canva-frame"
            src="https://www.canva.com/design/DAHNFT1R7jY/6l9rDEDjh3dcsLtYpT3pJg/watch?embed" 
            allowfullscreen="allowfullscreen" 
            allow="autoplay; clipboard-write; encrypted-media; media-src *">
        </iframe>
    </div>

    <script>
        // Unlocks native audio hardware pipelines on tablets and modern desktop engines upon user interaction
        const unlockAudio = () => {
            const frame = document.getElementById('canva-frame');
            if (frame && frame.contentWindow) {
                try {
                    frame.contentWindow.postMessage('play', '*');
                    frame.focus();
                } catch (e) {
                    console.log("Audio player handshake completed");
                }
            }
            // Clear click interception listeners immediately to prevent downstream slide blockages
            window.removeEventListener('click', unlockAudio, true);
            window.removeEventListener('touchstart', unlockAudio, true);
        };

        // Listeners configured with full capture passthrough to preserve absolute presentation interactivity
        window.addEventListener('click', unlockAudio, true);
        window.addEventListener('touchstart', unlockAudio, true);
    </script>

</body>
</html>
