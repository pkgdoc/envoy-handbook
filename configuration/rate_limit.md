# 速率限制服务

[速率限制服务](../intro/arch_overview/global_rate_limiting.md#arch-overview-rate-limit)指定了全局速率限制服务 Envoy 在需要制定全局速率限制决策时应该与之交互。如果没有配置速率限制服务, 则会是用 “null” 服务，如果配置了则会始终返回 “ok”。

- [v1 API 参考](https://www.envoyproxy.io/docs/envoy/latest/api-v1/rate_limit#config-rate-limit-service-v1)
- [v2 API 参考](https://www.envoyproxy.io/docs/envoy/latest/api-v2/config/ratelimit/v2/rls.proto#envoy-api-msg-config-ratelimit-v2-ratelimitserviceconfig)

## gRPC service IDL

Envoy 期望速率限制服务支持 [/source/common/ratelimit/ratelimit.proto](https://github.com/envoyproxy/envoy/blob/master//source/common/ratelimit/ratelimit.proto) 指定GRPC IDL。关于 API 的更多信息见IDL文件。点击[这里](https://github.com/lyft/ratelimit)看 Lyft 的参考实例。
