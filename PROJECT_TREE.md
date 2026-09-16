# Telco-RAG 项目文件树

> 生成时间: 2026-09-14

## 项目概览

这是一个基于 Next.js + Python FastAPI 的电信领域 RAG (Retrieval-Augmented Generation) 系统。

## 完整文件树

```
Telco-RAG/
│
├─── .eslintrc.json                          # ESLint 配置
├─── .gitignore                              # Git 忽略规则
├─── license                                 # 许可证
├─── next.config.js                          # Next.js 配置
├─── package-lock.json                       # npm 依赖锁定文件
├─── package.json                            # npm 包配置
├─── postcss.config.js                       # PostCSS 配置
├─── README.md                               # 项目说明
├─── tailwind.config.js                      # Tailwind CSS 配置
├─── tsconfig.json                           # TypeScript 配置
├─── video_720p.gif                          # 演示视频
│
├─── components/                             # React 组件
│   ├─── Answer.tsx                          # 答案展示组件
│   ├─── NetopLogo.tsx                       # Logo 组件
│   └─── Search.tsx                          # 搜索组件
│
├─── pages/                                  # Next.js 页面
│   ├─── index.tsx                           # 主页面
│   ├─── _app.tsx                            # App 入口
│   └─── _document.tsx                       # Document 自定义
│
├─── styles/                                 # 样式文件
│   └─── globals.css                         # 全局样式
│
├─── types/                                  # TypeScript 类型定义
│   └─── index.ts                            # 类型定义
│
└─── Telco-RAG_api/                          # Python API 服务
    ├─── __init__.py
    ├─── Online_TelcoRAG.py                  # 在线 RAG 主入口
    ├─── Online_TelcoRAG_validator.py        # RAG 验证器
    ├─── requirements.txt                    # Python 依赖
    ├─── setup.py                            # Python 包配置
    │
    ├─── api/                                # API 服务层
    │   ├─── __init__.py
    │   ├─── call_api.py                     # API 调用
    │   ├─── deploy_api.py                   # API 部署 (FastAPI)
    │   ├─── generate.py                     # 生成逻辑
    │   ├─── LLM.py                          # LLM 接口
    │   ├─── pipeline.py                     # 处理管道
    │   ├─── utils.py                        # 工具函数
    │   └─── settings/
    │       └─── config.py                   # API 配置
    │
    ├─── src/                                # 核心算法层
    │   ├─── __init__.py
    │   ├─── chunking.py                     # 文本分块
    │   ├─── embeddings.py                   # 嵌入向量
    │   ├─── generate.py                     # 文本生成
    │   ├─── get_definitions.py              # 获取定义
    │   ├─── index.py                        # 索引构建
    │   ├─── input.py                        # 输入处理
    │   ├─── NNRouter.py                     # 神经网络路由
    │   ├─── query.py                        # 查询处理
    │   ├─── retrieval.py                    # 文档检索
    │   ├─── storage.py                      # 存储管理
    │   ├─── validator.py                    # 验证器
    │   │
    │   ├─── LLMs/                           # LLM 配置
    │   │   ├─── LLM.py
    │   │   └─── settings/
    │   │       └─── config.py
    │   │
    │   ├─── online_retrieval/               # 在线检索模块
    │   │   ├─── __init__.py
    │   │   ├─── chunk.py                    # 在线分块
    │   │   ├─── embeddings.py               # 在线嵌入
    │   │   ├─── google_page.py              # Google 搜索
    │   │   └─── pdf_reader.py               # PDF 读取
    │   │
    │   └─── resources/                      # 静态资源
    │       ├─── 3GPP_vocabulary.docx        # 3GPP 词汇表
    │       ├─── router_new.pth              # 路由模型
    │       └─── series_description.json     # 系列描述
    │
    ├─── experiments/                        # 实验代码
    │   ├─── __init__.py
    │   └─── Online_Telco_RAG._on_TeleQnA.py # TeleQnA 实验
    │
    └─── Telco-RAG_paper_version/            # 论文版本
        ├─── __init__.py
        └─── pipeline_offline.py             # 离线管道
```

## 目录说明

| 目录 | 说明 |
|------|------|
| `components/` | React UI 组件 |
| `pages/` | Next.js 路由页面 |
| `styles/` | CSS 样式文件 |
| `types/` | TypeScript 类型定义 |
| `Telco-RAG_api/` | Python 后端服务 |
| `Telco-RAG_api/api/` | FastAPI API 服务层 |
| `Telco-RAG_api/src/` | RAG 核心算法实现 |
| `Telco-RAG_api/src/LLMs/` | 大语言模型配置 |
| `Telco-RAG_api/src/online_retrieval/` | 在线检索功能 |
| `Telco-RAG_api/src/resources/` | 静态资源文件 |
| `Telco-RAG_api/experiments/` | 实验性代码 |
| `Telco-RAG_api/Telco-RAG_paper_version/` | 论文版本实现 |

## 排除的目录

以下目录因包含非业务代码或体积较大而被排除:

- `node_modules/` - npm 依赖包
- `.next/` - Next.js 构建产物
- `logs/` - 运行日志
- `Telco-RAG_api/logs/` - API 运行日志
- `Telco-RAG_api/3GPP-Release18/` - 3GPP 标准文档(体积大)
- `__pycache__/` - Python 缓存
- `new_venv4/` - Python 虚拟环境

## 文件统计

| 类型 | 数量 | 说明 |
|------|------|------|
| TypeScript (.ts) | 1 | 类型定义 |
| TypeScript React (.tsx) | 6 | React 组件和页面 |
| Python (.py) | 35 | 后端业务逻辑 |
| CSS (.css) | 1 | 全局样式 |
| JavaScript (.js) | 3 | 项目配置文件 |
| JSON (.json) | 5 | 配置和数据文件 |
| 其他 | 6 | 配置、文档、媒体 |
| **总计** | **57** | 业务源码和配置文件 |
