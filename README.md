# 🌌 Aesthetic Space Dotfiles

Welcome to my personal Linux configuration files. This setup is built on **Arch Linux** using the **Hyprland** compositor, designed for high efficiency, minimalist aesthetics, and a keyboard-centric workflow.

---

## 🧠 HCI Philosophy
This setup is inspired by **Human-Computer Interaction (HCI)** principles to bridge the gap between the user and the machine:

* **Keyboard > Mouse:** Designed to minimize mouse usage. Keyboard shortcuts reduce "travel time," saving significant time during long sessions.
* **Reduced Cognitive Load:** A clean, tiling interface removes visual clutter, allowing you to focus purely on your code or task.
* **Immersive Feedback:** Integrated tools like **Cava** and **Axshell** provide real-time sensory feedback, making the system feel responsive and "alive."

---

## 🛠️ Components
| Component | Description |
| :--- | :--- |
| **Hyprland** | Smooth, dynamic tiling Wayland compositor |
| **Kitty** | Fast, GPU-accelerated terminal emulator |
| **Zshrc** | Optimized shell config for speed and efficiency |
| **Cava** | Console-based audio visualizer for vibe |
| **Axshell** | Custom-tuned shell environment & status |
| **Wallpapers** | Curated space-themed wallpaper collection |

---

## 🚀 Installation

> **Note:** Always back up your existing configurations before overwriting!

### 1️⃣ Clone the repository
```bash
git clone https://github.com/hassan-635/dotfiles.git
cd dotfiles
```

### 2️⃣ Copy Configurations

Move the folders to your .config directory:

```bash
# Copy app configs
cp -r hypr kitty cava axshell ~/.config/

# Copy shell config
cp .zshrc ~/
```
### 3️⃣ Apply Wallpapers

Wallpapers are stored in the /wallpapers directory. You can set them using your preferred utility, such as swww or hyprpaper.

_____________________________

### One-Command Setup Script

You can create a simple install.sh script to automate the setup:
```bash
#!/bin/bash
echo "Backing up existing configs..."
mkdir -p ~/.config/backup
cp -r ~/.config/hypr ~/.config/backup/ 2>/dev/null
cp -r ~/.config/kitty ~/.config/backup/ 2>/dev/null
cp -r ~/.config/cava ~/.config/backup/ 2>/dev/null
cp -r ~/.config/axshell ~/.config/backup/ 2>/dev/null
cp ~/.zshrc ~/.config/backup/ 2>/dev/null

echo "Copying new configurations..."
cp -r hypr kitty cava axshell ~/.config/
cp .zshrc ~/

echo "Setup complete! You may now apply wallpapers using your preferred tool."
```

Save it as install.sh in your repo and make it executable:
```bash
chmod +x install.sh
./install.sh
```

### 🤝 Connect

Built with care by Hassan Ali Abrar.
If these configs improved your workflow, feel free to ⭐ the repo!
