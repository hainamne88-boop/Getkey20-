<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HNam Script - Get Your Free Key</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #334155 100%);
            color: #e2e8f0;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            background: rgba(15, 23, 42, 0.8);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5),
                        0 0 0 1px rgba(59, 130, 246, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(59, 130, 246, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        /* Hiệu ứng ánh sáng */
        .container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(59, 130, 246, 0.1) 0%, transparent 70%);
            z-index: -1;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .logo {
            font-size: 48px;
            color: #3b82f6;
            margin-bottom: 15px;
            text-shadow: 0 0 20px rgba(59, 130, 246, 0.5);
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from { text-shadow: 0 0 10px rgba(59, 130, 246, 0.5); }
            to { text-shadow: 0 0 30px rgba(59, 130, 246, 0.8), 0 0 40px rgba(59, 130, 246, 0.6); }
        }
        
        h1 {
            font-size: 2.8rem;
            background: linear-gradient(to right, #3b82f6, #8b5cf6);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 10px;
            font-weight: 800;
            letter-spacing: 1px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: #94a3b8;
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.6;
        }
        
        .steps-container {
            display: flex;
            flex-direction: column;
            gap: 25px;
            margin-bottom: 40px;
        }
        
        .step {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 15px;
            padding: 25px;
            border-left: 4px solid #3b82f6;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
        }
        
        .step:hover {
            background: rgba(30, 41, 59, 0.8);
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }
        
        .step-number {
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: bold;
            margin-right: 20px;
            flex-shrink: 0;
        }
        
        .step-content h3 {
            font-size: 1.4rem;
            margin-bottom: 8px;
            color: #f8fafc;
        }
        
        .step-content p {
            color: #cbd5e1;
            line-height: 1.6;
        }
        
        /* Nút Get Key - Hiệu ứng bóng đổ mạnh */
        .btn-get-key {
            display: block;
            width: 100%;
            padding: 20px;
            background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
            color: white;
            border: none;
            border-radius: 15px;
            font-size: 1.4rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            margin: 30px 0;
            letter-spacing: 1px;
            box-shadow: 
                0 10px 20px rgba(59, 130, 246, 0.3),
                0 6px 6px rgba(59, 130, 246, 0.2),
                inset 0 1px 0 rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .btn-get-key::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }
        
        .btn-get-key:hover {
            transform: translateY(-5px);
            box-shadow: 
                0 15px 30px rgba(59, 130, 246, 0.4),
                0 10px 10px rgba(59, 130, 246, 0.3),
                inset 0 1px 0 rgba(255, 255, 255, 0.3);
        }
        
        .btn-get-key:hover::before {
            left: 100%;
        }
        
        .btn-get-key:active {
            transform: translateY(-2px);
        }
        
        /* Nút Follow TikTok - Hiệu ứng TikTok */
        .btn-follow-tiktok {
            display: none;
            width: 100%;
            padding: 20px;
            background: linear-gradient(135deg, #000000 0%, #25F4EE 30%, #FE2C55 100%);
            color: white;
            border: none;
            border-radius: 15px;
            font-size: 1.4rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            margin: 20px 0;
            letter-spacing: 1px;
            box-shadow: 
                0 10px 20px rgba(37, 244, 238, 0.3),
                0 6px 6px rgba(254, 44, 85, 0.2),
                inset 0 1px 0 rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .btn-follow-tiktok i {
            margin-right: 10px;
            font-size: 1.6rem;
        }
        
        .btn-follow-tiktok::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }
        
        .btn-follow-tiktok:hover {
            transform: translateY(-5px);
            box-shadow: 
                0 15px 30px rgba(37, 244, 238, 0.4),
                0 10px 10px rgba(254, 44, 85, 0.3),
                inset 0 1px 0 rgba(255, 255, 255, 0.3);
        }
        
        .btn-follow-tiktok:hover::before {
            left: 100%;
        }
        
        /* Countdown timer */
        .countdown-container {
            display: none;
            text-align: center;
            margin: 30px 0;
            padding: 25px;
            background: rgba(30, 41, 59, 0.6);
            border-radius: 15px;
            border: 1px solid rgba(59, 130, 246, 0.3);
        }
        
        .countdown-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: #f8fafc;
        }
        
        .countdown {
            font-size: 3.5rem;
            font-weight: 800;
            color: #3b82f6;
            text-shadow: 0 0 15px rgba(59, 130, 246, 0.5);
            margin: 10px 0;
            font-family: 'Courier New', monospace;
        }
        
        .countdown-text {
            color: #94a3b8;
            font-size: 1.1rem;
        }
        
        /* Key display */
        .key-container {
            display: none;
            text-align: center;
            margin: 30px 0;
            padding: 30px;
            background: rgba(30, 41, 59, 0.6);
            border-radius: 15px;
            border: 1px solid rgba(59, 130, 246, 0.3);
            animation: fadeIn 0.8s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .key-title {
            font-size: 1.6rem;
            margin-bottom: 20px;
            color: #f8fafc;
        }
        
        .key-display {
            background: rgba(15, 23, 42, 0.8);
            border: 2px solid #3b82f6;
            border-radius: 10px;
            padding: 20px;
            font-size: 1.3rem;
            font-family: 'Courier New', monospace;
            color: #3b82f6;
            margin: 20px 0;
            word-break: break-all;
            box-shadow: 0 0 20px rgba(59, 130, 246, 0.2);
            position: relative;
        }
        
        .copy-btn {
            background: linear-gradient(135deg, #10b981 0%, #047857 100%);
            color: white;
            border: none;
            border-radius: 10px;
            padding: 12px 25px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 15px;
            box-shadow: 0 5px 15px rgba(16, 185, 129, 0.3);
        }
        
        .copy-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(16, 185, 129, 0.4);
        }
        
        .copy-btn:active {
            transform: translateY(-1px);
        }
        
        /* Footer */
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(59, 130, 246, 0.2);
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
        }
        
        .social-link {
            color: #94a3b8;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            color: #3b82f6;
            transform: translateY(-3px);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .container {
                padding: 25px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .step {
                flex-direction: column;
                text-align: center;
                padding: 20px;
            }
            
            .step-number {
                margin-right: 0;
                margin-bottom: 15px;
            }
            
            .countdown {
                font-size: 2.8rem;
            }
        }
        
        /* Animation for key generation */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .generating {
            animation: pulse 1.5s infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="logo">
                <i class="fas fa-key"></i>
            </div>
            <h1>HNam Script Key Generator</h1>
            <p class="subtitle">Nhận key miễn phí để kích hoạt script Teleport & Fly to Base độc quyền từ HNam Script</p>
        </div>
        
        <div class="steps-container">
            <div class="step">
                <div class="step-number">1</div>
                <div class="step-content">
                    <h3>Bấm Get Key</h3>
                    <p>Bấm nút "GET KEY NOW" để bắt đầu quá trình nhận key miễn phí</p>
                </div>
            </div>
            
            <div class="step">
                <div class="step-number">2</div>
                <div class="step-content">
                    <h3>Follow TikTok</h3>
                    <p>Follow tài khoản TikTok <strong>@hnam.script</strong> để hỗ trợ chúng tôi</p>
                </div>
            </div>
            
            <div class="step">
                <div class="step-number">3</div>
                <div class="step-content">
                    <h3>Chờ 30 Giây</h3>
                    <p>Chờ đếm ngược 30 giây để nhận key kích hoạt script</p>
                </div>
            </div>
            
            <div class="step">
                <div class="step-number">4</div>
                <div class="step-content">
                    <h3>Copy & Sử Dụng</h3>
                    <p>Copy key và dán vào script Teleport to Base của bạn</p>
                </div>
            </div>
        </div>
        
        <button class="btn-get-key" id="getKeyBtn">
            <i class="fas fa-key"></i> GET KEY NOW
        </button>
        
        <a href="https://www.tiktok.com/@hnam.script" target="_blank" class="btn-follow-tiktok" id="followTikTokBtn">
            <i class="fab fa-tiktok"></i> FOLLOW @hnam.script ON TIKTOK
        </a>
        
        <div class="countdown-container" id="countdownContainer">
            <div class="countdown-title">Đang đếm ngược để nhận key:</div>
            <div class="countdown" id="countdown">30</div>
            <div class="countdown-text">Vui lòng chờ trong giây lát...</div>
        </div>
        
        <div class="key-container" id="keyContainer">
            <div class="key-title">
                <i class="fas fa-gift"></i> KEY CỦA BẠN ĐÃ SẴN SÀNG!
            </div>
            <div class="key-display" id="keyDisplay">newkeyfree_token__@key=</div>
            <button class="copy-btn" id="copyBtn">
                <i class="fas fa-copy"></i> COPY KEY
            </button>
            <p style="margin-top: 15px; color: #94a3b8; font-size: 0.9rem;">
                Key có định dạng: newkeyfree_token__@key=xxxxxxxxxxxxxx
            </p>
        </div>
        
        <div class="footer">
            <p>© 2024 HNam Script. All rights reserved.</p>
            <p>Script Teleport to Base với tính năng Fly độc quyền</p>
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-tiktok"></i></a>
                <a href="#" class="social-link"><i class="fab fa-youtube"></i></a>
                <a href="#" class="social-link"><i class="fab fa-discord"></i></a>
                <a href="#" class="social-link"><i class="fab fa-github"></i></a>
            </div>
        </div>
    </div>
    
    <script>
        // DOM Elements
        const getKeyBtn = document.getElementById('getKeyBtn');
        const followTikTokBtn = document.getElementById('followTikTokBtn');
        const countdownContainer = document.getElementById('countdownContainer');
        const countdownElement = document.getElementById('countdown');
        const keyContainer = document.getElementById('keyContainer');
        const keyDisplay = document.getElementById('keyDisplay');
        const copyBtn = document.getElementById('copyBtn');
        
        // Biến trạng thái
        let countdown = 30;
        let countdownInterval;
        let isFollowing = false;
        
        // Sự kiện khi bấm nút Get Key
        getKeyBtn.addEventListener('click', function() {
            // Ẩn nút Get Key
            getKeyBtn.style.display = 'none';
            
            // Hiển thị nút Follow TikTok
            followTikTokBtn.style.display = 'block';
            
            // Thêm hiệu ứng cho nút Follow TikTok
            followTikTokBtn.classList.add('generating');
            
            // Hiển thị thông báo
            alert("Vui lòng follow TikTok @hnam.script để nhận key miễn phí!");
        });
        
        // Sự kiện khi bấm nút Follow TikTok
        followTikTokBtn.addEventListener('click', function() {
            // Mở TikTok trong tab mới (đã có trong href)
            // Đánh dấu đã follow
            isFollowing = true;
            
            // Ẩn nút Follow TikTok
            followTikTokBtn.style.display = 'none';
            followTikTokBtn.classList.remove('generating');
            
            // Hiển thị countdown
            countdownContainer.style.display = 'block';
            
            // Bắt đầu đếm ngược
            startCountdown();
        });
        
        // Hàm đếm ngược
        function startCountdown() {
            countdownElement.textContent = countdown;
            
            countdownInterval = setInterval(function() {
                countdown--;
                countdownElement.textContent = countdown;
                
                // Khi đếm ngược kết thúc
                if (countdown <= 0) {
                    clearInterval(countdownInterval);
                    
                    // Ẩn countdown
                    countdownContainer.style.display = 'none';
                    
                    // Hiển thị key
                    showKey();
                }
            }, 1000);
        }
        
        // Hàm tạo key ngẫu nhiên
        function generateRandomKey() {
            const chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
            let key = '';
            const keyLength = 14; // Độ dài phần xxxxxxxxxxxxxx
            
            for (let i = 0; i < keyLength; i++) {
                key += chars.charAt(Math.floor(Math.random() * chars.length));
            }
            
            return `newkeyfree_token__@key=${key}`;
        }
        
        // Hàm hiển thị key
        function showKey() {
            // Tạo key ngẫu nhiên
            const key = generateRandomKey();
            
            // Hiển thị key với hiệu ứng từng ký tự
            keyDisplay.textContent = '';
            keyContainer.style.display = 'block';
            
            let i = 0;
            const typeKey = setInterval(function() {
                if (i < key.length) {
                    keyDisplay.textContent += key.charAt(i);
                    i++;
                } else {
                    clearInterval(typeKey);
                    
                    // Thêm hiệu ứng hoàn thành
                    keyDisplay.style.animation = 'pulse 0.5s 3';
                    
                    // Hiển thị thông báo
                    setTimeout(function() {
                        alert("🎉 Chúc mừng! Key của bạn đã sẵn sàng. Hãy copy và sử dụng trong script!");
                    }, 500);
                }
            }, 50);
        }
        
        // Sự kiện copy key
        copyBtn.addEventListener('click', function() {
            const keyText = keyDisplay.textContent;
            
            // Sử dụng Clipboard API
            navigator.clipboard.writeText(keyText)
                .then(() => {
                    // Thay đổi text nút copy
                    const originalText = copyBtn.innerHTML;
                    copyBtn.innerHTML = '<i class="fas fa-check"></i> COPIED!';
                    copyBtn.style.background = 'linear-gradient(135deg, #10b981 0%, #047857 100%)';
                    
                    // Khôi phục sau 2 giây
                    setTimeout(() => {
                        copyBtn.innerHTML = originalText;
                    }, 2000);
                    
                    // Hiển thị thông báo
                    alert("✅ Key đã được copy vào clipboard! Dán vào script để sử dụng.");
                })
                .catch(err => {
                    console.error('Lỗi khi copy: ', err);
                    alert("❌ Không thể copy key. Vui lòng copy thủ công.");
                });
        });
        
        // Hiệu ứng khi load trang
        window.addEventListener('load', function() {
            document.querySelector('.container').style.opacity = '0';
            document.querySelector('.container').style.transform = 'translateY(20px)';
            
            setTimeout(function() {
                document.querySelector('.container').style.transition = 'opacity 0.8s ease, transform 0.8s ease';
                document.querySelector('.container').style.opacity = '1';
                document.querySelector('.container').style.transform = 'translateY(0)';
            }, 300);
        });
        
        // Hiệu ứng cho các step khi scroll
        const steps = document.querySelectorAll('.step');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });
        
        steps.forEach(step => {
            step.style.opacity = '0';
            step.style.transform = 'translateY(20px)';
            step.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(step);
        });
    </script>
</body>
</html>
