Motion Detector - Real-time Motion Extraction

A lightweight web application that captures camera feed and extracts motion using frame differencing techniques. Features multiple display modes with customizable opacity controls and blend modes similar to video editing software.

🎉 Demo

Try the live demo: https://mhmdrza.github.io/motion/

✨ Features


Real-time Motion Detection - Uses frame differencing to detect and visualize motion

Multiple Display Modes - Choose from camera-only, motion-only, or various blend modes

Customizable Frame Intervals - Adjust sensitivity for different types of motion (1-30 frames)

Adjustable Motion Threshold - Fine-tune detection sensitivity

Blend Modes - Screen, Multiply, Difference, and Exclusion blend modes

Opacity Controls - Separate opacity sliders for camera and motion layers

Mirrored Output - Natural mirror-like display (hand right = display right)

Professional UI - Clean, dark interface with real-time FPS counter

No Dependencies - Pure HTML5, CSS3, and JavaScript

Responsive Design - Works on desktop and mobile devices


🚀 Quick Start


Clone or download this repository

Open index.html in a modern web browser

Allow camera permissions when prompted

Click “Start Detection” to begin

Move around to see motion detection in action!


🎮 Display Modes

Mode	 | 	Description
--------------------
Camera Feed Only	 | 	Shows just the live camera feed
Motion Detection Only	 | 	White motion pixels on black background
Camera + Motion Overlay	 | 	Layered view with customizable opacity
Screen Blend	 | 	Brightens areas where motion occurs
Multiply Blend	 | 	Darkens areas where motion occurs
Difference Blend	 | 	Creates color shifts based on motion
Exclusion Blend	 | 	Inverted color effects for motion areas
⚙️ Controls

Motion Detection Settings


Frame Difference Interval (1-30 frames): Higher values detect slower motion

Motion Threshold (10-100): Lower values detect more subtle motion


Display Settings


Display Mode: Choose how to visualize the output

Camera Opacity (0-100%): Control camera feed visibility

Motion Opacity (0-100%): Control motion detection visibility


🛠️ Technical Details

How It Works


Frame Capture: Continuously captures frames from the camera feed

Frame Buffering: Maintains a buffer of recent frames based on the interval setting

Pixel Comparison: Compares RGB values between current and older frames

Threshold Filtering: Only pixels exceeding the threshold are marked as motion

Blend Rendering: Combines camera and motion data using various blend modes

Mirror Display: Horizontally flips output for natural interaction


Browser Compatibility


✅ Chrome 61+

✅ Firefox 55+

✅ Safari 11+

✅ Edge 79+


Performance


Optimized canvas operations

Efficient frame differencing algorithm

Real-time FPS monitoring

Minimal CPU usage


🔧 Customization

Adding New Blend Modes

        
        javascript
        
    
  
      // Add to the displayMode select options
<option value="newmode">New Blend Mode</option>

// Add case in renderDisplay method
case 'newmode':
  this.renderBlendMode(motionData, 'new-blend-mode');
  break;
    
    
  
  
Adjusting Detection Algorithm

        
        javascript
        
    
  
      // Modify the motion detection sensitivity in detectMotion()
const totalDiff = (rDiff + gDiff + bDiff) / 3;
// You can weight colors differently:
const totalDiff = (rDiff * 0.3 + gDiff * 0.59 + bDiff * 0.11);
    
    
  
  
Changing Video Resolution

        
        javascript
        
    
  
      // Modify the getUserMedia constraints
this.stream = await navigator.mediaDevices.getUserMedia({ 
  video: { 
    width: { ideal: 1280 },  // Change resolution
    height: { ideal: 720 }
  } 
});
    
    
  
  
🎯 Use Cases


Security Monitoring - Basic motion detection for surveillance

Interactive Art - Motion-triggered visual effects

Fitness Applications - Movement tracking and analysis

Educational Projects - Learning computer vision concepts

Accessibility Tools - Motion-based interfaces

Creative Photography - Artistic motion visualization


🐛 Troubleshooting

Camera Not Working


Ensure HTTPS connection (required for camera access)

Check browser permissions for camera access

Try refreshing the page

Test with different browsers


Poor Motion Detection


Adjust the Motion Threshold (lower = more sensitive)

Try different Frame Intervals (higher = slower motion)

Ensure good lighting conditions

Check camera is not obstructed


Performance Issues


Close other applications using the camera

Try lower video resolution

Use a modern browser with hardware acceleration

Check system resources


📱 Mobile Usage

The app is fully responsive and works on mobile devices:


Touch-friendly controls

Automatic layout adaptation

Front/rear camera selection (browser dependent)

Optimized for mobile performance


🔒 Privacy


No data collection - Everything runs locally in your browser

No server communication - Pure client-side application

No storage - No data is saved or transmitted

Secure - Camera access only when explicitly granted


🤝 Contributing

Contributions are welcome! Here are some ideas:


New blend modes - Add more creative visualization options

Motion tracking - Track motion paths over time

Recording features - Save motion clips or screenshots

Advanced algorithms - Implement background subtraction or optical flow

UI improvements - Enhanced controls and settings

Mobile optimization - Better mobile experience


📄 License

This project is open source and available under the MIT License.


📞 Support

Found a bug or have a feature request? Please open an issue.


Built with ❤️ using vanilla JavaScript and HTML5 Canvas API


