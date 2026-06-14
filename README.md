# 智能轻食减脂助手

一款基于 AI 的智能饮食管理应用，为减脂人群提供个性化饮食建议、智能食材替代推荐、天气联动运动建议等功能。

## ✨ 功能特色

- **智能聊天交互** - 自然语言对话，上下文记忆
- **图片食物识别** - 拍照识别食物，获取营养信息
- **饮食记录管理** - 自动记录，营养统计
- **天气查询与运动建议** - 自动定位，智能联动
- **智能食材替代推荐** - 25+种高热量食材替代方案
- **食谱推荐** - 三餐推荐，多样化推荐
- **意图识别系统** - 精准区分意愿表达与实际摄入

## 🛠️ 技术栈

| 层级 | 技术 |
|------|------|
| 前端 | Vue 3 + Vite |
| 后端 | FastAPI |
| 图片识别 | Kimi API |
| 文本生成 | DeepSeek API |
| 天气数据 | OpenWeatherMap API |
| 数据库 | SQLite |

## 🚀 快速开始

### 环境要求

- Python 3.10+
- Node.js 18+
- npm 9+

### 后端安装

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Linux/Mac
# 或
venv\Scripts\activate     # Windows

pip install -r requirements.txt
```

### 前端安装

```bash
cd frontend
npm install
```

### 配置环境变量

在 `backend/.env` 中配置：

```env
MOONSHOT_API_KEY=your_kimi_api_key
DEEPSEEK_API_KEY=your_deepseek_api_key
OPENWEATHER_API_KEY=your_weather_api_key
IMAGE_API_TYPE=kimi
TEXT_API_TYPE=deepseek
```

### 启动服务

```bash
# 启动后端
cd backend
python main.py

# 启动前端（新终端）
cd frontend
npm run dev
```

### 访问地址

- 前端：http://localhost:5173
- 后端API：http://localhost:8080

## 📁 项目结构

```
smart-diet-assistant/
├── backend/                 # 后端代码
│   ├── app/                # 应用代码
│   │   ├── api/           # API路由
│   │   ├── services/      # 业务服务
│   │   ├── models/        # 数据模型
│   │   └── main.py        # 入口文件
│   ├── requirements.txt   # Python依赖
│   └── .env               # 环境变量
├── frontend/               # 前端代码
│   ├── src/               # 源代码
│   ├── index.html         # HTML入口
│   ├── vite.config.js     # Vite配置
│   └── package.json       # npm依赖
├── docs/                  # 文档
└── README.md
```

## 📡 API接口

| 接口 | 方法 | 描述 |
|------|------|------|
| `/api/v1/chat` | POST | 聊天交互 |
| `/api/v1/image/recognize` | POST | 图片识别 |
| `/api/v1/diet/records` | GET/POST | 饮食记录 |
| `/api/v1/weather/current` | GET | 天气查询 |
| `/api/v1/substitution/find` | GET | 食材替代 |

## 📄 文档

- [软件需求说明书](docs/软件需求说明书.md)
- [测试用例](docs/TEST_CASES.md)
- [测试方案](docs/TEST_PLAN.md)
- [测试报告](docs/TEST_REPORT.md)
- [部署指南](docs/部署指南.md)

## 📝 许可证

MIT License
