# LIEGU 设计与样品周报 · GitHub Pages 发布版

这个发布包可以直接放到 GitHub 仓库。首页是 `index.html`，样式和交互代码都已包含在首页中，不需要 npm、构建命令或外部服务器。

## 先弄清 404

此前截图中的文件名为 `LIEGU DESIGN.html`。访问仓库网站首页时，GitHub Pages 需要在发布目录最外层找到 `index.html`（大小写敏感）。如果只有其他文件名，首页就可能出现 404。

本包已经固定首页文件名。发布源未开启、目录选错、构建未完成或网址路径错误，也可能导致 404；只上传文件不会自动开启 Pages。

## 上传步骤

1. 下载并解压发布包。不要把 ZIP 压缩包本身当成网站上传。
2. 进入你的 GitHub 仓库 `onepunchwang/LIEGU-DESIGN`。
3. 选择 `Add file` → `Upload files`。
4. 上传解压后里面的文件，让 `index.html` 直接出现在 `main` 分支根目录。
5. 点击 `Commit changes`。如果同名首页已经存在，上传本包的 `index.html` 作为更新。

根目录应能直接看见以下文件，不要多套一层文件夹：

| 文件 | 作用 |
| --- | --- |
| `index.html` | 网站首页；包含全部样式和页面交互 |
| `.nojekyll` | 按普通静态文件发布，跳过 Jekyll 处理 |
| `404.html` | 网址路径错误时的提示页 |
| `README.md` | 本说明 |
| `部署说明.txt` | 可用记事本打开的步骤 |

最低限度上传 `index.html` 即可。完整上传建议同时带上 `.nojekyll` 和 `404.html`。

## 开启 GitHub Pages

1. 仓库顶部点击 `Settings`。
2. 左侧点击 `Pages`。
3. 在 `Build and deployment` 中设置：
   - `Source`：`Deploy from a branch`。
   - `Branch`：`main`。
   - 文件夹：`/(root)`。
4. 点击 `Save`。
5. 到 `Actions` 查看 Pages 发布任务；成功后回到 `Settings` → `Pages`，点击 `Visit site`。
6. 分享 `Visit site` 打开的网页地址，不要分享 GitHub 的代码文件页地址。

在没有自定义域名的情况下，这个仓库的网站地址通常为：

`https://onepunchwang.github.io/LIEGU-DESIGN/`

这是按仓库名推算的预期地址，本包没有替你开启 Pages，最终以 Pages 页面实际显示的地址为准。官方说明发布更新可能需要最多约 10 分钟。

## 如何使用

- 上方有五项本周任务；编辑任务名称后，下方分类名称同步变化。
- “全部设计图”显示全部作品，其余五个菜单按本周任务筛选。
- 在某个分类中点击“提交作品”，会自动选中该任务。
- 填写鞋款名称、设计师、设计说明、工艺及风险，并插入图片。
- 多图作品保留主图，其余图片固定在右上角，点击可放大。
- “分享网页”可复制当前 GitHub Pages 地址，保留仓库子路径。
- “导出展示 HTML”可导出本周已经填写的文字和图片，生成一个可独立分享的展示文件。
- “导出备份”保留历史周报、文字和图片；“导入备份”可恢复。

## 数据保存范围

本版本保留浏览器本机保存方式。别人打开同一个链接后，填写的是他自己浏览器里的内容；你不会自动收到对方上传的作业。分享入口、分享已填内容、团队集中收作业是三个不同需求：

| 需求 | 本版本的做法 |
| --- | --- |
| 分享可操作的网页 | 发布后使用“分享网页” |
| 分享本周文字和图片 | 导出展示 HTML，再发送文件或自行发布 |
| 统一接收设计师的作业 | 需要另外配置云端数据库和图片存储，本包未包含 |

此前的本机数据不会因为你在 GitHub 上更新文件而自动上传到 GitHub。清理浏览器数据或换设备可能丢失本机记录，请导出备份保留。

国内微信的可访问性需要使用国内网络实际验证，本包不承诺 GitHub Pages 的国内访问稳定性。

## 官方排查资料

- https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
