# gsmtoday.github.io

Personal GitHub Pages site for `gsmtoday0329`.

The site is intentionally simple: a personal homepage plus writing categories
for Agent evaluation, AI learning, chip knowledge, fitness, the "码农姐妹"
podcast, and other learning notes.

## Publish

This site is plain static HTML/CSS. GitHub Pages can publish it directly from the repository root.

Expected repository name:

```text
gsmtoday0329.github.io
```

Expected public URL:

```text
https://gsmtoday0329.github.io
```

## Add a post

1. Add the new static page.
2. Add a new card in `index.html`.
3. Set the card category with `data-category`.

Available categories:

```text
agent-eval
ai-learning
fitness
podcast
health
```

## Comments

Comments use [utterances](https://utteranc.es/) and are stored as GitHub Issues in:

```text
gsmtoday0329/gsmtoday0329.github.io
```

Before publishing comments, install the utterances GitHub App for the repository and make sure Issues are enabled.

## Local preview

Open `index.html` directly in a browser, or run a small local server:

```bash
python3 -m http.server 8080
```
