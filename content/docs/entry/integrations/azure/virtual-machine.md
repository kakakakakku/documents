---
Title: Azure Integration - Virtual Machine
Date: 2017-11-24T17:23:53+09:00
URL: https://mackerel.io/docs/entry/integrations/azure/virtual-machine
EditURL: https://blog.hatena.ne.jp/mackerelio/mackerelio-docs.hatenablog.mackerel.io/atom/entry/8599973812320734054
---

Mackerel supports obtaining and monitoring <a href="https://azure.microsoft.com/ja-jp/services/virtual-machines/" target="_blank">Virtual Machine</a> metrics in Azure Integration.

Please refer to the following page for Azure Integration configuration methods and a list of supported Azure services. <br>
<a href="https://mackerel.io/ja/docs/entry/integrations/azure">Azure Integration</a>

## Obtaining metrics

The metrics obtainable with Virtual Machine Azure Integration support are as follows. For `metric` explanations, refer to the <a href="https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-supported-metrics#a-namemicrosoftcomputevirtualmachinesamicrosoftcomputevirtualmachines" target="_blank">Azure help page</a>.

|Graph name|Metric|Metric name in Mackerel|Unit|Aggregation Type|
|:---|:---|:---|:---|:---|
|CPU|Percentage CPU|azure.virtual_machine.cpu.percent|percentage|Average|
|Disk IOPS|Disk Read Operations/Sec<br>Disk Write Operations/Sec|azure.virtual_machine.disk_iops.read<br>azure.virtual_machine.disk_iops.write|iops|Average|
|Network In/Out|Network In<br>Network Out|azure.virtual_machine.network.in<br>azure.virtual_machine.network.out|bytes|Total|
|Disk Read/Write Bytes|Disk Read Bytes<br>Disk Write Bytes|azure.virtual_machine.disk.read<br>azure.virtual_machine.disk.write|bytes|Total|


## Using with mackerel-agent 

If mackerel-agent has already been installed on the target Virtual Machine instance, host information from Mackerel will automatically be integrated and registered as one host. It will not be counted twice as a billable host.

If you prefer a more detailed style of monitoring with AWS Integration, we recommend installing mackerel-agent for Virtual Machine.