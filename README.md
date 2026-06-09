# Quilixis

A data visualization framework built on two modes — **encode with rigor, edit with discipline** — that turns raw data into graphics people actually read.

## What this is

A decision framework for anyone designing charts, diagrams, dashboards, or data graphics. It provides:

- **A 6-step workflow** from data classification through structural encoding to editorial refinement
- **Five named tensions** between the encoding and editing impulses, each resolved into a concrete design rule
- **An encoding quick reference** mapping data types to visual channels with priority rankings
- **Implementation notes** for SVG, D3, Chart.js, Recharts, and Plotly

## The two modes

Every data graphic is built in two passes:

**Mode A — The Encoder** defines the grammar. Seven visual channels (position, size, value, texture, color, orientation, shape) each have specific perceptual properties. The encoder matches data types to channels using those constraints, not aesthetic preference.

**Mode B — The Editor** enforces discipline. Having encoded the data, the editor removes everything that does not serve it. Data-ink ratio, smallest effective difference, integration of evidence.

## The 5 tensions

The encoder and editor can pull in opposite directions. The framework names five conflict points and resolves each:

| # | Tension | Encoder says | Editor says | Resolution |
|---|---------|-------------|------------|------------|
| 1 | Density vs. immediacy | Simplify until the gestalt is instant | Maximize data per square inch | Clarity first, then density |
| 2 | Narrative vs. autonomy | The graphic should decode itself | Graphics should integrate with argument | Build autonomous, enhance with narrative |
| 3 | Color | Hue is a formal channel — use it for categories | Color is suspect — restrain it | Encode categorically, render quietly |
| 4 | Decoration | Texture and borders can serve structure | All chartjunk must die | Structural ornament stays, gratuitous goes |
| 5 | Reader's role | Design for passive, instant decoding | Design for active, investigative study | Instant at a glance, rich on inspection |

## The 6-step workflow

1. **Classify the data** — quantitative, ordered, categorical, geographic
2. **Choose the reading level** — elementary, intermediate, or comprehensive
3. **Draft the graphic** — encode using channel-to-data-type mappings
4. **Apply the editorial pass** — erase non-data-ink, check Lie Factor, smallest effective difference
5. **Apply the density pass** (gated by the encoder) — add detail without destroying the image
6. **Test at both distances** — arm's length for instant structure, nose to glass for investigative detail

## Quick start

Read [`SKILL.md`](./SKILL.md) — the complete framework in a single file.

Browse [`examples/`](./examples/) for annotated demonstrations.

## Using as a Claude skill

Point to `SKILL.md` as a skill file. It works as a system-level reference that Claude can consult when generating any data visualization.

## File structure

```
quilixis/
├── README.md           ← You are here
├── SKILL.md            ← The complete framework
├── CHANGELOG.md        ← Version history
├── LICENSE             ← MIT License
└── examples/
    ├── good-chart.md   ← Annotated example applying all 6 steps
    └── bad-chart.md    ← Anti-pattern with 9 violations identified
```

## Contributing

Open an issue or PR. The framework is opinionated by design — if you disagree with a resolution, argue your case. The tensions are genuine and reasonable people can resolve them differently.

## License

MIT. See [LICENSE](./LICENSE).
