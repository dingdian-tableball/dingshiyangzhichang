# 丁氏养殖场 - 官方网站

专业肉牛养殖场官方网站，支持百度等搜索引擎收录。

## 项目结构

```
firstLove/
├── index.html      # 主页面
├── styles.css      # 样式文件
├── robots.txt      # 搜索引擎爬虫规则
├── sitemap.xml     # 网站地图
└── README.md       # 本说明文件
```

## 本地预览

用浏览器打开 `index.html` 即可预览，或使用本地服务器：

```bash
# Python 3
python -m http.server 8080

# 然后访问 http://localhost:8080
```

## 部署到线上

1. 购买域名和服务器/虚拟主机
2. 将全部文件上传到网站根目录
3. 确保可通过 `https://你的域名.com` 访问

## 让百度搜索到您的网站

### 第一步：百度站长平台注册与验证

1. 打开 [百度站长平台](https://ziyuan.baidu.com/)
2. 用百度账号登录
3. 点击「用户中心」→「站点管理」→「添加网站」
4. 输入您的网站域名（如 `www.dingshi-ranch.com`）
5. 选择验证方式：
   - **文件验证**：下载验证文件，放到网站根目录
   - **HTML 标签验证**：在 `index.html` 的 `<head>` 中已预留位置，填入验证码：
     ```html
     <meta name="baidu-site-verification" content="您的验证码">
     ```

### 第二步：提交网站资源

验证通过后：

1. 在站长平台点击「普通收录」→「资源提交」
2. 选择「sitemap」方式，提交您的 sitemap 地址，例如：
   ```
   https://你的域名.com/sitemap.xml
   ```
3. 也可使用「API 提交」或「手动提交」录入首页链接

### 第三步：配置 sitemap 和 robots

部署前请修改以下文件中的域名：

- **sitemap.xml**：将 `your-domain.com` 替换为您的实际域名
- **robots.txt**：将 `your-domain.com` 替换为您的实际域名
- **index.html**：将 `your-domain.com`（canonical 和 ld+json 中的 url）替换为您的实际域名

### 第四步：完善联系方式

在 `index.html` 中搜索「请填写」，填入真实联系电话和地址，方便客户联系，也有利于百度对网站可信度的判断。

## 收录时间说明

- 百度收录通常需要 **数天至数周**
- 新站收录相对较慢，建议坚持更新内容、保持服务器稳定
- 可在百度搜索 `site:你的域名.com` 检查是否已被收录

## 其他搜索引擎

- **Google**：可到 [Google Search Console](https://search.google.com/search-console) 提交
- **搜狗、360**：同样提供站长平台，可按类似流程提交

## 技术说明

- 纯静态 HTML/CSS，无需后端，适合各类虚拟主机
- 已做移动端适配
- 已添加 Schema.org 结构化数据，利于搜索引擎理解
