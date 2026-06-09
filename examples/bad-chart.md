# Example: Financial crises bar chart (bad)

Same 12 crises, same underlying data. A dual-axis bar chart with rainbow colors. Every design choice violates a specific Quilixis principle.

## The 9 violations

### 1. Rainbow colors encode nothing

**Principle violated:** Encoder — channel/data type mismatch

12 crises get 12 arbitrary hues. Color hue is a selective and associative channel — it should encode the categorical variable (crisis type: banking, currency, sovereign) so the viewer can perceive group structure. Instead, each bar gets a unique color, making hue an index of individual identity. The viewer cannot "see all banking crises at once" because they are scattered across the rainbow.

### 2. Dual y-axes create false correlations

**Principle violated:** Editor — Lie Factor

GDP decline (left axis) and duration (right axis) are plotted on independently scaled axes. The visual relationship is entirely manufactured by the scaling choices. Change the right axis range and the "relationship" changes. There is no honest way to read correlation from dual axes because the correspondence is an artifact of axis alignment, not a property of the data.

### 3. Truncated baseline inflates differences

**Principle violated:** Editor — Lie Factor

The left y-axis starts at 3%, not 0%. Brazil's 4.7% and the US's 5.1% differ by 0.4 percentage points, but their bars look dramatically different because the viewer perceives bar length, not bar endpoint. Lie Factor exceeds 1.0.

### 4. No comprehensive reading possible

**Principle violated:** Encoder — the image / reading levels

Can you name the overall structure in 3 seconds? No. The chart forces sequential, elementary-level reading. The most important insight (banking crises are systematically worse than currency crises) requires categorical grouping, which is not encoded anywhere.

### 5. Legend forces eye-shuttling

**Principle violated:** Editor — integration of evidence

Look at a bar → identify its color → shuttle to the legend → match the color → read the name → return to the bar. With 12 similar hues, matching errors are frequent. Direct labels eliminate the round trip.

### 6. Heavy borders, background pattern, and frame

**Principle violated:** Editor — data-ink ratio, chartjunk

3px border. Diagonal stripe background. Decorative title. None of this is data-ink. The frame is louder than the content.

### 7. Two dimensions collapsed to one

**Principle violated:** Encoder — information capacity

The good chart encoded four variables simultaneously using four channels (x-position, y-position, size, hue). This chart encodes only two (GDP decline and duration) and discards recovery time and crisis type entirely. Two dimensions of the data are destroyed.

### 8. Thick gridlines dominate the data

**Principle violated:** Editor — smallest effective difference

Heavy gridlines at 2px and full opacity compete with data bars. Gridlines should be the quietest element — present only to support value estimation. Here the grid is louder than the signal.

### 9. Arbitrary x-axis ordering violates monosemy

**Principle violated:** Encoder — monosemy, position properties

The x-axis places crises in an arbitrary order. But position is inherently perceived as ordered. The viewer assumes left-to-right arrangement means something — chronological? by severity? — but it is arbitrary. A false signal is transmitted through a channel the viewer cannot ignore.

## The core lesson

These are not cosmetic problems. They are information problems. The bad chart cannot answer the most important question the data contains because the encoding choices destroyed the categorical structure. The ugliness is a symptom. The real failure is that insight is unreachable.
