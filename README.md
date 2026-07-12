<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>My Canva Presentation Website</title>
    <style>
        /* Forces the background to be completely black and locked in place */
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            min-height: 100vh;
            min-height: -webkit-fill-available; /* Fixes mobile Safari/iPad address bar jumps */
            overflow: hidden;
            background-color: #000000;
            position: relative;
        }

        /* Universal responsive container that works on Laptops, iPads, and Samsung Galaxies */
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
        }

        /* Forces the Canva frame to fill the entire active screen space safely */
        iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100% !important;
            height: 100% !important;
            border: none !important;
            outline: none !important;
        }
    </style>
</head>
<body>

    <div class="presentation-container">
        <!-- 
          DIRECTIONS: Replace the entire web link inside the src="..." quotes below 
          with your own copied Canva embed URL. Do not include any extra text or tags.
        -->
        <iframe 
            id="canva-frame"
            src="<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https://www.canva.com/design/DAHNFT1R7jY/6l9rDEDjh3dcsLtYpT3pJg/view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAHNFT1R7jY&#x2F;6l9rDEDjh3dcsLtYpT3pJg&#x2F;view?utm_content=DAHNFT1R7jY&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">Yellow Orange Autumn Sunset Illustration Presentation</a> by ALbedo" 
            allowfullscreen 
            allow="autoplay; clipboard-write; encrypted-media; media-src *">
        </iframe>
    </div>

    <script>
        // Tablets (iPad/Samsung) strictly require a user gesture to unlock web audio pipelines.
        // This simple event listener safely wakes up audio context on the first user interaction.
        const unlockAudio = () => {
            const frame = document.getElementById('canva-frame');
            if (frame) {
                // Sending a gentle postMessage focus request can re-trigger audio playback elements inside the frame
                frame.contentWindow.postMessage('play', '*');
            }
            // Remove the triggers once the audio is successfully initialized to save memory
            window.removeEventListener('click', unlockAudio);
            window.removeEventListener('touchstart', unlockAudio);
        };

        window.addEventListener('click', unlockAudio);
        window.addEventListener('touchstart', unlockAudio); // Critical handler specifically for iPad and Android tablets
    </script>

</body>
</html>
