# 安全管理

**ActorCloud** 提供提供 SSL/TLS 证书加密接入方式，同时也支持发布、订阅权限的自定义：


## 证书

在使用设备编号、设备密钥、连接用户名认证的基础上，平台还可以使用设备证书进行认证，进一步保障通信安全性。

**ActorCloud** 提供设备证书生成功能，支持证书与账户下任意设备绑定并配置其可用性。

依次点击**设备管理** -> **安全管理** -> **证书** 可进行证书的管理。


### 证书创建

- 输入证书名称，选择证书可用性后创建证书。创建后请立即下载并妥善保管相关证书。

![](/assets/certs_create.png)


### 绑定设备

- 设备使用 SSL/TLS 安全连接时应当使用已绑定证书进行加密通信，在证书详情页可以修改证书信息，管理绑定设备。

![](/assets/certs_bind.png)


### 使用指南

- 单向认证：使用端口 8883 进行 SSL/TLS 加密连接，客户端使用证书验证服务器连接合法性。

- 双向认证：使用端口 8884 进行 SSL/TLS 加密连接，客户端、服务器进行双向认证；

- 接入示例详见[设备快速接入指南 -> 设备证书](../access_guide/certs.md)。


## 策略

业务中如有更加精细的设备发布，订阅权限控制需要，用户可在 **ActorCloud** 创建相关策略进行事件控制。

策略提供主题级别的权限控制，依次点击**设备管理** -> **安全管理** -> **策略** 可进行策略的管理。


### 策略创建

- 输入策略名称，作用主题与控制操作、访问规则可以创建证书，其中主题需满足 MQTT 主题规则。

![](/assets/policies_create.png)


### 绑定设备

- 策略详情页中提供新增设备绑定、已绑定设备列表进行相关规则管理，符合规则的设备将被阻止或允许触发相关事件。

![](/assets/policies_bind.png)
