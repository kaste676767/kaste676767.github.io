<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exodus — Premium Script</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700&family=JetBrains+Mono:wght@300;400&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-primary: #000000;
            --bg-secondary: #0a0a0a;
            --accent: #a855f7;
            --accent-dim: #9333ea;
            --accent-glow: rgba(168, 85, 247, 0.15);
            --text-primary: #ffffff;
            --text-secondary: #808080;
            --border: rgba(255, 255, 255, 0.06);
        }

```
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        font-family: 'JetBrains Mono', monospace;
        background: var(--bg-primary);
        color: var(--text-primary);
        overflow-x: hidden;
        line-height: 1.6;
        position: relative;
    }

    /* Grid background effect */
    body::before {
        content: '';
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: 
            linear-gradient(var(--border) 1px, transparent 1px),
            linear-gradient(90deg, var(--border) 1px, transparent 1px);
        background-size: 50px 50px;
        pointer-events: none;
        opacity: 0.3;
        z-index: 0;
    }

    /* Radial gradient overlay */
    body::after {
        content: '';
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 800px;
        height: 800px;
        background: radial-gradient(circle, var(--accent-glow) 0%, transparent 70%);
        pointer-events: none;
        z-index: 0;
    }

    .container {
        position: relative;
        z-index: 1;
        max-width: 900px;
        margin: 0 auto;
        padding: 0 24px;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    /* Logo/Brand */
    .brand {
        font-family: 'Syne', sans-serif;
        font-size: clamp(3rem, 10vw, 6rem);
        font-weight: 700;
        letter-spacing: -0.03em;
        margin-bottom: 12px;
        background: linear-gradient(135deg, var(--text-primary) 0%, var(--accent) 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        animation: fadeInUp 0.8s ease-out;
    }

    .tagline {
        font-size: 16px;
        color: var(--text-secondary);
        font-weight: 300;
        letter-spacing: 0.05em;
        text-transform: uppercase;
        margin-bottom: 60px;
        animation: fadeInUp 0.8s ease-out 0.2s backwards;
    }

    /* Description */
    .description {
        font-size: 18px;
        line-height: 1.8;
        color: var(--text-secondary);
        max-width: 600px;
        margin-bottom: 48px;
        animation: fadeInUp 0.8s ease-out 0.4s backwards;
    }

    /* Features */
    .features {
        display: grid;
        gap: 16px;
        margin-bottom: 60px;
        animation: fadeInUp 0.8s ease-out 0.6s backwards;
    }

    .feature {
        display: flex;
        align-items: center;
        gap: 12px;
        padding: 16px 20px;
        background: var(--bg-secondary);
        border: 1px solid var(--border);
        border-radius: 4px;
        font-size: 14px;
        color: var(--text-secondary);
        transition: all 0.3s ease;
    }

    .feature:hover {
        border-color: var(--accent);
        transform: translateX(4px);
    }

    .feature-icon {
        width: 6px;
        height: 6px;
        background: var(--accent);
        border-radius: 50%;
        flex-shrink: 0;
    }

    /* CTA Button */
    .cta-container {
        animation: fadeInUp 0.8s ease-out 0.8s backwards;
    }

    .discord-btn {
        display: inline-flex;
        align-items: center;
        gap: 12px;
        padding: 18px 36px;
        background: var(--accent);
        color: var(--bg-primary);
        text-decoration: none;
        font-family: 'Syne', sans-serif;
        font-weight: 600;
        font-size: 16px;
        letter-spacing: 0.02em;
        border-radius: 4px;
        transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        position: relative;
        overflow: hidden;
    }

    .discord-btn::before {
        content: '';
        position: absolute;
        top: 0;
        left: -100%;
        width: 100%;
        height: 100%;
        background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
        transition: left 0.5s ease;
    }

    .discord-btn:hover::before {
        left: 100%;
    }

    .discord-btn:hover {
        background: var(--accent-dim);
        transform: translateY(-2px);
        box-shadow: 0 8px 24px rgba(168, 85, 247, 0.4);
    }

    .discord-btn:active {
        transform: translateY(0);
    }

    .discord-icon {
        width: 20px;
        height: 20px;
    }

    /* Footer */
    .footer {
        position: fixed;
        bottom: 24px;
        left: 50%;
        transform: translateX(-50%);
        font-size: 12px;
        color: var(--text-secondary);
        letter-spacing: 0.05em;
        opacity: 0.6;
        z-index: 1;
    }

    /* Status indicator */
    .status {
        position: fixed;
        top: 24px;
        right: 24px;
        display: flex;
        align-items: center;
        gap: 8px;
        font-size: 12px;
        color: var(--text-secondary);
        z-index: 1;
        animation: fadeIn 1s ease-out 1s backwards;
    }

    .status-dot {
        width: 8px;
        height: 8px;
        background: var(--accent);
        border-radius: 50%;
        animation: pulse 2s ease-in-out infinite;
    }

    /* Animations */
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }

    @keyframes pulse {
        0%, 100% {
            opacity: 1;
            transform: scale(1);
        }
        50% {
            opacity: 0.5;
            transform: scale(0.95);
        }
    }

    /* Responsive */
    @media (max-width: 768px) {
        .container {
            padding: 0 20px;
        }

        .brand {
            font-size: 3rem;
        }

        .description {
            font-size: 16px;
        }

        .discord-btn {
            width: 100%;
            justify-content: center;
        }

        .status {
            top: 16px;
            right: 16px;
        }
    }
</style>
```

