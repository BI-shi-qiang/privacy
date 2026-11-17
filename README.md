# 一页风景 · 隐私政策页面

独立的静态 HTML 页面，通过 GitHub Pages 发布。无需安装依赖、编译或配置后端。

## 页面文件

- `index.html`：网站首页，直接显示完整隐私政策。
- `privacy.html`：隐私政策的独立路径，保留原有文件名。
- `.nojekyll`：让 GitHub Pages 直接发布静态文件。

两个 HTML 文件的内容保持一致。修改政策时，请同步修改这两个文件。

## GitHub Pages 设置

仓库： https://github.com/BI-shi-qiang/privacy

进入仓库 **Settings → Pages → Build and deployment**，设置：

- Source：**Deploy from a branch**
- Branch：**main**
- Folder：**/(root)**

点击 Save。构建和部署状态可在仓库的 Actions 页面查看。部署成功后，以 Pages 设置页显示的 **Visit site** 地址为准。

未使用自定义域名时，默认首页是 https://bi-shi-qiang.github.io/privacy/ ，独立页面是 https://bi-shi-qiang.github.io/privacy/privacy.html 。若账号的用户站点配置了自定义域名，项目站点可能继承该域名，请使用 GitHub 返回的实际发布地址。

将实际页面地址填入扩展商店后台的 Privacy policy URL。提交前，在未登录的浏览器窗口中确认能直接看到“一页风景”的隐私政策正文。

## 更新与发布

在此目录修改页面后执行：

```powershell
git add index.html privacy.html
git commit -m "Update privacy policy"
git push
```

每次推送到 main 后，GitHub Pages 会自动重新部署。如果本机 GitHub 直连失败，而已开启的本地 HTTP 代理仍使用 7897 端口，可以只对这次推送指定代理：

```powershell
git -c http.proxy=http://127.0.0.1:7897 push
```

官方说明：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site