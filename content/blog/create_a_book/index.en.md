+++
title = "Publishing a Book at ST.U"
date = 2024-08-25
updated = 2024-08-25
description = "Publishing an open-source book at ShanTou.University using mdBook."

[taxonomies]
tags = ["book", "domain"]

[extra]
quick_navigation_buttons = true
toc = true
+++


At ST.U, everything is publicly accessible, and everything is open. Besides creating a blog page like [ST.U・ShanTou.University](https://shantou.University), we can also publish (or, less formally, "release") a book.

Currently, a technical book called [Leptos Chinese Guide](https://leptos.ShanTou.University) has been launched as a sample project.

All the source code for this book is hosted on [GitHub](https://github.com/ShanTouUniversity/leptos_cn). It is generated using the open-source tool `mdBook` and published via GitHub Actions to GitHub Pages. We can access this book through [leptos.ShanTou.University](https://leptos.ShanTou.University) because ST.U added a CNAME DNS record, pointing `letpos.ShanTou.University` to `ShanTouUniversity.github.io`, and configured a custom domain in the corresponding repository.

The most crucial step in publishing a book at ST.U is adding that CNAME DNS record. If you need to publish a book, you should:
   1. Choose a tool you are familiar with, such as mdBook, Zola, or another static page generator;
   2. Deploy your book to a service like GitHub Pages, Vercel, Netlify, or Cloudflare Pages;
   3. Record your book's address, such as `ShanTouUniversity.github.io/leptos_cn`;
   4. Use your alumni email to send the desired subdomain and the above address to [`dev@ShanTou.University`](mailto:dev@ShanTou.University);
   5. After receiving a reply, you can configure the backend, and once successful, your book will be accessible at `xxx.ShanTou.University`.

If the above steps are unclear, you can also send your manuscript to [`dev@ShanTou.University`](mailto:dev@ShanTou.University), and ST.U will use mdBook to create and publish the book on ST.U's GitHub organization, assigning it a suitable domain. You will then receive an email reply. If you need to revise your book, you can directly clone the repository and submit a PR, or simply open an issue in the repository (the easiest method).
