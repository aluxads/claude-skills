---
name: ux-laws
description: Apply named UX laws and measured interface specs to any screen, audit or build. Trigger /ux-laws, "ux laws", "ux audit", or before shipping a new screen, form, login, button or mobile layout.
metadata:
  trigger: /ux-laws, ux laws, ux audit, screen review, button spec, login form, mobile layout
---

# UX laws (named laws plus measured specs, one findings table)

Rule: every finding names the law or spec it breaks. No law invented, no number without a source row in `references/sources.md`.

## When to use

- Audit an existing screen, component or flow.
- Build a new screen: choose the governing laws first, then apply the numbers.
- Review a design or a pull request that touches buttons, forms, tables or fixed bars.
- Skip for copy, SEO or brand questions. This skill covers interaction and layout only.

## Run order

### Audit an existing screen

1. List every element on the screen: headings, fields, buttons, links, icons, table rows, bars, messages.
2. Test each element against The laws table (screen type column tells which rows matter most) and the Numeric specs.
3. Write one findings row per break: path, element, law or spec broken, fix.
4. Apply the fixes, re test the changed elements, then print the score line (Output format).

### Build a new screen

1. Name the screen type: form, login, checkout, dashboard, list, navigation, onboarding, content, mobile.
1b. Check a screen library of tested flows from live apps (for example Mobbin or Screen Design) for that screen type before designing from scratch: those screens were A/B tested on large user bases. Adapt the winning pattern to the design tokens, record the source in the brief, never on the page.
2. Pick the laws that govern that type (screen type column). Write the picks down before any code.
3. Apply the Numeric specs for every button, field and mobile rule on the screen.
4. Run the audit steps on the result before calling it done.

## The laws

29 rows: 26 named laws and effects plus 3 principles that have no common name. Screen types: all, form, login, checkout, dashboard, list, nav, onboarding, content, mobile.

| Law | Meaning | Do | Bites most on |
|---|---|---|---|
| Hick's law | More choices, slower decision. | Cut options per screen, split long menus into steps. | nav, form, onboarding |
| Fitts's law | Time to hit a target depends on distance and size. | Make targets large, put the main one in easy reach. | mobile, form, checkout |
| Minimize target distance | Related actions far apart cost time and errors. | Keep key actions next to the content they act on. | list, dashboard, form |
| Jakob's law | Users expect your screen to work like others they know. | Use familiar patterns and keep your own patterns consistent. | nav, login, checkout |
| Law of proximity | Things placed close read as one group. | Group related items with space, separate groups with more space. | form, dashboard, content |
| Law of similarity | Things that look alike read as related. | Style same function items the same, different function differently. | nav, list, dashboard |
| Common region | Items inside one boundary read as a group. | Put related items in one card or panel. | dashboard, form, list |
| Uniform connectedness | Items joined by a line or shape read as related. | Link related elements visually with rules, lines or shared fills. | form, onboarding, dashboard |
| Law of Pragnanz | The eye reads the simplest shape it can. | Use clean, simple forms, avoid ambiguous layouts. | all |
| Visual hierarchy | Size, weight and colour set reading order. | One clear first read, then second, then third. | all |
| Von Restorff effect | The item that differs is the one remembered. | Make the primary action the one thing that stands out. | form, checkout, dashboard |
| Miller's law | Working memory holds a short list. | Break content into chunks, keep lists short. | list, content, form |
| Doherty threshold | Productivity rises when the system answers fast. | Answer every interaction inside 400 milliseconds, show progress if not. | all |
| Feedback loops | Every action needs a visible answer. | Show a state change for each tap: pressed, loading, done. | form, checkout, mobile |
| Serial position effect | First and last items are remembered best. | Put essentials first and last, weak items in the middle. | nav, list, content |
| Peak end rule | People judge a flow by its high point and its end. | End the flow with a clear, pleasant finish. | checkout, onboarding |
| Zeigarnik effect | Unfinished tasks stay in mind. | Show what is left and let people resume. | onboarding, form |
| Goal gradient | Effort rises as the finish gets closer. | Show visible progress and make completion feel near. | onboarding, checkout, form |
| Tesler's law | Complexity cannot be removed, only moved. | Absorb the hard part in the system, simplify the interface. | form, onboarding, dashboard |
| Postel's law | Be liberal in what you accept, strict in what you send. | Accept messy input formats, output clean consistent results. | form, checkout, login |
| Parkinson's law | Work expands to fill the time given. | Cut steps and fields to shorten task completion time. | form, checkout, onboarding |
| Occam's razor | Prefer the simplest solution that works. | Remove elements that do not earn their place. | all |
| Pareto principle | A minority of features serves most of the use. | Design the common path first, tuck rare options away. | dashboard, nav |
| Aesthetic usability effect | Pleasant screens feel easier to use. | Polish spacing, alignment and type, users forgive more. | all |
| Progressive disclosure | Show advanced detail only when asked. | Reveal complexity gradually, defaults first. | form, dashboard, onboarding |
| Recognition over recall | Seeing is easier than remembering. | Show options and labels, never make users remember them. | nav, form, list |
| Sensible defaults | Most users keep what is pre set. | Pre fill the likely answer, let users change it. | form, onboarding, checkout |
| Prevent errors, make them recoverable | Errors cost trust and time. | Block bad input early, offer undo and clear fix messages. | form, checkout, login |

