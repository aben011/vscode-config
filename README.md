# vscode-config
This repository stores my personal, unified VS Code setup.

## Installation (Linux/MacOS)
Clone this repo into your home directory:
```bash
rm -rf https://github.com/aben011/vscode-config.git "$HOME/vscode-config"
git clone https://github.com/aben011/vscode-config.git "$HOME/vscode-config"
```

Link to files from workspace (`.vscode` directory must exist)
```bash
for filename in .prettierrc extensions.json README.md settings.json; do
    rm -f ".vscode/$filename"
    ln -s "$HOME/vscode-config/$filename" ".vscode/$filename"
done
```
