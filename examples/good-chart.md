# Example: Financial crises bubble chart (good)

This example applies all 6 steps of the Quilixis workflow to a dataset of 12 major financial crises.

## The data

| Crisis | Type | Duration (months) | Peak GDP decline (%) | Recovery (years) |
|--------|------|-------------------|---------------------|-----------------|
| US 2007 | Banking | 36 | 5.1 | 6 |
| Indonesia 1997 | Banking | 48 | 13.1 | 10 |
| Finland 1991 | Banking | 24 | 10.5 | 5 |
| Sweden 1991 | Banking | 30 | 8.0 | 7 |
| Japan 1992 | Banking | 42 | 7.5 | 8 |
| UK 2007 | Banking | 18 | 7.0 | 4 |
| Mexico 1994 | Currency | 6 | 7.6 | 3 |
| Thailand 1997 | Currency | 12 | 6.7 | 4 |
| Russia 1998 | Currency | 9 | 5.3 | 2 |
| Brazil 1999 | Currency | 8 | 4.7 | 3 |
| Greece 2010 | Sovereign | 60 | 9.5 | 8 |
| Argentina 2001 | Sovereign | 24 | 6.2 | 5 |

## Step 1 — Classify the data (Encoder)

| Variable | Data type | Channel | Justification |
|----------|-----------|---------|---------------|
| Duration | Quantitative | x-axis position | Position is the only channel that is selective, associative, ordered, and quantitative. Duration is a primary comparison dimension. |
| GDP decline | Quantitative | y-axis position | Same reasoning. Second most important variable gets the second position axis. |
| Recovery time | Quantitative | Bubble radius (size) | Size is the next-best quantitative channel. Ordered and quantitative but not associative — correct for a third-priority variable. |
| Crisis type | Categorical | Color hue | Hue is selective and associative but not ordered — matching the properties needed for a nominal category. |

## Step 2 — Choose the reading level (Encoder)

Target: **comprehensive**. The question is "what is the overall structure of financial crises across all four dimensions?"

## Step 3 — Draft

A bubble chart is the simplest geometry supporting three quantitative channels plus one categorical channel. Y-axis inverted so "worse" maps to visual descent (monosemy — the spatial metaphor reinforces the data meaning).

## Step 4 — Editorial pass

**Removed:** outer chart border, legend box (replaced by direct labels), background fill.

**Reduced to smallest effective difference:** gridlines (0.5px, low opacity), axis lines (same weight as gridlines), color saturation (35% opacity fills with 1.5px borders), axis labels (11px, muted).

**Kept:** gridlines (necessary for elementary-level GDP value estimation), axis titles (not self-evident from numbers alone).

## Step 5 — Density pass

**Added without breaking the image:** direct name labels on every bubble, annotation box narrating the comprehensive reading, hover tooltips for elementary precision.

**Not added (would break the image):** GDP trajectory sparklines inside bubbles, small multiples by decade.

## Step 6 — Test at both distances

**Arm's length (encoder test):** three clusters visible in under 3 seconds. Blue upper-right (banking: long, deep, slow). Coral lower-left (currency: short, sharp, fast). One extreme outlier (Indonesia). Pass.

**Nose to glass (editor test):** hover any bubble for exact figures. Compare Greece to Japan — similar depth, different duration. Labels enable individual identification. Pass.

## Key insight the encoding reveals

Banking crises cluster as systematically longer, deeper, and slower to recover than currency crises. This structural insight is only visible because crisis type is encoded in color hue (enabling categorical grouping) and duration/severity are encoded in position (enabling quantitative comparison). The encoding choice *creates* the insight.
