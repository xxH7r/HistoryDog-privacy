# 历史汪隐私政策 / HistoryDog Privacy Policy

> 适用版本 / Applicable version: `0.7.2`<br>
> 更新日期 / Last updated: `2026-07-19`

本隐私政策适用于“历史汪 / HistoryDog”浏览器扩展。历史汪的核心功能是帮助用户在自己的浏览器中搜索并重新打开浏览历史记录。核心检索在本地完成；只有用户主动配置 DeepSeek API Key 后，扩展才会调用 DeepSeek 提供可选的查询规划和结果排序。

This privacy policy applies to the HistoryDog browser extension. HistoryDog helps users search and reopen their own browsing history. Core retrieval is performed locally. The extension only calls DeepSeek for optional query planning and result ranking after the user explicitly configures a DeepSeek API key.

## 中文

### 1. 我们处理的数据

为提供浏览历史搜索功能，扩展可能在用户的浏览器本地读取或保存：

- 浏览历史记录：网页标题、URL、访问时间和访问次数。
- 用户输入：用户在扩展搜索框中输入的自然语言描述或关键词。
- 页面元数据索引：Title、Meta/OG Description、页面首个 H1、站点名、规范化 URL、最后访问时间和访问次数。
- 扩展设置与状态：界面语言、索引开关、最近搜索、当前搜索会话和用户主动配置的 DeepSeek API Key。

API Key 属于身份验证信息，仅保存在浏览器的扩展本地存储中，并仅在用户启用 AI 功能时用于直接鉴权 DeepSeek API 请求。开发者不会收到或保存该 API Key。

### 2. 本地页面元数据索引

页面元数据索引默认开启，用于改善仅靠历史记录标题和 URL 难以找回的网页。索引数据保存在本机 IndexedDB 中，最多保留约 50,000 条记录，超过容量时按最近访问时间清理。

- 只处理普通 HTTP/HTTPS 页面。
- 不保存页面正文、Cookie、表单值、密码或 URL hash。
- 检测到密码输入框的页面不会建立增强元数据索引。
- URL 入库前会移除凭据、常见追踪参数，以及 token、password、session、auth 等敏感参数。用于本地页面识别的规范化 URL 可能保留少量非敏感参数。
- 首次安装或升级时，扩展可从浏览器历史记录中导入最多约 365 天、50,000 条已有记录的标题和 URL，但不会联网回访旧网页以抓取内容。
- 无痕/InPrivate 标签页不会写入页面元数据索引；后台会根据浏览器提供的标签页私密状态拒绝保存。

用户可以随时在设置页关闭或清空本地页面索引。

### 3. DeepSeek 可选 AI 功能

未配置 DeepSeek API Key 时，扩展不会调用 AI 服务，浏览历史搜索仍可使用本地检索与排序完成。

配置 API Key 后，每次搜索最多发起两次 DeepSeek API 请求：

1. 查询规划：发送用户输入的搜索描述。
2. 结果精排：发送最多 20 条候选记录的标题、域名、脱敏 pathname、截断的页面元数据摘要、相对访问时间和本地匹配证据。

扩展不会向 DeepSeek 发送完整页面正文、Cookie、表单值、密码、URL query string 或 URL hash。API 请求由扩展直接发往 `https://api.deepseek.com/`，不经过开发者运营的中转服务器。发送给 DeepSeek 的信息由 DeepSeek 按其服务条款和隐私政策处理。

### 4. 数据共享、出售与用途限制

- 开发者不出售用户数据。
- 开发者不将用户数据用于广告、信用评估、贷款或与浏览历史搜索无关的用途。
- 除用户主动启用 DeepSeek 功能所必需的 API 请求外，扩展不会向第三方传输用户数据。
- 扩展不包含远程分析、遥测或开发者运营的远程日志收集功能。
- 扩展不会下载或执行远程代码；所有可执行代码均包含在发布的扩展程序包中。

### 5. 数据保留与用户控制

