# 14.5 为配置的属性加密

Config Server 提供的配置大多数是不需要加密的。但一些敏感信息（如密码）最好在后端存储库中以加密的形式存储。

Config Server 提供两种方式处理加密配置：

* 在 Git 存储的配置文件中，写入加密值
* 使用 HashiCorp 的保险库作为 Config Server 的后端存储，以代替 Git。

让我们看看 Config Server 为保持配置属性的机密性，是如何使用这两种方式的。我们先看一下将加密属性写入 Git 后端存储库。

