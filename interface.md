# 边缘侧API

***
***
测试请访问：**http://101.34.58.14:8080/**
***
***

## 状态码定义
|状态码|含义|
|-----|----|
|200|成功|
|404|未找到资源|

## 主页
### 搜索
GET /api/search/{搜索内容}
```json
{
  "msg": "操作成功",
  "code": 200,
  "size": 0,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>"
  }
}
```
### 轮播图
GET /api/rotate/
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "avatar": "<视屏封面>"
  }
}
```
### 历史记录
GET /api/history/{设备识别号}
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>",
    "preTime": "<上次播放时间>"
  }
}
```
### 推荐
GET /api/recommend/
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>"
  }
}
```

## 主题页
### 获取主题列表
GET /api/topic/list/
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<主题名称>",
    "keywords": "<主题关键词>"
  }
}
```
### 获取指定主题下的视屏（按id指定）
GET /api/topic/video/id/{id}
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>"
  }
}
```


### 获取指定主题下的视屏（按名称指定）
GET /api/topic/video/id/{name}
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>"
  }
}
```
## VR页
### 获取VR视屏列表
GET /api/vr
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>"
  }
}
```
## 分类页
### 获取分类列表
GET /api/class/list/
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<分类名称>",
    "avatar": "<分类封面>"
  }
}
```
### 获取各分类下视屏
GET /api/class/video/{分类名称}
```json
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>"
  }
}
```
### 在指定的分类下搜索视屏
GET /api/class/video?class=...&name=...
```
{
  "msg": "操作成功",
  "code": 200,
  "data": {
    "id": "id",
    "name": "<视屏名称>",
    "description": "<视屏描述>",
    "avatar": "<视屏封面>",
    "attr": "<分类>"
  }
}
```
## 详情页
### 获取指定id的视屏
GET /api/detail/id/{id}
```json
{ "msg":"操作成功", 
  "code":200,
  "data":{"id":"<视屏id>",
          "name":"<视屏名称>",
          "description":"<视屏描述>",
          "avatar":"<视屏封面>",
          "engName":"<英文名称>",
          "attr":"<视屏属性标签>",
          "showDate":"<上映时间>",
          "totalTime":"<总时长>",
          "grade":"<排行榜>",
          "fileAddr":"<资源地址>"}
}
```
### 获取指定名称的视屏
GET /api/detail/name/{name}
```json
{ "msg":"操作成功", 
  "code":200,
  "data":{"id":"<视屏id>",
          "name":"<视屏名称>",
          "description":"<视屏描述>",
          "avatar":"<视屏封面>",
          "engName":"<英文名称>",
          "attr":"<视屏属性标签>",
          "showDate":"<上映时间>",
          "totalTime":"<总时长>",
          "grade":"<排行榜>",
          "fileAddr":"<资源地址>"}
}
```
