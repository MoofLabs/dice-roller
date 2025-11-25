# 🎲 Dice Roller PWA

A Progressive Web App for rolling dice with rolling animations and shake-to-roll functionality. Perfect for tabletop gaming, D&D, and any game that needs dice!

## ✨ Features

### 🎯 Dice Types
Roll any combination of standard gaming dice:
- **d4** (4-sided) - Triangle
- **d6** (6-sided) - Cube with dots
- **d8** (8-sided) - Diamond
- **d10** (10-sided) - Kite
- **d12** (12-sided) - Pentagon
- **d20** (20-sided) - Hexagon
- **d100** (100-sided) - Percentile

### 🎨 Visual Features
- **Realistic dice shapes** - Each die type has its own geometric representation
- **Tumbling animation** - Watch dice spin and roll for 2 seconds
- **D6 with dots** - Traditional six-sided dice with actual dot patterns
- **Nat 20 celebration** - Special golden glow and fanfare for rolling 20 on a d20
- **Snake Eyes detection** - Shows 🐍 when you roll two 1s on two d6
- **Responsive design** - Works on phones, tablets, and desktop

### 📱 Mobile Features
- **Shake to roll** - Physically shake your phone to roll dice (iOS & Android)
- **PWA installable** - Add to home screen for app-like experience
- **Works offline** - Roll dice even without internet connection
- **Touch-optimized** - Large, easy-to-tap buttons

### 🔊 Sound Effects
- **Rolling sounds** - Dice rolling
- **Result chime** - Completion sound
- **Nat 20 fanfare** - Special triumphant music for natural 20s
- **Mute button** - Toggle all sounds on/off

### ⌨️ Keyboard Controls
- **Space** or **Enter** - Roll dice / Roll again
- Works at every stage for quick consecutive rolls

### 🎮 Game Flow
1. **Select dice** - Tap any dice buttons to add them
2. **Roll** - Press "Roll Dice!", shake your phone, or hit Space/Enter
3. **View results** - See individual dice and total
4. **Roll again** - Quickly re-roll the same dice
5. **Reconfigure** - Start over with new dice selection

## 🚀 Installation

### Install as PWA

**On iPhone/iPad:**
1. Open the site in Safari
2. Tap the Share button
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add"

**On Android:**
1. Open the site in Chrome
2. Tap the menu (⋮)
3. Tap "Install app" or "Add to Home screen"

**On Desktop (Chrome/Edge):**
1. Look for the install icon (⊕) in the address bar
2. Click it and confirm

## 📱 Shake to Roll Setup

### iOS (iPhone/iPad)
1. Open the app
2. Tap the green **"📱 Enable Shake to Roll"** button
3. Grant motion permission when prompted
4. Shake your phone to roll!

### Android
Shake detection works automatically - just shake your phone when dice are selected!

**Note:** There's a 2-second cooldown between shake-triggered rolls to prevent accidental double-rolls.

## 🛠️ Technology Stack

- **React 18** - UI framework (loaded via CDN)
- **Tailwind CSS** - Styling (loaded via CDN)
- **Web Audio API** - Procedural sound generation
- **DeviceMotion API** - Accelerometer access for shake detection
- **Service Workers** - PWA offline capabilities
- **SVG** - Custom dice shapes and graphics

## 🎯 Why This Approach?

This project uses a **single HTML file** approach:

✅ **Zero build process** - Edit and refresh to see changes  
✅ **No dependencies** - No npm, Node.js, or package.json needed  
✅ **Easy to understand** - All code in one place  
✅ **Fast deployment** - Just upload and go  
✅ **Portable** - Share as a single file  

Perfect for small projects where simplicity matters more than tooling.

## 🎲 Special Roll Detections

### Natural 20 (Nat 20)
- Roll a 20 on any d20
- Golden glowing die
- Triumphant fanfare (C-E-G chord)
- 🎉 celebration emoji

### Snake Eyes
- Roll exactly two d6
- Both dice show 1
- 🐍 snake emoji with special message
- Red warning box

## ⚙️ Customization

### Change Dice Colors
Edit the gradient colors in `index.html`:
```javascript
className="bg-gradient-to-br from-purple-500 to-pink-500"
// Change to any Tailwind colors
```

### Adjust Roll Duration
Change the animation length (default: 2000ms):
```javascript
setTimeout(() => {
  // ... roll logic
}, 2000); // Change this number (in milliseconds)
```

### Modify Shake Sensitivity
Adjust the magnitude threshold (default: 20):
```javascript
if (magnitude > 20) { // Lower = more sensitive
```

### Change Shake Cooldown
Modify the cooldown period (default: 2000ms):
```javascript
if (now - lastShakeTime.current > 2000) { // Change cooldown
```

## 🐛 Troubleshooting

### Shake detection not working
1. Make sure you tapped "Enable Shake to Roll" on iOS
2. Check that dice are selected
3. Shake firmly (not just a gentle tilt)
4. Wait 2 seconds between shakes (cooldown period)
5. On iOS, check Settings → Privacy → Motion & Fitness

### Sounds not playing
1. Check the mute button (🔊/🔇) - it should show 🔊
2. On iOS, check the physical mute switch on the side
3. Try tapping the screen first (some browsers require user interaction)

### Animation is choppy
1. Close other browser tabs
2. Try a different browser (Chrome recommended)
3. Check if device is in low-power mode

## 🤝 Contributing

This is a simple, self-contained project. Feel free to:
- Fork it and customize
- Share improvements
- Use it as a learning resource
- Build upon it for your own projects

## 📝 License

Free to use for personal projects. Attribution appreciated.

## 🎮 Perfect For

- **Tabletop RPGs** - D&D, Pathfinder, any dice-based game
- **Board games** - When you don't have physical dice
- **Quick rolls** - Faster than finding and rolling real dice
- **Virtual gaming** - Perfect for online play sessions
- **Teaching** - Learning dice mechanics and probability
- **Accessibility** - For those who have difficulty rolling physical dice

## 🌟 Why Make This?

Sometimes you need to roll dice but don't have any handy. This app provides:
- Fun interactions (shake to roll!)
- Instant results with automatic totals
- Works offline once installed

Perfect for game night, whether at the table or online!

## 📧 Support

Found a bug? Have a feature request? 

- Open an issue on GitHub
- Check the troubleshooting section above
- Make sure you're using the latest version

---

**Happy Rolling!** 🎲✨
