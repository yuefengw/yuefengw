# Hi there 👋 <img src="https://github.com/laixintao/laixintao/blob/master/assets/wave.gif" width="29px">
---


  你好！ 我是Yuefeng Wang 一名计算机科学与技术专业的硕士生（2027年毕业） 目前正在寻找一份工作机会  同时也喜欢在github上关注并分享一些开源项目和文章

  专业技能
  	
 	•Go:        掌握 Go 语言基础语法、并发编程（goroutine、channel）、包管理等核心特性；了解 Go 的垃圾回收机制、调度器原理；具备使用 Go 开发微服务的经验。
 	•Java基础:  掌握 Java 的集合、注解、反射及 Stream 流式编程等，精读 HashMap 源码，理解其扩容机制与实现原理。
 	•Web框架:   熟悉 SpringBoot、MyBatisPlus、Maven 等主流 Java 开发框架，了解其核心机制如 IoC 和 AOP；熟悉 Flask 框架，具备基于 RESTful 风格的 API 开发经验。
  	•并发编程:  熟悉Java中的并发容器,如ConcurrentHashMap、CopyOnWriteArrayList等常用容器的原理;深入理解线程池、synchronized 关键字、volatile 关键字、ThreadLocal等的底层原理。
  	•JVM:       熟悉JVM的运行机制和内存模型,包括运行时数据区、类加载过程、垃圾回算法与主流垃圾回收器的工作原理，对双亲委派机制有一定的了解。
	•Redis:     熟悉Redis的常见数据结构和操作命令,理解内存淘汰策略、数据持久化机制、Redis集群的工作原理,能够解决高并发场景下的缓存穿透、雪崩和击穿问题。
  	•MySQL:     熟练使用MySQL ,有一定的慢 SQL优化经验;熟悉事务、MVCC、索引结构、锁机制等数据库核心原理。
  	•Linux:     熟练使用 Linux 常用命令，了解 Linux 的启动流程、文件架构、进程调度、用户管理、虚拟内存和文件系统原理；熟悉shell脚本编写，具备计算、磁盘、网络等的基础监控能力及日志分析能力。
	•操作系统:  熟悉操作系统基本原理，包括进程调度、内存管理、文件系统、I/O管理等核心概念；了解虚拟内存、页面置换算法、死锁处理等机制。
 	•计算机网络: 熟悉 OSI 七层网络模型，了解 HTTP、TCP、IP 等常见网络协议，掌握基础网络配置
  	•Elasticearch: 熟悉其在数据搜索、增量全量导入、自动推荐、纠错和补全等场景的应用。深入理解其核心机制，包括逻辑与物理设计、数据写入和查询流程。了解缓存预热、冷热数据分离、索引优化、字段预索引以及操作系统参数调优等性能提升策路
 	

### Contribution Calendar

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://cdn.jsdelivr.net/gh/yuefengw/yuefengw@output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://cdn.jsdelivr.net/gh/yuefengw/yuefengw@output/github-contribution-grid-snake.svg" />
    <img alt="github-snake" src="https://cdn.jsdelivr.net/gh/yuefengw/yuefengw@output/github-contribution-grid-snake-dark.svg" />
  </picture>
</div>

*generated with [Platane/snk](https://github.com/Platane/snk)*

## 📬 联系方式

| 平台          | 信息               | 链接/账号                                                 |
| ------------- | ------------------ | --------------------------------------------------------- |
| 🐙 GitHub     | 开源项目与代码仓库 | [AHUA-Official](https://github.com/yuefengw)            |
| 📧 Email      | 邮箱联系           | [wyf010219@163.com](mailto:wyf010219@163.com)                    |
| 🌐 个人博客   | 技术分享与思考     | [https://yuefengw.github.io/](https://yuefengw.github.io/) |
| 📝 语雀       | 知识库与文档       | [语雀空间](https://www.yuque.com/wyf)               |
| QQ           |  	聊天						| 921592559  |

## 🚀 项目经历

### **GeekTown - 开发者学习交流社区**

**项目描述：** GeekTown是一个前后端分离的，面向互联网开发者的技术内容分享与交流平台，包括前端 PC 和管理后台。我们通过文章、教程、AI 助手等产品和服务，旨在打造一个激发开发者创作灵感，传播优质技术内容，陪伴开发者快速成长的技术社区。

**技术栈：** Spring Boot、MyBatis-Plus、MySQL、Redis、ElasticSearch、RabbitMQ、Docker

**核心技术：** 
- 通过验证码和前端保持半长链接映射关系，当用户扫码关注公众号并输入验证码后，发起回调，识别用户信息并找到对应半长链接，实现系统自动登录。
- 将用户评论、点赞、收藏、系统消息发送到 RabbitMQ，实现消息的异步解耦，提升系统效率和服务稳定性。通过 Redis 实现计数统计和用户活跃度排行，并通过先写 MSQL再删Redis 的方案来保证高并发场景下的缓存一致性。
- 采用 HandlerExceptionResolver 的全局异常处理策略，提高了代码的健壮性和可维护性，优化了用户体验。基于 ThreadLocal 在登录校验拦截器中封装线程隔离的全局上下文，以便在线程内部存储用户信息，减少用户信息的数据库查询次数。
- 通过 AOP +TracelD 记录接口访问日志，实现任务的追踪、监控和诊断。
- 借助 Redis 的 zet 数据结构实现轻量级的作者白名单，提升优秀作者发布文章的用户体验。
- 采用自旋锁策略优化缓存架构，针对热 key 的并发访问进行同步，防止其失效时导致的缓存击穿。
- 通过 Nginx 代理，将客户端请求转发到目标服务器的后端 API 接口，从而解决跨域问题。
> 💡 *如果您对这个项目感兴趣，欢迎通过issue或邮件联系我：wyf010219@163.com*

### **GeekSeek - 基于RAG的知识库问答助手**

**角色：** *后端开发*

**项目描述：** GeekSeek是一个基于私有知识库的企业级智能对话平台，允许用户上传文档构建专属知识空间，并通过自然语言交互方式查询和获取知识。它结合了大语言模型和向量检索技术，能够让用户能够通过对话的形式与自己的知识库进行高效交互。

**技术栈：** Spring Boot、MySQL、MyBatis、Redis、Kafka、Elasticsearch、MinIO、Ollama

**核心技术：** 
- 基于 MinIO 搭建对象存储承载大文件上传，使用 Kafka 构建文档异步处理，把上传、解析、切块、向量化彻底解耦，同时将向量和关键词存入 Elasticsearch 供混合检索。
- 集成 Elasticsearch + IK 分词器构建多格式文档索引，融合通义千问 Embedding 模型实现 2048 维向量转换，结合 KNN 向量召回与 BM25 重排序，支持关键词与语义双引擎检索。
- 使用 Redis 持久化多轮对话历史，针对超长对话引入摘要记忆策略，触发大模型对早期上下文进行压缩总结，减少上下文长度带来的推理成本。
- 设计文档分块与索引方案，用文档层级树组织章/段/句结构，以句子作为最小向量单元，并实现动态粒度检索，减少语义链被硬切导致的召回断裂，使检索 F1 提升约 10%。
- 本地部署向量模型完成文本块向量化，落地关键词检索加向量检索的混合检索，采用 RRF 倒数排名融合策略计算 TopK。
- 构建 RAG 效果评测与模型对比机制，设计多层次文档匹配算法评估检索质量，针对 bge、qwen 等向量模型输出 Precision、Recall、F1、MRR 等指标，为优化提供量化依据。
