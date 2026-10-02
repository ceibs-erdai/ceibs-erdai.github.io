# CEIBS二代聚会

CEIBS校友会二代在多伦多的活动报名板：https://ceibs-erdai.github.io/

- 整个网站就是 `index.html`。改完推到 `main` 分支，GitHub Pages 大约一分钟后自动更新。
- 报名数据存在 Supabase。网页里的 publishable key 本来就是公开的，谁能读写由数据库的行级安全策略控制。
- `.github/workflows/keepalive.yml` 每天访问一次数据库，防止 Supabase 免费版因为没人访问被暂停；失败时 GitHub 会发邮件。
