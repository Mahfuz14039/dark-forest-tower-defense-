# 🌲 Dark Forest Defense 3D

A lightweight 3D browser tower-defense game built with **HTML, CSS, JavaScript, and Three.js**.

Defend your tower from increasingly dangerous waves of ogres, earn gold, repair your defenses, and upgrade your tower to survive as long as possible.

---

## 🎮 Features

* 🌲 Atmospheric 3D dark-forest environment
* 👹 Waves of incoming ogres
* 🏹 Automatic tower attacks
* 💰 Gold rewards for defeating enemies
* ❤️ Tower health system
* 🔧 Tower repair system
* ⚔️ Multiple tower upgrades
* 💥 Critical-hit system
* ✨ Particle effects and glowing effects
* 🌟 Fireflies and atmospheric lighting
* 🔊 Synthesized sound effects
* 🌌 Bloom and FXAA post-processing
* 📱 Responsive UI for smaller screens
* ⚡ Lightweight object pooling for enemies, arrows, and particles

The game uses Three.js for its 3D rendering and includes post-processing effects such as bloom and FXAA.

---

## 🕹️ How to Play

### Objective

Your objective is simple:

> **Survive as many waves of ogres as possible while keeping your tower alive.**

Enemies spawn around the edges of the forest and move toward your tower. If they reach the tower, they damage it. If the tower's HP reaches zero, the game ends.

---

## ▶️ Starting a Wave

Press:

**`Start Wave 1`**

to begin the first wave.

After a wave begins, enemies will continuously spawn until the wave is cleared. The wave button displays the number of remaining enemies while a wave is active.

Each new wave becomes progressively harder:

* More enemies
* Higher enemy HP
* Faster enemies
* Increasing gold rewards
* Faster spawning

---

## 🏹 Tower Combat

The tower automatically searches for enemies within its attack range and fires arrows at them.

You do **not** need to manually aim or shoot.

The tower automatically:

1. Finds the closest enemy within range.
2. Fires an arrow.
3. Tracks the enemy.
4. Deals damage when the arrow hits.
5. Has a chance to perform a critical hit.

---

## 💰 Gold

Defeating enemies rewards you with gold.

Gold can be spent on:

* Tower upgrades
* Repairs

The game starts with **100 gold**.

Enemy gold rewards increase as waves progress.

---

## 🔧 Repair

Your tower can be repaired when it has lost HP.

Click the:

**🔧 Repair**

button.

The repair cost depends on how much HP the tower has lost. Repairing restores the tower to its maximum HP.

### Tip

Don't wait until the tower is almost destroyed.

Use your gold strategically between waves to keep your tower healthy.

---

# ⬆️ Upgrades

There are **six upgrade categories**.

### ❤️ Tower HP

Increases the tower's maximum health.

Each upgrade adds **20 maximum HP** and restores the additional HP immediately.

### ⚔️ Damage

Increases the damage dealt by each arrow.

Each upgrade adds **5 damage**.

### ⚡ Fire Rate

Increases how frequently the tower can fire.

### 🎯 Range

Increases the tower's attack range.

Each upgrade adds **4 range**.

### 🏹 Arrow Speed

Makes arrows travel faster toward enemies.

Each upgrade adds **12 arrow speed**.

### 💥 Crit %

Increases the chance of landing a critical hit.

Each upgrade increases critical-hit chance by **4%**, up to a maximum of **75%**.

Upgrade costs increase with every purchase, so choose your upgrades carefully.

---

## ❤️ Tower Health

The tower begins with:

**100 / 100 HP**

Enemies that reach the tower deal damage based on the current wave.

If the tower reaches:

**0 HP**

the game ends.

---

# 👹 Enemies

The primary enemy in the current version is an **ogre-like creature**.

Enemies:

* Spawn from the edges of the map
* Move toward the tower
* Have visible health bars
* Become stronger in later waves
* Reward gold when defeated

---

# 💀 Game Over

The game ends when the tower is destroyed.

