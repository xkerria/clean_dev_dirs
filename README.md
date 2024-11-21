# Clean Dev Dirs

一个用于清理开发目录和临时文件的 zsh 脚本，帮助清理项目中的依赖、缓存、构建产物和系统临时文件。

## 功能特点
- 自动查找并清理常见的开发目录（如 node_modules, dist 等）
- 清理系统临时文件（如 .DS_Store, Thumbs.db 等）
- 清理编译缓存文件（如 .pyc, .pyo 等）
- 彩色输出界面，清晰区分文件与目录
- 交互式确认，防止误删除
- 支持当前目录及一级子目录的查找

## 支持清理的内容

### 目录
- node_modules (Node.js 依赖)
- dist (构建输出)
- vendor (第三方依赖)
- __pycache__ (Python 缓存)
- .venv (Python 虚拟环境)
- build (构建目录)
- .pytest_cache (Python 测试缓存)
- .next (Next.js 构建输出)
- target (Rust/Java 构建输出)
- .gradle (Gradle 构建缓存)
- .idea (IntelliJ 配置)
- .vscode (VSCode 配置)

### 文件
- .DS_Store (macOS 目录属性)
- Thumbs.db (Windows 缩略图缓存)
- *.pyc (Python 编译文件)
- *.pyo (Python 优化文件)
- ._.DS_Store (macOS 目录属性)
- ._* (macOS 文件属性)
## 使用方法

**克隆仓库**
git clone [repository-url]
cd clean_dev_dirs_project

**添加执行权限（如果需要）**
chmod +x clean_dev_dirs

**运行脚本**
./clean_dev_dirs

## 运行效果
```shell
将要清理的目录统计：
node_modules: 2 个
dist: 1 个

将要清理的文件统计：
.DS_Store: 3 个
.pyc: 5 个

找到以下目录：
./project/node_modules
./apps/node_modules
./project/dist

找到以下文件：
./project/.DS_Store
./apps/.DS_Store
./src/.DS_Store
./src/test.pyc

是否删除这些内容？(y/N)
```

## 注意事项
- 使用前请确保了解将要删除的内容
- 建议先查看列出的文件和目录，确认无误后再确认删除
- 删除操作不可恢复，请谨慎使用
