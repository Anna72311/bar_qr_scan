<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Barcode & QR Code Generator & Scanner</title>
  <script src="https://cdn.jsdelivr.net/npm/jsbarcode@3.11.5/dist/JsBarcode.all.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/quagga/0.12.1/quagga.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/jsqr@1.4.0/dist/jsQR.min.js"></script>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom right, #bcb270, #55ecf7);
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;  
      justify-content: center;
      min-height: 100vh;
      padding: 20px;
      font-size: 1.2rem;
    }
    .button {
      background: white;
      color: #4f46e5;
      font-size: 1.5rem;
      font-weight: bold;
      padding: 1.5rem 3rem;
      border: none;
      border-radius: 1.5rem;
      margin: 1rem;
      cursor: pointer;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    }
    .card {
      background: white;
      color: black;
      padding: 3rem;
      border-radius: 1.5rem;
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
      max-width: 500px;
      margin-top: 1rem;
    }
    input {
      width: 100%;
      padding: 1rem;
      margin: 1.5rem 0;
      font-size: 1.2rem;
      border: 1px solid #ccc;
      border-radius: 0.5rem;
    }
    #scan-result a {
      color: #4f46e5;
      text-decoration: underline;
    }
    #reader {
      width: 100%;
      height: 350px;
      border: 1px solid #ccc;
      background: #000;
    }
  </style>
