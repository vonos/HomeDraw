# HomeDraw - 乡村地图标绘工具 / HomeDraw — Village Map Drawing Tool

HomeDraw是一个为偏远乡村打造的简易网页地图工具，让地图上看不见的老家也能被清晰标记、被好好看见。
HomeDraw is a lightweight web mapping tool built for remote villages, so that hometowns invisible on the map can be clearly marked and seen.

## 功能特点 / Features

### 核心功能 / Core Features
- **绘制要素**：支持绘制房屋/地块（多边形）、道路（折线）和标记（点）
- **Draw features**: draw houses/plots (polygons), roads (polylines) and markers (points)
- **要素编辑**：支持选择、删除和修改已绘制的要素
- **Edit features**: select, delete and modify drawn features
- **属性信息**：支持为要素添加详细信息，如用途、面积、备注等
- **Attributes**: add detailed info to features, such as usage, area, notes, etc.
- **本地存储**：自动保存到浏览器本地存储，刷新页面不丢失数据
- **Local storage**: auto-saved to browser local storage; data persists across refreshes
- **地图定位**：支持输入地名自动定位到对应位置
- **Geolocation**: type a place name to auto-locate it
- **要素搜索**：支持按名称和类型搜索已绘制的要素
- **Feature search**: search drawn features by name and type
- **界面调整**：支持手动拉伸调整左右面板宽度
- **UI adjustment**: manually drag to resize the left/right panel widths

### 技术特点 / Technical Highlights
- **轻量化设计**：纯前端实现，无需后端服务
- **Lightweight**: pure frontend, no backend service needed
- **易上手操作**：直观的用户界面，简单易用
- **Easy to use**: intuitive UI, simple to operate
- **响应式布局**：适配不同屏幕尺寸
- **Responsive**: adapts to different screen sizes
- **实时反馈**：操作过程中提供实时状态提示
- **Real-time feedback**: live status hints during operation
- **美观图标**：使用高德地图提供的美观标记图标
- **Nice icons**: uses AMap's polished marker icons

## 使用方法 / How to Use

### 基本操作 / Basic Operations
1. **定位老家**：在顶部搜索框输入老家地名，点击"定位老家"按钮
1. **Locate hometown**: enter the hometown name in the top search box, click "定位老家 / Locate"
2. **绘制要素**：选择相应的绘制工具，在地图上点击绘制，双击结束
2. **Draw features**: pick a drawing tool, click on the map to draw, double-click to finish
3. **保存要素**：输入要素名称和详细信息，点击"保存要素"按钮
3. **Save feature**: enter a name and details, click "保存要素 / Save"
4. **编辑要素**：点击"选择要素"按钮，点击要编辑的要素，然后点击"修改要素"或"删除要素"按钮
4. **Edit feature**: click "选择要素 / Select", click the feature, then "修改 / Modify" or "删除 / Delete"
5. **搜索要素**：在左侧搜索框输入要素名称，选择要素类型，点击"搜索"按钮
5. **Search**: type the name in the left box, choose a type, click "搜索 / Search"
6. **调整界面**：拖动中间的分隔条可以调整左右面板的宽度
6. **Adjust UI**: drag the middle divider to resize panels

### 绘制操作 / Drawing
- **绘制房屋/地块**：点击"绘制房屋/地块"按钮，在地图上点击绘制多边形，双击结束
- **Houses/plots**: click "绘制房屋/地块 / Draw house/plot", click to draw polygon, double-click to finish
- **绘制道路**：点击"绘制道路"按钮，在地图上点击绘制折线，双击结束
- **Roads**: click "绘制道路 / Draw road", click to draw polyline, double-click to finish
- **添加标记**：点击"添加标记"按钮，在地图上点击添加标记
- **Markers**: click "添加标记 / Add marker", click on the map to place it

### 编辑操作 / Editing
- **选择要素**：点击"选择要素"按钮，然后点击地图上的要素
- **Select**: click "选择要素 / Select", then click the feature
- **删除要素**：选择要素后，点击"删除要素"按钮
- **Delete**: after selecting, click "删除要素 / Delete"
- **修改要素**：选择要素后，点击"修改要素"按钮，然后调整要素形状
- **Modify**: after selecting, click "修改要素 / Modify", then adjust the shape

## 技术实现 / Implementation

### 前端技术 / Frontend
- **HTML5**：页面结构 / page structure
- **CSS3**：页面样式 / styling
- **JavaScript**：交互逻辑 / interactivity
- **高德地图JSAPI 2.0**：地图服务 / map service

### 核心依赖 / Core Dependencies
- **高德地图JSAPI**：提供地图显示、绘制工具和地理编码服务
- **AMap JSAPI**: map display, drawing tools and geocoding
- **localStorage**：本地数据存储 / local data storage

### 项目结构 / Project Structure
```
homedraw.html          # 主页面文件 / main page
README.md             # 项目说明文件 / this file
```

## 浏览器兼容性 / Browser Compatibility

支持所有现代浏览器，包括：
Works on all modern browsers, including:
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 本地存储 / Local Storage

所有绘制的要素数据都存储在浏览器的localStorage中，键名为`villageMapFeatures`。数据格式为JSON，包含要素的名称、类型、坐标和属性信息。
All drawn feature data is stored in the browser's localStorage under the key `villageMapFeatures`, as JSON containing each feature's name, type, coordinates and attributes.

## 注意事项 / Notes

1. **数据安全**：本地存储数据仅保存在当前浏览器中，清除浏览器数据会导致数据丢失
1. **Data safety**: local-storage data lives only in the current browser; clearing browser data loses it
2. **地图精度**：高德地图在偏远乡村地区的精度可能有限
2. **Map accuracy**: AMap accuracy in remote villages may be limited
3. **性能优化**：绘制大量要素时可能会影响性能，建议合理控制要素数量
3. **Performance**: drawing many features may slow things down; keep the count reasonable

## 未来规划 / Roadmap

- [ ] 支持导出和导入数据 / Export & import data
- [ ] 添加更多要素类型 / More feature types
- [ ] 优化移动端体验 / Better mobile experience
- [ ] 增加测量功能 / Measurement tools
- [ ] 支持多用户协作 / Multi-user collaboration

## 许可证 / License

本项目采用 MIT 许可证。
Licensed under the MIT License.

## 贡献 / Contributing

欢迎提交问题和建议，帮助改进这个工具。
Issues and suggestions are welcome to help improve this tool.

---

让我们一起为偏远乡村创建更清晰、更实用的地图！
Let's build clearer, more useful maps for remote villages, together!
