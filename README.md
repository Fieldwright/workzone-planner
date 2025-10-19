# Work Zone Planner Pro 🚧

A professional GPS-guided traffic work zone planning tool for road construction crews. Design work zones with MUTCD compliance checking, then generate QR codes for mobile field setup with turn-by-turn GPS navigation.

![Work Zone Planner](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-MIT-blue)

## ✨ Features

### Planning & Design
- **Interactive Map Editor** - Draw work zones on satellite imagery
- **Automatic Cone Placement** - Speed-based spacing calculations
- **MUTCD Compliance** - Real-time taper length validation
- **Single & Double Taper Modes** - Flexible work zone configurations
- **Traffic Sign Library** - 20+ draggable MUTCD signs
- **Measurement Tools** - Distance measurement and station markers
- **Cost Estimation** - Automatic device cost calculations

### GPS-Guided Field Setup
- **QR Code Generation** - Scan to load field setup on mobile
- **Turn-by-Turn Navigation** - Real-time directions to each device
- **Distance Tracking** - Live distance updates in feet
- **Compass Guidance** - Visual arrow pointing to target
- **Arrival Alerts** - Vibration notification within 10 feet
- **Progress Tracking** - Mark devices as placed, auto-advance
- **Offline Capable** - Works without internet after initial load

### Professional Output
- **Print-Ready Plans** - Multi-page traffic management plans
- **Device Inventory** - Automatic equipment lists
- **Compliance Reports** - MUTCD validation summaries
- **Multiple Export Formats** - GeoJSON, KML, and CSV

## 🚀 Quick Start

### Option 1: Use Online (Recommended)
Visit the live version: `https://yourusername.github.io/workzone-planner/`

### Option 2: Run Locally
1. Download `index.html`
2. Open in any modern web browser
3. No installation required!

## 📱 How to Use

### Planning Phase (Desktop/Tablet)

1. **Enter Project Information**
   - Project name, location, and date
   - Speed limit (auto-calculates spacing)

2. **Draw Work Zone**
   - Click the polyline tool (⬜)
   - Click points to define your work zone path
   - Double-click to finish

3. **Place Cones**
   - Click "Place" button
   - Cones auto-space based on speed limit
   - Adjust spacing in settings if needed

4. **Add Signs**
   - Drag signs from palette onto map
   - Signs include advance warning radius visualization
   - Rotate barricades with controls

5. **Generate Plan**
   - Click "Print" to create professional plan
   - QR code automatically included

### Field Setup Phase (Mobile)

1. **Scan QR Code** from printed plan
2. **Click "Start GPS"** to begin tracking
3. **Follow Navigation**
   - Large distance display
   - Turn-by-turn directions
   - Compass arrow points to target
4. **Place Device** at location
5. **Mark as Placed** - auto-advances to next
6. **Complete!** - Celebration when all devices placed

## 📋 Detailed Features

### MUTCD Compliance
- **Automatic Taper Calculations**: Uses formula L = WS/60 (speeds <40) or L = WS²/60 (speeds ≥40)
- **Visual Compliance Badges**: Green ✓ (compliant), Yellow ⚠ (close), Red ✗ (short)
- **Real-time Validation**: Updates as you edit
- **Compliance Reports**: Included in printed plans

### Traffic Control Devices

**Cones & Markers:**
- Traffic cones with auto-spacing
- Station labels (25 or 50 ft intervals)
- Custom placement patterns

**Signs (20+ types):**
- Road Work Ahead (with advance warning radius)
- Lane Closed (Left/Right)
- Merge (Left/Right)
- Flagger / Flagger Ahead
- Speed Limits (25, 35, 45 mph)
- Detour / Road Closed
- And more...

**Equipment:**
- 8 ft Barricades (rotatable)
- Arrow Boards (animated)
- Changeable Message Signs
- Custom devices

### GPS Navigation Features

**Real-Time Tracking:**
- Continuous GPS position updates
- Accuracy indicator (High/Good/Low)
- Battery-efficient toggle on/off

**Turn-by-Turn Guidance:**
- "30 feet ahead"
- "Continue to your right"
- "Behind and left"
- Distance-aware instructions

**Visual Aids:**
- Animated guidance line to target
- Rotating compass arrow
- Accuracy circle around position
- Color-coded markers

**Smart Alerts:**
- Arrival notification at 10 feet
- Vibration feedback
- Auto-popup device details
- Completion celebration

### Export Options

**GeoJSON** - Full feature collection with metadata
**KML** - Google Earth compatible
**CSV** - Simple coordinate list
**Print PDF** - Professional multi-page plan

