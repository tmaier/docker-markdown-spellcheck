# Docker image for node-markdown-spellcheck

This is a lightweight docker image for [`node-markdown-spellcheck`](https://github.com/lukeapage/node-markdown-spellcheck).
A spell checker for Markdown files.
See https://github.com/lukeapage/node-markdown-spellcheck

The working directory is at `/workdir`. Mount your volume into that directory.

```bash
$ docker run -ti -v $(pwd):/workdir tmaier/markdown-spellcheck:latest "**/*.md"
```

## Other languages

Many additional directories can be found at `/usr/share/hunspell`.

List all languages available:

```bash
docker run -ti tmaier/markdown-spellcheck:latest hunspell -D
```

```bash
$ docker run -ti -v $(pwd):/workdir tmaier/markdown-spellcheck:latest --dictionary /usr/share/hunspell/de_DE_comb "**/*.md"
```

## Continuous Integration (CI)

Run in report mode

```bash
$ docker run -ti -v $(pwd):/workdir tmaier/markdown-spellcheck:latest --report "**/*.md"
```

## Author

[Tobias L. Maier](http://tobiasmaier.info) for [BauCloud GmbH](http://www.baucloud.com)
