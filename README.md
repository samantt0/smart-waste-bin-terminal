# Smart Waste Bin Terminal

AI-powered waste sorting interface for public recycling stations.

## 🚀 Quick Start

### Option 1: VS Code + Live Server
1. Install VS Code: https://code.visualstudio.com/
2. Install "Live Server" extension
3. Open folder in VS Code
4. Right-click `index.html` → "Open with Live Server"

### Option 2: Python
```bash
cd SmartWasteBin
python -m http.server 8000
Open: http://localhost:8000
```

### Option 3: Double-click
⚠️ Camera won't work due to browser security (HTTPS required)

## 📁 Project Structure
text

SmartWasteBin/
├── index.html          # Main application (single-page)
├── assets/
│   ├── icons/          # Category icons (6 PNG files)
│   ├── ui/             # UI elements (scan animation, background)
│   └── test_images/    # Sample waste images for testing
├── docs/
│   ├── TechnicalSpec.pdf
│   └── StyleGuide.pdf
└── versions/           # Code iterations (for report)

## 🎯 Features
✅ Offline-first (no internet required)
✅ 7-state state machine (IDLE → CAMERA → PROCESSING → RESULT → ...)
✅ AI classification simulation (rule-based)
✅ Accessibility-optimized (64px+ touch targets)
✅ Outdoor-readable (high contrast, text shadows)

## 🔧 Technology Stack
Frontend: HTML5, Tailwind CSS (CDN)
Logic: Vanilla JavaScript (no frameworks)
AI: TensorFlow.js MobileNetV2 (optional)
Target Device: Raspberry Pi 4 + 10" touchscreen

## 🧪 Testing
Full User Flow Test
Open in browser
Wait 3 sec (auto-transition to CAMERA)
Upload test_plastic_bottle.jpg
Observe 3-sec processing animation
See RESULT: "PLASTIC DETECTED"
Click DEPOSIT → sorting animation
See CONFIRMATION → auto-return to IDLE
Performance Test
Open Chrome DevTools (F12) → Performance tab
Record full user flow
Check: FPS ≥ 60, CPU < 50%

## 📊 Statistics
Lines of Code: ~800 (HTML + CSS + JS)
File Size: 45 KB (without images)
Load Time: <2 seconds on Raspberry Pi 4
Supported Browsers: Chrome 90+, Firefox 88+, Safari 14+

## 🐛 Known Issues
Camera not working in local file mode

Solution: Use http-server or Live Server
Icons not displaying

Check: Files exist in assets/icons/
Alternative: Use base64 embedding
Animations choppy on Raspberry Pi

Applied: CSS transitions (GPU-accelerated)
Fallback: Reduce animation complexity
📝 License
MIT License - free for educational and commercial use.

👤 Author
Developed as part of Prompt Engineering Lab #6
Kirov State University, 2026