</head>
<body>
    <div class="status">
        <div class="status-dot"></div>
        AVAILABLE
    </div>

```
<div class="container">
    <h1 class="brand">EXODUS</h1>
    <p class="tagline">Premium Script Solution</p>
    
    <p class="description">
        Advanced scripting capabilities designed for professionals. 
        Reliable, efficient, and built with precision. 
        Join our community to access the full suite.
    </p>

    <div class="features">
        <div class="feature">
            <div class="feature-icon"></div>
            <span>Optimized performance & stability</span>
        </div>
        <div class="feature">
            <div class="feature-icon"></div>
            <span>Regular updates & support</span>
        </div>
        <div class="feature">
            <div class="feature-icon"></div>
            <span>Active community & documentation</span>
        </div>
    </div>

    <div class="cta-container">
        <a href="https://discord.gg/Q5qShnsEJH" class="discord-btn">
            <svg class="discord-icon" viewBox="0 0 24 24" fill="currentColor">
                <path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515a.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0a12.64 12.64 0 0 0-.617-1.25a.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057a.082.082 0 0 0 .031.057a19.9 19.9 0 0 0 5.993 3.03a.078.078 0 0 0 .084-.028a14.09 14.09 0 0 0 1.226-1.994a.076.076 0 0 0-.041-.106a13.107 13.107 0 0 1-1.872-.892a.077.077 0 0 1-.008-.128a10.2 10.2 0 0 0 .372-.292a.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127a12.299 12.299 0 0 1-1.873.892a.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028a19.839 19.839 0 0 0 6.002-3.03a.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03zM8.02 15.33c-1.183 0-2.157-1.085-2.157-2.419c0-1.333.956-2.419 2.157-2.419c1.21 0 2.176 1.096 2.157 2.42c0 1.333-.956 2.418-2.157 2.418zm7.975 0c-1.183 0-2.157-1.085-2.157-2.419c0-1.333.955-2.419 2.157-2.419c1.21 0 2.176 1.096 2.157 2.42c0 1.333-.946 2.418-2.157 2.418z"/>
            </svg>
            Join Discord to Purchase
        </a>
    </div>
</div>

<div class="footer">
    © 2026 EXODUS — ALL RIGHTS RESERVED
</div>
```

</body>
</html>
