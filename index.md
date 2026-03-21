# 历史汪隐私说明 / History Wang Privacy Policy

本隐私说明适用于 `历史汪` 浏览器扩展。  
This privacy policy applies to the `History Wang` browser extension.

## 中文

### 我们会处理什么数据

- 用户输入的自然语言查询
- 浏览器本地历史记录的脱敏摘要：
  - 标题
  - 域名
  - 路径 `pathname`
  - 访问时间

### 我们不会发送什么

- Cookie
- 页面正文
- 搜索参数 `query string`
- URL `hash`
- 账户密码或表单输入内容

### 数据流向

- 历史记录检索在本地扩展内完成
- AI 请求由扩展直接发往你在设置中选择的服务商
- 历史汪当前版本不提供自建中转服务，也不做远程日志采集

### 自定义 Provider

- 只有在你保存设置并授权对应域名后，扩展才会请求该自定义接口
- 权限粒度按 `origin` 控制，例如 `https://api.example.com/*`

### 用户可控项

- 你可以随时在设置中修改或删除 API Key
- 你可以切换 Provider，或完全停止使用插件
- 你可以通过浏览器扩展管理页移除扩展及其本地存储数据

---

## English

### What Data We Process

- The natural-language query entered by the user
- Sanitized summaries of local browser history entries, including:
  - Title
  - Domain
  - URL pathname
  - Visit time

### What We Do Not Send

- Cookies
- Full page content
- Query strings
- URL hashes
- Account passwords or form input contents

### Data Flow

- Browser history lookup is performed locally inside the extension
- AI requests are sent directly from the extension to the provider selected by the user in settings
- The current version of History Wang does not use a self-hosted relay service and does not collect remote analytics logs

### Custom Providers

- The extension only calls a custom provider after the user saves the settings and grants access to the corresponding domain
- Permission scope is controlled at the `origin` level, for example: `https://api.example.com/*`

### User Controls

- Users can modify or delete their API key at any time in settings
- Users can switch providers or stop using the extension entirely
- Users can remove the extension and its local storage data through the browser's extension management page
