# World News — 24 November 2026

A one-picture front page of the world on Tuesday, 24 November 2026:
**35 dated stories, 7 regions** — Nvidia brings back Jensen Huang,
Zelenskiy warns of new Russian strikes, and Trump takes on Newsom at
the Justice Department.

The poster (`entry.png`, 1024×1024, under 1 MiB) is drawn from
`stories.json` — 13 illustrated cards (the 3 biggest stories lead),
a numbered world map, 22 more stories, a 6-number key strip, and a
DATE CHECK box naming the 23 November stories that were dropped.
Every story was reported on 24 November 2026; the source is named
per story.

## Run locally

```sh
MAKEFUN_OUTPUT_DIR=/tmp/out node main.ts   # validate + copy entry.png
```

The poster was rendered from the day's `stories.json` with
`generate.py` (kept in the sibling `news-image-20261124-src` folder).

`main.ts` (Node 22, no dependencies) validates the PNG — signature,
chunk structure, IHDR 1024×1024, IEND at the end, ≤ 1 MiB — then
copies its bytes unchanged to `$MAKEFUN_OUTPUT_DIR` (default
`/output`)/`entry.png` and verifies the copy by reading it back.
