# Bike Demo Three.js

A 3D interactive bike visualization built with Three.js, featuring smooth scrolling animations and responsive design.

## Features

- **3D Bike Model**: Interactive 3D bike visualization with detailed geometry
- **Smooth Scrolling**: Custom smooth scroll implementation using ASScroll
- **Scroll Animations**: GSAP ScrollTrigger animations synchronized with scroll position
- **Responsive Design**: Optimized for both desktop and mobile devices
- **Debug Controls**: Built-in debug panel for development and fine-tuning
- **Draco Compression**: Optimized 3D model loading with Draco compression
- **Camera Controls**: Multiple camera perspectives (Perspective and Orthographic)

## Technologies Used

- **Three.js** - 3D graphics library
- **GSAP** - Animation library with ScrollTrigger plugin
- **ASScroll** - Smooth scrolling library
- **Draco** - 3D geometry compression
- **Vite** - Build tool and development server

## Usage

### Development Mode

The project includes a debug panel that can be activated for development purposes. The debug controls allow you to:

- Adjust camera position (X, Y, Z coordinates)
- Fine-tune animation parameters
- Toggle helpers and visual aids

### Camera Controls

The application features two camera modes:
- **Perspective Camera**: Standard 3D perspective view
- **Orthographic Camera**: Flat, architectural-style view

### Scroll Interactions

The bike model responds to scroll events with smooth animations:
- Model scaling and rotation
- Camera position changes
- Synchronized scroll-based animations

## Configuration

### Camera Settings

Camera parameters can be adjusted in `Experience/Camera.js`:

```javascript
// Perspective Camera
this.perspectiveCamera = new THREE.PerspectiveCamera(
  35,           // Field of view
  this.sizes.aspect,  // Aspect ratio
  0.1,          // Near clipping plane
  1000          // Far clipping plane
)
```

### Animation Controls

Scroll animations are configured in `Experience/Controls.js` using GSAP ScrollTrigger.

## Browser Support

- Modern browsers with WebGL support
- Mobile devices (iOS Safari, Chrome Mobile)
- Desktop browsers (Chrome, Firefox, Safari, Edge)

## Performance Optimization

- **Draco Compression**: 3D models are compressed for faster loading
- **Responsive Loading**: Different optimizations for mobile vs desktop
- **Efficient Rendering**: Optimized Three.js rendering pipeline

## Development

### Debug Mode

Enable debug mode by setting the debug flag in your Experience class:

```javascript
if(this.debug.active) {
  // Debug controls will be available
}
```

### Adding New Animations

To add new scroll-triggered animations:

1. Register ScrollTrigger in your controls
2. Define animation timelines
3. Set scroll triggers with appropriate start/end points

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Three.js community for excellent documentation
- GSAP for powerful animation capabilities
- Google Draco team for 3D compression technology
- ASScroll for smooth scrolling implementation

## Support

If you encounter any issues or have questions, please open an issue on GitHub.
