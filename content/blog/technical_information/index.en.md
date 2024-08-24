+++
title = "Technical Details"
date = 2024-08-23
updated = 2024-08-23
description = "ST.U is built using Zola + the tabi theme, and hosted on Cloudflare Pages."

[taxonomies]
tags = ["tech"]

[extra]
quick_navigation_buttons = true
toc = true
+++


[ST.U](https://shantou.University) is powered by [Zola](https://www.getzola.org/) and uses the [tabi](https://github.com/welpo/tabi) theme.

Thanks to Zola and tabi's internationalization support, the site allows you to choose the language (zh-Hans | en) in the top left corner.

> PS:
> The English version of this site is translated with support from ChatGPT. If the Chinese version seems unclear, please refer to the English version.


By running `zola build`, you can generate and export a static site, so any service provider that supports static site hosting can host our site, even GitHub Pages. Cloudflare Pages has built-in support for Zola and makes it easy to manage domain DNS records, which is why ST.U chose Cloudflare Pages.

In the future, if ST.U grows large enough and the demand for static site hosting and deployment exceeds Cloudflare Pages' free tier limit of 500 deployments per month, we can also use Vercel or other service providers that support Zola for hosting.
