# vscode-config

This repository stores my personal, unified VS Code setup.

## Installation

Clone this repo into your home directory:

```bash
rm -rf "$HOME/vscode-config"
git clone https://github.com/aben011/vscode-config.git "$HOME/vscode-config"
```

## Link to Configuration Files (Linux/MacOS)

Link to `.vscode` files from the **workspace**:

```bash
mkdir -p ./.vscode
for filename in .prettierrc extensions.json README.md settings.json; do
    rm -f ".vscode/$filename"
    ln -s "$HOME/vscode-config/$filename" ".vscode/$filename"
done
```

Link to other files from the **workspace**:

```bash
for filename in .bash_profile .bashrc; do
    rm -f "./$filename"
    ln -s "$HOME/$filename" "./$filename"
done

rm -f ./.kube_config
ln -s "$HOME/.kube/config" ./.kube_config
```
