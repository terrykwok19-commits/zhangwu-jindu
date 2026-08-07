# 账务完成进度表

金哪达集团月度账务完成进度跟踪网页。

## 功能

- 9 家公司 × 8 个账务步骤（收款 / 付款 / 销项 / 进项 / 报销 / 工资 / 增值税及附加税、印花税（季度申报）/ 折旧摊销）
- 点击单元格即可勾选 / 取消，标记该步骤是否已完成
- **按月份独立保存**：顶部月份切换条（◀ / ▶ / ＋ 新建月份），每个月的勾选记录互不影响
- **自动云端同步（默认开启）**：配置一次后，勾选数据自动写入本仓库的 `data.json`，任意设备 / 浏览器打开同一页面即可读到最新进度
- 每家公司实时进度条 + 百分比；顶部总完成度环形图
- 添加 / 删除公司、添加 / 删除步骤
- 数据自动保存在浏览器 localStorage；支持导出 / 导入 JSON 备份
- 打印优化（打印当前月份表格）

## 使用

直接打开 [GitHub Pages 地址](https://terrykwok19-commits.github.io/zhangwu-jindu/) 即可使用，或本地双击 `index.html`。

### 自动同步

**默认开启**，配置一次即可全自动云端保存：
1. 打开我提供的「专属配置链接」（URL 带 `?setup=<token>`），页面会自动把 Token 存入当前浏览器并清掉地址栏参数 —— 之后无需任何设置。
2. 每台要用同步的设备 / 浏览器，各打开一次专属链接即可。
3. 之后每次勾选都会自动写入仓库 `data.json`；打开页面、切换回本页时自动拉取最新数据。

> 安全说明：Token 只保存在各浏览器 localStorage，不会写入页面或仓库（GitHub 密钥推送保护也会拦截把令牌写进公开仓库）。也可以手动在页面「⤓ 同步设置」中粘贴自己新建的 Fine-grained token：GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens → 仓库只选 `zhangwu-jindu` → Contents 权限选 Read and write。
