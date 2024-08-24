+++
title = "技术细节"
date = 2024-08-23
updated = 2024-08-23
description = "ST.U 的是由 Zola + tabi 主题构建，然后托管在 Cloudfalre Pages 上的。"

[taxonomies]
tags = ["tech"]

[extra]
quick_navigation_buttons = true
toc = true
+++


[ST.U](https://shantou.University)是由[Zola](https://www.getzola.org/)驱动的，使用的主题是 [tabi](https://github.com/welpo/tabi)。

得益于 Zola 和 tabi 的国际化支持，本站支持在左上角选择语言（ zh-Hans | en）。

> PS: 
> 本站的英文版本由 ChatGPT 提供翻译支持，如果中文版本的语句不通顺，请参阅英文版本。

通过 `zola build` 可以构建导出一个静态页面，因此，支持托管静态页面的服务商都可以存放我们的站点；甚至是 Github Page 都行。Cloudflare Pages 内建了对 Zola 的支持，而且便于管理域名的 DNS 解析记录，所以 ST.U 选择了 Cloudflare Pages。 

未来，如果 ST.U 发展得足够壮大，对静态页面的托管和部署需求量超过了 Cloudflare Pages 每月 500 次的部署限制（免费版），也可以用 Vecel 或其他支持 Zola 的服务商托管。