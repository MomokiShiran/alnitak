# 文件上传相关接口

## 图片上传接口

#### 请求URL
- `/api/v1/upload/image `
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数
| 参数名 | 必选 | 类型 | 说明     |
| :----- | :--- | :--- | -------- |
| image  | 否   | file | 图片文件 |

- 在postman中使用form-data类型进行测试

#### 返回示例 

``` json
{
  "code": 200,
  "data": {
    "url":"",
  },
  "msg":"ok"
}
```

#### 返回参数说明 

| 参数名 | 类型   | 说明    |
| :----- | :----- | ------- |
| url    | string | 图片url |

#### 备注
无

<!-- ************************ 分隔符 ************************ -->    

## ~~视频上传接口-创建~~ (v1.2.0废弃)

#### 请求URL
- `/api/v1/upload/video `
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数

| 参数名 | 必选 | 类型 | 说明     |
| :----- | :--- | :--- | -------- |
| video  | 否   | file | 视频文件 |

- 在postman中使用form-data类型进行测试

#### 返回示例 
``` json
{
  "code": 200,
  "data": {
    "resource": {
      "id": 1,
      "createdAt": "",
      "vid": 1,
      "title": "",
      "duration": 10,
      "status": 0
    }
  },
  "msg":"ok"
}
```

#### 返回参数说明 
| 参数名    | 类型   | 说明     |
| :-------- | :----- | -------- |
| id        | int    | 分集ID   |
| createdAt | string | 上传时间 |
| vid       | int    | 视频ID   |
| title     | string | 标题     |
| duration  | float  | 视频时长 |
| status    | int    | 审核状态 |

#### 备注
无

<!-- ************************ 分隔符 ************************ -->    

## ~~视频上传接口-追加~~ (v1.2.0废弃)

#### 请求URL
- `/api/v1/upload/video/:vid`
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数

| 参数名 | 必选 | 类型   | 说明              |
| :----- | :--- | :----- | ----------------- |
| vid    | 否   | string | 视频id（在URL中） |
| video  | 否   | file   | 视频文件          |

- 在postman中使用form-data类型进行测试

#### 返回示例 
``` json
{
  "code": 200,
  "data": {
    "resource": {
      "id": 1,
      "createdAt": "",
      "vid": 1,
      "title": "",
      "duration": 10,
      "status": 0
    }
  },
  "msg":"ok"
}
```

#### 返回参数说明 
| 参数名    | 类型   | 说明     |
| :-------- | :----- | -------- |
| id        | int    | 分集ID   |
| createdAt | string | 上传时间 |
| vid       | int    | 视频ID   |
| title     | string | 标题     |
| duration  | float  | 视频时长 |
| status    | int    | 审核状态 |

#### 备注
无

<!-- ************************ 分隔符 ************************ -->    

## 视频上传接口-创建 (v1.2.0)

#### 请求URL
- `/api/v1/upload/video `
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数

| 参数名 | 必选 | 类型   | 说明           |
| :----- | :--- | :----- | -------------- |
| hash   | 是   | string | 视频文件Hash值 |


#### 返回示例 
``` json
{
  "code": 200,
  "data": {
    "resource": {
      "id": 1,
      "createdAt": "",
      "vid": 1,
      "title": "",
      "duration": 10,
      "status": 0
    }
  },
  "msg":"ok"
}
```

#### 返回参数说明 
| 参数名    | 类型   | 说明     |
| :-------- | :----- | -------- |
| id        | int    | 分集ID   |
| createdAt | string | 上传时间 |
| vid       | int    | 视频ID   |
| title     | string | 标题     |
| duration  | float  | 视频时长 |
| status    | int    | 审核状态 |

#### 备注
无

<!-- ************************ 分隔符 ************************ -->    

## 视频上传接口-追加 (v1.2.0)

#### 请求URL
- `/api/v1/upload/video/:vid`
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数

| 参数名 | 必选 | 类型   | 说明              |
| :----- | :--- | :----- | ----------------- |
| vid    | 否   | string | 视频id（在URL中） |
| hash   | 是   | string | 视频文件Hash值    |

#### 返回示例 
``` json
{
  "code": 200,
  "data": {
    "resource": {
      "id": 1,
      "createdAt": "",
      "vid": 1,
      "title": "",
      "duration": 10,
      "status": 0
    }
  },
  "msg":"ok"
}
```

#### 返回参数说明 
| 参数名    | 类型   | 说明     |
| :-------- | :----- | -------- |
| id        | int    | 分集ID   |
| createdAt | string | 上传时间 |
| vid       | int    | 视频ID   |
| title     | string | 标题     |
| duration  | float  | 视频时长 |
| status    | int    | 审核状态 |

#### 备注
无

<!-- ************************ 分隔符 ************************ -->    

## 获取视频上传进度 (v1.2.0)

#### 请求URL
- `/api/v1/upload/checkVideo`
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数

| 参数名 | 必选 | 类型   | 说明           |
| :----- | :--- | :----- | -------------- |
| hash   | 是   | string | 视频文件Hash值 |

#### 返回示例 
``` json
{
  "code": 200,
  "data": {
    "chunks": [1, 2, 3]
  },
  "msg":"ok"
}
```

#### 返回参数说明 
| 参数名 | 类型  | 说明             |
| :----- | :---- | ---------------- |
| chunks | []int | 已上传的视频分片 |

#### 备注
无

<!-- ************************ 分隔符 ************************ -->    

## 上传视频文件分片 (v1.2.0)

#### 请求URL
- `/api/v1/upload/chunkVideo`
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数

| 参数名      | 必选 | 类型   | 说明             |
| :---------- | :--- | :----- | ---------------- |
| video       | 是   | file   | 视频文件         |
| hash        | 是   | string | 视频文件Hash值   |
| name        | 是   | string | 视频文件名称     |
| chunkIndex  | 是   | int    | 当前文件分片编号 |
| totalChunks | 是   | int    | 文件分片数量     |

- 在postman中使用form-data类型进行测试

#### 返回示例 
``` json
{
  "code": 200,
  "data": null,
  "msg":"ok"
}
```

#### 备注
无

<!-- ************************ 分隔符 ************************ -->    

## 合并视频文件分片 (v1.2.0)

#### 请求URL
- `/api/v1/upload/mergeVideo`
  
#### 请求方式
- POST 

#### 请求头
- `Authorization': token `

#### 参数

| 参数名      | 必选 | 类型   | 说明             |
| :---------- | :--- | :----- | ---------------- |
| hash        | 是   | string | 视频文件Hash值   |

#### 返回示例 
``` json
{
  "code": 200,
  "data": null,
  "msg":"ok"
}
```

#### 备注
无