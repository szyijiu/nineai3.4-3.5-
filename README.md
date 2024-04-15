# nineai3.4-3.5魔改版

nineAI 魔改版：基于 NineAI 二开的可商业化 AI Web 应用（免授权，无后门，支持快速部署）

## 页面预览

<img width="1229" alt="image" src="https://gya.wpzllq.cn/GitHub3.4/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20240415130344.png">

<img width="1229" alt="image" src="https://gya.wpzllq.cn/GitHub3.4/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20240415130357.png">

<img width="1229" alt="image" src="https://gya.wpzllq.cn/GitHub3.4/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20240415130413.png">

<img width="1229" alt="image" src="https://gya.wpzllq.cn/GitHub3.4/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20240415130419.png">

<img width="1229" alt="image" src="https://gya.wpzllq.cn/GitHub3.4/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20240415130425.png">

<img width="1229" alt="image" src="https://gya.wpzllq.cn/GitHub3.4/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20240415130435.png">

<img width="1229" alt="image" src="https://gya.wpzllq.cn/GitHub3.4/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20240415131045.png">

## 更新日志

### v3.4.1

NineAi 程序已支持ChatGPT3.5/4.0题、ai绘画、中途绘画（完全自定义参数调整）、中途图片绘图、Dall-E2绘画、思维导图生成、知识库（可定制培训） ）、AI画坊，邀请函+代理分发模式、用户每日签到功能、会话记录保存、访客体验模式、微信公众号+邮箱+手机号注册登录等功能。

NineAi 程序安装还是比较复杂的。建议使用比较干净的主机来安装，或者重装系统。如果使用旧主机，会出现很多问题。两种方法如下。如果不行，可以重新安装系统+环境。安装的话一般不会有什么问题。整套体验下来，最大的优点应该是支持Midjourney绘图界面。大多数人选择使用它就是因为这个功能。

### v3.3.1

1. 新增支持GPT-4-Turbo-Vision插件
2. 新增已支持GPT-4图片对话能力（上传图片并识图理解对话）可同时支持5张图同时上传对话
3. OpenAI DALL-E3文生图对话形式及图片大小占比优化，效果与OpenAI PLUS一致
4. 优化合并DALL-E3和GPT-4-Turbo-Vision的计费方式为GPT-4-Turbo，只需配置gpt-4-1106-Preview模型即可
5. 新增MJ绘画系统并发执行数量设置，可后台设置系统并发数量
6. 新增阿里云OSS存储可配置自定义域名，实现用户可以直接预览图片
7. 新增大模型Agent代理多插件调用处理任务并总结返回结果
8. 修复GPT联网提问失效和不稳定问题（后期将开发新的联网功能，可控制联网模块）
9. 优化MJ单次绘画查询的超时时间为4分钟，应对MJ官方慢速绘画太慢可能导致绘画失败的问题
10. 修复绘画存储不走绘画池Discord-CND代理，导致部分时候存储失败问题
11. 新增DALL-E3文生图连续对话可对同一张图提出修改意见，DALL-E3文生图插件的调用时机由大模型理解用户提问动态择机调用。与OpenAI同步，支持gpt-4、gpt-4-1106-preview、gpt-4-0613、gpt-3.5-turbo、gpt-3.5-turbo-1106、gpt-3.5-turbo-0613模型调用。


## 环境准备

1. **安装 Node.js 环境**

   - 请根据您的操作系统下载并安装 Node.js。
   - 可以从[Node.js 官网](https://nodejs.org/)下载。

2. **安装 PM2**

   - 使用 npm 安装 PM2：`npm install pm2 -g`
   - PM2 是一个带有负载均衡功能的 Node 应用的进程管理器。

3. **安装 PNPM**
   - 使用 npm 安装 PNPM：`npm install -g pnpm`
   - PNPM 是一个快速、节省磁盘空间的包管理工具。

## 配置项目

1. **配置环境变量**

   - 复制`.env.example`文件为`.env`。
   - 根据需要修改`.env`文件中的配置项。

2. **安装项目依赖**
   - 运行命令：`pnpm install`(若安装失败可尝试使用国内源)
   - 这将根据`package.json`文件安装所有必需的依赖。

## 启动项目

1. **启动服务**

   - 使用命令：`pnpm start`
   - 这将启动项目，并默认在 9520 端口监听。

2. **访问项目**
   - 在浏览器中访问`http://localhost:9520`，或者如果配置了 nginx 反向代理，则通过配置的域名访问。

## 管理平台

- **管理端地址**：`/admin`
- **普通管理员账号**：`admin`
- **超级管理员账号**：`super`
- **密码**：`123456`
- 
## 体验地址
https://a.wpzllq.top

## 项目升级

1. **拉取更新**

   - 拉取新的整合包：`git pull`

2. **删除旧进程**

   - 删除旧的 PM2 进程。

3. **安装依赖**

   - 运行命令：`pnpm install` 以安装 `package.json` 中定义的必需依赖。

4. **启动服务**
   - 使用命令：`pnpm start` 来启动项目，它将默认在 9520 端口监听。

