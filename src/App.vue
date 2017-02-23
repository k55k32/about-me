<template lang="pug">
div
  .header
    .container.header-container
      .left
        h1.light-font 周超-前端工程师简历
        .title-mark 生活和代码一样，都是对艺术的极致追求与探索
      .qr-code-container
        .qr-desc
          p 您还可以使用手机或iPad
          p 扫描左侧二维码打开本页
        .qr-code
          img(src="./assets/qrcode.png")
  .content
    row
      div(slot="left")
        .title 个人信息
        field(name="姓名" value="周 超")
        field(name="电话" value="13795462311")
        field.mini-font(name="学历" value="华中师范大学 · 计算机网络工程 · 大专")
        field(name="邮箱")
          .mark
            d-link(href="mailto://diamondfsd@gmail.com" name="diamondfsd@gmail.com")
        field(name="个人博客")
          .mark
            d-link(href="https://diamondfsd.com")
      div(slot="right")
        .title 工作经历
        experience(time="2016 ~ 2017" title="知学云科技" mark="前端工程师 / 研发工程师")
          p 公司移动版前端整体架构，移动版开发，包括
          ul
            li 使用 vue + webpack + eslint 实现前端工程化开发，自动代码检查，构建打包等
            li 使用 nodejs 实现中间代理层，方便本地调试，以及复杂业务逻辑处理
            li 为项目组提供前端开发相关文档
          p 此外，还负责公司新版本产品前后端研发，以及前端相关的一些技术支持
        experience(time="2015 ~ 2016" title="餐加企业咨询管理" mark="Team Loader")
          p 前期负责公司项目初期基础框架搭建，以及产品开发相关工作，包括:
          ul
            li 前端整体框架搭建，前端基础库的封装，以及UI组件编写
            li Hybird APP 内嵌页面开发
            li 后端微服务框架搭建，实现基础代码生成器，方便团队实现基础功能
            li 产品数据库设计(mysql)，表设计
          p 后期主要是管理团队，团队成员的一些培训，开发过程中提供前后端的技术支持。
        experience(time="2013 ~ 2015" title="中衡生物科技" mark="软件工程师")
          p 给公司各级服务商提供微信官网定制开发（定制模块，UI效果）。
          p 以及公司内部的一些管理系统的java方面开发
    row.no-line
      div(slot="left")
        .title 社交网络
        d-link(icon="G" href="https://github.com/k55k32")
        d-link(icon="Z" href="https://zhuanlan.zhihu.com/diamondfsd")
        d-link(icon="S" href="https://segmentfault.com/u/k55k32")
      div(slot="right")
        .title 项目经验
        experience(title="移动在线学习平台")
          tags(slot="tags", :tags="['Vue', 'node.js']")
          p 纯前端项目，使用 vue + vuex + vue-router，
            | 基于公司现有产品，完成的独立移动版。兼容各APP内置的WebView（微信，钉钉，QQ等）
          p 实现了PDF文档阅读，在线音视频查看，实现了学习记录上传同步等功能
          p 音频播放的过程中曾遇到部分浏览器请求时不发送 referer 头，导致防盗链机制生效，无法播放。
            | 最后写了个 node.js 代理，来完成音频播放，以及一些复杂api的中转处理。
          p 快速稳定的开发完该产品，让公司在新一轮的竞标中，以极大的优势，赢得了对手。
        experience(title="你画我猜多人在线游戏")
          tags(slot="tags", :tags="['Vue', 'WebSocket', 'Node.js']")
          p 实现了多人在线玩你画我猜，实时聊天功能。
          p 使用 WebSocket 发送实时发送指令，前端对应产生效果。
          p 封装了 WebSocket 客户端组件，封装了 canvas 的一些基本操作，转化为可逆转的指令进行发送。
          p 项目及源码开放后，获得社区用户大量好评，并且给社区人民带来了无尽的欢乐与喜悦:)。
          .link-group
            d-link(icon="-" href="https://zhuanlan.zhihu.com/p/25358509" name="知乎文章")
            d-link(icon="-" href="http://yd.diamondfsd.com" name="在线地址(移动端打开最佳)")
            d-link(icon="-" href="https://github.com/k55k32/cms-admin-front" name="项目源码")
        experience(title="个人博客")
          tags(slot="tags", :tags="['Node.js', 'Express', 'Nuxt.js(Vue SSR框架)', 'SSR', 'Webpack']")
          p 博客系统需要支持搜索引擎爬取，所以采用 nodejs + express + nuxt.js搭建博客前端渲染层。
          p 使用了 媒体查询，CSS图标 等技术，适配 PC/移动端，浏览体验良好。
          p 使用 Webpack 进行构建，代码使用 eslint 进行预检查，规范了开发期间的语法，避免未知的错误。
          p 顺带还开发了个 nodejs 写的针对于 github-webhooks 的服务，用于实现自动化发布。
          .link-group
            d-link(icon="-" href="https://diamondfsd.com" name="在线地址")
            d-link(icon="-" href="https://github.com/k55k32/cms-admin-front" name="项目源码")
        experience(title="微信点餐系统")
          tags(slot="tags", :tags="['Vue', 'SPA', '微信JS-SDK', '微信支付']")
          p 使用 Vue 进行组件化开发，所有页面封装为自定义组件，易扩展。并且根据场景，实现了基本的路由功能。
          p 使用了微信的登录服务，用户免注册即使用。可以在线进行点餐，支付。
          p 首屏性能良好，对各种新老机型内置浏览器做了适配以及个别屏幕大小调优。实现图片延迟加载，异步加载组件等
            | 优化性能。
          p 项目初期的快速稳定上线，帮助公司在极短的时间内拉拢到一批忠实用户，并且现在稳健发展中。
        experience(title="内部 OA 系统重构")
          tags(slot="tags", :tags="['Ajax', 'Bootstrap']")
          p 将公司内部使用的 OA 系统进行了一次重构。
          p 将公司原有的 链接 + jsp 的模式，改为了单页面 Ajax 进行异步加载页面。
          p 避免反复转跳浪费资源，并且将前端框架替换为Bootstrap。
          p 封装了一些基础组件表单，表格，弹窗，全局提示框等，方便业务人员开发。通过这次重构，
            | 极大的优化了前端的性能
            | 和用户体验。并且对开发人员更加的友好，易于开发。
        experience(title="微信打印服务")
          .tags(slot="tags")
            i(v-for="tag in ['微信SDK', 'WebSocket', 'Javascript']") {{tag}}
          p 实现了向微信公众号发送消息，服务端接受，并通过WebSocket转发到对应的PC端。
          p PC端进行快递单打印功能，基于js打印插件Lodop来完成。
          p PC端使用WebSocket接受打印消息，并进行队列打印。实现了实时应答，实时打印，快速的返回结果。帮助供货商更好的处理订单。
        experience(title="微官网定制开发")
          .tags(slot="tags")
            i(v-for="tag in ['Javascript', 'HTML5', 'CSS3']") {{tag}}
          p 给公司各级服务商提供微官网定制开发，前端使用 zepto.js + HTML + CSS 完成的页面以及交互效果。
          p 并且对多种机型的移动端做了专门的适配，优化用户体验。微官网用于展示企业基本信息，和一些新闻动态。
          p 原来的公众号就有很多内容，所以用Java写了个爬虫抓取原来的文章，放到微官网数据库。实现了官网内容的快速填充，
            | 有效的支持了营销及外宣活动。
    row.single
      div(slot="left")
        .title 自我总结
        .myself.light-font
          p 熟练掌握 HTML5/CSS3/Javascript [ES5/ES6/ES7] 等前端语言
          p 熟练掌握前端主流框架，对前端工程化，SPA 应用开发，ES6/ES7 开发，有着丰富的实战经验
          p 善于学习思考，并对新技术有用于探索的能力（不前进，就淘汰）
          p 有良好的团队管理能力，能够快速培养新人，普及新技术
          p 良好的编码规范，习惯写文档而不是写注释
          p 丰富的架构经验，我的目标是让每个团队成员写出简单，易懂的代码。用更少的代码，完成更复杂的需求
          p 开源社区活跃，自己有写一些小项目。也比较积极的参与开源项目贡献和讨论
          d-link.mobile-only(icon="画" href="http://yd.diamondfsd.com"
          name="移动版彩蛋，你画我猜在线地址，点开玩玩吧")
  footer.container
    d-link(href="http://about.diamondfsd.com" name="本简历线上地址为: http://about.diamondfsd.com")
    d-link(href="https://github.com/k55k32/about-me" name="本简历源码: https://github.com/k55k32/about-me")
</template>

<script>
import Row from './components/Row'
import Field from './components/Field'
import DLink from './components/DLink'
import Tags from './components/Tags'
import Experience from './components/Experience'
export default {
  name: 'app',
  components: {
    Row, Field, Experience, DLink, Tags
  }
}
</script>

<style lang="less">
@import "./assets/base.less";
</style>
