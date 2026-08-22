DICE-NX website
===============

Initial setup:

```bash
asdf plugin add npm
asdf plugin add hugo
asdf install
npm install --include=dev
```

Localhost server for previewing the website during development:

```bash
hugo serve --buildDrafts --buildFuture --disableFastRender
```

Using "lo" theme:

```bash
hugo serve --buildDrafts --buildFuture --disableFastRender --theme dice-nx-lo
```
