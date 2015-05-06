# Wiki

- https://github.com/open-falcon/doc/wiki

# Intro
监控系统是整个运维环节，乃至整个产品生命周期中最重要的一环，事前及时预警发现故障，事后提供翔实的数据用于追查定位问题。监控系统作为一个成熟的运维产品，业界有很多开源的实现可供选择。当公司刚刚起步，业务规模较小，运维团队也刚刚建立的初期，选择一款开源的监控系统，是一个省时省力，效率最高的方案。之后，随着业务规模的持续快速增长，监控的对象也越来越多，越来越复杂，监控系统的使用对象也从最初少数的几个SRE，扩大为更多的DEVS，SRE。这时候，监控系统的容量和用户的“使用效率”成了最为突出的问题。

监控系统业界有很多杰出的开源监控系统。我们在早期，一直在用zabbix，不过随着业务的快速发展，以及互联网公司特有的一些需求，现有的开源的监控系统在性能、扩展性、和用户的使用效率方面，已经无法支撑了。

因此，我们在过去的一年里，从互联网公司的一些需求出发，从各位SRE、SA、DEVS的使用经验和反馈出发，结合业界的一些大的互联网公司做监控，用监控的一些思考出发，设计开发了小米的监控系统：open-falcon。

**open-falcon的目标是做最开放、最好用的互联网企业级监控产品。**

# Highlights and features

- 强大灵活的数据采集：自动发现，支持falcon-agent、snmp、支持用户主动push、用户自定义插件支持、opentsdb data model like（timestamp、endpoint、metric、key-value tags）
- 水平扩展能力：支持每个周期上亿次的数据采集、告警判定、历史数据存储和查询
- 高效率的告警策略管理：高效的portal、支持策略模板、模板继承和覆盖、多种告警方式、支持callback调用
- 人性化的告警设置：最大告警次数、告警级别、告警恢复通知、告警暂停、不同时段不同阈值、支持维护周期
- 高效率的graph组件：单机支撑200万metric的上报、归档、存储（周期为1分钟）
- 高效的历史数据query组件：采用rrdtool的数据归档策略，秒级返回上百个metric一年的历史数据
- dashboard：多维度的数据展示，用户自定义Screen
- 高可用：整个系统无核心单点，易运维，易部署，可水平扩展
- 开发语言： 整个系统的后端，全部golang编写，portal和dashboard使用python编写。


# Committers
  
- laiwei:  https://github.com/laiwei     来炜没睡醒@微博 / hellolaiwei@微信
- 秦晓辉: https://github.com/ulricqin  Ulricqin@微博 cnperl@微信

# Contributors

- 近期我们会把绝大数的组件整理到 http://github.com/open-falcon ， 期待大家一起贡献，推动，做最开放、最好用的企业级监控系统。
- QQ群：373249123

# License

Copyright 2014-2015 Xiaomi, Inc.
Licensed under the Apache License,
Version 2.0:
http://www.apache.org/licenses/LICENSE-2.0
