<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Detector Doji M1 – V6 Tanpa Chart</title>

<style>
  body {
    background:#000;
    color:#00eaff;
    font-family: Arial;
    text-align:center;
    padding:20px;
  }

  h1 {
    text-shadow:0 0 15px #00eaff;
    margin-bottom:20px;
  }

  .box {
    border:1px solid #00eaff;
    padding:20px;
    margin-top:20px;
    border-radius:15px;
    box-shadow:0 0 15px rgba(0,255,255,0.3);
  }

  .signal {
    font-size:35px;
    font-weight:bold;
    margin-top:10px;
  }

  .buy { color:#00ff7f; text-shadow:0 0 10px #00ff7f; }
  .sell { color:#ff4d4d; text-shadow:0 0 10px #ff4d4d; }
  .wait { color:#ffe066; text-shadow:0 0 10px #ffe066; }
</style>
</head>

<body>

<h1>Detector Doji + 3 Candle M1 – V6 (Tanpa Chart)</h1>

<div class="box">
  <h2>Status Deteksi</h2>
  <div id="status">Mengambil data...</div>
</div>

<div class="box">
  <h2>Sinyal Otomatis</h2>
  <div id="signalText" class="signal wait">MENUNGGU SINYAL...</div>
</div>

<!-- SUARA BUY -->
<audio id="buySound">
  <source src="https://actions.google.com/sounds/v1/alarms/beep_short.ogg" type="audio/ogg">
</audio>

<!-- SUARA SELL -->
<audio id="sellSound">
  <source src="https://actions.google.com/sounds/v1/cartoon/cartoon_boing.ogg" type="audio/ogg">
</audio>

<script>
async function getData() {
    try {
        let url = "https://api.binance.com/api/v3/klines?symbol=XAUUSDT&interval=1m&limit=20";
        let response = await fetch(url);
        let data = await response.json();

        document.getElementById("status").innerHTML = "Data M1 diterima ✔";

        return data.map(c => ({
            open: parseFloat(c[1]),
            high: parseFloat(c[2]),
            low:  parseFloat(c[3]),
            close:parseFloat(c[4])
        }));
    } catch (e) {
        document.getElementById("status").innerHTML = "Gagal mengambil data...";
        return [];
    }
}

function isDoji(c) {
    let body = Math.abs(c.close - c.open);
    let range = c.high - c.low;
    return body <= range * 0.10;
}

function detectSignals(arr) {
    if (arr.length < 5) return;

    let dojiC = arr[arr.length - 5];
    let a = arr[arr.length - 4];
    let b = arr[arr.length - 3];
    let c = arr[arr.length - 2];

    let signalBox = document.getElementById("signalText");

    /* BUY — Doji + 3 Hijau */
    if (isDoji(dojiC) &&
        a.close > a.open &&
        b.close > b.open &&
        c.close > c.open &&
        (c.close - c.open) > ((c.high - c.low) * 0.5)) {

        signalBox.innerHTML = "📈 BUY • Doji + 3 Hijau Penuh";
        signalBox.className = "signal buy";
        document.getElementById("buySound").play();
    }

    /* SELL — Doji + 3 Merah */
    if (isDoji(dojiC) &&
        a.close < a.open &&
        b.close < b.open &&
        c.close < c.open &&
        (a.open - a.close) > ((a.high - a.low) * 0.5)) {

        signalBox.innerHTML = "📉 SELL • Doji + 3 Merah Penuh";
        signalBox.className = "signal sell";
        document.getElementById("sellSound").play();
    }
}

async function start() {
    setInterval(async () => {
        let data = await getData();
        detectSignals(data);
    }, 3000);
}

start();
</script>

</body>
</html>
