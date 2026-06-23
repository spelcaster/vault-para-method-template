Guidance for working in this Obsidian vault. This is a personal knowledge base,
not a software project — commits should capture **what changed in the thinking**,
not just which files moved.

## Commit philosophy

- A commit represents one coherent change to the knowledge base.
- The message should let me understand what happened without opening the diff.
- Describe the idea/content, not the file operation:
  `add: note on spaced repetition` — not `create Untitled.md`.

## Message format

```
<type>: <what changed, in plain language>
```

**Types**

- `add` — a new note, or a new section of genuine content
- `expand` — meaningful new material added to an existing note
- `revise` — reworking or rewriting content that already existed
- `link` — connecting notes, adding backlinks, building/updating an MOC
- `restructure` — moving, renaming, or reorganizing files and folders
- `fix` — typos, broken links, formatting
- `meta` — vault config, templates, plugins, `.obsidian` changes

Keep the subject under ~70 characters, lowercase, no trailing period. Add a body
(after a blank line) only when the *why* isn't obvious from the subject.

**Examples**

- `add: note on the Zeigarnik effect, linked to memory MOC`
- `expand: add CAP theorem section to distributed-systems note`
- `revise: rewrite intro of "Deep Work summary" for clarity`
- `link: connect spaced-repetition note to Anki workflow`
- `restructure: move career notes under areas/work/`
- `fix: repair broken wikilinks across literature notes`

## Grouping changes

- Bundle edits that serve **one idea** into a single commit, even across files
  (e.g. a new note plus the MOC entry that references it).
- Split **unrelated** changes into separate commits — a typo fix in one note and
  a brand-new note are two commits, not one.
- Never mix `meta`/config changes into a content commit.

## Before committing

- Review the diff and summarize the actual intellectual change — don't narrate
  file paths.
- Don't stage churn that should be ignored: `workspace.json`, caches, `.trash/`.
- Respect the existing `.gitignore`; don't add anything it deliberately excludes.

## Tone

- Write each subject so it completes the sentence: "This commit will ⟶ _____".
- Brevity is fine. For notes, a single clear subject line is usually enough.
