# 应用内部通信说明

## API Endpoint

测试环境:
```
https://central-staging.adachina.net
```

演示环境:
```
```

生产环境:
```
```

## 请求规范

### Header

如需确保API回应数据为```JSON```格式，Header需带上```Content-Type```

```
{ Content-Type: application/json }
```

## 错误信息

如请求出现错误，将会返回标准HTTP状态码以及应用错误码

```
400 Bad Request
```

```json
{
  "error_code": 1003,
  "message": "参数缺失或不正确"
}
```
