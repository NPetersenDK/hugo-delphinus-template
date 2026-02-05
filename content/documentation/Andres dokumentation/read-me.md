---
title: "API Reference"
date: 2026-02-05
weight: 1
---

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `parm1` | string | Yes | Project ID |
| `parm2` | integer | No | Page number (default: 1) |
| `parm3` | integer | No | Items per page (default: 20) |

**Response:**

```json
{
  "data": [
    {
      "id": "file_123",
      "name": "example.txt",
      "size": 1024,
      "created_at": "2026-02-05T10:00:00Z"
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 100
  }
}
```

#### Create File

```
POST /api/v1/files
```

**Body:**

```json
{
  "project_id": "proj_123",
  "name": "newfile.txt",
  "content": "File content here"
}
```

#### Get File

```
GET /api/v1/files/{file_id}
```

#### Update File

```
PUT /api/v1/files/{file_id}
```

#### Delete File

```
DELETE /api/v1/files/{file_id}
```

## Error Codes

| Code | Description |
|------|-------------|
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 429 | Rate Limited |
| 500 | Internal Server Error |
