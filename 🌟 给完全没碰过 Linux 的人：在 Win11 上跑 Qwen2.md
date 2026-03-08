🌟 给完全没碰过 Linux 的人：在 Win11 上跑 Qwen2.5:7B
你不需要知道：
什么是 Linux / Ubuntu / WSL
什么是命令行 / PowerShell
什么是 GitHub 或 Docker
你只需要：
✅ 一台 Windows 11 电脑
✅ 能上网
✅ 敢点“下一步”
🔧 第一步：先启用 WSL（必须最先做！只需一次）
这是微软官方的功能，安全免费。它像“隐形的引擎”，你不用看见它，但 AI 需要它。
按键盘 Win + X（Windows 徽标键 + X 键）
在弹出菜单中，点击 “Windows PowerShell (管理员)”
（如果弹窗问“是否允许此应用对设备更改？”，点 是）
在黑色窗口里，复制下面这整行（注意中间有空格！）：
powershell

编辑



wsl --install
在黑色窗口里 右键一下（就会自动粘贴），然后按 回车
等它自动下载完成（会显示进度，可能几分钟）
完成后，必须重启电脑！
💡 重启后，你不需要打开任何叫 “Ubuntu” 或 “Linux” 的东西！一切都在后台运行。
🔽 第二步：下载两个软件（像装微信一样）
. 下载 Ollama（用来运行 AI 模型）
打开浏览器，访问：https://ollama.com/download/OllamaSetup.exe
点击页面上的蓝色按钮 “Download for Windows”
下载完成后，双击它 → 一路点“下一步” → 安装完成
安装完后，桌面会出现一个 Ollama 图标（黑色圆圈+白色字母）
. 下载 Docker Desktop（用来打开网页聊天界面）
打开浏览器，访问：https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe
下载完成后，双击它
安装时，务必勾选 ✅ Use WSL 2 based engine
然后一路点“下一步”，安装完成
再次重启电脑（确保所有组件生效）
▶️ 第三步：启动你的本地 AI
重启后，双击桌面上的 Ollama 图标（让它在后台运行）
按 Win + R，输入 cmd，按回车（会弹出黑色窗口）
在黑色窗口里，复制下面这整行：
bash

编辑



ollama run qwen2.5:7b
右键黑色窗口 → 粘贴 → 按回车
等它下载模型（第一次很慢，4–8GB，像下电影，不要关窗口）
下载完成后，你会看到 >>>，说明 AI 已经 ready！
💬 第四步：用网页和 AI 聊天（更简单！）
双击打开 Docker Desktop（桌面有鲸鱼图标）
等左上角变成绿色 ✔️（可能要等 1–2 分钟）
点顶部菜单 Images → Browse public images
搜索框输入：open-webui
找到 ghcr.io/open-webui/open-webui → 点右边的 Run
在弹出窗口中：
Host port 改成 3000
Container port 保持 8080
点 Run
打开浏览器，访问：http://localhost:3000
✅ 现在你可以像用微信一样，和你的本地 AI 聊天了！
❓ 常见问题
Q：黑色窗口报错，英文看不懂？
最常见的是因为 没做第一步（WSL），或者 wsl --install 中间没空格
解决：回去做第一步，确保有英文空格，然后重启
Q：下载特别慢？
这是网络问题，不是你操作错了。可以晚上再试。
Q：我点了好多次还是不行？
没关系！你已经比大多数人勇敢了。
欢迎在 我的文章评论区 留言，我会尽力帮你。
❤️ 最后的话
我写这个指南时，自己也什么都不懂。
但我相信：只要步骤够傻瓜，普通人也能拥有自己的 AI。
愿你的数据，永远留在你自己的电脑里。