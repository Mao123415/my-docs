# 使用指南

按以下步骤在本地检查文档，再将改动发布到 GitHub Pages。

## 常用命令

| 命令 | 用途 |
| --- | --- |
| `python -m mkdocs serve` | 启动本地预览，检查导航和页面内容 |
| `python -m mkdocs build --strict` | 构建到 `site/`，并将构建警告视为错误 |

## 本地操作示例

在仓库根目录创建虚拟环境。下面是 Windows PowerShell 命令，直接调用环境里的 Python。

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs build --strict
.\.venv\Scripts\python.exe -m mkdocs serve
```

打开终端显示的地址，通常为 `http://127.0.0.1:8000/my-docs/`。从左侧导航逐一进入四页，检查表格、代码块和页面链接。退出预览时按 `Ctrl+C`。

## 更新与发布检查

| 阶段 | 操作 | 完成标准 |
| --- | --- | --- |
| 编辑文档 | 修改 `docs/` 中的文件，新增页面时同步维护 `nav` | 本地预览能看到新增内容，导航可以跳转 |
| 严格构建 | 运行 `mkdocs build --strict` | 构建成功，`site/` 生成页面 |
| 自动部署 | 将修改推送到 `main`，查看对应的 Actions 运行 | `build` 和 `deploy` 均成功 |
| 线上验收 | 刷新公开站点 | 页面显示本次修改 |

!!! tip "核对更新"
    将 Actions 页面上的提交与本次推送的提交对应起来，再检查页面中新加的文字。这样能区分旧版本仍可访问和新版本已发布这两种情况。

## 相关阅读

- [API 参考](api.md)
- [返回首页](index.md)
