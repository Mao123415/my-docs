# 我的技术文档

这是 Mao123415 的 GitHub Pages 课程实践项目。站点使用 MkDocs Material 生成四个文档页面，由 GitHub Actions 在文档变更推送到 `main` 后自动构建和发布。

- [访问 GitHub Pages 网站](https://mao123415.github.io/my-docs/)
- [个人实验报告](report/README.md)
- [查看部署记录](https://github.com/Mao123415/my-docs/actions/workflows/deploy.yml)

## 本地预览

准备 Python 3.12，在仓库根目录执行。以下示例使用 Windows PowerShell。

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs build --strict
.\.venv\Scripts\python.exe -m mkdocs serve
```

在浏览器访问 [本地预览](http://127.0.0.1:8000/)。站点源码位于 `docs/`，导航和主题配置位于 `mkdocs.yml`。
