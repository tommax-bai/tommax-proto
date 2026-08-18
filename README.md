# tommax-proto

全部服务的 API 契约（buf 管理）。`tommax/<domain>/v1/*.proto` 为唯一事实源；`gen/go` 为提交的生成代码（独立 go module，服务直接依赖）。

```bash
make lint      # buf lint
make generate  # 重新生成 gen/go
```
变更规则：破坏性变更由 `make breaking` 在 CI 卡死；需要不兼容变更时升 v2 包并双跑（docs/04 §1.3）。
