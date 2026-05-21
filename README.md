# Light Pillars Component ✨

A stunning, highly customizable, and interactive **Light Pillar** React component built with **Three.js** and **Custom WebGL Shaders**. Perfect for adding a premium, atmospheric glowing light beam effect to your web applications, landing pages, and creative portfolios.

## 👁️ Preview

<div align="center">
  <img width="1578" height="875" alt="Image" src="https://github.com/user-attachments/assets/4caf291e-f13d-4dff-9d7f-bb42f53ec468" />
</div>


## 🌟 Features

- **Custom Shaders:** Powered by custom WebGL shaders for high-performance visual effects.
- **Highly Customizable:** Control colors, intensity, rotation speed, glow amount, dimensions, and noise intensity.
- **Interactive:** Optional mouse interaction to dynamically alter the pillar's rotation and perspective.
- **Responsive & Performance Optimized:** Includes automatic quality scaling (`low`, `medium`, `high`) based on device capabilities (e.g., mobile vs. desktop) to maintain a smooth frame rate.
- **Blend Modes:** Easily integrate into any background using CSS mix-blend modes (e.g., `screen`).
- **Tailwind CSS Ready:** Built to work seamlessly with Tailwind CSS utility classes.

## 🚀 Technologies Used

- **Framework:** React 19
- **3D Library:** Three.js
- **Styling:** Tailwind CSS 4
- **Build Tool:** Vite
- **Shaders:** GLSL (Custom Vertex & Fragment Shaders)

## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone <your-repository-url>
   cd Light-Pillars-Comp
   ```

2. **Install dependencies:**
   Make sure you have Node.js installed, then run:
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   ```
   This will start Vite on a local port.

4. **Build for production:**
   ```bash
   npm run build
   ```

## 💻 Usage

To use the `LightPillar` component in your project, simply import it and drop it into a relative or absolute positioned container with a defined width and height.

```jsx
import React from 'react';
import LightPillar from './components/LightPillar';

function App() {
  return (
    <div style={{ width: '100vw', height: '100vh', position: 'relative', backgroundColor: '#000' }}>
      <LightPillar
        topColor="#5227FF"
        bottomColor="#FF9FFC"
        intensity={1}
        rotationSpeed={0.3}
        glowAmount={0.002}
        pillarWidth={3}
        pillarHeight={0.4}
        noiseIntensity={0.5}
        pillarRotation={25}
        interactive={true}
        mixBlendMode="screen"
        quality="high"
      />
    </div>
  );
}

export default App;
```

## ⚙️ Component Props (API)

| Prop | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `topColor` | `String` | `'#5227FF'` | Hex color code for the top gradient of the pillar. |
| `bottomColor` | `String` | `'#FF9FFC'` | Hex color code for the bottom gradient of the pillar. |
| `intensity` | `Number` | `1.0` | Overall brightness intensity of the light pillar. |
| `rotationSpeed` | `Number` | `0.3` | Speed of the continuous ambient rotation. |
| `interactive` | `Boolean` | `false` | Enables mouse tracking to distort the light pillar based on cursor position. |
| `className` | `String` | `''` | Additional Tailwind or CSS classes to apply to the container. |
| `glowAmount` | `Number` | `0.005` | Intensity of the soft outer glow. |
| `pillarWidth` | `Number` | `3.0` | Base width of the light pillar. |
| `pillarHeight` | `Number` | `0.4` | Height scale of the noise/wave effect inside the pillar. |
| `noiseIntensity` | `Number` | `0.5` | Intensity of the static/noise overlay effect. |
| `mixBlendMode` | `String` | `'screen'` | CSS mix-blend mode for compositing over backgrounds. |
| `pillarRotation` | `Number` | `0` | Static rotation offset of the pillar in degrees. |
| `quality` | `String` | `'high'` | Shader iteration quality (`'low'`, `'medium'`, `'high'`). Auto-adjusts on mobile/low-end devices. |

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute.

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.
