idea配置github

1.先有github账号，https://github.com/
2.在 GitHub 生成并配置 SSH 密钥或使用 HTTPS + 密码 / 令牌认证
3.在github网页创建新项目
   创建新项目：点击右上角的 “+” 号，选择 “New repository”。
   填写项目信息：
       Repository name：输入项目名称（如 my-project）。
       Description：可选，简短描述项目。
       Public/Private：选择项目可见性。
       Initialize this repository with：可勾选添加 README、.gitignore 或 LICENSE。
   创建仓库：点击 “Create repository” 完成创建。

4.安装git
    Windows 系统
    下载安装程序
        访问 Git for Windows https://gitforwindows.org/ 下载最新版本的安装包。
    运行安装程序
        双击下载的 .exe 文件，按向导提示安装。
    关键选项建议：
        选择 "Use Git from the Windows Command Prompt"（允许在 CMD/PowerShell 中使用 Git）。
        选择 "Checkout as-is, commit Unix-style line endings"（保持代码格式一致性）。
    验证安装
        打开 CMD 或 PowerShell，输入以下命令检查版本：
        任何文件夹下右键打开 open git bash here :git --version
        若显示版本号（如 git version 2.41.0.windows.1），则安装成功。
    配置 Git（安装后必做）
        设置用户名和邮箱（用于提交记录）：
            bash:
            git config --global user.name "Your Name"
            git config --global user.email "your.email@example.com"
        在 Git 全局配置中设置换行符处理规则，避免后续文件出现警告：
            # 提交时转换为LF，检出时转换为CRLF bash：
            git config --global core.autocrlf true
    可选配置：
        设置默认文本编辑器（如 VS Code）：
        bash:
        git config --global core.editor "code --wait"
    查看所有配置：
    bash
    git config --list


5.IDEA 配置并拉取项目
配置 Git：
    打开 IDEA，进入File > Settings > Version Control > Git。
    确保 “Path to Git executable” 指向本地 Git 安装路径（如C:\Program Files\Git\xxxx\bin\git.exe）。
    点击 “Test” 验证配置是否成功。
拉取项目：
    进入VCS > Get from Version Control。
    在弹出窗口的 “URL” 字段中，粘贴 GitHub 项目的克隆地址（如https://github.com/your-username/my-project.git）。
    选择本地存储路径，点击 “Clone”。
    IDEA 会自动下载项目代码并导入。

分支管理：拉取后可通过Git > Branches切换分支。

更新代码：使用Git > Pull获取最新提交