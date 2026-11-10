# API 参考

本页用一个虚构的文档索引接口演示怎样记录请求和响应。GitHub Pages 上展示的是接口说明，示例路径没有对应的后端服务。

## 查询文档列表

| 项目 | 示例 |
| --- | --- |
| 方法 | `GET` |
| 路径 | `/api/docs` |
| 成功状态 | `200 OK` |
| 响应类型 | `application/json` |

### 请求与响应

```http
GET /api/docs HTTP/1.1
Accept: application/json
```

```json
{
  "items": [
    {"id": 1, "title": "使用指南", "path": "guide/"},
    {"id": 2, "title": "API 参考", "path": "api/"}
  ]
}
```

| 字段 | 类型 | 含义 |
| --- | --- | --- |
| `items` | 数组 | 文档条目列表。没有结果时示例响应使用空数组。 |
| `items[].id` | 整数 | 文档条目的标识 |
| `items[].title` | 字符串 | 导航中显示的标题 |
| `items[].path` | 字符串 | 相对于站点根目录的页面路径 |

[打开使用指南](guide.md) · [返回首页](index.md)
