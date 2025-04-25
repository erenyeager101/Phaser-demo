# Phaser Boilerplate
I am also learning Phaser library while this repo will help you build your own!
Welcome to your Phaser.js starter project! This README will introduce you to Phaser, guide you through installation, and show you how to leverage this boilerplate to build your own interactive games or visual experiences.

---

## 🚀 What is Phaser?

Phaser is a fast, free, and open source HTML5 game framework that supports Canvas and WebGL rendering across desktop and mobile web browsers. It provides a comprehensive suite of features for 2D game development, including:

- **Scenes & State Management**: Organize your game into manageable states (loading, menu, playing, game over).
- **Arcade Physics**: Simple yet powerful physics engine for collisions, gravity, and motion.
- **Sprites & Tilemaps**: Easy handling of animated sprites, sprite sheets, and tile-based maps.
- **Input Handling**: Built-in support for keyboard, mouse, touch, and gamepad controls.
- **Audio**: Play music and sound effects with Web Audio API support.
- **Camera & Effects**: Pan, zoom, shake, and apply shaders or filters.

Phaser’s intuitive API and active community make it a top choice for both beginners and seasoned developers looking to create engaging web-based games and interactive content.

---

## ⚙️ Getting Started

Follow these steps to get the boilerplate up and running locally:

1. **Clone this repository**

   ```bash
   git clone https://github.com/your-username/phaser-boilerplate.git
   cd phaser-boilerplate
   ```

2. **Install a static-server (optional)**

   You can serve the files directly via any static server. For example, using `npm`:

   ```bash
   npm install -g serve
   serve .
   ```

3. **Open in Browser**

   Navigate to `http://localhost:5000` (or the port indicated) to see the default scene.

*No build step is required—this is a zero-dependency, CDN-powered setup.*

---

## 📁 Project Structure

```
/ 
├─ index.html        ← Main HTML file, loads Phaser and your scripts
├─ js/
│   ├─ preload.js    ← PreloadScene: load assets
│   ├─ main.js       ← MainScene: core game logic
│   └─ config.js     ← Phaser game configuration
└─ assets/
    ├─ sprites/      ← Sprite sheets and images
    ├─ audio/        ← Music and SFX files
    └─ tilemaps/     ← JSON tilemap definitions
```

- **index.html**: Includes Phaser via CDN and bootstraps your JavaScript files.
- **js/config.js**: Central place to adjust canvas size, physics settings, and scene order.
- **js/preload.js**: Demonstrates asset loading (images, audio, tilemaps).
- **js/main.js**: Example scene showing how to create sprites and enable physics.

---

## 📝 How to Use This Boilerplate

1. **Configure the Game**
   - Open `js/config.js` and modify the `width`, `height`, and `physics` settings.
   - Add or remove scenes in the `scene: [...]` array.

2. **Load Your Assets**
   - Place images, sprite sheets, audio, and tilemaps into the `assets/` folder.
   - In `js/preload.js`, use `this.load.image()`, `this.load.spritesheet()`, or `this.load.audio()` to register them.

3. **Build Scenes**
   - Each scene is a class extending `Phaser.Scene` with `preload()`, `create()`, and `update()` methods.
   - Use Arcade Physics with `this.physics.add.sprite()` or `this.physics.add.group()`.
   - Handle input via `this.input.keyboard.createCursorKeys()` or pointer events.

4. **Run & Iterate**
   - Refresh your browser to see changes immediately.
   - Debug with browser developer tools and the built-in Phaser debugger (enable in config).

---

## 📦 Deployment

This is a static project—ideal for hosting on Vercel, Netlify, GitHub Pages, or any static-file host:

1. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial Phaser boilerplate"
   git push origin main
   ```

2. **Import on Vercel**
   - In your Vercel dashboard, click **Import Project** → select your GitHub repo.
   - Choose **Other** as the framework preset.
   - Deploy—Vercel will serve your `index.html` automatically.

3. **Go Live**
   - Your game is instantly available at `https://<your-project>.vercel.app`.

---

## 🎯 Next Steps

- Replace placeholder assets with your own graphics and sounds.
- Add additional scenes (Menu, Pause, Game Over).
- Integrate UI elements—scoreboards, health bars, timers.
- Explore Phaser plugins for advanced features (Spine, Matter.js physics).

Happy coding! 🎮✨
