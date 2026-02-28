# Dice Roller

A simple PWA for rolling dice. Built for D&D nights when you forget your dice at home, or when you just want something quick on your phone.

Live at [mooflabs.github.io/dice-roller](https://mooflabs.github.io/dice-roller/)

## What it does

Pick any combination of standard dice (d4, d6, d8, d10, d12, d20, d100), shake or tap to roll, and see your results. That's it.

- Tap a die type to add it to your pool
- Hit "Start Shaking" (or press Space/Enter)
- Tap "THROW" to roll (or shake your phone)
- Results show one at a time with a slot-machine effect
- Total is calculated automatically for multi-die rolls

### Notable bits

- **Nat 20**: Gets a golden glow and a triumphant fanfare chord.
- **Nat 1**: Gets the grim treatment it deserves -- dark card, red glow, sad trombone.
- **Shake to roll**: On mobile, physically shaking your phone during the shake phase will throw the dice. iOS requires granting motion permission on first use.
- **Haptic feedback**: Vibrates on throw and as each die settles (Android; iOS doesn't support the Vibration API).
- **Die-type colors**: Each die type gets its own color on result cards so mixed rolls are easy to scan.

## Install as an app

It's a PWA, so you can add it to your home screen and use it offline.

**iPhone/iPad**: Open in Safari, tap Share, then "Add to Home Screen."

**Android**: Open in Chrome, tap the menu, then "Install app."

**Desktop**: Look for the install icon in Chrome or Edge's address bar.

## How it's built

Single HTML file, no build step, no dependencies. Everything is inline -- styles, markup, and script. The only external files are the PWA manifest, service worker, and icon PNGs.

- Vanilla JavaScript (no framework)
- Hand-written CSS (no utility framework)
- Web Audio API for procedural sound effects
- DeviceMotion API for shake detection
- `crypto.getRandomValues()` for uniform random rolls
- Service worker with cache-first strategy for offline use

## Tweaking things

**Shake sensitivity** -- the magnitude threshold is `20` in the `devicemotion` handler. Lower it for more sensitive detection, raise it if you're getting false triggers.

**Shake-to-throw cooldown** -- currently 500ms between shake-triggered throws. Adjust the debounce in the `devicemotion` listener if needed.

**Roll animation speed** -- the cycling interval is 70ms per tick, and cards settle with a staggered 200ms delay (capped). The total roll time scales with the number of dice.

## License

Free to use. Attribution appreciated but not required.
