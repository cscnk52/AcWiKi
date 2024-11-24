# 网络空间安全————浏览网站安全

---
## https:// 与 http://

### 什么是 HTTPS？

- HTTPS 是一种在 Web 服务器和 Web 浏览器之间发送数据的安全方式。

超文本传输协议安全 (HTTPS) 是 HTTP 的安全版本，HTTP 是用于在 Web 浏览器和网站之间发送数据的主要协议。HTTPS 经过加密，以提高数据传输的安全性。当用户传输敏感数据（例如通过登录银行账户、电子邮件服务或健康保险提供商）时，这一点尤其重要。
任何网站都应使用 HTTPS，尤其是那些需要登录凭据的网站。在现代 Web 浏览器（例如 Chrome）中，未使用 HTTPS 的网站与使用 HTTPS 的网站的标记有所不同。URL 栏中如出现挂锁，则表示该网页是安全的。Web 浏览器非常重视 HTTPS；[Google Chrome 和其他浏览器将所有非 HTTPS 网站标记为不安全。](https://www.cloudflare.com/learning/ssl/why-use-https/) </br>
![image](https://github.com/user-attachments/assets/7903824d-137b-4ceb-80d0-81325bbf5877)


### HTTPS 为什么很重要？如果网站没有 HTTPS，那会如何？

HTTPS 阻止网站以任何在网络上窥探的人都能轻松查看的方式广播信息。通过常规 HTTP 发送信息时，信息会分解为数据包，使用免费软件即可轻松“嗅探”这些数据包。这使得通过不安全的媒介（例如公共 Wi-Fi）进行的通信极易受到拦截。实际上，所有通过 HTTP 进行的通信都是以纯文本形式进行的，因而能够为任何使用正确工具的人轻松访问，而且容易遭受在途攻击。

使用 HTTPS 时，流量会经过加密，即使嗅探到数据包或以其他方式截取数据包，它们也会呈现为无意义的字符。我们来看一个例子：

> - 加密前：</br>

` 这是完全可读的文本字符串 `

> - 加密后：</br>

` ITM0IRyiEhVpa6VnKyExMiEgNveroyWBPlgGyfkflYjDaaFf/Kn3bo3OfghBPDWo6AfSHlNtL8N7ITEwIXc1gU5X73xMsJormzzXlwOyrCs+9XCPk63Y+z0= `

### HTTP 为什么不安全

- HTTP 由于是明文传输，主要存在三大风险

|     |         |
|:---:|:---:|
|1、 窃听风险 <br> 中间人可以获取到通信内容，由于内容是明文，所以获取明文后有安全风险 | ![image](https://github.com/user-attachments/assets/90d82d50-8d3c-4c7d-9f9b-e8b55ce89fb7) |
|2、 篡改风险 <br> 中间人可以篡改报文内容后再发送给对方，风险极大 |  ![image](https://github.com/user-attachments/assets/3ba95012-58be-4132-b9bd-31cda09bed3f) |
|3、 冒充风险 <br> 比如你以为是在和某宝通信，但实际上是在和一个钓鱼网站通信。 |   ![image](https://github.com/user-attachments/assets/1807e749-aa5d-4c5c-a21e-f1b342ef8a02) |

### 总结

增强安全性：HTTPS通过SSL/TLS协议对数据进行加密，保护用户数据不被窃取或篡改，确保通信的安全性。

提升信任度：使用HTTPS的网站更受用户信赖，因为它表明网站采取了额外的安全措施来保护用户隐私和数据。

浏览器支持：现代浏览器如Chrome将HTTP网站标记为“不安全”，而HTTPS网站则不会，这影响了用户对网站安全性的感知。

搜索引擎优化：搜索引擎倾向于提升使用HTTPS的网站的搜索排名，因为它们被认为是更安全、更可靠的资源。

---
## 常见域名


## 域名（Domain Name）

是互联网上用来识别和访问网站的一个易于记忆的地址。它将IP地址（一串数字）转换为人类可读的格式，比如 www.example.com。域名系统（DNS）负责将域名解析为对应的IP地址，以便用户的设备能够找到并访问相应的服务器。
顶级域名（Top-Level Domain, TLD）：  </br>

![image](https://github.com/user-attachments/assets/29a37ddd-379c-452d-98c4-1e7b43bce374)

---
### 子域名（Subdomain）：

位于域名的最左侧部分，可以自定义。例如，在subdomain.example.com中，subdomain就是子域名。
二级域名（Second-Level Domain, SLD）：

紧随子域名之后，通常是注册时选择的主要域名部分。例如，在example.com中，example是二级域名。
顶级域名（Top-Level Domain, TLD）：

位于域名的最右侧部分，分为两类：
通用顶级域名（Generic Top-Level Domains, gTLDs）：如.com、.org、.net等。
国家代码顶级域名（Country Code Top-Level Domains, ccTLDs）：如.cn（中国）、.us（美国）、.uk（英国）等。
根域名（Root Domain）：

根域名是域名层次结构的最顶层，用.表示，但不在域名中显示。例如，example.com.实际上是example.com。

一个完整的域名示例是`www.example.com` ，其结构如下：

> - www：子域名
> - example：二级域名
> - com：顶级域名

---

1. **域名的合法性**：
   - 域名的合法性涉及到域名是否按照ICANN（互联网名称与数字地址分配机构）的规定进行注册和使用，以及是否遵守了相关的法律法规。
   - 合法的域名不会侵犯他人的商标权、版权或其他知识产权。
   - 合法性还意味着域名的注册和使用没有违反任何国家或地区的法律，例如，没有用于非法活动或欺诈行为。

2. **域名的完整性**：
   - 完整性指的是域名是否完整且正确，没有拼写错误或遗漏的部分。
   - 一个完整的域名应该包括所有的子域名和顶级域名（TLD），例如 `www.example.com`。
   - 完整性还涉及到域名是否正确地指向了预期的服务器或网站，没有被错误地重定向到其他网站。

3. **顶级域名（TLD）**：
   - 顶级域名是域名结构中的最后一部分，如 `.com`、`.org`、`.net` 等。
   - TLD 分为几种类型，包括通用顶级域名（gTLDs）如 `.com`、`.net`，以及国家代码顶级域名（ccTLDs）如 `.uk`、`.de`。
   - TLD 可以提供关于网站性质和目的的信息，例如 `.gov` 通常用于政府网站，`.edu` 用于教育机构。

4. **子域名**：
   - 子域名是主域名的一个分支，用于指向同一主域名下的不同部分或服务。
   - 例如，在 `mail.example.com` 中，`mail` 是一个子域名，用于指向该域的邮件服务。
   - 子域名的使用可以帮助组织网站内容，但也可能导致安全问题，如子域名劫持。

5. **国别域名**：
   - 国别域名是特定国家的顶级域名，如 `.uk`（英国）、`.de`（德国）等。
   - 这些域名通常用于标识网站的地理位置和目标受众，有助于用户识别与自己地区相关的网站。
   - 国别域名也可以用于表示网站内容的语言或文化背景。

6. **混合域名**：
   - 混合域名是指那些故意将字母和数字混合使用的域名，以模仿知名品牌或网站。
   - 例如，将知名品牌的域名中的某个字母替换为相似的数字（如将 "e" 替换为 "3"），以欺骗用户。
   - 这种域名通常用于钓鱼攻击，目的是诱使用户输入敏感信息，如用户名和密码。

## 总结

**需注意以下几点：1. 核实域名的合法性和完整性，避免拼写错误或遗漏。2. 识别顶级域名（TLD），区分通用和国别域名。3. 警惕子域名和混合域名，防范钓鱼网站。4. 使用HTTPS协议，确保数据传输安全。5. 检查域名WHOIS信息，确认注册人和注册日期。6. 使用安全工具检测域名声誉，避免访问有不良记录的网站。简而言之，用户应保持警惕，仔细检查域名，以确保网络安全。**


## 参考文章

https://cloud.tencent.com/developer/article/1758154

https://www.cloudflare.com/zh-cn/learning/ssl/what-is-https/







 