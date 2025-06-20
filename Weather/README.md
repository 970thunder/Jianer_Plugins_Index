# 天气查询插件文档

## 🌤️ 概述

这是一个基于消息事件的天气查询插件，当用户发送特定格式的消息时，它会调用聚合数据API获取天气信息，并以可爱风格回复用户。插件还会记录每个用户的使用次数，数据保存在本地JSON文件中。

## 📦 功能特性

- **实时天气查询**：获取指定城市的实时天气信息
- **天气预报**：提供今明后三天的天气预测
- **可爱风格回复**：使用颜文字和emoji增强用户体验
- **使用次数记录**：记录每个用户的查询次数
- **空气质量报告**：提供AQI空气质量指数
- **智能提示**：根据天气状况给出生活建议
- **错误友好处理**：网络错误时提供可爱提示

## 🛠️ 安装与配置

### 依赖安装

```
pip install requests
```

### API密钥配置

在插件代码中替换您的聚合数据API密钥：

```
ctrl+f查找代码中的下面字段
API_KEY = 'xxx'  # 替换为您的实际API密钥，聚合数据API
```

## 📝 使用方法

### 基础命令

```
[唤醒机器人的命令，如-]天气 [城市名]
-天气 北京
-天气 上海
```

### 响应示例

```
喵~ 北京的实时天气来咯！✧٩(ˊωˋ*)و✧
✨ 这是你本月第 3 次查询天气啦！
☀️ 今天是大晴天，晴！心情也要阳光起来呀！
🌡️ 温度：25°C (温度刚刚好，超舒服的！😊)
💧 湿度：60% (湿度刚刚好，皮肤润润的！)
🍃 风儿：东南风 轻轻吹 (记得带伞或帽子哦！)
🌳 空气质量：AQI 45 (空气超新鲜，深呼吸一下！)
☀️ 明天会是 晴, 温度在 22/30℃ 之间哦! (｡･ω･｡)ﾉ♡
🌤️ 后天呢, 多云, 温度大约 24/31℃~ (＾▽＾)
```

## 💾 数据存储

插件会记录每个用户的使用次数，数据保存在以下路径：

Jianer_QQ_bot\data\weather

存储文件会以json格式保存

- `count`: 用户总使用次数
- `last_used`: 最后使用日期（YYYY-MM-DD格式）

## ⚙️ 自定义配置

| 配置项             | 说明            | 默认值            |
| :----------------- | :-------------- | :---------------- |
| `reminder`         | 命令前缀符号    | `-`               |
| `API_KEY`          | 聚合数据API密钥 | 需替换            |
| `WEATHER_DATA_DIR` | 数据存储目录    | `../data/weather` |

