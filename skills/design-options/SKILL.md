---
name: design-options
description: Trigger this if the user says 'design options' or 'mock it'.
metadata:
  credits: Grew out of the user's /mock skill.
---

# Design options

Show the UI change being discussed as one picture in the thread: options side by side, a before and after, or one picture of the end state. Text the user wrote with the trigger is part of the request.

1. **Learn the real UI.** Read the components the change touches and the theme tokens: colors, fonts, spacing, corners, real labels and data. Match the current code, not older mocks or prototypes.
2. **Choose the shape.**
   - **Options** when the user is choosing: three, or the number asked for. They differ on the axis being decided (where the thing lives, what it joins with, when it shows), not on wording. Mark one **recommended**, with the reason in one line under its title.
   - **Before and after** when the change is decided or the user asks for one. Exactly two panels, Before and After, with no options and no recommendation.
   - **One picture** when the user asks how something will look.

   When the change touches existing UI, the first panel is **Today**.
3. **Change only what was asked.** No new controls, links, or switches beyond the request, and no unrelated fixes. State each fact once per panel.
4. **Build one page.** One self-contained HTML document: `<meta charset="utf-8">`, the product's font stack and page background set on `body`, panels stacked, numbered, and named. Draw each panel inside the real UI around it. Use flexible widths that stack below 600px, so nothing is cut off at 390px.
5. **Check it.** Preview at the default width and at 390. Look at both: every label, button, and value visible, nothing clipped, no console errors. Never claim a width works without seeing it.
6. **Show it** with `html_render`. Outside T3 Code, write the page to a file and `open` it.

Reply in under 60 words: the recommendation and anything the user must decide. The picture carries the rest, so do not narrate the process.
