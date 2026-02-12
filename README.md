# dinn<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🌟 OPERATION: DINNER DATE with washo_luv 🌟</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', Courier, monospace;
            background: #0a0f0f;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            position: relative;
        }

        /* Matrix Rain Effect */
        #matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            opacity: 0.15;
        }

        /* Main Terminal */
        .terminal {
            background: rgba(10, 20, 10, 0.95);
            border: 3px solid #00ff9d;
            border-radius: 15px;
            padding: 30px;
            max-width: 800px;
            width: 100%;
            position: relative;
            z-index: 10;
            box-shadow: 0 0 30px rgba(0, 255, 157, 0.3);
            backdrop-filter: blur(5px);
            color: #00ff9d;
            animation: flicker 4s infinite;
        }

        @keyframes flicker {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.98; }
        }

        .terminal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #00ff9d;
            padding-bottom: 15px;
            margin-bottom: 25px;
            font-size: 14px;
        }

        .terminal-title {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .led {
            width: 12px;
            height: 12px;
            background: #00ff9d;
            border-radius: 50%;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.3; }
        }

        /* ASCII Art */
        .ascii-art {
            font-family: monospace;
            white-space: pre;
            font-size: 10px;
            line-height: 1.2;
            color: #00ff9d;
            text-align: center;
            margin-bottom: 20px;
            animation: glow 3s infinite;
        }

        @keyframes glow {
            0%, 100% { text-shadow: 0 0 5px #00ff9d; }
            50% { text-shadow: 0 0 15px #00ff9d; }
        }

        /* Progress Bar */
        .system-status {
            background: #1a2a1a;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 25px;
            border: 1px solid #00ff9d;
        }

        .status-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 15px;
        }

        .status-label {
            width: 150px;
            font-size: 14px;
        }

        .status-bar-container {
            flex: 1;
            height: 20px;
            background: #0a1a0a;
            border: 1px solid #00ff9d;
            position: relative;
            overflow: hidden;
        }

        .status-bar-fill {
            height: 100%;
            width: 0%;
            background: linear-gradient(90deg, #00ff9d, #00cc7a);
            animation: fillBar 2s ease-out forwards;
            position: relative;
        }

        .status-bar-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Command Line */
        .command-line {
            background: #0a1a0a;
            border: 1px solid #00ff9d;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 25px;
            font-family: monospace;
        }

        .prompt {
            color: #00ff9d;
            margin-bottom: 10px;
            font-size: 16px;
        }

        .prompt::before {
            content: '$ ';
            font-weight: bold;
        }

        .cursor {
            display: inline-block;
            width: 10px;
            height: 20px;
            background: #00ff9d;
            animation: blink 1s infinite;
            vertical-align: middle;
        }

        .command-history {
            max-height: 150px;
            overflow-y: auto;
            margin-bottom: 15px;
            padding: 10px;
            background: #0a150a;
            border-radius: 5px;
        }

        .command-entry {
            margin-bottom: 8px;
            font-size: 14px;
            color: #aaffdd;
        }

        .command-entry.error {
            color: #ff6b6b;
        }

        .command-entry.success {
            color: #00ff9d;
        }

        /* Encryption Panel */
        .encryption-panel {
            background: #1a2a1a;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 25px;
            border: 1px solid #00ff9d;
        }

        .encryption-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
        }

        .encryption-key {
            font-family: monospace;
            font-size: 12px;
            word-break: break-all;
            background: #0a1a0a;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
        }

        .encryption-bars {
            display: flex;
            gap: 5px;
            height: 30px;
            align-items: flex-end;
        }

        .encryption-bar {
            flex: 1;
            background: linear-gradient(0deg, #00ff9d, #00cc7a);
            height: 0%;
            transition: height 0.5s;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        /* Neural Network Visualization */
        .neural-network {
            background: #0a1a0a;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 25px;
            display: flex;
            justify-content: space-around;
            border: 1px solid #00ff9d;
        }

        .node {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }

        .node-circle {
            width: 30px;
            height: 30px;
            border: 2px solid #00ff9d;
            border-radius: 50%;
            animation: pulse 2s infinite;
        }

        .node-line {
            width: 2px;
            height: 40px;
            background: linear-gradient(to bottom, #00ff9d, transparent);
        }

        /* Binary Rain */
        .binary-rain {
            font-size: 12px;
            line-height: 1;
            opacity: 0.5;
            height: 60px;
            overflow: hidden;
            margin-bottom: 20px;
        }

        /* Main Question */
        .main-question {
            text-align: center;
            margin: 30px 0;
            padding: 25px;
            background: linear-gradient(135deg, #1a3a1a, #0a1f0a);
            border: 2px solid #00ff9d;
            border-radius: 15px;
            animation: borderGlow 2s infinite;
        }

        @keyframes borderGlow {
            0%, 100% { border-color: #00ff9d; box-shadow: 0 0 20px rgba(0,255,157,0.3); }
            50% { border-color: #00cc7a; box-shadow: 0 0 40px rgba(0,255,157,0.6); }
        }

        .question-text {
            font-size: 32px;
            font-weight: bold;
            color: #00ff9d;
            text-transform: uppercase;
            letter-spacing: 4px;
            margin-bottom: 15px;
            animation: glitch 3s infinite;
        }

        @keyframes glitch {
            0%, 100% { transform: skew(0deg); }
            95% { transform: skew(5deg); }
            96% { transform: skew(-5deg); }
            97% { transform: skew(3deg); }
            98% { transform: skew(-3deg); }
        }

        .sub-question {
            font-size: 18px;
            color: #88ffaa;
            margin-top: 10px;
        }

        /* Control Panel */
        .control-panel {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-bottom: 25px;
        }

        .panel-section {
            background: #1a2a1a;
            padding: 15px;
            border-radius: 10px;
            border: 1px solid #00ff9d;
        }

        .panel-title {
            font-size: 12px;
            text-transform: uppercase;
            margin-bottom: 15px;
            color: #88ffaa;
            border-bottom: 1px solid #00ff9d;
            padding-bottom: 5px;
        }

        .date-selector {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }

        .date-option {
            padding: 10px;
            background: #0a1a0a;
            border: 1px solid #00ff9d;
            color: #00ff9d;
            cursor: pointer;
            text-align: center;
            font-size: 12px;
            transition: all 0.3s;
        }

        .date-option:hover {
            background: #00ff9d;
            color: #0a1a0a;
            box-shadow: 0 0 15px #00ff9d;
        }

        .date-option.selected {
            background: #00ff9d;
            color: #0a1a0a;
            border: 2px solid white;
        }

        /* Authorization Buttons */
        .auth-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 30px;
        }

        .auth-btn {
            padding: 15px 40px;
            font-size: 18px;
            font-family: 'Courier New', monospace;
            font-weight: bold;
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            transition: all 0.3s;
        }

        .btn-approve {
            background: #0a1a0a;
            color: #00ff9d;
            border: 2px solid #00ff9d;
            box-shadow: 0 0 20px rgba(0,255,157,0.3);
        }

        .btn-approve:hover {
            background: #00ff9d;
            color: #0a1a0a;
            box-shadow: 0 0 40px #00ff9d;
        }

        .btn-deny {
            background: #1a0a0a;
            color: #ff6b6b;
            border: 2px solid #ff6b6b;
            box-shadow: 0 0 20px rgba(255,107,107,0.3);
        }

        .btn-deny:hover {
            background: #ff6b6b;
            color: #0a0a0a;
            box-shadow: 0 0 40px #ff6b6b;
        }

        .btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }

        /* Quantum State Indicator */
        .quantum-state {
            background: #0a1a0a;
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
            border: 1px solid #00ff9d;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .quantum-spinner {
            width: 30px;
            height: 30px;
            border: 3px solid transparent;
            border-top: 3px solid #00ff9d;
            border-right: 3px solid #00ff9d;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Terminal Output */
        .terminal-output {
            background: #0a150a;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
            border-left: 4px solid #00ff9d;
            font-size: 14px;
            max-height: 100px;
            overflow-y: auto;
        }

        /* Hack Effect */
        .hack-effect {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1000;
            display: none;
        }

        .hack-effect.active {
            display: block;
            animation: hackFlash 0.5s;
        }

        @keyframes hackFlash {
            0%, 100% { background: rgba(0,255,157,0); }
            50% { background: rgba(0,255,157,0.2); }
        }

        /* Frequency Analyzer */
        .frequency-analyzer {
            display: flex;
            gap: 5px;
            height: 50px;
            margin-top: 15px;
        }

        .freq-bar {
            flex: 1;
            background: #00ff9d;
            height: 0%;
            transition: height 0.1s;
            animation: frequency 0.5s infinite;
        }

        @keyframes frequency {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }
    </style>
</head>
<body>
    <!-- Matrix Background -->
    <canvas id="matrix-bg"></canvas>

    <!-- Main Terminal -->
    <div class="terminal">
        <!-- Header -->
        <div class="terminal-header">
            <div class="terminal-title">
                <span class="led"></span>
                <span>OPERATION: DATE_NIGHT // TERMINAL v2.0</span>
            </div>
            <div>ENCRYPTED CONNECTION • wash o_luv@dinner.date</div>
        </div>

        <!-- ASCII Art -->
        <div class="ascii-art">
            ╔══════════════════════════════════════╗
            ║     ░▒▓█ D I N N E R   D A T E █▓▒░     ║
            ║     ════════════════════════════     ║
            ║     [ SYSTEM:// WASHO_LUV ]          ║
            ╚══════════════════════════════════════╝
        </div>

        <!-- System Status -->
        <div class="system-status">
            <div class="status-item">
                <span class="status-label">> HEARTBEAT SIGNAL:</span>
                <div class="status-bar-container">
                    <div class="status-bar-fill" style="width: 98%;"></div>
                </div>
                <span>98%</span>
            </div>
            <div class="status-item">
                <span class="status-label">> EXCITEMENT LEVEL:</span>
                <div class="status-bar-container">
                    <div class="status-bar-fill" style="width: 100%;"></div>
                </div>
                <span>100%</span>
            </div>
            <div class="status-item">
                <span class="status-label">> NERVOUSNESS:</span>
                <div class="status-bar-container">
                    <div class="status-bar-fill" style="width: 75%;"></div>
                </div>
                <span>75%</span>
            </div>
        </div>

        <!-- Binary Rain -->
        <div class="binary-rain" id="binaryRain">
            01010111 01100001 01110011 01101000 01101111 01011111 01101100 01110101 01110110
        </div>

        <!-- Command Line Interface -->
        <div class="command-line">
            <div class="command-history" id="commandHistory">
                <div class="command-entry">$ system.scan --target=washo_luv</div>
                <div class="command-entry success">>> Target acquired: wash o_luv 💫</div>
                <div class="command-entry">$ emotions.detect --user=washo_luv</div>
                <div class="command-entry success">>> Compatibility: 99.9%</div>
            </div>
            <div class="prompt">
                ./ask_for_date --user=washo_luv --query="dinner" 
                <span class="cursor"></span>
            </div>
        </div>

        <!-- Encryption Panel -->
        <div class="encryption-panel">
            <div class="encryption-header">
                <span>🔐 HEART ENCRYPTION PROTOCOL</span>
                <span>AES-256 • SECURE</span>
            </div>
            <div class="encryption-key" id="encryptionKey">
                4D 69 73 73 20 79 6F 75 20 77 61 73 68 6F 5F 6C 75 76
            </div>
            <div class="encryption-bars" id="encryptionBars">
                <!-- Bars generated by JS -->
            </div>
        </div>

        <!-- Neural Network Visualization -->
        <div class="neural-network">
            <div class="node">
                <div class="node-circle"></div>
                <div class="node-line"></div>
                <div style="font-size: 10px;">YOU</div>
            </div>
            <div class="node">
                <div class="node-circle" style="animation-delay: 0.5s;"></div>
                <div class="node-line"></div>
                <div style="font-size: 10px;">💕</div>
            </div>
            <div class="node">
                <div class="node-circle" style="animation-delay: 1s;"></div>
                <div class="node-line"></div>
                <div style="font-size: 10px;">WASHO</div>
            </div>
        </div>

        <!-- MAIN QUESTION -->
        <div class="main-question">
            <div class="question-text">
                🚀 INITIATE DATE SEQUENCE?
            </div>
            <div class="sub-question">
                >> Access permission required from washo_luv <<
            </div>
            <div style="font-size: 24px; margin: 20px 0; color: #00ff9d;">
                "can we go for a dinner date?"
            </div>
        </div>

        <!-- Control Panel -->
        <div class="control-panel">
            <div class="panel-section">
                <div class="panel-title">📡 DATE LAUNCH SEQUENCE</div>
                <div class="date-selector" id="dateSelector">
                    <div class="date-option" onclick="selectDate(0, this)">T-24h • FRIDAY</div>
                    <div class="date-option" onclick="selectDate(1, this)">T-48h • SATURDAY</div>
                    <div class="date-option" onclick="selectDate(2, this)">T-72h • SUNDAY</div>
                    <div class="date-option" onclick="selectDate(3, this)">T-0 • SURPRISE</div>
                </div>
            </div>
            
            <div class="panel-section">
                <div class="panel-title">🎯 TARGET COORDINATES</div>
                <div style="margin-bottom: 10px;">
                    <div>LAT: 13°44'24.5"N</div>
                    <div>LONG: 100°29'42.6"E</div>
                    <div style="font-size: 10px; margin-top: 10px;">>> YOUR LOCATION</div>
                </div>
            </div>
        </div>

        <!-- Quantum State -->
        <div class="quantum-state">
            <div>⚛️ QUANTUM STATE: Superposition of YES/NO</div>
            <div class="quantum-spinner"></div>
        </div>

        <!-- Authorization Buttons -->
        <div class="auth-buttons">
            <button class="auth-btn btn-approve" onclick="authorize('approve')" id="approveBtn" disabled>
                🔓 GRANT ACCESS [YES]
            </button>
            <button class="auth-btn btn-deny" onclick="authorize('deny')" id="denyBtn">
                🔒 DENY ACCESS [NO]
            </button>
        </div>

        <!-- Frequency Analyzer -->
        <div class="frequency-analyzer" id="frequencyAnalyzer">
            <!-- Bars generated by JS -->
        </div>

        <!-- Terminal Output -->
        <div class="terminal-output" id="terminalOutput">
            [*] System ready. Awaiting authorization from washo_luv...
        </div>
    </div>

    <!-- Hack Effect Overlay -->
    <div class="hack-effect" id="hackEffect"></div>

    <script>
        // Matrix Rain Effect
        const canvas = document.getElementById('matrix-bg');
        const ctx = canvas.getContext('2d');

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        resizeCanvas();

        const matrixChars = "01アイウエオカキクケコサシスセソタチツテトナニヌネノハヒフヘホマミムメモヤユヨラリルレロワヲン";
        const fontSize = 14;
        const columns = canvas.width / fontSize;
        const drops = [];

        for (let x = 0; x < columns; x++) {
            drops[x] = Math.floor(Math.random() * canvas.height / fontSize);
        }

        function drawMatrix() {
            ctx.fillStyle = 'rgba(0, 20, 0, 0.05)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            ctx.fillStyle = '#00ff9d';
            ctx.font = fontSize + 'px monospace';
            
            for (let i = 0; i < drops.length; i++) {
                const text = matrixChars.charAt(Math.floor(Math.random() * matrixChars.length));
                ctx.fillText(text, i * fontSize, drops[i] * fontSize);
                
                if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    drops[i] = 0;
                }
                drops[i]++;
            }
        }

        setInterval(drawMatrix, 50);

        // Binary Rain Animation
        function updateBinaryRain() {
            const binaryEl = document.getElementById('binaryRain');
            setInterval(() => {
                const binary = Math.random().toString(2).substr(2, 32);
                binaryEl.textContent = binary + ' ' + binary + ' ' + binary;
            }, 100);
        }
        updateBinaryRain();

        // Encryption Bars
        function initEncryptionBars() {
            const container = document.getElementById('encryptionBars');
            for (let i = 0; i < 20; i++) {
                const bar = document.createElement('div');
                bar.className = 'encryption-bar';
                bar.style.height = Math.random() * 30 + 10 + 'px';
                bar.style.animationDelay = i * 0.1 + 's';
                container.appendChild(bar);
            }
        }
        initEncryptionBars();

        // Frequency Analyzer
        function initFrequencyAnalyzer() {
            const container = document.getElementById('frequencyAnalyzer');
            for (let i = 0; i < 20; i++) {
                const bar = document.createElement('div');
                bar.className = 'freq-bar';
                bar.style.animationDelay = i * 0.05 + 's';
                bar.style.height = Math.random() * 40 + 10 + 'px';
                container.appendChild(bar);
                
                setInterval(() => {
                    bar.style.height = Math.random() * 40 + 10 + 'px';
                }, 200);
            }
        }
        initFrequencyAnalyzer();

        // Date Selection
        let selectedDateElement = null;
        let selectedDateText = '';

        window.selectDate = function(index, element) {
            if (selectedDateElement) {
                selectedDateElement.classList.remove('selected');
            }
            element.classList.add('selected');
            selectedDateElement = element;
            selectedDateText = element.textContent;
            
            // Enable approve button
            document.getElementById('approveBtn').disabled = false;
            
            // Update terminal
            const terminal = document.getElementById('terminalOutput');
            terminal.innerHTML = `[+] Date target acquired: ${selectedDateText}<br>[*] Ready for authorization`;
            
            // Update encryption key
            const dates = ['FRI', 'SAT', 'SUN', 'SURP'];
            document.getElementById('encryptionKey').textContent = 
                `DATE_SEQUENCE: ${dates[index]} // AWAITING_CONFIRMATION`;
        };

        // Authorization System
        window.authorize = function(action) {
            const hackEffect = document.getElementById('hackEffect');
            hackEffect.classList.add('active');
            
            setTimeout(() => {
                hackEffect.classList.remove('active');
            }, 500);

            if (action === 'approve') {
                if (!selectedDateElement) {
                    alert('⚠️ ERROR: Date sequence not selected!');
                    return;
                }
                
                // Success sequence
                document.getElementById('terminalOutput').innerHTML = `
                    [✓] ACCESS GRANTED! ✅<br>
                    [✓] Date confirmed with washo_luv! 💕<br>
                    [✓] Launch sequence: ${selectedDateText}<br>
                    [✓] Encrypting feelings...<br>
                    [✓] Mission status: SUCCESS!
                `;
                
                // Change ASCII art
                document.querySelector('.ascii-art').innerHTML = `
                    ╔══════════════════════════════════════╗
                    ║     ░▒▓█ D A T E   S E T ! █▓▒░     ║
                    ║     ════════════════════════════     ║
                    ║     [ STATUS: // APPROVED ]          ║
                    ║     [ WITH: // WASHO_LUV ]          ║
                    ╚══════════════════════════════════════╝
                `;
                
                // Update quantum state
                document.querySelector('.quantum-state').innerHTML = `
                    <div>⚛️ QUANTUM STATE: COLLAPSED TO YES</div>
                    <div style="color: #00ff9d;">💖 DATE CONFIRMED 💖</div>
                `;
                
                // Disable buttons
                document.getElementById('approveBtn').disabled = true;
                document.getElementById('denyBtn').disabled = true;
                
                // Add success to command history
                const history = document.getElementById('commandHistory');
                history.innerHTML += `
                    <div class="command-entry success">$ sudo grant_permission --user=washo_luv</div>
                    <div class="command-entry success">>> Permission granted! Date confirmed! 🎉</div>
                `;
                
            } else {
                // Deny sequence - but it's tricky!
                const denyBtn = document.getElementById('denyBtn');
                const x = Math.random() * window.innerWidth * 0.7;
                const y = Math.random() * window.innerHeight * 0.7;
                
                denyBtn.style.position = 'fixed';
                denyBtn.style.left = x + 'px';
                denyBtn.style.top = y + 'px';
                denyBtn.style.zIndex = '9999';
                
                document.getElementById('terminalOutput').innerHTML = `
                    [✗] ACCESS DENIED?<br>
                    [*] Initiating override protocol...<br>
                    [*] washo_luv permission required<br>
                    [*] Please try again with YES 💝
                `;
                
                // Make approve button pulse more
                document.getElementById('approveBtn').style.animation = 'pulse 0.5s infinite';
            }
        };

        // Encryption Key Animation
        function updateEncryptionKey() {
            const keyEl = document.getElementById('encryptionKey');
            setInterval(() => {
                if (!selectedDateElement) {
                    const hex = Array.from('washo_luv').map(c => 
                        c.charCodeAt(0).toString(16)
                    ).join(' ');
                    keyEl.textContent = hex.toUpperCase();
                }
            }, 2000);
        }
        updateEncryptionKey();

        // Glitch Effect on Terminal
        function glitchTerminal() {
            const terminal = document.querySelector('.terminal');
            setInterval(() => {
                if (Math.random() > 0.95) {
                    terminal.style.transform = 'skew(' + (Math.random() * 2 - 1) + 'deg)';
                    setTimeout(() => {
                        terminal.style.transform = 'skew(0deg)';
                    }, 100);
                }
            }, 2000);
        }
        glitchTerminal();

        // Easter Egg: Type "washo_luv" for secret effect
        let typed = '';
        document.addEventListener('keydown', (e) => {
            typed += e.key;
            if (typed.toLowerCase().includes('washo_luv')) {
                document.body.style.background = 'linear-gradient(45deg, #0a0f0f, #1a3a1a)';
                for (let i = 0; i < 50; i++) {
                    setTimeout(() => {
                        const bar = document.createElement('div');
                        bar.className = 'encryption-bar';
                        bar.style.position = 'fixed';
                        bar.style.left = Math.random() * 100 + '%';
                        bar.style.top = Math.random() * 100 + '%';
                        bar.style.width = '20px';
                        bar.style.height = '20px';
                        bar.style.background = '#00ff9d';
                        bar.style.zIndex = '9999';
                        document.body.appendChild(bar);
                        setTimeout(() => bar.remove(), 1000);
                    }, i * 20);
                }
                typed = '';
            }
        });

        // Window resize handler
        window.addEventListener('resize', resizeCanvas);

        // Initialize with message
        window.onload = function() {
            setTimeout(() => {
                document.getElementById('terminalOutput').innerHTML += `
                    <br>[*] washo_luv detected in system...
                    <br>[*] Initializing date protocol...
                `;
            }, 1000);
            
            setTimeout(() => {
                const history = document.getElementById('commandHistory');
                history.innerHTML += `
                    <div class="command-entry">$ feelings.analyze --target=washo_luv</div>
                    <div class="command-entry success">>> Status: 💕 💕 💕</div>
                `;
            }, 2000);
        };
    </script>
</body>
</html>
