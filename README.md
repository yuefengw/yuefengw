# Hi there <img src="https://github.com/laixintao/laixintao/blob/master/assets/wave.gif" width="29px">
---


  你好！ 我是Yuefeng Wang, 一名计算机科学与技术专业的硕士生（2027年毕业）, 目前正在寻找一份工作机会, 同时也喜欢在github上关注并分享一些开源项目和文章~

  专业技能
  	•AI编程:	熟练运用Cursor、Codex等AI编程工具开展工程化开发，高效完成代码编写与项目实现；
	•Agent开发:	了解 LoRA、QLoRA 等参数微调方法，具备微调数据构造、Ollama本地模型部署与基础调用能力；
				熟悉MCP、Skills封装与Function Calling机制；掌握提示词工程、上下文工程、结构化输出等Agent开发技能；
				熟悉LangChain、LangGraph等大模型应用开发框架；熟悉ReAct、Plan-and-Execute、Reflection、Multi-Agent 等智能体执行模式，具备Memory管理与工作流编排能力。
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
    <source media="(prefers-color-scheme: dark)" srcset="https://cdn.jsdelivr.net/gh/yuefengw/yuefengw@snk/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://cdn.jsdelivr.net/gh/yuefengw/yuefengw@snk/github-contribution-grid-snake.svg" />
    <img alt="github-snake" src="https://cdn.jsdelivr.net/gh/yuefengw/yuefengw@snk/github-contribution-grid-snake-dark.svg" />
  </picture>
</div>

*generated with [Platane/snk](https://github.com/Platane/snk)*

## 📬 联系方式

<div align="center">

| 平台          | 信息               | 链接/账号                                                     |
| ------------- | ------------------ | --------------------------------------------------------- |
| 🐙 GitHub     | 开源项目与代码仓库 | [yuefengw](https://github.com/yuefengw)                   |
| 📧 Email      | 邮箱联系           | [wyf010219@163.com](mailto:wyf010219@163.com)             |
| 🌐 个人博客   | 技术分享与思考     | [CSDN 摸个小yu](https://blog.csdn.net/qq_41725967?spm=1011.2124.3001.5343) |
| 📝 语雀       | 知识库与文档       | [语雀空间](https://www.yuque.com/u55081998)                |

</div>

## 🚀 项目经历

### **ClaimAssist – 基于RAG的保险条款智能问答平台**

**项目描述：** 针对保险条款复杂、责任边界模糊及理赔规则难以理解的用户痛点，设计并开发了一套基于RAG架构的结构化解析与混合检索架构的智能问答系统，实现条款理解、语义检索与精准问答自动化。

**技术栈：** Spring Boot / MinIO / Elasticsearch / Kafka / Redis / RAGAS / LLMs

**核心技术：** 
- 基于MinIO+Kafka搭建异步文档处理链路，支持大文件**分片上传**、**断点续传**、合并及解析、切块、向量化、索引化并行处理。
- 基于**MinerU解析**后的 JSON 文件设计文档切块策略，按type组织语义块，结合**递归细切**、**列表前导句**和**表头绑定**及**VLM图片描述回填**，减少语义断裂并补全文档语义信息。
- 设计**Query Rewrite**机制，融合规则清洗、疑问词过滤、同义词扩展与**Few-shot约束**的**MultiQuery**生成，提升弱表达查询检索效果。
- 基于 Elasticsearch+IK分词器实现**BM25+KNN混合召回**，并结合**RRF**融合与**Cross-Encoder**二阶重排优化检索排序，多轮测试下MRR、NDCG 提升 20%+。
- 构建**长短期记忆融合**机制，结合短期Redis窗口上下文、长期LLM摘要抽取与ES记忆召回，增强多轮对话一致性。
- 基于RAGAS构建自动化评估闭环，在600条测试集上系统忠实度由71%提升至85%，上下文精确度与召回率均接近90%，并支持证据引用与结果可追溯分析。

---

### **Shannon – 面向复杂任务的多智能体编排平台**

**项目描述：** 负责构建面向复杂任务的智能体执行平台，围绕任务拆解、路由编排、工具扩展、多智能体协同和记忆管理等核心问题进行系统设计与实现，支撑复杂任务在多角色Agent间的高效协作与稳定执行。

**技术栈：** FastAPI / LangGraph / LangChain / ReAct / Milvus / Redis 

**核心技术：** 
- 面向复杂任务构建任务理解与动态路由机制，依据任务分解结果将请求智能分发至不同执行路径，并基于LangGraph编排链路支持DAG、Research、Multi-Agent等多种Agent执行模式。
- 实现基于ReAct的Multi-Agent协作框架，采用主 Agent 规划调度、多角色并发执行；通过任务板、共享工作区与点对点消息机制实现多Agent协作，并支持基于idle状态的任务再分配以及运行中的human-in-the-loop干预。
- 设计并实现统一工具调用与能力扩展框架，在LangChain Tool抽象之上构建ToolRegistry管理工具元数据，支持原生工具、MCP工具与OpenAPI工具的统一注册、发现、动态暴露和受控执行。
- 实现会话记忆检索与上下文压缩链路，基于Milvus存储会话问答与摘要向量，并通过历史裁剪和摘要注入控制请求上下文大小；在多智能体场景下为子智能体分别维护执行历史与关键记忆，并通过上下文裁剪降低长链路执行成本。
> 💡 *如果您对这个项目感兴趣，欢迎通过issue或邮件联系我：wyf010219@163.com*
