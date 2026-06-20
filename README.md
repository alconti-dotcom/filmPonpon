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
        <iframe src="https://www.canva.com/design/DAHBdpnCC-c/SG2ezP0r8noQz8Sa_i0zsQ/view?embed" allowfullscreen allow="autoplay; clipboard-write"></iframe>
    </div>

</body>
</html>
