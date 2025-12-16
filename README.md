# 电影推荐系统

基于Python FastAPI和React的电影推荐系统，包含前后端数据交互和数据库连接。

## 项目结构

```
PPPP/
├── backend/                 # FastAPI后端
│   ├── main.py            # 主应用文件
│   ├── config.py          # 配置文件
│   ├── database.py        # 数据库连接
│   ├── requirements.txt   # Python依赖
│   ├── models/            # 数据模型
│   ├── routers/           # API路由
│   ├── schemas/           # Pydantic模式
│   └── utils/             # 工具函数
├── frontend/              # React前端
│   ├── public/            # 静态资源
│   ├── src/               # 源代码
│   │   ├── components/    # React组件
│   │   ├── pages/         # 页面组件
│   │   ├── services/      # API服务
│   │   ├── types/         # TypeScript类型
│   │   └── utils/         # 工具函数
│   ├── package.json       # Node.js依赖
│   └── tsconfig.json      # TypeScript配置
├── database/              # 数据库脚本
│   └── init_db.py         # 数据库初始化
├── start.bat              # Windows启动脚本
└── README.md              # 项目说明
```

## 功能特性

- 用户注册/登录
- 电影浏览和搜索（支持按类型、年份筛选）
- 电影详情展示
- 电影评分和评论
- 基于协同过滤和内容的推荐算法
- 个性化推荐页面
- 用户个人中心（展示评分历史）

## 技术栈

### 后端
- Python 3.9+
- FastAPI
- SQLAlchemy
- PyMySQL
- JWT认证
- NumPy, Pandas, Scikit-learn（推荐算法）

### 前端
- React 18
- TypeScript
- React Router
- Axios
- CSS Modules

## 快速开始

### 前置要求

- Python 3.9+
- Node.js 16+
- MySQL 5.7+ 或 8.0+

### 数据库设置

1. 创建名为`moves`的数据库：
```sql
CREATE DATABASE moves;
```

2. 运行数据库初始化脚本：
```bash
cd database
python init_db.py
```

### 使用启动脚本（推荐）

Windows用户可以直接运行`start.bat`脚本：
```bash
start.bat
```

然后按照提示选择启动方式。

### 手动启动

#### 后端设置
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

#### 前端设置
```bash
cd frontend
npm install
npm start
```

## 访问地址

- 前端应用: http://localhost:3000
- 后端API: http://localhost:8000
- API文档: http://localhost:8000/docs

## 测试账户

系统初始化时创建了以下测试账户：
- 用户名: `admin` 密码: `admin123`
- 用户名: `moviefan` 密码: `password123`
- 用户名: `cinephile` 密码: `password123`

## 环境变量

复制`.env.example`为`.env`并根据需要修改配置：
- 数据库连接信息
- JWT密钥

## API文档

启动后端服务后，访问 http://localhost:8000/docs 查看交互式API文档。

## 项目截图

[TODO: 添加项目截图]

## 贡献

欢迎提交Issue和Pull Request！

## 许可证

MIT License