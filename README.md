# wx

Linux 下一键切换微信窗口的命令行工具。

- 微信未运行：提示先启动
- 微信窗口可见：隐藏到托盘
- 微信窗口隐藏：唤起到前台

## 依赖

- Linux + X11 桌面环境（不支持 Wayland）
- [微信 Linux 版](https://linux.weixin.qq.com/)
- `wmctrl`
- `xprop`（通常已预装）
- `dbus-send`（通常已预装）

### 安装依赖

```bash
# Ubuntu/Debian
sudo apt install wmctrl x11-utils

# Fedora
sudo dnf install wmctrl xorg-x11-utils
```

## 安装

```bash
git clone https://github.com/Lirqui/wx.git
cp wx/wx ~/.local/bin/wx
chmod +x ~/.local/bin/wx
```

确保 `~/.local/bin` 在 PATH 中：

```bash
echo $PATH | grep -q "$HOME/.local/bin" || echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
```

## 使用

```bash
wx
```

反复执行即可在显示/隐藏之间切换。
