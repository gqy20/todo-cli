# Todo CLI - 命令行待办事项工具

一个用 TDD 方式开发的简单命令行待办事项工具。

## 安装

```bash
# 从源码安装（开发模式）
pip install -e .

# 或构建并安装
pip install .
```

## 使用方法

```bash
# 添加任务
todo add "购买牛奶"

# 列出所有任务
todo list

# 标记任务为完成
todo done 1

# 删除任务
todo delete 1

# 清空所有已完成的任务
todo clear

# 查看帮助
todo --help
todo add --help
```

## 技术栈

- Python 3.8+
- pytest（测试框架）
- argparse（命令行解析）
- JSON（数据存储）
- TDD 开发模式

## 开发

```bash
# 安装开发依赖
pip install -e ".[dev]"

# 运行测试
pytest

# 查看测试覆盖率
pytest --cov=todo
```

## 项目结构

```
todo-cli/
├── src/
│   └── todo/
│       ├── __init__.py
│       ├── models.py      # 数据模型
│       ├── manager.py     # 核心业务逻辑
│       └── cli.py         # 命令行接口
├── tests/
│   └── unit/
│       ├── test_models.py
│       ├── test_manager.py
│       └── test_cli.py
├── pyproject.toml         # 包配置
├── todo.json              # 数据存储（自动生成）
└── README.md
```

## 功能

| 命令 | 说明 |
|------|------|
| `add <text>` | 添加新任务 |
| `list` | 列出所有任务（✓ 表示已完成） |
| `done <id>` | 标记指定 ID 的任务为完成 |
| `delete <id>` | 删除指定 ID 的任务 |
| `clear` | 清除所有已完成的任务 |

## 测试

项目采用 TDD 开发模式，33 个单元测试全部通过：

- 数据模型测试（9 个）
- 业务逻辑测试（14 个）
- CLI 命令测试（10 个）

## License

MIT
