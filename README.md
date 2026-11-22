# norn-lang.org

The website of [Norn](https://github.com/norn-lang/norn), the coordination
language for teams of people and AI agents. GitHub Pages publishes this
repository as it is, at <https://norn-lang.org>. The playground at
<https://norn-lang.org/norn/> is published from the language repository.

## Changing the page

Edit `src/index.html`, and the programs in `src/programs`, then rebuild
`index.html` and commit both:

```sh
git clone https://github.com/norn-lang/norn ../norn && (cd ../norn && npm ci)
node tools/build.ts --norn ../norn     # Node 22.18 or newer
python3 -m http.server                 # then open http://localhost:8000
```

The build runs `norn check` on every program the page shows and stops if one
fails, colours the code with the playground's highlighter, and links each
program to the playground. CI rebuilds the page against the language's main
branch and fails when the committed `index.html` differs.

`styles.css`, `404.html`, `robots.txt`, `sitemap.xml` and `og.png` are written
by hand, as are the icons: `favicon.svg` is the source (the wordmark's n, its
right leg hanging straight down into a moorit knot, like thread on a drop spindle), and `favicon.ico`,
`favicon-96x96.png` (the size Google Search asks for), `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` and
`icon-maskable-512.png` are rendered from it, for `site.webmanifest`. `llms.txt` is a copy of the one in the language repository.

## License

The site is [Apache-2.0](https://github.com/norn-lang/norn/blob/main/LICENSE),
like the language. The typefaces in `fonts` are Geist and Commit
Mono, each under the SIL Open Font License; their licenses are beside them.
