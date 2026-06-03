# MetroVisualization（深圳地铁乘客出行可视化）

这是一个纯前端可视化页面：使用 Leaflet 作为底图，叠加 D3 的 SVG 图层，展示深圳地铁线路、站点，以及基于问卷/访谈数据（`interview.csv`）生成的乘客出行起终点与路径（起点为绿色、终点为红色的渐变曲线）。

## 在线/本地运行

本项目会在浏览器中通过 `fetch` 读取同目录下的 `geojson/csv` 数据文件，因此需要通过本地静态服务器访问（不要直接双击打开 `metro.html`）。

### 本地启动（推荐）

在项目目录执行：

```bash
python -m http.server 8000
```

然后在浏览器打开：

```
http://localhost:8000/metro.html
```

## 目录结构

- `metro.html`：主页面（Leaflet + D3 可视化逻辑）
- `shenzhen_lines.geojson`：地铁线路数据
- `shenzhen_stations.geojson`：地铁站点数据
- `interview.csv`：乘客基本信息与出行路径数据
- `#出行信息可视化网页.md`：可视化交互与实现说明

## 交互说明（页面内）

- 右侧按钮：切换“工作日 / 节假日”模式
- 底部滑块：按年龄段筛选
- 地铁线路/站点/路径支持悬停提示与点击弹窗查看详细信息

## GitHub Pages（可选）

如果需要用 GitHub Pages 在线展示：

1. 在仓库 Settings → Pages 中选择部署分支（例如 `main`）与目录（`/root`）。
2. 等待 GitHub 自动构建完成后，访问生成的 Pages 链接即可。

