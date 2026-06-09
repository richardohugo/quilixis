---
name: quilixis
description: A data visualization framework for encoding data into visual form with structural rigor and editorial discipline. Use this skill when designing any chart, diagram, dashboard, or data graphic. It provides a decision framework for matching data types to visual channels, eliminating noise, and achieving the highest ratio of insight to cognitive effort.
license: MIT
---

# The Quilixis Framework

A unified method for designing data graphics that speak instantly and reward study.

---

## Part 1: The Two Modes

Every data graphic is built in two passes. The first is structural: you decide *what encodes what*. The second is editorial: you decide *what stays and what goes*. Most bad charts fail in one or both passes. The framework treats them as sequential and non-negotiable.


### Mode A — The Encoder

The encoder pass is about grammar. Visual marks on a surface form a language with rules, and those rules are not aesthetic preferences — they are perceptual constraints hardwired into the human visual system.

**The seven visual channels:**

Every mark on a chart surface encodes data through one or more of these channels. Each channel has specific perceptual properties that determine which data types it can carry.

| Channel     | Selective | Associative | Ordered | Quantitative |
|-------------|-----------|-------------|---------|--------------|
| Position    | Yes       | Yes         | Yes     | Yes          |
| Size        | Yes       | No          | Yes     | Yes          |
| Value       | Yes       | No          | Yes     | No           |
| Texture     | Yes       | Yes         | No      | No           |
| Color (hue) | Yes       | Yes         | No      | No           |
| Orientation | Yes       | Yes         | No      | No           |
| Shape       | No        | Yes         | No      | No           |

What these properties mean:

- **Selective**: the viewer can isolate all marks sharing a channel value ("show me all the blue ones"). Most channels are selective except shape.
- **Associative**: the viewer can group marks that differ in this channel but share others ("these are all the same category despite different shapes"). Most channels are associative except size.
- **Ordered**: the viewer perceives a natural sequence (small → large, light → dark, left → right). Position, size, and value are ordered; hue, shape, texture, and orientation are not.
- **Quantitative**: the viewer can estimate ratios ("A is twice B"). Only position and size support quantitative reading.

**Core encoding principles:**

1. **Position is king.** It is the only channel that is simultaneously selective, associative, ordered, and quantitative. Always encode the most important data dimension in position (x/y axes). This is non-negotiable.

2. **The three reading levels.** A graphic operates at three levels of information processing:
   - *Elementary*: reading a single data point ("What is the value for X?")
   - *Intermediate*: reading a group or subset ("How does group A compare to group B?")
   - *Comprehensive*: reading the overall pattern ("What is the structure of this dataset?")
   A well-constructed graphic enables the comprehensive level — the viewer grasps the overall pattern before reading any individual value.

3. **The image.** The ultimate goal. When a graphic achieves "the image," the viewer perceives the entire structure in a single moment of vision. The graphic has done its job when the reader does not need to scan sequentially. The data speaks as a gestalt.

4. **Monosemy.** Each visual sign should have exactly one meaning. Ambiguity is a design failure, not cleverness.

5. **Reorderability.** Rows and columns of a matrix should be reorderable to reveal hidden structure. A graphic is not a fixed picture but a manipulable analytical tool.

6. **Match channel to data type.** Ordered data demands ordered channels (position, size, value). Categorical data demands selective/associative channels (color, shape, texture). Mismatching these is the most common encoding error in visualization.


### Mode B — The Editor

The editor pass is about discipline. Having encoded the data correctly, you now remove everything that does not serve the data. The editor's tools are erasure, reduction, and restraint.

**Core editorial principles:**

1. **Data-ink ratio.** The proportion of ink devoted to non-redundant data information. Maximize it. Every drop of ink should have a reason.

   `Data-ink ratio = data-ink / total ink used in the graphic`

2. **Chartjunk.** Decorative elements that carry no information: heavy gridlines, 3D effects, gradient fills, background patterns, branded ornament. Eliminate ruthlessly.

3. **The Lie Factor.** The size of an effect shown in the graphic divided by the size of the effect in the data. A Lie Factor of 1.0 is honest. Truncated axes, area distortions, and perspective effects push it away from 1.0.

   `Lie Factor = (size of effect shown in graphic) / (size of effect in data)`

4. **Small multiples.** Repeat the same graphic design across panels, changing only the data. The eye compares effortlessly. The structure of the comparison is held constant so the viewer's cognitive load is spent entirely on the data differences.

5. **Sparklines.** Word-sized, high-resolution graphics embedded in the flow of text. Intense, simple, data-dense.

6. **Micro/macro readings.** A great graphic rewards both the glance (macro pattern) and the study (micro detail). Detail and overview coexist without conflict.

