# Blog

Each post lives in its own folder, with its page and images together:

```
blog/
  <post-slug>/
    index.html   ← the article page
    cover.png    ← card + header image
```

## Adding a post

1. Copy an existing post folder and rename it to the new slug (lowercase, hyphens).
2. In the new `index.html`, update the title, description, `og:image` URL and cover alt text, then paste the article HTML (`h2`, `h3`, `p`, `ul`, `blockquote`, ...) into `<div class="post-body">`.
3. Replace `cover.png` with the new image.
4. In the root `index.html`, add a `<li class="blog-post-item">` (banner, title, short description) to the `#BLOG` list (newest first) linking to `./blog/<post-slug>/`.

Post styles are shared in `assets/css/blog-post.css`.

When you change a CSS or JS file, bump its `?v=` number in the `<link>`/`<script>` tags so browsers load the new version instead of a cached one.
