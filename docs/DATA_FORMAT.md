# Data format

## Choir song

```json
{
  "id": "ave-maria",
  "type": "choir",
  "title": "Ave Maria",
  "artist": "Composer",
  "key": "F major",
  "tags": ["chant à la Vierge", "polyphonie"],
  "overallAudio": "audio/ave-maria/full.mp3",
  "score": "scores/ave-maria.pdf",
  "tutorials": {
    "soprano": "audio/ave-maria/soprano.mp3"
  }
}
```

## Pop/guitar song

```json
{
  "id": "song-id",
  "type": "pop",
  "title": "Song title",
  "artist": "Artist",
  "key": "G",
  "capo": 2,
  "tags": ["pop"],
  "content": "[G]Words with [C]chords"
}
```
