# Nicole · 记账工作台

手机优先、无后端、无广告的本地记账网页。粉色 #FFE5ED + 薄荷绿 #E8FFF4。

## 功能
- 统计：月度/年度收支、结余、近 12 个月趋势、分类统计
- 明细：搜索、月份和类型筛选、编辑、删除、照片附件
- 记账：收入、支出、转账、金额、分类、账户、日期、备注、照片
- 账本：账户余额、多账本名称
- 我的：JSON 备份/恢复、预算、A4 打印、清空数据
- IndexedDB 本地保存，Service Worker 缓存网页

## 部署到 GitHub Pages
1. 将本项目文件上传到仓库根目录，保留 `.github/workflows/deploy.yml`。
2. GitHub 仓库 Settings → Pages → Build and deployment → Source 选择 GitHub Actions。
3. 推送到 main/master 后，等待 Actions 成功。
4. 默认网址：https://nicole96fang.github.io/keep-check-money/

## 数据安全
账目和照片保存在当前浏览器 IndexedDB，不会上传到 GitHub。清除 Safari 网站数据可能删除本机资料。定期在「我的」导出 JSON，并保存到 iCloud Drive 或「文件」。


## Dreamy Garden visual refresh
- The supplied Big Ben watercolor image is included as `dreamy-garden-bg.jpeg` and used as the app-wide background.
- Existing IndexedDB ledger storage and transaction workflows are retained.
- The statistics category section now uses a donut chart with a category legend.

## Watercolor glass v5
- Dashboard cards use a lighter 15% white glass layer and a restrained 3px backdrop blur.
- The page-wide white wash is reduced so the garden watercolor background remains visible.
- Service worker cache key updated to v9 to help browsers fetch the new styling.
- Ledger logic and local IndexedDB data structure are unchanged.