</head>
<body>
  <h1>Barcode & QR Code Generator & Scanner</h1>

  <div id="main-options">
    <button class="button" onclick="showGenerator()">Generate Barcode</button>
    <button class="button" onclick="showQRCodeGenerator()">Generate QR Code</button>
    <button class="button" onclick="showScanner()">Scan Barcode</button>
    <button class="button" onclick="showQRCodeScanner()">Scan QR Code</button>
  </div>

  <div id="generator" class="card" style="display:none">
    <h2>Generate a Barcode</h2>
    <input id="barcode-input" type="text" placeholder="Enter text to encode" oninput="generateBarcode()" />
    <svg id="barcode"></svg>
    <button class="button" onclick="goBack()">Back</button>
    <button class="button" onclick="goHome()">Home</button>
  </div>

  <div id="qr-generator" class="card" style="display:none">
    <h2>Generate a QR Code</h2>
    <input id="qr-input" type="text" placeholder="Enter text to encode" oninput="generateQRCode()" />
    <canvas id="qr-code"></canvas>
    <button class="button" onclick="goBack()">Back</button>
    <button class="button" onclick="goHome()">Home</button>
  </div>

  <div id="scanner" class="card" style="display:none">
    <h2>Scan a Barcode</h2>
    <div id="reader"></div>
    <p id="scan-result"></p>
    <p>Scanned Items: <span id="scan-count">0</span></p>
    <button class="button" onclick="stopScanner()">Back</button>
    <button class="button" onclick="restartScanner('barcode')">Restart Barcode Scanner</button>
    <button class="button" onclick="goHome()">Home</button>
  </div>

  <div id="qrscanner" class="card" style="display:none">
    <h2>Scan a QR Code</h2>
    <div id="qr-reader"></div>
    <p id="qrscan-result"></p>
    <p>Scanned QR Codes: <span id="qrscan-count">0</span></p>
    <button class="button" onclick="stopScanner()">Back</button>
    <button class="button" onclick="restartScanner('qr')">Restart QR Code Scanner</button>
    <button class="button" onclick="goHome()">Home</button>
  </div>

  <script>
    let scanCount = 0; // Counter for barcode scans
    let qrScanCount = 0; // Counter for QR code scans

    function showGenerator() {
      document.getElementById('main-options').style.display = 'none';
      document.getElementById('generator').style.display = 'block';
    }

    function showQRCodeGenerator() {
      document.getElementById('main-options').style.display = 'none';
      document.getElementById('qr-generator').style.display = 'block';
    }

    function showScanner() {
      document.getElementById('main-options').style.display = 'none';
      document.getElementById('scanner').style.display = 'block';
      startBarcodeScanner();
    }

    function showQRCodeScanner() {
      document.getElementById('main-options').style.display = 'none';
      document.getElementById('qrscanner').style.display = 'block';
      startQRCodeScanner();
    }

    function goBack() {
      document.getElementById('generator').style.display = 'none';
      document.getElementById('qr-generator').style.display = 'none';
      document.getElementById('scanner').style.display = 'none';
      document.getElementById('qrscanner').style.display = 'none';
      document.getElementById('main-options').style.display = 'block';
      stopScanner();
    }

    function goHome() {
      document.getElementById('generator').style.display = 'none';
      document.getElementById('qr-generator').style.display = 'none';
      document.getElementById('scanner').style.display = 'none';
      document.getElementById('qrscanner').style.display = 'none';
      document.getElementById('main-options').style.display = 'block';
      stopScanner();
    }

    function generateBarcode() {
      const text = document.getElementById('barcode-input').value;
      JsBarcode("#barcode", text || " ", { format: "CODE128", lineColor: "#000", width: 2, height: 100, displayValue: true });
    }

    function generateQRCode() {
      const text = document.getElementById('qr-input').value;
      const qrCodeCanvas = document.getElementById('qr-code');
      const ctx = qrCodeCanvas.getContext('2d');
      const qrCode = new QRCode();
      qrCode.makeCode(text || " ");
      const imgData = qrCode.getModuleCount();
      ctx.clearRect(0, 0, qrCodeCanvas.width, qrCodeCanvas.height);
      ctx.fillStyle = "black";
      const size = qrCodeCanvas.width / imgData.length;
      imgData.forEach((row, rowIndex) => {
        row.forEach((col, colIndex) => {
          if (col) {
            ctx.fillRect(colIndex * size, rowIndex * size, size, size);
          }
        });
      });
    }

    function startBarcodeScanner() {
      scanCount = 0;
      document.getElementById("scan-count").textContent = scanCount;

      Quagga.init({
        inputStream: {
          name: "Live",
          type: "LiveStream",
          target: document.querySelector('#reader'),
          constraints: { facingMode: "environment" }
        },
        decoder: { readers: ["code_128_reader", "ean_13_reader", "upc_reader"] }
      }, function(err) {
        if (err) {
          console.error("Quagga initialization failed:", err);
          return;
        }
        Quagga.start();
      });

      Quagga.onDetected(function(result) {
        const code = result.codeResult.code;
        handleBarcodeScan(code);
      });
    }

    function startQRCodeScanner() {
      qrScanCount = 0;
      document.getElementById("qrscan-count").textContent = qrScanCount;

      if (navigator.mediaDevices && navigator.mediaDevices.getUserMedia) {
        navigator.mediaDevices.getUserMedia({ video: { facingMode: "environment" } })
          .then(function(stream) {
            const video = document.createElement('video');
            video.srcObject = stream;
            video.setAttribute('playsinline', true);
            video.play();
            const canvas = document.createElement('canvas');
            const context = canvas.getContext('2d');
            document.getElementById('qr-reader').appendChild(video);

            const scanFrame = () => {
              context.drawImage(video, 0, 0, canvas.width, canvas.height);
              const imageData = context.getImageData(0, 0, canvas.width, canvas.height);
              const code = jsQR(imageData.data, canvas.width, canvas.height);

              if (code) {
                handleQRCodeScan(code.data);
              }
              requestAnimationFrame(scanFrame);
            };

            scanFrame();
          }).catch(function(err) {
            console.error("Camera access denied or not available:", err);
            alert("Camera access is required for scanning QR codes.");
          });
      } else {
        alert("Your browser doesn't support camera access.");
      }
    }

    function handleBarcodeScan(scannedData) {
      scanCount++;
      document.getElementById("scan-count").textContent = scanCount;

      const resultEl = document.getElementById("scan-result");
      if (scannedData.startsWith("http://") || scannedData.startsWith("https://")) {
        resultEl.innerHTML = `Scanned Result: <a href="${scannedData}" target="_blank">${scannedData}</a>`;
      } else {
        resultEl.textContent = "Scanned Result: " + scannedData;
      }
    }

    function handleQRCodeScan(scannedData) {
      qrScanCount++;
      document.getElementById("qrscan-count").textContent = qrScanCount;

      const resultEl = document.getElementById("qrscan-result");
      if (scannedData.startsWith("http://") || scannedData.startsWith("https://")) {
        resultEl.innerHTML = `Scanned Result: <a href="${scannedData}" target="_blank">${scannedData}</a>`;
      } else {
        resultEl.textContent = "Scanned Result: " + scannedData;
      }
    }

    function stopScanner() {
      if (Quagga) {
        Quagga.stop();
        Quagga.offDetected();
      }
    }

    function restartScanner(scannerType) {
      stopScanner();
      if (scannerType === 'barcode') {
        startBarcodeScanner();
      } else if (scannerType === 'qr') {
        startQRCodeScanner();
      }
    }
  </script>
</body>
</html>