- 浏览历史数据由浏览器管理；扩展按需读取，不会将其上传到开发者服务器。
- 页面元数据索引、设置、最近搜索和搜索会话保存在用户设备本地。
- 用户可以不配置或随时删除 DeepSeek API Key。
- 用户可以关闭或清空页面元数据索引，并清除最近搜索记录。
- 用户可以通过浏览器的扩展管理页面卸载扩展；浏览器会移除该扩展的本地存储数据。

### 6. 联系方式

如对本隐私政策有疑问，可以通过 [HistoryDog-privacy GitHub Issues](https://github.com/xxh7r/HistoryDog-privacy/issues) 联系开发者。请勿在公开 Issue 中提交 API Key、完整浏览历史或其他敏感信息。

---

## English

### 1. Data We Process

To provide browsing-history search, the extension may read or store the following data locally in the user's browser:

- Browsing history: page titles, URLs, visit times, and visit counts.
- User input: natural-language descriptions or keywords entered in the extension's search box.
- Local page metadata index: Title, Meta/OG Description, the first H1, site name, normalized URL, last-seen time, and visit count.
- Extension settings and state: interface language, index preferences, recent searches, current search sessions, and a DeepSeek API key explicitly configured by the user.

The API key is authentication information. It is stored only in the browser's local extension storage and is used solely to authenticate direct DeepSeek API requests when the user enables AI features. The developer does not receive or store the API key.

### 2. Local Page Metadata Index

The local page metadata index is enabled by default to improve retrieval of pages that are difficult to find using history titles and URLs alone. The index is stored in local IndexedDB and retains up to approximately 50,000 records. Older records are removed based on last-visit time when the limit is exceeded.

- Only regular HTTP/HTTPS pages are processed.
- The extension does not store full page body text, cookies, form values, passwords, or URL hashes.
- Enhanced metadata is not indexed on pages where a password input is detected.
- Before storage, URL credentials, common tracking parameters, and sensitive parameters such as token, password, session, and auth are removed. A normalized URL used only for local page identity may retain a limited number of non-sensitive parameters.
- On first installation or upgrade, the extension may import titles and URLs for up to approximately 365 days and 50,000 existing browser-history records. It does not revisit old URLs over the network to fetch page content.
- InPrivate/Incognito tabs are not written to the page metadata index. The background process rejects storage based on the private-tab state supplied by the browser.

Users can disable or clear the local page metadata index at any time in the settings page.

### 3. Optional DeepSeek AI Features

If no DeepSeek API key is configured, the extension does not call an AI service. Browsing-history search remains available through local retrieval and ranking.

After the user configures an API key, each search may make up to two DeepSeek API requests:

1. Query planning: the search description entered by the user.
2. Result ranking: up to 20 candidate records containing title, domain, sanitized pathname, truncated page-metadata summary, relative visit time, and local matching evidence.

The extension does not send full page body text, cookies, form values, passwords, URL query strings, or URL hashes to DeepSeek. Requests are sent directly from the extension to `https://api.deepseek.com/` and do not pass through a developer-operated relay server. Information sent to DeepSeek is processed under DeepSeek's terms and privacy policy.

### 4. Data Sharing, Sale, and Purpose Limitations

- The developer does not sell user data.
- The developer does not use user data for advertising, credit assessment, lending, or purposes unrelated to browsing-history search.
- Except for API requests required when the user explicitly enables DeepSeek features, the extension does not transfer user data to third parties.
- The extension contains no remote analytics, telemetry, or developer-operated remote logging.
- The extension does not download or execute remote code. All executable code is included in the published extension package.

### 5. Retention and User Controls

- Browsing history is managed by the browser. The extension reads it as needed and does not upload it to developer servers.
- Page metadata, settings, recent searches, and search sessions are stored locally on the user's device.
- Users may choose not to configure a DeepSeek API key or may delete it at any time.
- Users can disable or clear the page metadata index and clear recent searches.
- Users can uninstall the extension through the browser's extension-management page; the browser will remove the extension's local storage.

### 6. Contact

For privacy questions, contact the developer through [HistoryDog-privacy GitHub Issues](https://github.com/xxh7r/HistoryDog-privacy/issues). Do not post API keys, complete browsing histories, or other sensitive information in a public issue.
