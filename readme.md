# Lounge Mail📧 使用指南

Lounge Mail Viewer 是一款在线临时邮箱工具，可以让你方便地查看临时邮箱收到的邮件。你可以通过网页界面或 API 两种方式进行查询。

## 🌐 网页使用方式

### 🚀 如何访问

[点击这里](https://www.loungemail.eu.org/) 🔗

### ✨ 基本功能

- **🔍 直接查询**：输入邮箱前缀，即可查看最新的三封邮件。
- **🎲 随机邮箱**：一键生成随机邮箱前缀并进行查询。
- **⏱️ 实时显示**：邮件内容包含发件人、主题、日期等详细信息。

### ⚙️ 使用步骤

1. 在左侧输入框中输入邮箱前缀 (例如: `abc`，将查询 `abc@loungemail.eu.org`)。
2. 点击 "查询" 按钮或直接按回车键。
3. 在右侧查看邮件内容。
4.  也可以点击 "随机" 按钮生成随机邮箱进行查询。

## 💻 API 使用方式

### 🛠️ 基本请求

```http
GET /api/{email_prefix}?pass={get-by-connect-me}
```

-   `{email_prefix}`:  要查询的邮箱前缀。
-   `pass`:  验证参数，请联系 me@supage.eu.org 获取。🔑

### 📦 响应格式

```json
[
  {
    "from": "sender@example.com",
    "subject": "邮件主题",
    "date": "Wed, 20 Mar 2024 10:00:00 +0800",
    "content": "邮件内容"
  }
]
```

### 📜 示例

查询 `abc@loungemail.eu.org` 的邮件：
```bash
curl "https://loungemail.eu.org/api/abc?pass={get-by-connect-me}"
```

### ⚠️ 错误响应

-   密码错误：`{"error": "Invalid password"}` ⛔
-   未找到邮件：`[]` 📭
-   其他错误：`{"error": "错误信息"}` ❗

## 📝 注意事项

-   本工具仅支持查询 `loungemail.eu.org` 域名下的邮件。
-   每次查询最多返回最新的 3 封邮件。
-   请勿用于非法用途。🚫
-   API 请求需要包含正确的 `pass` 参数。

## ❓ 常见问题

**Q: 为什么查询不到邮件？**

-   请确保输入的邮箱前缀正确。✅
-   请确认该邮箱是否已收到邮件。📧
-   请检查你的网络连接是否正常。📶

**Q: API 请求返回错误？**

-   请检查 `pass` 参数是否正确。🔑
-   请确认请求格式是否符合要求。⚙️
-   请仔细查看错误信息以获取具体原因。❗

## 📧 联系方式

如有任何问题，欢迎通过以下方式联系：

me@supage.eu.org ✉️