Count check: Hick, Fitts, Minimize target distance, Jakob, proximity, similarity, common region, uniform connectedness, Pragnanz, visual hierarchy, Von Restorff, Miller, Doherty, feedback loops, serial position, peak end, Zeigarnik, goal gradient, Tesler, Postel, Parkinson, Occam, Pareto, aesthetic usability, progressive disclosure, recognition over recall = 26 named. Sensible defaults, prevent errors, make errors recoverable = 3 principles. The last row merges two principles, so rows and laws differ by one.

## Numeric specs

### Button (primary)

- Height: 44 pixel minimum, aim 48. Side padding 24 pixels.
- Label: 17 pixel semibold, sentence case, verb plus object ("Add to cart", never "OK" or "Submit").
- Contrast: label above 4.5 to 1, edge above 3 to 1. A flat grey fill at 1.6 to 1 fails.
- Radius: pill = height divided by 2 (24 at 48 pixels).
- Icon: one only, 20 pixels wide, 10 pixels from the label.
- Depth: light from above, shadow falls down (8 pixels down, 24 blur).
- Hover: rim light in 200 milliseconds. Press: sinks 1 pixel.
- Feedback in 100 milliseconds, done in 300. Sequence: spinner, then check.

### Form and login

- One primary action, everything else is a link.
- 8 pixel grid. Fields 56 pixels tall, 16 pixels between fields, 32 pixels before the button. 40 pixel fields fail (hard to tap).
- Real label above each field. Placeholder is an example, never the name.
- One accent colour, kept for the button and links.
- Focus ring 2 pixels, always visible, fades in within 150 milliseconds.
- Three text tiers: title, subtitle, hint.
- Radius: 24 on the card, 12 on fields and buttons. Shadow falls down.

### Mobile

- Under 640 pixels, table rows become cards.
- Amounts stay on one line, shrink big figures on phones.
- Input text 16 pixels minimum, or Safari zooms on tap. Set the keyboard type per field.
- 44 pixel targets on touch only, mouse keeps the dense layout.
- Fixed bottom bars: pad with the safe area and leave room under the content.

### Timing

- Every interaction answers inside 400 milliseconds (Doherty threshold).
- Tap feedback 100 milliseconds, completion 300, focus ring 150, hover 200.

## Output format

Findings table, one row per break:

| Path | Element | Law or spec broken | Fix |
|---|---|---|---|

Last line, one score: `elements checked: N, broken: N, fixed: N`.

## Do not

- Invent a law. Only rows in The laws table count.
- Quote a number without a row in `references/sources.md`.
- Apply the 44 pixel rule to mouse layouts.
- Report a finding without the law or spec name and a concrete fix.
- Hunt for every law on every screen: use the screen type column and test the governing ones.

Sources and transcription notes: `references/sources.md`.
