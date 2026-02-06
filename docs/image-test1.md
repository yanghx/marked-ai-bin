# TinyPro v1.2.0 正式发布，趁着 TinyPro 项目刚创建不久，快来参与贡献（蹭 PR）吧！

[](https://juejin.cn/user/1504599026445150/posts)

2025-04-141,019阅读6分钟

关注

你好，我是 Kagol，个人公众号：`前端开源星球`。

[TinyPro](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro) 是一个基于 [TinyVue](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-vue) 打造的前后端分离的后台管理系统，支持在线配置菜单、路由、国际化，支持页签模式、多级菜单，支持丰富的模板类型，支持多种构建工具，功能强大、开箱即用。

- 源码：[github.com/opentiny/ti…](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro)（欢迎 Star ⭐）[[技术架构文档：结构化 Markdown 编辑器 (V2.0 - JSON Native)]]123
- 官网：[opentiny.design/vue-pro](https://link.juejin.cn/?target=https%3A%2F%2Fopentiny.design%2Fvue-pro)


我们非常高兴地宣布，2025年4月10日，[TinyPro](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro) 发布了 [v1.2.0](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Freleases%2Ftag%2Fv1.2.0) 🎉。

本次 1.2.0 版本主要有以下重大变更：

- 列表页面增加综合搜索，只需要一个输入框，解决所有数据筛选问题
- 增加更丰富的单元测试，目前后端服务的单测覆盖率 85% 左右
- 升级 Vite(`^6.1.0`) / Vue(`^3.5.10`) / TinyVue(`^3.21.0`) 等依赖到最新版本，并优化部分样式问题
- 移除 Mock，将 Mock 数据迁移到后端（因为有后端，所以不需要 Mock 服务了）


详细的 Release Notes 请参考：[github.com/opentiny/ti…](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Freleases%2Ftag%2Fv1.2.0)

本次版本共有3位贡献者参与开发，其中 [discreted66](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fdiscreted66) 是新朋友👏

- [discreted66](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fdiscreted66) - 新增贡献者✨
- [GaoNeng-wWw](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2FGaoNeng-wWw)
- [kagol](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fkagol)


感谢新老朋友们对 TinyPro 的辛苦付出！

你可以更新 `@opentiny/tiny-toolkit-pro@1.2.0` 进行体验！

```
tiny install @opentiny/tiny-toolkit-pro@1.2.0
```

TinyPro 效果图：

![](./assets/img_3fef5420.webp)

## 1 列表增加综合搜索

之前的列表搜索比较传统，每个筛选项是一个单独的组件，比如按姓名搜索是一个输入框，按角色搜索是一个下拉框，按日期搜索是一个日期选择框等。

这样会有一个问题：一旦过滤字段增多，会不断地占用主体内容的空间，直到屏幕显示的全是过滤条件，没有主体内容，虽然右上角增加了一个展开收起的功能，但也是治标不治本。

所以我们开发了一个 SearchBox 综合搜索组件，只需要一个输入框，就能把所有的过滤条件全部收拢在内，大大提升了用户体验！

以下是新旧过滤器的效果对比：

![](./assets/img_bae4f840.webp)

## 2 更丰富的单元测试

为了尽可能保障质量，给自己多一点安全感，我们给 NestJS 后端服务增加了大量单元测试，目前一共有97个单元测试（欢迎大家一起参与共建，我们的单元测试基于 Jest）。

执行以下命令即可执行单元测试：

```
cd template/nestJs
pnpm test
```

![](./assets/img_208a1e41.webp)

我们非常欢迎你一起参与 TinyPro 项目共建，通过参与 TinyPro 项目共建，你

- 不仅可以了解一个后台管理模板的前后端原理，学习 Vite、Vue、TypeScript、NestJS、Jest 等流行的技术
- 而且可以结识一批技术大牛，一起学习和交流前端技术
- 还有机会获得 OpenTiny 社区的定制礼品


另外由于 TinyPro 项目刚创建不久（之前是作为 TinyCLI 项目的一个目录，现在作为独立的仓库，可见官方也是非常重视这个项目的），还有很多值得完善的地方，大家也可以多多探索，欢迎提出你的优化想法，且在 TinyPro 项目中落地。

可以在 discussion 中参与讨论：

[github.com/opentiny/ti…](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Fdiscussions)

## 3 如何参与贡献

之前给大家介绍了 TinyPro 项目的初始化、本地启动和二次开发等内容。

[TinyPro 后台管理系统从启动到使用，再到二次开发，看这一篇就够了！](https://juejin.cn/post/7489638329052430355)

接下来给大家介绍如何参与 TinyPro 项目的贡献。

### 3.1 Fork 和克隆代码

- 打开 [TinyPro](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro) 项目，点击右上角的“Fork”按钮，将仓库复制到你的 GitHub 账户下
- 使用以下命令将 Fork 后的仓库克隆到本地：`git clone https://github.com/yourname/tiny-pro.git`


### 3.2 安装依赖和本地启动

- 进入克隆后的仓库目录：`cd tiny-pro`


本地 TinyPro 目录如下：

```
- template
  - nestJs    # 后端服务
  - tinyvue   # 前端服务
```

#### 启动后端

```
cd template/nestJs

pnpm i
```

将 `.env.example` 改成 `.env`，然后执行以下命令即可：

```
pnpm start
```

出现以下界面，说明后端启动成功：

![](./assets/img_d8378636.webp)

#### 启动前端

启动前端和启动后端差不多。

```
cd template/tinyvue

pnpm i

pnpm start
```

出现以下界面，说明前端启动成功：

![](./assets/img_fa3582f1.webp)

访问链接：[http://localhost:3031/](https://link.juejin.cn/?target=http%3A%2F%2Flocalhost%3A3031%2F)，即可查看效果。

详细的前后端启动步骤可以参考之前的文章：[TinyPro 后台管理系统从启动到使用，再到二次开发，看这一篇就够了！](https://juejin.cn/post/7489638329052430355#heading-2)

或者看之前的演示视频（从 08:00 开始）：[TinyPro使用指南：手把手带你本地启动 TinyPro 前后端](https://link.juejin.cn/?target=https%3A%2F%2Fwww.bilibili.com%2Fvideo%2FBV1PuZBYeEGb%2F)

### 3.3 创建分支和提交代码

- 为你的修改创建一个新分支，避免直接在主分支上操作：`git checkout -b 你的分支名称`
- 在本地仓库中进行代码修改，确保遵循项目的代码风格和规范，避免格式化问题。
- 添加修改的文件到暂存区：`git add .`
- 提交修改，编写清晰的提交信息：`git commit -m "你的提交信息"`
- 将本地分支推送到你的 Fork 仓库：`git push origin 你的分支名称`


### 3.4 创建 Pull Request(PR)

- 在 GitHub 上，进入你的 Fork 仓库页面，点击"Compare & pull request"按钮，选择目标仓库的主分支 dev。
- 填写 PR 的标题和描述，说明你的修改内容和目的。
- 提交 PR，等待维护者审核。
- 如果维护者提了检视意见，需要及时修复和回复，并重新 commit && push


### 3.5 提交 Issue 和讨论

- 如果你发现项目中的问题，可以在 GitHub 上创建 [Issue](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Fissues)，描述问题并提供复现步骤
- 如果你有解决方案，可以在 Issue 中提出建议，或直接通过 [PR](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Fpulls) 修复问题
- 如果你有好的想法和点子，欢迎在 [Discussion](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Fdiscussions) 中创建讨论


## 4 领取任务

你可以在 Issue 列表中找到自己感兴趣的任务，回复“领取任务”：

[github.com/opentiny/ti…](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Fissues)

或者你在使用过程中，发现了问题，有了好点子，都可以参与贡献。

如果你对以下任务感兴趣，也欢迎进行认领：

- [建议默认支持原子化 CSS：UnoCSS](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-cli%2Fissues%2F219)
- [使用 umzug 管理数据库的 migration 和 seeds](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-cli%2Fissues%2F234)
- [增加参数化初始化](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-cli%2Fissues%2F228)
- [页面配置可是本地生效](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-cli%2Fissues%2F220)
- [使用 TinyCharts Vue 替代现有的 echarts 图表](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Fissues%2F21)
- [使用 @opentiny/icons 图标替换现有的图标，并在创建菜单时显示图标预览效果](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro%2Fissues%2F19)
- 从 [TinyPro 优化建议](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-cli%2Fissues%2F233) 中选择部分任务
- 给前端和后端补充单元测试用例


欢迎添加小助手微信：opentiny-official（回复：TinyPro），一起交流！

## 往期文章

- [TinyPro 后台管理系统从启动到使用，再到二次开发，看这一篇就够了！](https://juejin.cn/post/7489638329052430355)
- [OpenTiny 开源社区招募贡献者啦！](https://juejin.cn/post/7485572202701799464)
- [TinyPro Vue v1.1.0 正式发布：增加细粒度权限管理、页签模式、多级菜单，支持 Webpack/Vite/Rspack/Farm 多种构建工具](https://juejin.cn/post/7441231659394433039)
- [优化永不止步：TinyVue v3.20.0 正式发布，更美观的官网UI，更友好的文档搜索，更强大的主题配置能力](https://juejin.cn/post/7445930510021656613)
- [TinyEditor v3.25.0 正式发布！2025年第一个版本，增加标题列表导航、分隔线、多图多文件上传等实用特性](https://juejin.cn/post/7455243039655067657)


## 联系我们

GitHub：[github.com/opentiny/ti…](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fopentiny%2Ftiny-pro)（欢迎 Star ⭐）

官网：[opentiny.design/vue-pro](https://link.juejin.cn/?target=https%3A%2F%2Fopentiny.design%2Fvue-pro)

个人博客：[kagol.github.io/blogs](https://link.juejin.cn/?target=https%3A%2F%2Fkagol.github.io%2Fblogs)

小助手微信：opentiny-official

公众号：OpenTiny