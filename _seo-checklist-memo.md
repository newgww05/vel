# Velcura 新产品落地页 · SEO/GEO 标准清单

> 每次制作新的独立产品落地页（如 hydrogel-dressing.html、super-absorbent-dressing.html 等），
> 必须逐项完成以下5件事，不需要用户再次提醒。

## 1. 独立 canonical 标签
<link rel="canonical" href="https://velcura.net/[文件名].html">

## 2. 结构化数据（JSON-LD）
- Product schema：name、description、brand、manufacturer（含统一地址）、image
- BreadcrumbList：Home > Wound Care > [产品名]

## 3. 收录进 sitemap.xml
- 新增 <url> 条目，lastmod 填当天日期，参照同类产品页的 changefreq / priority
- **【工作流更新】不再手动编辑XML。用 generate_sitemap.py 脚本自动生成/更新**
  - 用户固定把网站文件存放在本地 `E:\p网页存放\上线版本\website`
  - 需要更新sitemap时，用户上传该 website 文件夹（或至少所有.html文件）
  - Claude 自动运行 generate_sitemap.py 扫描全部页面、生成完整准确的sitemap.xml
  - 用户拿到新文件后手动替换到本地文件夹，再上传到线上仓库
  - 脚本位置：/home/claude/generate_sitemap.py（每次新会话如果脚本不在，需要重新生成一份，逻辑见脚本内注释）

## 4. 英文长尾词自然融入
- <title>
- <meta name="description">
- <h1>
- 不堆砌关键词，语句要自然

## 5. 内链回链至 wound-care.html 分类页
- 页面内加一个链接指回 wound-care.html 对应分类（形成主题集群 topic cluster）
- 如有相关产品/内容页，也互相加内链（如 pressure-injury-care.html、diabetic-foot-ulcer-care.html 等）

## 6. 全英文化
- 页面可见文字、代码注释、meta信息、alt文本、结构化数据——全部使用英文，不夹杂中文
- 禁止把地址、产品参数等信息翻译成中文
- 完稿后全文扫描一遍中文字符（\u4e00-\u9fff），确认零残留

---

## 待完成落地页队列（按优先级，来自修正版SEO报告；2026-09-03起顺序反转，从队尾开始做）
1. ~~hydrogel-dressing.html — 水凝胶敷料~~ ✅ 已完成 2026-09-02
2. ~~wound-cleanser.html — 伤口清洗液~~ ✅ 已完成 2026-09-03（用户要求顺序反转，优先做这个；后又按AD006模板重做一版）
3. ~~biocellulose-dressing.html — 生物纤维素敷料~~ ✅ 已完成 2026-09-03
4. ~~collagen-wound-dressing.html — 胶原蛋白敷料~~ ✅ 已完成 2026-09-03
5. ~~npwt-foam-dressing.html — 负压伤口治疗~~ ✅ 已完成 2026-09-03
6. ~~super-absorbent-dressing.html — 超吸收敷料~~ ✅ 已完成 2026-09-03

每做完一个，从队列划掉，继续下一个。
