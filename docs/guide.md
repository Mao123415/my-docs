# 使用指南

## 本地预览

在仓库根目录创建虚拟环境。下面是 Windows PowerShell 命令，直接调用环境里的 Python。

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs build --strict
.\.venv\Scripts\python.exe -m mkdocs serve
```

打开 `http://127.0.0.1:8000/`。从首页逐一进入关于、使用指南和 API 参考，检查导航、表格、代码高亮和页面内链接。退出预览时按 `Ctrl+C`。

## 发布改动

1. 修改 `docs/` 中的文件。新增文档时同步维护 `mkdocs.yml` 的 `nav`。
2. 运行严格构建，处理路径和链接警告。
3. 将修改提交并推送到 `main`。
4. 在仓库的 **Actions** 页面打开与提交对应的运行，依次检查 `build` 和 `deploy`。
5. 打开公开站点，刷新页面并核对这次修改是否出现。

!!! tip "核对更新"
    将 Actions 页面上的提交与本次推送的提交对应起来，再检查页面中新加的文字。这样能区分旧版本仍可访问和新版本已发布这两种情况。

[查看 API 文档示例](api.md) · [返回首页](index.md)
