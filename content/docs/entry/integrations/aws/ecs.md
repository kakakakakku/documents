---
Title: AWS Integration - ECS
Date: 2019-03-14T18:00:00+09:00
URL: https://mackerel.io/docs/entry/integrations/aws/ecs
EditURL: https://blog.hatena.ne.jp/mackerelio/mackerelio-docs.hatenablog.mackerel.io/atom/entry/17680117126999845154
CustomPath: integrations/aws/ecs
---

Mackerel supports obtaining and monitoring <a href="https://aws.amazon.com/jp/ecs/" target="_blank">Amazon Elastic Container Service</a> metrics in AWS Integration. When integrating with AWS Integration, billable targets are determined using the conversion 1 Cluster = 1 Host.

Please refer to the following page for AWS Integration configuration methods and a list of supported AWS services.<br>
<a href="https://mackerel.io/docs/entry/integrations/aws">AWS Integration</a>

## Obtaining metrics
The metrics obtainable with AWS Integration's support for ECS are as follows. For `Metric` explanations, refer to the <a href="https://docs.aws.amazon.com/AmazonECS/latest/developerguide/cloudwatch-metrics.html" target="_blank">AWS help page</a>.

|Graph name|Metric|Metric name in Mackerel|Unit|Statistics|
|:--|:--|:--|:--|:--|
|CPU Utilization|CPUUtilization|ecs.cpu_utilization.minimum<br>ecs.cpu_utilization.average<br>ecs.cpu_utilization.maximum|percentage|Minimum<br>Average<br>Maximum|
|Memory Utilization|MemoryUtilization|ecs.memory_utilization.minimum<br>ecs.memory_utilization.average<br>ecs.memory_utilization.maximum|percentage|Minimum<br>Average<br>Maximum|
|CPU Reservation|CPUReservation|ecs.cpu_reservation.minimum<br>ecs.cpu_reservation.average<br>ecs.cpu_reservation.maximum|percentage|Minimum<br>Average<br>Maximum|
|Memory Reservation|MemoryReservation|ecs.memory_reservation.minimum<br>ecs.memory_reservation.average<br>ecs.memory_reservation.maximum|percentage|Minimum<br>Average<br>Maximum|
|Running Task|CPUUtilization|ecs_running_task.#.count|integer|SampleCount|
|Service CPU Utilization|CPUUtilization|ecs.service_cpu_utilization.#.minimum<br>ecs.service_cpu_utilization.#.average<br>ecs.service_cpu_utilization.#.maximum|percentage|Minimum<br>Average<br>Maximum|
|Service Memory Utilization|MemoryUtilization|ecs.service_memory_utilization.#.minimum<br>ecs.service_memory_utilization.#.average<br>ecs.service_memory_utilization.#.maximum|percentage|Minimum<br>Average<br>Maximum|

- Enter the ECS service name in place of the # in "Metric name in Mackerel".