The Game Over screen displays:

* The wave you reached
* Total gold earned
* A Restart button

Click **Restart** to start a new run.

---

# 🔊 Audio

The game uses lightweight synthesized sound effects rather than external audio files.

Sound effects are generated through the browser's **Web Audio API**.

The 🔊 button can be used to mute the game's audio.

---

# 🖥️ Requirements

You need a modern web browser with **WebGL support**.

Recommended browsers:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Opera
* Other modern Chromium/WebGL-compatible browsers

The game uses Three.js/WebGL for its 3D rendering. If WebGL is unavailable, the game displays a browser compatibility message.

---

# 🚀 How to Run

No installation or build system is required.

### Method 1 — Double Click

1. Download or copy the HTML file.
2. Keep the file as:
   `dark-forest-defense-3d-v3.html`
3. Double-click the file.
4. Open it with a modern browser.
5. Start playing.

### Method 2 — Open With Browser

Right-click the HTML file and select:

**Open With → Google Chrome / Microsoft Edge**

---

# 📁 Project Structure

The current version is packaged as a **single HTML file** containing:

```text
Dark Forest Defense 3D
│
└── dark-forest-defense-3d-v3.html
    ├── HTML interface
    ├── CSS styling
    ├── Three.js rendering
    ├── Game logic
    ├── Upgrade system
    ├── Enemy system
    ├── Wave system
    ├── Combat system
    ├── Repair system
    ├── Audio system
    ├── Particle effects
    └── Post-processing effects
```

Three.js version **128** is loaded by the game from a CDN.

---

# ⚙️ Technical Details

### Rendering

The game uses:

* Three.js
* WebGL
* Perspective camera
* Dynamic shadows
* Fog
* ACES filmic tone mapping
* Bloom
* FXAA

The renderer is configured with a fixed internal resolution and optimized post-processing settings.

### Performance Optimization

The game uses object pooling for:

* Enemies
* Arrows
* Particles

Objects are hidden and reused instead of constantly being destroyed and recreated.

The environment also uses instanced meshes for trees and bushes to reduce rendering overhead.

---

# 📈 Wave Progression

Wave difficulty scales dynamically.

The number of enemies is calculated from the wave number, while enemy HP and speed also increase over time.

This creates an endless survival-style progression rather than a fixed number of levels.

---

# 🎯 Strategy Tips

### 1. Upgrade Damage Early

Increasing damage allows the tower to eliminate enemies faster.

### 2. Don't Ignore Range

More range allows the tower to engage enemies earlier.

### 3. Use Repair Wisely

Repairing costs gold, so balance repairs against upgrades.

### 4. Improve Fire Rate

Higher fire rate is especially useful when enemy numbers become large.

### 5. Invest in Critical Hits

Critical hits can deal significantly more damage and become increasingly useful during later waves.

### 6. Keep Upgrading

Enemies continuously scale in strength, so saving all your gold can eventually leave your tower overwhelmed.

---

# 🛠️ Customization

Because the game is contained in a single HTML file, developers can modify the source directly.

Some useful areas to modify include:

* Enemy statistics
* Wave scaling
* Tower statistics
* Upgrade costs
* Upgrade effects
* Environment generation
* Visual effects
* Sound effects
* UI
* Game difficulty

For example, the starting tower statistics are defined directly in the JavaScript game state.

---

# 📜 License & Third-Party Components

This project includes third-party code/components used for rendering and post-processing, including Three.js-related components and shader implementations.

The HTML file contains the relevant third-party license/redistribution notices where applicable.

If redistributing the project, review the included third-party notices and licenses.

---

# 🌲 Credits

**Dark Forest Defense 3D**

A browser-based 3D tower-defense prototype focused on:

* Survival gameplay
* Progressive waves
* Tower upgrades
* Atmospheric visuals
* Lightweight WebGL performance

---

## ⭐ Enjoy the Forest

**Defend the tower.**

**Upgrade your defenses.**

**Survive the night.**

**How far can you reach?**
