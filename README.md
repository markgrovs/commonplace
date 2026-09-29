# Commonplace

A small Hugo theme for a personal commonplace book. It has no theme dependencies, JavaScript, web fonts, or build step. Its templates cover the home page, individual writing, sections, taxonomy lists, feeds, and a 404 page. The site supplies its own content and configuration.

Use Hugo Extended 0.165.0 or newer. Set `theme = "commonplace"` in the site's Hugo configuration. The theme reads `params.author.first_name` for the footer email label and `params.author.full_name` for bylines and identity, plus `params.description` and an optional `params.welcome`. It uses the `email` item in `params.social` for the footer link. Optional `params.gitUrl` enables commit links for tracked writing. IndieAuth, Webmention, and Pingback discovery URLs come from `params.indieweb`.

The stylesheet follows the device's light or dark appearance setting. Site assets such as favicons live in the site repository.

The optional Reactions section reads Webmention.io JSON files from the site's `data/webmentions/` directory. It omits private and self-authored records, groups the rest by target page, and orders them by their received timestamp. Add a `content/reactions/_index.md` page to publish the index; writing with responses gets a short link below its entry metadata. Author names link to their profiles or source posts; avatar images are not displayed because stored image URLs may no longer work.
