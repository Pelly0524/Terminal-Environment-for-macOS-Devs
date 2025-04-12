🎯 Terminal Environment for macOS Devs
=====================================

本指南協助你在 macOS 上建立一個現代化、高效的開發終端環境，包含 iTerm2、Zsh、Oh My Zsh、Powerlevel10k，以及常用插件如 autosuggestions 和 syntax-highlighting。

---

📦 工具清單 Tools Overview
-------------------------

- iTerm2：功能豐富的終端模擬器
- Zsh：現代化 shell
- Oh My Zsh：Zsh 的設定框架
- Powerlevel10k：自訂提示符主題
- MesloLGS Nerd Font：支援提示符符號的字型
- Plugins：zsh-autosuggestions、zsh-syntax-highlighting

---

🚀 安裝步驟 Installation Steps
----------------------------

1️⃣ 安裝 Homebrew：

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

---

2️⃣ 安裝 iTerm2：

```bash
brew install --cask iterm2
```

---

3️⃣ 安裝 Nerd Font：

```bash
brew tap homebrew/cask-fonts
brew install --cask font-meslo-lg-nerd-font
```

設定字體：iTerm2 → Preferences → Profiles → Text → Font → 選擇 `MesloLGS NF`

---

4️⃣ 確保使用 Zsh：

```bash
chsh -s /bin/zsh
```

---

5️⃣ 安裝 Oh My Zsh：

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

---

6️⃣ 安裝 Powerlevel10k 主題：

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

修改 `~/.zshrc`：

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

重新載入：

```bash
source ~/.zshrc
```

首次載入會自動啟動設定嚮導。

---

🔌 安裝 Plugins
------------------

zsh-autosuggestions：

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

zsh-syntax-highlighting：

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

編輯 `~/.zshrc`：

```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

套用設定：

```bash
source ~/.zshrc
```

---

⚙️ 實用技巧 Additional Tips
------------------------

- 常用 alias 可加入 `.zshrc`：

```bash
alias gs="git status"
alias ll="ls -alF"
```

- 重新設定 Powerlevel10k：

```bash
p10k configure
```

- VS Code 終端可使用相同 Zsh 與字體，以保持一致顯示效果。

---

✅ 環境完成 Finish
------------------

終端環境安裝完畢。你現在擁有一個清爽、高效、具擴充性的開發終端機設定。
