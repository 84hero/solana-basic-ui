# Solana 集群性能指标

Solana 集群性能通过网络可以持续处理的平均每秒交易数（TPS）和交易被集群超多数确认所需的时间（确认时间）来衡量。

每个集群节点都维护着在特定事件发生时递增的各种计数器。这些计数器会定期上传到云上的数据库中。Solana 的指标仪表板会获取这些计数器，计算性能指标并在仪表板上显示。

## TPS（每秒交易数）

每个节点的库运行时会维护它处理的交易数量计数。仪表板首先计算集群中所有启用了指标的节点交易的中位数。然后，将集群交易中位数在 2 秒内平均并显示在 TPS 时间序列图中。仪表板还显示了从交易中位数计算得出的平均 TPS、最大 TPS 和总交易数统计数据。

## 确认时间

每个验证者节点维护一个对节点可见的活动账本分叉列表。当节点收到并处理了与分叉对应的所有条目时，认为该分叉被冻结。当一个分叉收到累计超多数票并且其子分叉之一被冻结时，认为该分叉已确认。

节点会为每个新分叉分配一个时间戳，并计算确认分叉所需的时间。这个时间在性能指标中反映为验证节点确认时间。性能仪表板显示每个验证节点确认时间的平均值，作为时间序列图。

## 硬件设置

验证者软件部署在 GCP n1-standard-16 实例上，配备 1TB pd-ssd 磁盘和 2x Nvidia V100 GPUs。这些部署在 us-west-1 区域。

网络从客户端机器（n1-standard-16 CPU-only 实例）启动 solana-bench-tps，使用以下参数：`--tx_count=50000 --thread-batch-sleep 1000`

TPS 和确认时间指标是从仪表板的数据上捕获的，基于 bench-tps 传输阶段开始后 5 分钟的平均值。
