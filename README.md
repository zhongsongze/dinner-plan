# 成都聚餐地点规划工具

一个基于百度地图 JSAPI 的 Web 应用，帮助在成都居住的三位朋友找到合适的聚餐地点。

## 功能特点

- **三方位置标注**：在地图上显示三个人的居住位置
- **智能中间点搜索**：自动计算三人地理中心点，搜索附近候选地点
- **自定义搜索关键词**：支持搜索餐厅、酒店、网吧、电影院等各种目的地
- **精细通勤时间显示**：显示地铁通勤时间（分钟/小时）
- **路线可视化**：点击任意候选点，显示三人到该地点的地铁线路
- **自动排序**：已计算的候选点按最长通勤时间自动排序
- **API 优化**：按需加载路线，避免百度地图 API 限流

## 使用方法

1. 访问在线地址：https://zhongsongze.github.io/dinner-plan/
2. 等待地图加载完成，三个人的位置会自动标注
3. 在搜索框输入目的地类型（如：餐厅、酒店、网吧）
4. 点击「搜索候选地点」按钮
5. 点击任意候选点查看详细路线和通勤时间

## 技术栈

- HTML5 + CSS3 + JavaScript
- 百度地图 JSAPI GL 版本
- GitHub Pages 部署

## 项目结构

```
dinner-plan/
├── dinner-plan.html    # 主应用文件
└── README.md           # 项目文档
```

## 配置说明

如需使用自己的百度地图 AK：

1. 访问 [百度地图开放平台](https://lbsyun.baidu.com/)
2. 创建应用获取 AK
3. 修改 `dinner-plan.html` 中的 AK：

```javascript
// 找到这一行，替换为你的 AK
<script src="//api.map.baidu.com/api?v=1.0&type=webgl&ak=你的AK"></script>
```

## 本地开发

```bash
# 启动本地服务器
python3 -m http.server 8080

# 访问 http://localhost:8080/dinner-plan.html
```

## 许可证

MIT License