## 🛠️ Technical Details

### Built With
- **Leaflet.js** - Interactive mapping
- **Leaflet.Draw** - Drawing tools
- **Turf.js** - Geospatial calculations
- **QRCode.js** - QR code generation
- **Vanilla JavaScript** - No frameworks required

### Browser Requirements
- Modern browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- For field setup: GPS-enabled mobile device

### Data Storage
- **All client-side** - No server required
- **QR codes encode full plan** - Self-contained
- **No data collection** - Completely private
- **Works offline** - After initial page load

## 🌐 Deployment on GitHub Pages

### First Time Setup

1. **Create GitHub Account** at github.com (free)

2. **Create New Repository**
   - Click "New" repository
   - Name it: `workzone-planner`
   - Set to "Public"
   - Click "Create repository"

3. **Upload Files**
   - Click "uploading an existing file"
   - Drag `index.html` onto the page
   - **Important:** Rename to `index.html` if needed
   - Click "Commit changes"

4. **Enable GitHub Pages**
   - Go to Settings → Pages
   - Source: Select "main" branch
   - Click "Save"
   - Wait 2-3 minutes

5. **Get Your URL**
   - Your site will be live at:
   - `https://YOUR-USERNAME.github.io/workzone-planner/`

### Updating Your Site

1. Go to your repository
2. Click on `index.html`
3. Click the pencil icon (Edit)
4. Make changes
5. Click "Commit changes"
6. Updates appear in 1-2 minutes

## 📖 Usage Tips

### Best Practices

**Planning:**
- Use satellite view to align with actual road
- Place "Road Work Ahead" signs at MUTCD distances
- Verify taper lengths show green ✓ badges
- Include flagger stations if needed

**Field Setup:**
- Print plan before heading to site
- Ensure phone has GPS enabled
- Allow location permissions when prompted
- Use "Start GPS" for continuous tracking
- Mark devices as placed for progress tracking

**Accuracy:**
- GPS accuracy typically 10-30 feet
- Get closer if "Low accuracy" shown
- Open sky improves GPS performance
- Buildings/trees may reduce accuracy

### Keyboard Shortcuts
- **Esc** - Cancel current drawing
- **Delete** - Enable delete mode checkbox
- **Ctrl+P** - Print plan (when ready)

## 🔧 Customization

### Adjusting Device Costs
Edit the `DEVICE_COSTS` object in the code:
```javascript
const DEVICE_COSTS = {
  'Cone': 15,
  'ROAD WORK AHEAD': 150,
  'ARROW BOARD': 2500,
  // Add your costs here
};
```

### Adding Custom Signs
Add to the signs palette HTML:
```html
<div class="sign-pill" draggable="true" data-sign="YOUR SIGN">YOUR SIGN</div>
```

### Changing Default Settings
Edit initial values:
```javascript
speedLimit: 35  // Default speed
spacing: 35     // Default cone spacing
bufferSpacing: 70  // Default buffer spacing
```

## 📄 License

MIT License - Feel free to use for commercial or personal projects.

## 🙏 Credits

**Mapping:**
- Leaflet - Open-source mapping library
- Esri - Satellite imagery tiles

**Libraries:**
- Turf.js - Geospatial analysis
- QRCode.js - QR code generation
- Leaflet.Draw - Drawing tools

## 🐛 Troubleshooting

### QR Code Not Working
- Make sure site is hosted online (not local file)
- Check that URL starts with https://
- Verify QR code includes full URL

### GPS Not Working
- Enable location services on phone
- Allow browser location permission
- Try refreshing the page
- Check if outside with clear sky view

### Cones Not Placing
- Make sure polyline is drawn first
- Click "Place" button after drawing
- Check that polyline has at least 2 points

### Print Issues
- Use Chrome or Firefox for best results
- Check printer settings (Letter/A4)
- Enable background graphics
- May print across multiple pages

## 📞 Support

For issues or questions:
1. Check the troubleshooting section above
2. Review the usage tips
3. Check browser console for errors
4. Create an issue on GitHub

## 🗺️ Roadmap

Future enhancements:
- [ ] Save/load project files
- [ ] Photo capture for verification
- [ ] Weather integration
- [ ] Multi-language support
- [ ] Offline map caching
- [ ] Team collaboration features
- [ ] Custom device library
- [ ] Advanced reporting

## 📸 Screenshots

*Add screenshots of your tool in action here after deployment!*

---

**Made for road work crews who deserve better tools.** 🚧

Star ⭐ this repo if you find it useful!
