# 账务完成进度表

金哪达集团月度账务完成进度跟踪网页。

## 功能

- 9 家公司 × 8 个账务步骤（收款 / 付款 / 销项 / 进项 / 报销 / 工资 / 增值税及附加税、印花税（季度申报）/ 折旧摊销）
- 点击单元格即可勾选 / 取消，标记该步骤是否已完成
- **按月份独立保存**：顶部月份切换条（◀ / ▶ / ＋ 新建月份），每个月的勾选记录互不影响
- **自动云端同步（默认开启，零配置）**：勾选数据自动写入本仓库的 `data.json`，任意设备 / 浏览器打开同一页面即可读到最新进度
- 每家公司实时进度条 + 百分比；顶部总完成度环形图
- 添加 / 删除公司、添加 / 删除步骤
- 数据自动保存在浏览器 localStorage；支持导出 / 导入 JSON 备份
- 打印优化（打印当前月份表格）

## 使用

直接打开 [GitHub Pages 地址](https://terrykwok19-commits.github.io/zhangwu-jindu/) 即可使用，或本地双击 `index.html`。

### 多设备同步（推荐：GitHub 同步）

**每台要使用的电脑只需一次性配置**（约 1 分钟），之后该浏览器自动读写本仓库的 `data.json`：

1. 先创建一个 Fine-grained token（GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens）：仓库访问仅选 `zhangwu-jindu`，权限里 Contents 选 **Read and write**。
2. 在这台电脑的浏览器打开（把 `<你的token>` 换成上面生成的 token）：

   ```
   https://terrykwok19-commits.github.io/zhangwu-jindu/?setup=<你的token>
   ```

3. 页面会把 token 存入**当前浏览器**的 localStorage 并切换为 GitHub 同步，自动清理地址栏。之后勾选自动上传、打开 / 切回页面自动拉取最新数据。

> 每台电脑都要做一次；token 只存在各自的浏览器里，不会写入页面或仓库。

### 默认同步方式（未配置时）

未配置 GitHub 同步的浏览器默认使用免费云端 JSON 存储（jsonblob.com）临时同步，数据桶公开可读写、闲置会被清理，仅适合临时查看；**正式使用请按上面的方法配置一次 GitHub 同步**。所有数据均可通过「导出 Excel」随时备份。