7. **Data density.** The best published graphics achieve 150-300 data entries per square inch. Most business graphics underperform by an order of magnitude.

8. **Integration of evidence.** Words, numbers, images, and diagrams belong together on the same surface. Segregating them into "the chart" and "the caption" fractures the reader's attention.

9. **Smallest effective difference.** Make all visual distinctions as subtle as they can be while still being clear. Thin lines over thick. Quiet colors over loud. Let the data be loud; let the frame be silent.


---

## Part 2: The Five Tensions

The encoder and editor pulls can conflict. The framework identifies five genuine tension points and resolves each into a usable design rule.

### Tension 1: Density vs. Perceptual Immediacy

The editor pushes for maximum data density — more data per pixel is always better. But the encoder pushes for "the image" — the instant gestalt. Sometimes achieving the image requires *reducing* data, aggregating, or abstracting so the pattern becomes perceptually immediate. A scatterplot with 50,000 points may be dense but illegible.

**Resolution:** Apply a two-pass test.
- *First pass (encoder test):* Can the viewer name the overall structure in under 3 seconds? If not, the graphic is too dense or poorly encoded. Aggregate, filter, or re-encode.
- *Second pass (editor test):* Having achieved structural clarity, can you now *add back* detail without destroying the pattern? If so, do it.

The synthesis: **Clarity first, then density.** The editor's density is the ceiling; the encoder's image is the floor.

### Tension 2: Narrative Integration vs. Structural Autonomy

The editor insists that graphics should integrate with text, argument, and evidence. Annotations and labels enrich the surface. But the encoder treats the graphic as structurally autonomous — a well-constructed graphic should reveal its pattern without narrative scaffolding.

**Resolution:** These address different audiences.
- For *exploratory* analysis (discovering patterns): favor the encoder. The graphic should be self-decoding.
- For *explanatory* communication (presenting findings): favor the editor. Integrate the argument. Annotate the turning points.

The synthesis: **Autonomous structure, integrated narrative.** Build the graphic so it *works* without text, then *enhance* it with text.

### Tension 3: Color Attitude

The encoder treats color (hue) as a channel with specific, limited properties: selective and associative but neither ordered nor quantitative. It grants color equal formal status alongside shape and texture. The editor is deeply suspicious of color — advocating restraint, muted tones, and the smallest effective difference.

**Resolution:** The encoder is right about *when* to use color (categorical distinctions); the editor is right about *how much* (as little as the task requires).
- Use hue for categorical variables (encoding rule).
- Use muted, distinguishable hues at low saturation (editorial restraint).
- Reserve high-saturation color for a single element that demands attention.
- For ordered data, use value (light-to-dark) not hue.

The synthesis: **Encode categorically, render quietly.**

### Tension 4: The Status of Decoration

The editor is absolutist: chartjunk is always bad. But the encoder's system includes texture — a channel that can shade into decoration. Borders, frames, and heavy graphical structure can serve as organizational devices.

**Resolution:** Distinguish *structural ornament* from *gratuitous ornament*.
- Structural ornament (borders that delineate panels, textures that encode a variable, frames that anchor a reorderable matrix) serves information. Keep it.
- Gratuitous ornament (3D bevels, drop shadows, gradient fills, background patterns, logos inside the data region) serves nothing. Remove it.

The synthesis: **If the ornament encodes or organizes, it stays. If it merely decorates, it goes.**

### Tension 5: The Reader's Role

The encoder designs for perceptual efficiency — the graphic should be engineered so decoding happens automatically, with minimal effort. The editor designs for an engaged, sophisticated reader who rewards close study and re-reading.

**Resolution:** Layer the graphic for both readers.
- The *surface layer* (color, position, overall shape) delivers instant comprehension to the passive reader.
- The *detail layer* (annotations, secondary axes, fine-grained marks, small multiples) rewards investigation by the active reader.

The synthesis: **Instant at a glance, rich on inspection.**

---

## Part 3: The Workflow

When designing any data graphic, apply this sequence:

### Step 1 — Classify the data (Encoder)

For each variable in the dataset, classify it:
- **Quantitative** (continuous numeric): position, then size
- **Ordered** (ranked, sequential): position, then value (lightness)
- **Categorical** (nominal, no order): color hue, shape, texture
- **Geographic** (spatial): map position

The most important variable gets **position** (x or y axis). Always.

### Step 2 — Choose the reading level (Encoder)

What question does the graphic answer?
- *Elementary* ("What is the value of X?"): table or labeled bar chart
- *Intermediate* ("How does A compare to B?"): grouped bars, scatterplot, small multiples
- *Comprehensive* ("What is the overall structure?"): heatmap, contour, treemap, reorderable matrix

