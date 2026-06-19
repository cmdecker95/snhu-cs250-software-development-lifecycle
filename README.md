# CS250 Software Development Lifecycle

This course uses a Java Swing travel agency project to exercise agile software development practices.

## [List View](./list-view)

Developed a Java Swing desktop app that renders a destination list with images, descriptions, and accessibility metadata.

### Lessons Learned

- Learned how to render rich list rows in `Java` Swing using `JList` and `ListCellRenderer`.
- Implemented Event Dispatch Thread-safe startup with `SwingUtilities.invokeLater`.
- Architected UI code into focused model, frame, and renderer components.
- Fixed usability issues by embedding accessible descriptions for assistive technology support.

## [Slide Show](./slide-show)

Built a Java Swing slideshow that cycles through five themed destination slides with synchronized images and descriptions driven by Previous/Next navigation.

### Lessons Learned

- Learned how to swap synchronized views in `Java` Swing using `CardLayout` to keep each slide's image and text in step.
- Implemented Event Dispatch Thread-safe startup with `EventQueue.invokeLater` so the UI builds on the correct thread.
- Architected slide content behind `getResizeIcon` and `getTextDescription` helpers so adding or re-theming slides stays data-driven instead of duplicating layout code.
- Improved accessibility by giving every image descriptive `alt` text and adjusting layout spacing and contrast for readability.
- Packaged the app into a runnable JAR (`javac` to `bin/`, copy resources, `jar cfe`) to produce a distributable build.

---

## Portfolio Reflection

### How do I interpret user needs and implement them into a program? How does creating "user stories" help with this?

I start by translating what a user is actually trying to accomplish into small, concrete outcomes rather than jumping straight to code. Writing user stories in the "as a [user], I want [goal] so that [reason]" format keeps me anchored to the underlying motivation instead of my assumptions about the UI. On the travel agency project, framing features as stories (for example, "as a traveler, I want each destination to show an image and description so that I can compare options at a glance") made it obvious what the list view had to render and why accessibility metadata mattered. Stories also gave me natural acceptance criteria, so I knew when a feature was genuinely done versus just visually present.

### How do I approach developing programs? What Agile processes do I hope to incorporate into my future development work?

I work in small, testable increments and try to keep the application runnable at every step rather than building everything before checking it. I break a feature into the smallest slice that delivers visible value, implement it, verify it, and then iterate. Going forward I want to keep using sprint planning to scope realistic chunks of work, maintain a prioritized backlog so the most valuable work surfaces first, and hold regular retrospectives to turn what went wrong into concrete process changes. The incremental rhythm I used to separate the model, frame, and renderer components is something I want to carry into larger projects, because it kept each change easy to reason about and easy to undo.

### What does it mean to be a good team member in software development?

To me a good team member is reliable, communicative, and considerate of the people who read and maintain the code after them. That means writing code and commit history that others can follow, surfacing blockers early instead of going quiet, and giving and receiving feedback without ego. It also means respecting shared process: showing up prepared for standups and reviews, keeping work visible on the board, and picking up unglamorous tasks when the team needs them. Ultimately the goal is to make the whole team more effective, not just to finish my own tickets.
