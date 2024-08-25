+++
title = "在 ST.U 发布一本书"
date = 2024-08-25
updated = 2024-08-25
description = "使用 mdBook 在 ShanTou.University 发布一本开源的书籍。"

[taxonomies]
tags = ["book", "domain"]

[extra]
quick_navigation_buttons = true
toc = true
+++


在 ST.U ,一切都是公开可访问的，一切也都是开放的。除了创建 [ST.U・ShanTou.University](https://shantou.University) 这样的博客页面外，我们还可以发布（或者不太严格地说“出版”）一本书籍。

目前，有一本名为 [Leptos中文指南](https://leptos.ShanTou.University) 的技术书籍，已经作为示例项目上线。

这本书的所有源代码都托管在 [GitHub](https://github.com/ShanTouUniversity/leptos_cn)。它使用 `mdBook` 这个开源工具生成，并通过 GitHub Action 发布到 GitHub Pages。我们能通过 [leptos.ShanTou.University](https://leptos.ShanTou.University) 访问这本书，是因为 ST.U 添加了一条 CNAME 类型的 DNS 解析记录，把`letpos.ShanTou.University` 指向了 `ShanTouUniversity.github.io`， 然后在对应仓库配置了自定义域名。

在 ST.U 出版一本书，最关键的一个步骤，就是添加那条 CNAME 类型的 DNS 解析记录。如果你需要发布一本书，你应当：
1. 选择一个你熟悉的且合适的工具，mdBook 或者 Zola 或者其他支持生成静态页面的工具；
2. 将你的书籍部署到 Github Pages、Vecel、Netlify、Cloudflare Pages等之类的服务商；
3. 记录下你的书籍的地址，比如 `ShanTouUniversity.github.io/leptos_cn`;
4. 用你的校友邮箱，把你想要的二级域名和上述地址发送给 [`dev@ShanTou.University`](mailto:dev@ShanTou.University)；
5. 收到回复后，便可以在你自己的后台操作，操作成功后就可以在 `xxx.ShanTou.University` 访问你的书籍了。
   
如果你对上述所言不知所以，你也可以将你的书稿发送给 [`dev@ShanTou.University`](mailto:dev@ShanTou.University)， ST.U 会使用 mdBook 制作成书籍后公开在 ST.U 的 GitHub 组织， 并分配一个适合的域名；然后你会收到邮件回复。如果你需要修订你的书籍，可以直接 Clone 那个仓库然后提PR，或者直接在对应仓库提 issue（最简单）。

