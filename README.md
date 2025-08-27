<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shaxsanem Sultamuratova</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
        }

        .container {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 25px;
            padding: 50px;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.2);
            text-align: center;
            max-width: 500px;
            width: 90%;
            position: relative;
            transform: translateY(0);
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            font-weight: bold;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }

        .profile-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            color: #7f8c8d;
            margin-bottom: 40px;
            font-size: 1.2rem;
            font-weight: 300;
        }

        .social-links {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .social-link {
            display: flex;
            align-items: center;
            padding: 20px 25px;
            border-radius: 15px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }

        .social-link:hover::before {
            left: 100%;
        }

        .instagram {
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            box-shadow: 0 10px 25px rgba(240, 148, 51, 0.4);
        }

        .telegram {
            background: linear-gradient(45deg, #0088cc, #229ed9);
            box-shadow: 0 10px 25px rgba(0, 136, 204, 0.4);
        }

        .linkedin {
            background: linear-gradient(45deg, #0077b5, #00a0dc);
            box-shadow: 0 10px 25px rgba(0, 119, 181, 0.4);
        }

        .facebook {
            background: linear-gradient(45deg, #1877f2, #42a5f5);
            box-shadow: 0 10px 25px rgba(24, 119, 242, 0.4);
        }

        .social-link:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }

        .social-link:active {
            transform: translateY(-2px) scale(1.01);
        }

        .icon {
            margin-right: 15px;
            font-size: 1.5rem;
            width: 30px;
            display: flex;
            justify-content: center;
        }

        .floating-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }

        .floating-element {
            position: absolute;
            width: 10px;
            height: 10px;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        .floating-element:nth-child(1) {
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-element:nth-child(2) {
            top: 60%;
            right: 15%;
            animation-delay: 2s;
        }

        .floating-element:nth-child(3) {
            bottom: 20%;
            left: 20%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px) rotate(0deg);
                opacity: 0.3;
            }
            50% {
                transform: translateY(-20px) rotate(180deg);
                opacity: 0.8;
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 30px 25px;
                margin: 20px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .profile-image {
                width: 120px;
                height: 120px;
                font-size: 48px;
            }
            
            .social-link {
                padding: 18px 20px;
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
    </div>
    
    <div class="container">
        <div class="profile-image">
            SS
        </div>
        
        <h1>Shaxsanem Sultamuratova</h1>
        <p class="subtitle">Connect with me on social media</p>
        
        <div class="social-links">
            <a href="https://www.instagram.com/shakhsanem.sultamuratova?igsh=aWZyemw5dXhvZTc2" class="social-link instagram" target="_blank" rel="noopener">
                <span class="icon">📸</span>
                Instagram
            </a>
            
            <a href="https://t.me/Shaxsanem_Sultamuratova" class="social-link telegram" target="_blank" rel="noopener">
                <span class="icon">✈️</span>
                Telegram
            </a>
            
            <a href="https://www.linkedin.com/in/shaxsanem-sultamuratova-0129aa353" class="social-link linkedin" target="_blank" rel="noopener">
                <span class="icon">💼</span>
                LinkedIn
            </a>
            
            <a href="https://www.facebook.com/profile.php?id=61572316086170&mibextid=ZbWKwL" class="social-link facebook" target="_blank" rel="noopener">
                <span class="icon">👥</span>
                Facebook
            </a>
        </div>
    </div>

    <script>
        // Smooth hover effects
        document.querySelectorAll('.social-link').forEach(link => {
            link.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-8px) scale(1.05)';
            });
            
            link.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Add click ripple effect
        document.querySelectorAll('.social-link').forEach(link => {
            link.addEventListener('click', function(e) {
                const ripple = document.createElement('div');
                const rect = this.getBoundingClientRect();
                const size = Math.max(rect.width, rect.height);
                const x = e.clientX - rect.left - size / 2;
                const y = e.clientY - rect.top - size / 2;
                
                ripple.style.width = ripple.style.height = size + 'px';
                ripple.style.left = x + 'px';
                ripple.style.top = y + 'px';
                ripple.style.position = 'absolute';
                ripple.style.borderRadius = '50%';
                ripple.style.background = 'rgba(255, 255, 255, 0.5)';
                ripple.style.transform = 'scale(0)';
                ripple.style.animation = 'ripple 0.6s linear';
                ripple.style.pointerEvents = 'none';
                
                this.style.position = 'relative';
                this.style.overflow = 'hidden';
                this.appendChild(ripple);
                
                setTimeout(() => {
                    ripple.remove();
                }, 600);
            });
        });

        // CSS for ripple animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple {
                to {
                    transform: scale(4);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
