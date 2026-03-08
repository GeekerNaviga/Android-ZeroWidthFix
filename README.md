# Android-ZeroWidthFix
修复安卓零宽字符 (U+200D) 路径绕过漏洞，通过 SELinux 规则 / Android/data 目录访问安全.

Android-ZeroWidthFix 是一款基于 SELinux 强制访问控制的安卓安全加固模块，核心用于修复**零宽字符（U+200D）路径绕过漏洞**，从内核层面阻断恶意应用通过隐形字符构造路径、越权访问 `/Android/data` 等应用私有目录的行为。

> **AI辅助编写 | 试配度未知,谨慎刷入!**

#### 核心特性

- 🛡️ 内核级防护：通过 SELinux neverallow 规则封堵漏洞，不依赖应用层校验

- 🌐 多语言适配：自动识别系统语言（目前仅支持中文和英文），支持扩展更多语言

- ⚡ 低功耗设计：采用 timerfd+epoll 事件驱动，无轮询开销

- 📱 一键修复：内置 SELinux 强制模式恢复按钮，操作便捷

- 🧪 实时检测：持续监听 SELinux 状态与漏洞修复效果，用户可随时查看他们的设备安全性

#### 适用场景

- 修复安卓设备 `/Android/data` 零宽字符路径绕过漏洞

- 防止恶意应用越权扫描/窃取应用私有数据

- 定制 ROM/安全增强/权限管控场景的底层加固

#### 安装使用

1. 下载模块包刷入 KernelSU/Magisk

2. 查看日志：`logcat -s AndroidZeroWidthFix`

3. 一键恢复 SELinux 强制模式：模块界面点击对应按钮

## 📄 许可证

本项目采用 MIT 许可证开源，详见 [LICENSE](LICENSE) 文件。

---
