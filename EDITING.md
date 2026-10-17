# How to edit the website

Every page on the site comes from a plain text file in the `content/` folder.
Edit a file, save it, and the website updates itself in about a minute.

## The easy way: edit on github.com

1. Open the repository on github.com and click into the `content/` folder.
2. Click the file you want to change, then the **pencil icon** (top right of the file).
3. Make your change and click **Commit changes…** → **Commit changes**.
4. Wait about a minute, then refresh the website. (The **Actions** tab shows a
   green check when the update is live, or a red ✗ if something went wrong —
   usually a missing quote mark in the part between the `---` lines.)

## Which file is which

| Page on the site      | File to edit                              |
|-----------------------|-------------------------------------------|
| Homepage bio          | `content/_index.md`                       |
| Papers page (layout, working papers) | `content/papers/_index.md` |
| One paper             | `content/papers/<name>.md`                |
| Teaching              | `content/teaching.md`                     |
| Contact               | `content/contact.md`                      |
| CV / Scholar / social links, menu | `hugo.toml`                   |
| Pictures              | `static/images/`                          |

## Writing text

Files use **Markdown**, which is just text with a few symbols:

```
## A heading
**bold**, *italic*
[link text](https://example.com)
- a bullet point
```

Leave a blank line between paragraphs.

## Adding a paper

1. In `content/papers/`, click **Add file → Create new file**.
2. Name it something short, like `my_new_paper.md`.
3. Paste this in and fill it out:

```
---
title: "The Title of the Paper"
year: 2026
section: "Human Memory and Decision Making"
link: "https://doi.org/..."
image: "my_new_paper.jpg"
---

The abstract goes here.
```

- **section** must match one of the names in `content/papers/_index.md`
  (`Human Memory and Decision Making`, `Cognitive Processes`, or `Book Chapters`).
- Papers are sorted newest first automatically.
- **image** is optional. To add one, upload it to `static/images/papers/`
  (**Add file → Upload files**) and put its file name here. Leave it as `""` for no image.

To remove a paper, open its file, click the **⋯** menu → **Delete file**.

## Working papers

Open `content/papers/_index.md`. Each working paper is one line under
`working_papers:` — add, remove, or reorder lines. Keep the `- "..."` format.

When a working paper is published, delete its line there and add it as a paper (above).

## Adding a new section to the Papers page

Add its name to the `sections:` list in `content/papers/_index.md` (in the order
you want it to appear), then use that exact name in the papers' `section:` line.

## Updating the CV link

In `hugo.toml`, find `name = "CV"` and replace the `url` underneath it.

## Previewing on your own computer (optional)

If you have Hugo installed (`brew install hugo` on a Mac), run `hugo server`
in this folder and open http://localhost:1313. It refreshes as you save.
