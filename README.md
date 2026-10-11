# BR Architects: Plain CSS vs Tailwind CSS

This repository has two versions of the same landing page:

- `plain-css/`: the original page built with HTML and a separate `style.css`
- `tailwind/`: the same page rebuilt with Tailwind CSS utility classes (Tailwind browser build)

## What changed in my workflow

**One file instead of two.** With plain CSS I wrote HTML in one file and
styles in another, and I had to switch between them and invent class names
like `.team-card` and `.project-grid`. With Tailwind I style directly in the
HTML, so I stay in one place and I no longer think about naming.

**Responsive design was easier to read.** In plain CSS I wrote separate
`@media` blocks at the bottom of the file. In Tailwind I write the change next
to the element, for example `grid-cols-1 sm:grid-cols-2 lg:grid-cols-4`, and I
can see how one element changes at each screen size.

**Hover and focus states were quicker.** I added `hover:bg-gray-500` and
`focus-visible:ring-2` directly on links and buttons, without writing new CSS rules.

**What was harder.** The HTML became long and harder to read because each
element has many classes. I also had to learn the utility names, and when a
tag was broken (a missing closing tag) the layout fell apart and was hard to find.
Tailwind also resets headings, so they looked like normal text until I added
size and weight myself.

**What I would do next time.** For styles that repeat a lot, such as the cards
and buttons, I would use `@apply` to create reusable classes so the HTML stays shorter.