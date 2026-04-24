<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PNK - Security Dashboard</title>
    <style>
        body {
            background-color: #0a0a0a;
            color: #00ff41;
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }
        .monitor-box {
            border: 2px solid #00ff41;
            width: 80%;
            padding: 20px;
            box-shadow: 0 0 15px #00ff41;
            background: rgba(0, 50, 0, 0.1);
        }
        h1 { text-align: center; text-transform: uppercase; letter-spacing: 5px; }
        .status-active { color: #00ff41; font-weight: bold; }
        .log-container {
            background: black;
            border: 1px inset #00ff41;
            height: 200px;
            overflow-y: scroll;
            padding: 10px;
            margin-top: 20px;
            font-size: 14px;
        }
        .btn-link {
            background: #00ff41;
            color: black;
            padding: 10px 20px;
            text-decoration: none;
            font-weight: bold;
            display: inline-block;
            margin-top: 15px;
        }
        .admin-protected { border-left: 5px solid cyan; padding-left: 10px; margin: 5px 0; }
    </style>
</head>
<body>

    <h1>🛡️ PNK Anti-Kudeta 🛡️</h1>

    <div class="monitor-box">
        <p><strong>System Status:</strong> <span class="status-active">ONLINE (ENCRYPTED)</span></p>
        <p><strong>Owner ID:</strong> 628xxx (Satria)</p>
        
        <hr color="#00ff41">
        
        <h3>Admin Terlindungi:</h3>
        <div class="admin-protected">1. 628123456789 (Whitelist)</div>
        <div class="admin-protected">2. 628987654321 (Whitelist)</div>

        <div class="log-container" id="logs">
            [SYSTEM]: Mencari aktivitas mencurigakan...<br>
            [SYSTEM]: Perlindungan otomatis aktif.<br>
            [SYSTEM]: Link Grup terdeteksi: https://chat.whatsapp.com/LInkGrup...
        </div>

        <center>
            <a href="https://chat.whatsapp.com/LInkGrupAnda" class="btn-link">HUBUNGKAN KE GRUP</a>
        </center>
    </div>

    <script>
        // Simulasi Logika Website Memeriksa User Jahat
        const logBox = document.getElementById('logs');
        
        function addLog(message) {
            const time = new Date().toLocaleTimeString();
            logBox.innerHTML += `[${time}] ${message}<br>`;
            logBox.scrollTop = logBox.scrollHeight;
        }

        // Contoh simulasi otomatis
        setTimeout(() => addLog("⚠️ Deteksi upaya 'Demote' dari Admin Luar!"), 3000);
        setTimeout(() => addLog("🔍 SCANNING: User terdeteksi berbahaya."), 5000);
        setTimeout(() => addLog("🛡️ ACTION: Jabatan dikembalikan. Pelaku di-ban."), 7000);
    </script>
</body>
</html>
