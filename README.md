# Amethyst Website

[![Build Status][s1]][tc] [![CC BY-SA License][s2]][cc] [![Join the chat][s3]][gc]

[s1]: https://travis-ci.org/amethyst/website.svg?branch=master
[s2]: https://img.shields.io/badge/license-CC%20BY--SA-blue.svg
[s3]: https://badges.gitter.im/amethyst/website.svg

[tc]: https://travis-ci.org/amethyst/website
[cc]: ./LICENSE.md
[gc]: https://gitter.im/amethyst/website?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badgeontent=badge

This is the source code for the Amethyst website and blog, accessible from
either https://amethyst.github.io/website/ or https://www.amethyst.rs/. The HTML
is generated by [Zola][za] and hosted online with [GitHub Pages][gp].

[za]: https://www.getzola.org/
[gp]: https://pages.github.com/

Any changes to the `master` branch of this repository should automatically
trigger a rebuild and republish of the site through [Travis CI][tc].

## Structure

Content                              | Source Path               | Website Path
-------------------------------------|---------------------------|-------------
Main Content                         | `src/content`             | `/`
News from Amethyst                   | `src/content/blog`        | `/blog/`
Amethyst Book                        | [`amethyst/book/src`][bs] | `/book/`
Generated API Documentation          | [`amethyst/src/`][ds]     | `/doc/`

[bs]: https://github.com/amethyst/amethyst/tree/master/book/src
[ds]: https://github.com/amethyst/amethyst/tree/master/src

## Building Locally

To generate a complete local copy of the website with documentation, run:
```
$ ./generate.sh
```

Note that this is a long process.  If you are looking to get up and running quickly for development, first install [Zola](https://www.getzola.org/documentation/getting-started/installation/) and then run the following:


```
$ cd src && zola serve
```

This will generate temporary files in `src/public` as well as start a local server with live updates.  If you are just looking to generate files without a webserver, you can use `zola build` instead of `serve`.  The homepage can be found at `public/index.html`.

## Contributing

We are a community project that welcomes contribution from anyone. If you're
interested in helping out, please read the [CONTRIBUTING.md][cm] file before
getting started. Don't know what to hack on? Feel free to search though
[our issue tracker][it].

[cm]: https://github.com/amethyst/amethyst/blob/master/CONTRIBUTING.md
[it]: https://github.com/amethyst/website/issues
