#!/bin/bash

# Variables for the README content
REPO_NAME="Customize_vscode"
REPO_LINK="https://github.com/DSnake0/Customize_vscode.git"
DESCRIPTION="✨ Transform your Visual Studio Code editor with 🎨 custom CSS, 💻 JavaScript, and a pre-configured settings.json file. Personalize your coding environment with animations, styles, and an optimized setup 🚀."

# Create the README.md file
cat << EOF > README.md
# $REPO_NAME

$DESCRIPTION

## 📂 Repository Contents
- `custom.css`: Custom styles for the VS Code interface.
- `custom.js`: JavaScript for animations and interactivity.
- `settings.json`: Pre-configured settings to enable customization.

## 🛠️ Installation Steps

### Linux
1. Clone the repository:
   ```bash
   git clone $REPO_LINK
   ```
2. Navigate to the cloned directory:
   ```bash
   cd Customize_vscode
   ```
3. Copy the `custom.css`, `custom.js`, and `settings.json` files to your VS Code configuration directory:
   ```bash
   cp custom.css custom.js settings.json ~/.config/Code/User/
   ```
4. Restart VS Code and ensure that custom settings are enabled.

### macOS
1. Clone the repository:
   ```bash
   git clone $REPO_LINK
   ```
2. Navigate to the cloned directory:
   ```bash
   cd Customize_vscode
   ```
3. Copy the `custom.css`, `custom.js`, and `settings.json` files to your VS Code configuration directory:
   ```bash
   cp custom.css custom.js settings.json ~/Library/Application\ Support/Code/User/
   ```
4. Restart VS Code and ensure that custom settings are enabled.

### Windows
1. Clone the repository:
   ```cmd
   git clone $REPO_LINK
   ```
2. Navigate to the cloned directory:
   ```cmd
   cd Customize_vscode
   ```
3. Copy the `custom.css`, `custom.js`, and `settings.json` files to your VS Code configuration directory:
   ```cmd
   copy custom.css custom.js settings.json "%APPDATA%\Code\User\"
   ```
4. Restart VS Code and ensure that custom settings are enabled.

## ⚙️ How It Works
1. The `custom.css` file applies new styles to your VS Code interface.
2. The `custom.js` file enables animations and interactive elements.
3. The `settings.json` file links the CSS and JS files to VS Code's settings, ensuring seamless integration.

### Example `settings.json` Configuration
```json
{
  "vscode_custom_css.imports": [
    "file:///path/to/your/custom.css",
    "file:///path/to/your/custom.js"
  ]
}
```

## 🚀 Start Customizing
Unleash your creativity and make VS Code truly yours! Modify the provided files as needed to match your style and preferences.

## 📃 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

### 🌟 Support
If you enjoy this project, give it a ⭐ on [GitHub]($REPO_LINK) and share it with others!
EOF

# Notify the user that the README file has been created
echo "README.md has been created successfully for $REPO_NAME!"
