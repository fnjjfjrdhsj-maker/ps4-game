<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PS4 Exploit</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    background: #05070d;
    color: #fff;
    font-family: Arial, sans-serif;
    text-align: center;
    overflow-x: hidden;
}

.container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.logo {
    font-size: 70px;
    color: #00aaff;
    text-shadow:
        0 0 10px #0088ff,
        0 0 30px #0066ff;
    margin-bottom: 10px;
}

h1 {
    font-size: 32px;
    margin: 5px 0;
    color: #eee;
}

.subtitle {
    color: #777;
    font-size: 14px;
    letter-spacing: 2px;
    margin-bottom: 40px;
}

.card {
    width: 100%;
    max-width: 520px;
    background: rgba(15, 20, 32, 0.95);
    border: 1px solid #1d5c91;
    border-radius: 15px;
    padding: 30px;
    box-shadow: 0 0 30px rgba(0, 110, 255, .15);
}

.status {
    font-size: 18px;
    color: #00aaff;
    margin-bottom: 20px;
}

.firmware {
    font-size: 42px;
    font-weight: bold;
    margin: 20px 0;
    color: white;
}

button {
    width: 100%;
    padding: 16px;
    border: none;
    border-radius: 8px;
    background: #087cf5;
    color: white;
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 0 20px rgba(0, 120, 255, .3);
    transition: .2s;
}

button:hover {
    background: #1591ff;
    transform: scale(1.02);
}

button:active {
    transform: scale(.98);
}

#result {
    margin-top: 25px;
    min-height: 25px;
    color: #aaa;
}

.loading {
    color: #00aaff;
}

.success {
    color: #00ff88;
}

.warning {
    color: #ffcc00;
}

.info {
    margin-top: 30px;
    color: #666;
    font-size: 13px;
}

footer {
    margin-top: 30px;
    color: #444;
    font-size: 12px;
}

.circle {
    position: fixed;
    width: 400px;
    height: 400px;
    border-radius: 50%;
    background: #006eff;
    filter: blur(180px);
    opacity: .08;
    z-index: -1;
}
</style>
</head>

<body>

<div class="circle"></div>

<div class="container">

    <div class="logo">△</div>

    <h1>PlayStation 4</h1>

    <div class="subtitle">
        EXPLOIT ARCHITECTURE
    </div>

    <div class="card">

        <div class="status">
            SYSTEM STATUS
        </div>

        <div class="firmware" id="firmware">
            READY
        </div>

        <button onclick="startCheck()">
            PRESS X
        </button>

        <div id="result">
            Press the button to start a demo check.
        </div>

    </div>

    <div class="info">
        PS4 Firmware Information Interface
    </div>

    <footer>
        © 2026 PS4 Project
    </footer>

</div>

<script>

function startCheck() {

    const firmware = document.getElementById("firmware");
    const result = document.getElementById("result");

    firmware.innerHTML = "SCANNING...";
    firmware.style.color = "#00aaff";

    result.className = "loading";
    result.innerHTML = "Detecting firmware...";

    setTimeout(() => {

        firmware.innerHTML = "CHECKING";
        result.innerHTML = "Checking system information...";

    }, 1200);

    setTimeout(() => {

        firmware.innerHTML = "DEMO";
        firmware.style.color = "#00ff88";

        result.className = "success";
        result.innerHTML =
            "Demo completed successfully. No system modifications were performed.";

    }, 2500);
}

</script>

</body>
</html>
