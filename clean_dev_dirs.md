# Clean Dev Dirs 开发记录

## 开发目标
创建一个高效的开发环境清理工具，用于清理项目中的临时文件、构建产物和系统缓存文件。

## 主要需求
1. 查找并清理指定类型的目录
2. 查找并清理系统临时文件
3. 只查找顶层目录，避免递归子目录
4. 提供清晰的用户界面
5. 安全的确认机制

## 开发过程
1. 初始实现：使用 find 命令递归查找
2. 优化查找：改用 zsh 内置功能，提高效率
3. 改进输出：添加彩色显示提升用户体验
4. 简化逻辑：移除复杂的父子目录处理
5. 扩展功能：添加文件清理功能

## 技术细节
- 使用 zsh 的 null_glob 选项处理无匹配情况
- 使用通配符匹配文件和目录
- 使用 ANSI 转义序列实现彩色输出
- 分别处理文件和目录的删除操作

## 未来改进
1. 添加更多文件类型支持
2. 添加排除目录功能
3. 添加深度控制选项
4. 添加备份功能