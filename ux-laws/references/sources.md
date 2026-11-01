# Sources

All captured 2026-10-22 from short video reels and two screenshot lists. Definitions in the laws table are standard UX textbook meanings written by the skill author, not quotes. Only the numbers and law names below come from the sources.

## Reels

| Id | Creator | Date captured | Gives |
|---|---|---|---|
| reel 07 `Deq_kvJBI3g` | @designmotionhq | 2026-10-22 | Mobile specs: under 640 px table rows become cards, amounts on one line, 16 px input text (Safari zoom), keyboard per field, 44 px touch targets (touch only), safe area padding on fixed bottom bars with room under the content |
| reel 08 `DdxddtWBsl_` | @motion_ui_interface | 2026-10-22 | Form and login specs: one primary action, 8 px grid, 56 px fields, 16 between, 32 before the button, 40 px fields fail, label above, placeholder is an example, one accent, 2 px focus ring, three text tiers, radius 24 card and 12 fields and buttons, shadow falls down, focus ring fades in within 150 ms, feedback 100 ms and done 300 ms |
| reel 16 `Ddy5RJOha1U` | @motion_ui_interface | 2026-10-22 | Button specs: 44 px minimum aim 48, 24 px side padding, 17 px semibold sentence case verb plus object, label contrast above 4.5 to 1, edge above 3 to 1, flat grey 1.6 to 1, pill radius height divided by 2, one icon 20 px wide 10 px from label, shadow 8 px down 24 blur, hover 200 ms, press sinks 1 px, spinner then check, feedback 100 ms done 300 ms |
| reel 24 `DcwkX6OyduT` | @adam_ha_yes | 2026-10-22 | The 20 principles list, including interactions within 400 ms (Doherty), sensible defaults, prevent errors, make errors recoverable |

## Screenshot lists

Creator not named in the capture (caption said to comment for the full instructions file). Captured 2026-10-22.

| Id | Title | Items |
|---|---|---|
| S2 | 20 UX Laws to tell Claude for better Design | Hick's, Fitts's, Jakob's, proximity, Miller's, Doherty threshold, Von Restorff, minimize target distance, serial position, peak end, Zeigarnik, Pragnanz, similarity, uniform connectedness, Tesler's, Postel's (twice), Parkinson's, Occam's razor, Pareto |
| S3 | UX Laws your Claude Needs | Aesthetic usability, Hick's, Fitts's, Jakob's, Miller's, Doherty threshold, proximity, similarity, common region, visual hierarchy, progressive disclosure, recognition over recall, Von Restorff, peak end, goal gradient, serial position, Tesler's, Postel's, Occam's razor, feedback loops |

## Law to source map

| Law | Source |
|---|---|
| Hick, Fitts, Jakob, proximity, Miller, Doherty, Von Restorff, serial position, peak end, Tesler, Postel, Occam | S2 and S3 |
| Minimize target distance, Zeigarnik, Pragnanz, uniform connectedness, Parkinson, Pareto | S2 only |
| Aesthetic usability, common region, visual hierarchy, progressive disclosure, recognition over recall, goal gradient, feedback loops | S3 only |
| Sensible defaults, prevent errors, make errors recoverable | reel 24 only (no common law name) |

Reel 24 items folded into existing rows (mapping by the skill author): reduce choices (Hick), large targets (Fitts), familiar patterns and pattern consistency (Jakob), group related information (proximity), chunks (Miller), 400 ms (Doherty), highlight primary action (Von Restorff, visual hierarchy), key actions nearby (minimize target distance), essentials first (serial position), memorable ending (peak end), visible progress and completion feels closer (goal gradient), simplify complex interfaces (Occam, Tesler), connect related elements (uniform connectedness), reduce task completion time (Parkinson), reveal complexity gradually (progressive disclosure).

## Dedupe

- Postel's law is listed twice in S2 (items 16 and 17). Counted once.
- S2 gives 19 unique laws, S3 adds 7 not in S2 (26 named). Reel 24 adds 3 principles. Total 29.

## Transcription errors in the raw transcripts

- Reel 08: "Upgrade one, Shreem" is garbage for "Upgrade one" (no content lost).
- Reel 16: "sync the button into a recess track" reads as "sink"; "one icon never 2" reads as "never two"; the transcript ends in a looping garbage tail after "follow for more UX engineering", ignored.
- Reel 16: the caption says 48 px tall, the transcript opens with a 40 px problem button. Spec uses 44 minimum, aim 48 (stated rule in the transcript).
- Reel 16 transcript contrast figures (rim 4 to 1, label 14 to 1) are not used as specs. The stated rule, label above 4.5 and edge above 3, is used.
- No "Hunt Tech 7" style name error found in the sources used.

## Unsourced numbers

None in the spec sections. Law definitions carry no numbers except the 400 ms Doherty figure from reel 24.
