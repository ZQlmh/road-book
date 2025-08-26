# 呼伦贝尔自驾路书（9.27-10.4）- 百度地图

本项目在浏览器中使用百度地图 JS API 自动绘制你的行程路线，并为每段行程标注距离、预估耗时与地点名称，同时展示每日景点与住宿信息。

## 快速开始

1) 申请并配置百度地图 AK：
- 打开百度地图开放平台，创建浏览器端 AK
- 在 Referer 白名单中添加开发地址：`http://localhost/*` 和 `http://127.0.0.1/*`
- 复制你的 AK

2) 替换 AK：
- 打开 `index.html`
- 替换脚本地址中的 `YOUR_BAIDU_MAP_AK_HERE` 为你的 AK：
  ```html
  <script src="https://api.map.baidu.com/api?v=3.0&ak=你的AK"></script>
  ```

3) 启动本地静态服务（任选其一）：
- Python 3：
  ```bash
  cd /workspace/roadbook-baidu && python3 -m http.server 5173
  ```
  然后访问：`http://127.0.0.1:5173`
- Node（若有）：
  ```bash
  npx http-server -p 5173 /workspace/roadbook-baidu
  ```

## 使用说明

- 页面顶部可切换具体日期，或一键“渲染全行程”
- 侧边栏展示每日合计里程、总耗时与分段详情
- 地图中的彩色线条为行车路线，打点为景点/地点标注
- 若某些关键词较模糊，可将 `itinerary.js` 中的名称改为更具体（如“白鹿岛景区”），以获得更稳定的路径规划

## 数据来源与说明

- 距离、耗时来自百度地图驾车路线规划，受实时路况/道路管制影响
- 本路书仅供参考，实际出行请注意安全并遵守当地交通法规

## 自定义

- 修改 `itinerary.js` 可调整行程、景点与住宿说明
- 如需添加更多打点或颜色区分，可在 `index.html` 的脚本内做简单扩展