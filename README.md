# RetroPixel Engine v1.0

A powerful web-based tool for transforming 3D models and textures into retro pixel art with advanced image processing capabilities.

## Overview

RetroPixel Engine is an interactive 3D texture processing application that combines modern web technologies (Three.js, Canvas API) with classic pixel art techniques. Load OBJ models, apply textures, and apply sophisticated pixelation, dithering, and color grading effects in real-time.

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/055c961c-3685-4a43-905c-b9283bfa15cc" />

## Core Features

### 3D Model Support
- **Load OBJ Models** - Import standard OBJ format 3D models
- **Interactive Viewer** - Rotate, zoom, and pan with OrbitControls
- **Automatic Camera Framing** - Models are automatically focused in the viewport

### Texture Processing
- **Texture Import** - Load image textures and apply them to 3D models
- **Real-time Preview** - See effects applied instantly as you adjust parameters
- **Non-destructive Processing** - Original textures are preserved; edits are applied on-the-fly

### Pixelation Effects
- **Pixel Size Control** - Adjust pixelation level from 1-20 pixels (1-20x reduction in resolution)
- **Dithering Algorithms**
  - **Ordered (Bayer)** - GameBoy-style grid dithering for classic retro feel
  - **Floyd-Steinberg** - Smooth error diffusion dithering for higher quality results
- **Dithering Strength** - Control the intensity of dithering effects (0-100%)
- **Dithering Size** - Adjust the scale of dithering patterns (1-10)

### Color Grading
- **Exposure** - Adjust image brightness/exposure (50-200%)
- **Brightness** - Shift overall brightness (-100 to +100)
- **Contrast** - Enhance or reduce contrast (0-200%)
- **Saturation** - Control color intensity (0-200%)

### Palette Management
- **Custom Color Palettes** - Build custom color palettes for pixel art style constraints
- **Palette Toggle** - Enable/disable palette impact on processing
- **Add Colors** - Manually add hex colors to your palette
- **Import/Export** - Load palette files (.hex) and export your custom palettes
- **Palette Gathering** - Use [lopsec](https://lospec.com/palette-list) to gather palettes from existing images and other sources

### Export & Storage
- **Texture Export** - Download processed textures as PNG files
- **State Persistence** - All settings and palettes are automatically saved to browser storage
- **Palette Export** - Save your custom palettes as .hex files for reuse

### Theme Support
- **Dark Mode** - Default retro-inspired dark interface with glowing cyan accents
- **Light Mode** - Professional light interface for daytime use
- **Theme Toggle** - Switch between themes with persistent preference storage

## Technical Capabilities

### Advanced Processing Pipeline
The engine processes textures through a sophisticated multi-stage pipeline:

1. **Pixelation** - Reduces resolution for retro appearance
2. **Palette & Dithering** - Applies color reduction with sophisticated dithering algorithms
3. **Grading** - Final color adjustments (exposure, brightness, contrast, saturation)

### Dithering Algorithms
- **Bayer Matrix** - Classic ordered dithering using 4x4 Bayer matrix for GameBoy-style effects
- **Floyd-Steinberg** - Serpentine error diffusion for smoother, more organic dithering

### Performance Optimizations
- Canvas pooling for efficient memory management
- Deferred update scheduling to prevent redundant processing
- Float32Array processing for high-precision color calculations

## Workflow

1. **Load a 3D Model** - Click "Load 3D Model (.obj)" and select an OBJ file
2. **Apply a Texture** - Click "Load Texture" and select an image
3. **Adjust Pixelation** - Use the Pixel Size slider to achieve desired pixelation level
4. **Configure Dithering** - Choose dithering type and adjust strength/size
5. **Fine-tune Colors** - Use grading controls (exposure, brightness, contrast, saturation)
6. **Manage Palette** (Optional) - Add custom colors or import a palette file
7. **Export Results** - Click "Export" to download processed textures

## Palette Gathering with Lopsec

To gather color palettes from existing images or sources:

1. Use [lopsec](https://lospec.com/palette-list) to extract or generate color palettes
2. Export the palette as a .hex file (one color per line)
3. In RetroPixel Engine, click "Import .hex" and select your palette file
4. Enable "Use Palette Impact" to apply the palette to your textures

Example .hex file format:
```
#ff0000
#00ff00
#0000ff
#ffff00
#ff00ff
#00ffff
```

## Interface

### Control Sections
- **IMPORT 3D ASSET** - Load 3D models and textures
- **PIXELATION** - Control pixel size, dithering type, strength, and scale
- **GRADING** - Adjust exposure, brightness, contrast, and saturation
- **PALETTE & COLORS** - Manage custom color palettes
- **OUTPUT & ACTIONS** - Export processed textures

### Theme Button
Toggle between **DARK** and **LIGHT** modes in the top-right corner

## Browser Requirements
- Modern browser with WebGL support (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- Canvas API support
- Local storage support (for state persistence)

## Tips & Tricks

- **Bayer Dithering** works best for pixel art and retro game aesthetics
- **Floyd-Steinberg Dithering** provides smoother results with less obvious patterns
- **Combine effects** - Use pixelation + dithering + saturation reduction for authentic retro look
- **Export multiple times** - Experiment with different settings; original texture is never modified
- **Palette constraints** - Limit palettes to 4-16 colors for true retro game console aesthetics

## Performance Notes

- Processing is optimized for textures up to 2K resolution
- Real-time preview may slow down on very large textures or low-end devices
- Canvas pooling ensures efficient memory usage during repeated processing

---

**RetroPixel Engine** - Transform your 3D graphics into retro pixel art masterpieces.
