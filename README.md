# Choir Library

A completely static choir repertoire and event-programme website for GitHub Pages.

## Features

- Fuzzy repertoire search and tag filters
- Choir songs with overall recording, optional PDF score and optional SATB tutorials
- Pop/guitar songs with key, capo, lyrics and inline chords
- Guitar fingering codes on chord hover
- Public, shareable event programmes
- Browser-based admin area for songs, events and tags
- JSON export workflow, with no database or user accounts

## Publish on GitHub Pages

1. Create a new GitHub repository.
2. Upload every file and folder from this project to the repository root.
3. In **Settings > Pages**, select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)`, then save.
5. Open the Pages URL shown by GitHub.

Because the site uses relative paths and hash-based navigation, it works from both a user/organisation Pages site and a project Pages subfolder.

## Admin workflow

Open `#/admin`, for example:

`https://YOUR-NAME.github.io/YOUR-REPO/#/admin`

Changes are stored only in that browser. In the **Export** tab, download:

- `songs.json`
- `events.json`
- `tags.json`

Replace the matching files in `/data` in GitHub and commit. GitHub Pages then republishes the updated files.

## Adding PDFs and audio

Put media in these folders:

- `/scores/song-name.pdf`
- `/audio/song-name/full.mp3`
- `/audio/song-name/soprano.mp3`

In Admin, enter a relative path such as `scores/song-name.pdf` or `audio/song-name/full.mp3`. External YouTube/audio URLs also work.

The admin exporter only exports JSON. Upload new PDF and audio files to GitHub separately.

## Local preview

Browsers block JSON loading when `index.html` is opened as a local file. Run a local static server instead:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Important practical limits

Large audio collections can make a Git repository cumbersome. Compress rehearsal audio before committing. Also make sure you have permission to publish lyrics, scores and recordings.
