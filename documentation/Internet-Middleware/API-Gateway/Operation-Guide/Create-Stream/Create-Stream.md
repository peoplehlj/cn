# 流控策略

目前 API 网关为您配置安全防护设置，提供了两种安全措施：后端签名密钥和流控策略。本章将介绍流控策略。

将流控策略绑定到 API分组上，流控策略才会对已绑定的 API 起作用。

- 流量控制策略可以对API分组次数限制、对单Access Key次数限制。流控的单位可以是分钟、天。请注意，单Access Key次数限制应不大于API分组流量限制。即 单Access Key次数限制 <= API分组流量限制。
- 由于 API 网关限制，当您设置 API 流量限制 值时，考虑每个 API 分组的默认流控上限是500QPS（该值可以通过提交工单申请提高）。

- 绑定 API分组。您可以将策略绑定于多个 API分组，流控策略的限制值将对该策略绑定的每一个 API 单独生效。当您绑定 API 时，如果该 API 已经与某个策略绑定，您的此次操作将替换之前的策略，实时生效。
- 在 API 网关控制台，您可以完成对流量控制策略的创建、修改、删除、查看等基本操作。还有流控策略与 API分组 的绑定解绑等操作。



## 操作步骤
当您创建流量控制策略时，需要选择 Region，Region 一旦选定不可更改，且仅能被应用于同一个 Region 下的 API。

1.点击左侧 **流控策略**，进入流控策略列表页，进行流控策略配置和绑定。

![流控策略列表页](https://github.com/jdcloudcom/cn/blob/edit/image/Internet-Middleware/API-Gateway/lkcl-list.png)


2.新增流控策略

![新增策略](https://github.com/jdcloudcom/cn/blob/edit/image/Internet-Middleware/API-Gateway/lkcl-add.png)


3.给分组绑定策略

![绑定策略](https://github.com/jdcloudcom/cn/blob/edit/image/Internet-Middleware/API-Gateway/lkcl-bd.png)



