# 用户认证

以下API提供用户创建以及认证功能。认证成功后，会签发一个Token。能够用于访问艾道体系内各应用的API。

## 微信小程序认证

使用微信小程序提供的用户数据，注册/认证艾道用户。

```
POST /auth/wechat
```

#### 请求参数
| 名称 | 类型 | 说明 | 必填 | 例子 |
| -- | -- | -- | -- | -- |
| client_source | string | 小程序来源 | 是 | cb_parent |
| code | string | 用户登录凭证 | 是 | - |
| raw_data | string | 用户信息水印 | 是 | - |
| signature | string | 微信数据签名 | 是 | - |
| encrypted_data | string | 微信加密数据 | 是 | - |
| iv | string | 微信加密IV | 是 | - |

##### 小程序来源对照表
| 小程序 | client_source |
| -- | -- |
| 艾道校园家长端 | cb_parent |
| 艾道校园学校端 | cb_school |
| 艾口算学生端 | ar_student |
| 艾口算老师端 | ar_teacher |

#### 返回值说明
| 名称 | 类型 | 说明 | 例子 |
| -- | -- | -- | -- |
| token | string | 艾道用户Token (JWT) | g2K2sc... |

#### 响应例子
```json
{
    "token": "321324fafkeiwlvae.23423ck100",
}
```
