# For Moon — memory journey

A star-by-star memory page. Click each star to reveal a memory; the path
only lights up (and the next star only appears) after the previous one
has been opened. Once all stars are found, tap the moon for the closing
message.

## Hosting on GitHub Pages

1. Create a repo and add these files (`index.html`, the `audio/` folder).
2. Drop your track into `audio/` and name it exactly `cafuneslowed.mp3`
   (the page already looks for `audio/cafuneslowed.mp3` — no code changes
   needed once the file's there).
3. In the repo settings, enable **GitHub Pages** → deploy from the
   branch you pushed to (root folder).
4. Your page will be live at `https://<username>.github.io/<repo-name>/`.

## Editing content

Everything you'll want to change lives inside `index.html`:

- **Memories** — search for `const memories = [` near the bottom of the
  `<script>` section. Each entry has `title`, `date`, `text`, and `photo`
  (a base64 data URI, or `null` for a placeholder).
- **Closing message** — `const finaleTitle` and `const finaleText`, just
  above the memories array.
- **Colors** — the `:root { ... }` block near the top of the `<style>`
  section (`--star-gold`, `--sky-deep`, `--lavender`, etc.).
- **Background music** — the `<audio>` tag's `src` points at
  `audio/cafuneslowed.mp3`. Swap the filename there (and in the audio
  folder) if you use a different track name.
