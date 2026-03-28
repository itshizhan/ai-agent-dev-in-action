# Claude Code 安装及环境配置

> 参考： [快速开始 - Claude Code Docs](https://code.claude.com/docs/zh-CN/quickstart)



:::  tip

当前以Windows11 powershell 为例，推荐使用macOs

:::


**Windows PowerShell:**

```bash
irm https://claude.ai/install.ps1 | iex
```

如果报错，注意使用管理员权限，切换ip（科学上网），官网可以查询支持的地区。


安装完成，提示如下：

```bash
PS C:\Users\64652> irm https://claude.ai/install.ps1 | iex
Setting up Claude Code...

✔ Claude Code successfully installed!

  Version: 2.1.86

  Location: C:\Users\64652\.local\bin\claude.exe


  Next: Run claude --help to get started

⚠ Setup notes:
  • Native installation exists but C:\Users\64652\.local\bin is not in your PATH. Add it by opening: System Properties →
   Environment Variables → Edit User PATH → New → Add the path above. Then restart your terminal.


✅ Installation complete!

PS C:\Users\64652> claude --help
```


注意给 `C:\Users\64652\.local\bin `，添加到环境变量，或执行一下语句：

```bash
[Environment]::SetEnvironmentVariable("PATH", $env:PATH + ";C:\Users\64652\.local\bin", "User")
```


重启终端，验证是否安装成功：

```bash
PS C:\Users\64652> claude -v
2.1.86 (Claude Code)
```
