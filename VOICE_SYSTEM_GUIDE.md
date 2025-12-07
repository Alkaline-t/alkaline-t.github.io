# 🎙️ Voice Control System - User Guide

## Overview
Your website now has a complete **Voice Control System** with audio playback, text-to-speech, and voice controls!

## Features

### 1. **Voice Control Panel**
- **Location**: Bottom-right corner of your website (microphone button 🎙️)
- **How to Open**: Click the microphone button to toggle the control panel
- **Panel Features**:
  - Background audio controls
  - Volume control slider
  - Text-to-speech functionality
  - Status display

### 2. **Background Audio Controls**
Three buttons to control audio playback:
- **▶️ Play**: Start playing background audio
- **⏸️ Pause**: Pause the currently playing audio
- **⏹️ Stop**: Stop and reset audio to the beginning

**To Add Your Own Background Music:**
1. Open your `index.html` file in a text editor
2. Find this line (around line 3240):
   ```javascript
   audioElement.src = 'path/to/your/background-music.mp3';
   ```
3. Replace `'path/to/your/background-music.mp3'` with the path to your audio file:
   ```javascript
   audioElement.src = 'your-audio-file.mp3';
   ```
4. Save the file

### 3. **Volume Control**
- **Slider**: Adjust volume from 0% to 100%
- **Display**: Current volume percentage shown next to slider
- **Default**: 70%

### 4. **Text-to-Speech**
Convert any text into spoken audio using Web Speech API:
1. Type text in the input box labeled "Text to Speech"
2. Click **🔊 Speak** button or press **Enter**
3. The device will speak the text aloud
4. Status bar shows speaking progress

### 5. **Voice Greeting**
- When the page loads, a welcome greeting is automatically spoken
- Greeting: *"Welcome to the AI Fitness Monitoring Device. This is your voice assistant."*
- You can customize this in the `voiceGreeting()` function

## Status Display
The status bar at the bottom of the control panel shows:
- **Ready**: System is ready to receive commands
- **🔊 Speaking...**: Text-to-speech is in progress
- **🎵 Playing audio...**: Background audio is playing
- **⏸️ Audio paused**: Audio is paused
- **⏹️ Audio stopped**: Audio has been stopped
- **✅ Speech complete**: Text-to-speech completed successfully
- **⚠️ Warning messages**: For any issues

## Dark Mode Support
The voice control system automatically adapts to your website's dark mode:
- When dark mode is active, the control panel changes to dark colors
- All text remains readable in both modes

## Mobile Responsiveness
- The control panel is fully responsive
- On mobile devices, the button and panel resize appropriately
- Panel width adjusts to fit mobile screens

## Customization Tips

### Change the Greeting Text
Find this code around line 3310:
```javascript
const greeting = new SpeechSynthesisUtterance(
  'Welcome to the AI Fitness Monitoring Device. This is your voice assistant.'
);
```
Replace with your custom text.

### Change Speech Rate/Pitch
In the same section:
```javascript
greeting.rate = 0.9;  // 0.5 to 2 (slower to faster)
greeting.pitch = 1;   // 0.5 to 2 (lower to higher)
greeting.volume = 0.8; // 0 to 1 (quiet to loud)
```

### Change Button Colors
Look for the CSS gradient definitions, for example:
```css
.voice-btn-play {
  background: linear-gradient(135deg, #0084ff, #0040ff);
}
```

## Browser Compatibility
✅ Works in all modern browsers that support:
- Web Audio API (for audio playback)
- Web Speech API (for text-to-speech)

Most recent versions of Chrome, Firefox, Safari, and Edge support these features.

## Troubleshooting

### Audio doesn't play
- Make sure the file path is correct
- Check that the audio file exists in your project folder
- Try using an absolute URL: `https://example.com/audio.mp3`

### Text-to-speech not working
- Check that your browser supports Web Speech API
- Make sure volume is not muted on your system
- Try using Chrome or Edge (better speech support)

### Voice control button not showing
- Make sure JavaScript is enabled
- Check browser console for errors (F12)
- Verify the HTML elements are in the correct location

## File Locations
- **Main file**: `index.html`
- **Styles**: Within `<style>` tag (lines 1960-2165)
- **JavaScript**: Within `<script>` tag (lines 3238-3370)
- **HTML Elements**: After the header (lines 2259-2281)

---

**Enjoy your new voice-controlled website! 🎉**
