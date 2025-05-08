# PtvAlert网页版

## 项目简介

PtvAlert网页版是一个基于Google Maps和Firebase的实时交通/事件上报与可视化平台。用户可以在地图上添加带有图片和描述的报告，所有用户都能实时看到这些报告。每个报告会以emoji标记显示在地图上，点击可查看详情、评论、编辑或删除。报告会在创建3小时后自动从地图和数据库消失。

## 主要功能
- 地图实时显示所有用户上报的事件（带emoji标记）
- 支持图片上传、文字描述
- 支持评论、编辑、删除自己的报告
- 报告3小时后自动过期消失
- 弹幕显示最新公告和交通信息
- 支持移动端和PC端自适应

## 使用方法

1. **克隆或下载本项目代码**
2. **打开 `index.html` 文件**（建议使用本地服务器环境，如VSCode Live Server、http-server等）
3. **首次加载会自动初始化Firebase和Google地图**
4. **点击"+" 添加报告"按钮**，在地图上点选位置，填写描述、上传图片，点击"确定"提交
5. **地图上会出现emoji标记**，点击标记可查看详情、评论、编辑或删除（仅限本人）
6. **报告3小时后自动消失**

## 依赖说明
- [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript/overview)
- [Firebase Realtime Database](https://firebase.google.com/docs/database)
- 无需后端服务器，所有数据实时同步到Firebase

## 本地开发与部署

1. **获取Google Maps API Key**
   - 申请并替换 `index.html` 中 `<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY...` 的 `YOUR_API_KEY`
2. **配置Firebase**
   - 使用你自己的Firebase项目，替换 `index.html` 里的 `firebaseConfig` 配置
3. **本地预览**
   - 推荐用VSCode插件"Live Server"或`npx http-server`等工具本地预览
   - 直接用浏览器打开`index.html`部分功能可能受限（如图片上传、定位等）

## 注意事项
- 本项目为前端纯静态实现，所有用户数据公开存储于Firebase
- 请勿上传敏感信息或隐私图片
- 若需正式部署，请自行配置域名、API密钥和Firebase安全规则

## 贡献与反馈
如有建议或Bug反馈，请提交Issue或PR。

---

MIT License 