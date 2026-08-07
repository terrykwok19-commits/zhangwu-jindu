# 账务完成进度表

金哪达集团月度账务完成进度跟踪网页。

## 功能

- 9 家公司 × 8 个账务步骤（收款 / 付款 / 销项 / 进项 / 报销 / 工资 / 增值税及附加税、印花税（季度申报）/ 折旧摊销）
- 点击单元格即可勾选 / 取消，标记该步骤是否已完成
- **按月份独立保存**：顶部月份切换条（◀ / ▶ / ＋ 新建月份），每个月的勾选记录互不影响
- **GitHub 自动同步**：开启后，勾选数据自动写入本仓库的 `data.json`，任意设备 / 浏览器打开同一页面即可读到最新进度
- 每家公司实时进度条 + 百分比；顶部总完成度环形图
- 添加 / 删除公司、添加 / 删除步骤
- 数据自动保存在浏览器 localStorage；支持导出 / 导入 JSON 备份
- 打印优化（打印当前月份表格）

## 使用

直接打开 [GitHub Pages 地址](https://terrykwok19-commits.github.io/zhangwu-jindu/) 即可使用，或本地双击 `index.html`。

### 开启自动同步（可选，推荐）

1. 页面右上角点击「⤓ 同步设置」。
2. 同步模式选择「GitHub 自动同步」。
3. 创建访问令牌（免费）：
   - GitHub → Settings → Developer settings → Personal access tokens → **Fine-grained tokens** → Generate new token
   - Repository access 选 **Only select repositories** → 勾选 `zhangwu-jindu`
   - Permissions 中 **Contents** 选择 **Read and write**
   - 生成后把 Token 粘贴到页面（Token 只保存在本机浏览器 localStorage）
4. 点击「测试连接」，再点「保存设置」即可。
5. 之后每次勾选都会自动写入仓库 `data.json`；打开页面、切换回本页时自动拉取最新数据。

> 说明：Token 若泄露，仅能读写 `zhangwu-jindu` 这一个仓库的代码文件，无法访问其他资源；可在 GitHub 随时撤销重建。
