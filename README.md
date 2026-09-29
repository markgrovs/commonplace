# Commonplace

A small Hugo theme for a personal commonplace book. It has no theme dependencies, JavaScript, web fonts, or build step. Its templates cover the home page, individual writing, sections, taxonomy lists, feeds, and a 404 page. The site supplies its own content and configuration.

Use Hugo Extended 0.165.0 or newer. Set `theme = "commonplace"` in the site's Hugo configuration. The theme reads `params.author.first_name` for the footer email label and `params.author.full_name` for bylines and identity, plus `params.description` and an optional `params.welcome`. It uses the `email` item in `params.social` for the footer link. Optional `params.gitUrl` enables commit links for tracked writing. IndieAuth, Webmention, and Pingback discovery URLs come from `params.indieweb`.

The stylesheet follows the device's light or dark appearance setting. Site assets such as favicons live in the site repository.

An ordinary page can include the `rss-subscribe` shortcode to show a reader-opening link and an HTTPS feed address. It combines the configured `params.productionBaseURL` with the homepage RSS output path, keeping subscriptions on production during preview builds. The site supplies the Follow page's explanatory copy.

Link posts use `content/links/`, `type: link`, and the existing `link` field for the original source URL. Listings lead to the local entry; the entry and its RSS item show the source alongside the author's commentary. A source link already present in Markdown is used without adding a duplicate. The homepage shows up to three published links from the preceding 30 days, using their publication dates at build time; the Links archive and feeds retain older entries. Draft and future links are omitted from the homepage even in preview builds.

The optional Reactions section reads Webmention.io JSON files from the site's `data/webmentions/` directory. It omits private and self-authored records, groups the rest by target page, and orders them by their received timestamp. Add a `content/reactions/_index.md` page to publish the index; writing with responses gets a short link below its entry metadata. Author names link to their profiles or source posts; avatar images are not displayed because stored image URLs may no longer work.
