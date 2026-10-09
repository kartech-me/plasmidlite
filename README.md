# PlasmidLite

A free, open-source plasmid viewer and cloning helper that runs entirely in your browser. No account, no upload: your sequences never leave your computer.

**Live app:** https://kartech-me.github.io/plasmidlite/

## Features
- Open GenBank, FASTA, JSON or a previously saved PlasmidLite HTML file (drag and drop works)
- Circular and linear maps with feature arrows and unique-cutter labels
- Sequence view with complement strand, feature bars and translation (CDS features or any of the 6 frames)
- Add, edit and delete features; edit the sequence (features shift automatically); reverse complement; set origin
- Restriction-site search (57 common enzymes), virtual digest with a simple gel and FASTA export of fragments
- Selection info: GC %, rough Tm, translation; find motif on both strands (IUPAC codes allowed)
- Autosave in the browser, undo/redo, export GenBank / FASTA / JSON
- **Save as HTML**: writes a self-contained copy with your sequence and features embedded. Anyone who opens that file sees your annotated plasmid immediately.
- Installable as an app (PWA) and works offline once loaded

## Limitations (v0.1)
- Restriction digests ignore overhangs; there is no ligation/Gibson/Golden Gate simulation yet
- Tm is a rough estimate (not nearest-neighbour)
- Always check important designs against a second tool before ordering anything

## Run locally
Open `index.html` in a browser. For the installable/offline version serve the folder over HTTP, e.g. `python -m http.server`.

## Contributing
Pull requests are welcome. The app is plain HTML/JS with no build step: the logic is in the first inline script of `index.html` (parsing, enzymes, editing) and the UI in the second.

## Licence
MIT, see `LICENSE`.