Design for the highest reading level the audience needs.

### Step 3 — Draft the graphic

Encode the data using the channel mappings from Step 1. Use the simplest geometry that supports the reading level from Step 2.

### Step 4 — Apply the editorial pass

Review every element and ask:
- Does this ink represent data? If not, can it be removed without loss of information?
- Is the Lie Factor at or near 1.0?
- Could any visual distinction be made subtler while remaining clear? (Smallest effective difference)
- Are labels, annotations, and data integrated on the same surface?

Erase, reduce, lighten. But *stop* before you damage the encoding. If removing a gridline makes it impossible to read values at the elementary level, keep the gridline — just make it thinner and lighter.

### Step 5 — Apply the density pass (gated by the encoder)

Can you add more data without destroying the image?
- Add small multiples for comparison across a categorical variable
- Add sparklines for temporal context
- Layer secondary data as muted background marks
- Embed summary statistics as annotations

If the image breaks — if the gestalt is lost — you have gone too far. Remove the last addition.

### Step 6 — Test at both distances

- **Arm's length (encoder test):** Can you describe the overall pattern in one sentence within 3 seconds?
- **Nose to glass (editor test):** Can you extract specific values, compare subsets, and discover secondary patterns?

If both tests pass, the graphic is done.

---

## Part 4: Encoding Quick Reference

### Quantitative data (ratios, amounts, continuous)
| Priority | Channel           | Notes                                    |
|----------|-------------------|------------------------------------------|
| 1        | Position (axis)   | Most accurate; use for primary variable  |
| 2        | Length / height    | Bar charts; avoid area encoding if possible |
| 3        | Area / size       | Bubbles; humans underestimate area ~0.7x |
| 4        | Value (lightness) | Choropleth; good for continuous surfaces  |
| 5        | Color saturation  | Limited resolution (~3-4 distinguishable steps) |

### Ordered data (ranks, sequences, ordinal scales)
| Priority | Channel         | Notes                                  |
|----------|-----------------|----------------------------------------|
| 1        | Position        | Axis order must match data order       |
| 2        | Value           | Light-to-dark encodes low-to-high      |
| 3        | Size            | Small-to-large encodes low-to-high     |

### Categorical data (types, groups, labels)
| Priority | Channel   | Notes                                          |
|----------|-----------|-------------------------------------------------|
| 1        | Position  | Separate panels (small multiples) if possible  |
| 2        | Color hue | Max 7-8 distinguishable hues; use muted tones  |
| 3        | Shape     | Max 5-6 distinguishable shapes                  |
| 4        | Texture   | Useful for print; avoid moiré on screen         |

### What to avoid
- 3D effects on 2D data (distorts position, the most important channel)
- Rainbow color scales for ordered data (hue is not ordered; use sequential value scales)
- Dual y-axes (creates false correlations through arbitrary scaling)
- Pie charts for more than 2-3 categories (angle/area perception is poor)
- Truncated baselines on bar charts (inflates Lie Factor)
- Legend-dependent encoding when direct labels are possible (forces the eye to shuttle)

---

## Part 5: Implementation Notes

### For SVG / D3 / Plotly / Chart.js / Recharts:

**Grid and frame:**
- Default: no outer border. Let the axes define the space.
- Gridlines: light gray (#e0e0e0 or lighter), thin (0.5-1px), only on the axis the reader needs for value lookup. Omit if not needed.
- Axis lines: thin, dark gray (#666), not black. Smallest effective difference.

**Color palette defaults:**
- Categorical: muted, distinguishable palette. Good defaults: ColorBrewer qualitative palettes at reduced saturation.
- Sequential: single-hue light-to-dark ramp.
- Diverging: two-hue ramp with neutral midpoint.
- Alert/highlight: one saturated hue against muted context.

**Typography:**
- Data labels directly on marks when possible. Remove legends when direct labeling is feasible.
- Annotation text: same typeface as body, smaller size, lighter weight. Do not compete with data marks.
- Axis titles: only if the variable name is not self-evident.

**White space:**
- Generous margins. Do not crowd the data region against the edge.
- Space between small-multiple panels: wide enough to prevent grouping confusion, narrow enough to enable comparison.

**Animation (if interactive):**
- Transition data changes, not decoration. A bar growing to its value aids comprehension. A spinning logo does not.
- Hover states should reveal elementary-level detail (exact value, label) without disrupting the comprehensive-level image.

---

## Part 6: The One-Line Summary

> **Encode with rigor, edit with discipline.** Match visual channels to data types using perceptual rules. Then strip away everything that does not serve the data. The result is a graphic that speaks instantly and rewards study.
