<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>System Update</title>
    <style>
        body {
            background-color: black;
            color: #00FF00;
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            text-align: center;
        }

        .container {
            border: 2px solid #00FF00;
            padding: 40px;
            box-shadow: 0 0 20px #00FF00;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            animation: blink 1s infinite;
        }

        .loading {
            width: 300px;
            height: 20px;
            border: 1px solid #00FF00;
            margin-top: 20px;
            position: relative;
        }

        .progress {
            width: 0%;
            height: 100%;
            background-color: #00FF00;
            animation: fill 5s forwards;
        }

        @keyframes blink {
            0% { opacity: 1; }
            50% { opacity: 0; }
            100% { opacity: 1; }
        }

        @keyframes fill {
            0% { width: 0%; }
            100% { width: 100%; }
        }

        .log {
            margin-top: 30px;
            font-size: 0.8rem;
            text-align: left;
            width: 100%;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>CRITICAL SYSTEM BREACH</h1>
        <p>Unauthorized access detected...</p>
        <p>Downloading private data: <strong>SUCCESS</strong></p>
        <p>Encrypting local files...</p>
        
        <div class="loading">
            <div class="progress"></div>
        </div>

        <div class="log" id="log-text"></div>
    </div>

    <script>
        const logs = [
            "> Connecting to remote server...",
            "> Bypassing firewall...",
            "> Accessing /root/gallery/photos...",
            "> Uploading contacts list...",
            "> Monitoring front camera...",
            "> SYSTEM COMPROMISED."
        ];

        let i = 0;
        const logElement = document.getElementById('log-text');

        function typeLog() {
            if (i < logs.length) {
                logElement.innerHTML += logs[i] + "<br>";
                i++;
                setTimeout(typeLog, 800);
            }
        }

        typeLog();
    </script>
</body>
</html>
