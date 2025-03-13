# AI Hedge Fund

这是一个基于AI的对冲基金项目，使用先进的机器学习算法进行金融市场分析和交易。

## 功能特点

- 多市场支持：同时支持传统金融市场和加密货币市场
- AI 驱动：结合机器学习模型和大语言模型进行市场分析和决策
- 实时数据：集成多个数据源，提供实时市场数据
- 自动化交易：支持自动化交易策略执行
- 回测系统：完整的策略回测功能

## 项目结构

```
src/
├── agents/     - AI 交易代理模块
├── crypto/     - 加密货币市场相关功能
├── data/       - 数据获取和处理模块
├── graph/      - 数据可视化和图表模块
├── llm/        - 大语言模型集成
├── models/     - 机器学习模型
├── tools/      - 通用工具函数
├── utils/      - 辅助功能模块
├── main.py     - 主程序入口
└── backtester.py - 策略回测系统
```

## 技术栈

- Python 3.9+
- PyTorch - 深度学习框架
- LangChain - LLM 应用框架
- Pandas & NumPy - 数据处理
- CCXT & Binance/OKX API - 加密货币交易
- YFinance - 传统市场数据

## 安装和设置

1. 克隆仓库：
```bash
git clone https://github.com/li367/ai-crypto-hedge-fund.git
cd ai-crypto-hedge-fund
```

2. 安装 Poetry（如果未安装）：
```bash
curl -sSL https://install.python-poetry.org | python3 -
```

3. 安装项目依赖：
```bash
poetry install
```

4. 配置环境变量：
```bash
cp .env.example .env
# 编辑 .env 文件，填写必要的配置信息
```

5. 运行项目：
```bash
poetry run python src/main.py
```

## 配置说明

项目需要配置以下环境变量：

- `OPENAI_API_KEY`: OpenAI API 密钥
- `ANTHROPIC_API_KEY`: Anthropic API 密钥
- `BINANCE_API_KEY`: Binance API 密钥
- `BINANCE_API_SECRET`: Binance API 密钥
- `OKX_API_KEY`: OKX API 密钥
- `OKX_API_SECRET`: OKX API 密钥
- `OKX_PASSPHRASE`: OKX API 密码

## 使用指南

1. 策略回测：
```bash
poetry run python src/backtester.py --strategy strategy_name --timeframe 1d --start 2023-01-01
```

2. 实时交易：
```bash
poetry run python src/main.py --mode live --strategy strategy_name
```

## 开发指南

- 使用 `black` 格式化代码：`poetry run black .`
- 运行测试：`poetry run pytest`
- 代码质量检查：`poetry run flake8`

## 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 贡献指南

欢迎提交 Pull Requests 和 Issues。请确保：
1. 代码符合项目规范
2. 添加适当的测试
3. 更新相关文档