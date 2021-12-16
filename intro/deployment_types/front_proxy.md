# 服务间外加前端代理

![../../images/front_proxy.svg](../../images/front_proxy.svg)

上图显示了作为 HTTP L7 边缘反向代理 Envoy 群集的 [服务到服务](service_to_service.md#deployment-type-service-to-service) 配置。反向代理提供以下功能：

- 终止 TLS。
- 支持 HTTP/1.1 和 HTTP/2。
- HTTP L7 全路由支持。
- 与服务到服务的 Envoy 集群使用标准 [ingress port](service_to_service.md#deployment-type-service-to-service-ingress) 通信，使用发现服务进行主机查找。因此，前端 Envoy 主机与任何其他 Envoy 主机的工作方式相同，除了他们不与其他服务搭配运行。这意味着以相同的方式操作他们并发出相同的统计数据。

## 配置模板

源代码发行版包含一个与 Lyft 在生产环境中运行的版本非常相似的示例前端代理配置。浏览[此处](../../install/ref_configs.md#install-ref-configs)获取更多信息。
