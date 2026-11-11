# 报价反馈系统 (Quotation Feedback System)

本项目已根据需求优化为 **一键直达反馈 + Vercel 免费托管** 模式。

## 目录结构
- `api/feedback.js`：处理 Medium/Low 一键反馈与邮件通知
- `api/submit-high.js`：处理 High 价格差距提交与邮件通知
- `public/high-form.html`：客户选择 High Price 时的百分比填写网页
- `sendMail.js`：发信测试脚本
- `vercel.json`：Vercel 部署路由配置文件

## 部署步骤
1. 解压项目，在 GitHub 新建仓库 `quotation-feedback` 并上传全部文件。
2. 登录 Vercel 导入该 GitHub 仓库。
3. 在 Vercel 环境变量中设置：
   - `SMTP_HOST`: `smtp.qq.com`
   - `SMTP_PORT`: `465`
   - `SMTP_USER`: `你的邮箱`
   - `SMTP_PASS`: `你的授权码`
4. 点击 Deploy 部署，将得到的线上域名更新至 `sendMail.js` 即可使用。
