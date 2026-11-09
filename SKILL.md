---
name: hci
description: Apply source-backed human-computer interaction guidance when designing, implementing, reviewing, or evaluating human-facing interfaces, interaction flows, information architecture, visualisations, AI behaviour, or usability research. Include backend changes when they affect observable interaction, waiting, errors, or user control. Skip purely internal refactors, numerical work, routine writing, and trivial edits without a meaningful user-experience decision, unless explicitly requested. Select relevant concepts and briefly report their application at the end.
---

# HCI: practical human-centred design

Help people understand what they can do, act comfortably, and recognise what happened. Use the concepts below as design lenses, not a universal checklist. Preserve the user's objective, scope, existing design language, and execution permissions.

## When to apply

Use this skill when the task makes a meaningful decision about how people perceive, understand, operate, or evaluate a system. Examples include websites and apps, maps and dashboards, XR and physical interfaces, developer-facing tools, forms and onboarding, assistant tools and conversations, user-facing loading/error behaviour, and interaction-study design.

The deciding factor is an interaction or usability decision, not simply that a human is mentioned or will receive the output. Ordinary email drafting, translation, spelling changes, isolated calculations, and invisible infrastructure work normally do not need this skill. Audience-facing instructions or documents can benefit when comprehension, navigation, or task completion is a central part of the request. Explicit invocation as `$hci` is always welcome; it need not produce a redesign when none is useful.

## How to use the guidance

- Identify the intended people, their goal, their context/device, and the main action or decision. Infer what is reasonably clear; ask only when an unanswered question materially affects the design.
- Choose the concepts that help this task. A small improvement may need one concept; a complex workflow may need several. No minimum concept count, fixed redesign process, or compulsory use of every row is intended.
- Connect each choice to an observable benefit or tradeoff. For example, putting frequently paired controls together can reduce navigation, while moving infrequent options into a labelled disclosure can preserve working space. Avoid hiding important controls merely to reduce their count.
- Work within scope. Improve the relevant flow without turning every feature request into a full redesign, a research study, new dependencies, or extra approval steps. Use existing components and conventions when they serve the task.
- Validate proportionally: review a representative user task, relevant states, keyboard/focus behaviour, and applicable device layouts. Use a small walkthrough for a minor change; use broader usability or accessibility evaluation when warranted or requested. Distinguish automated checks, expert judgement, and evidence from actual participants.

## Concept reference

This is a practical starting set, not an exhaustive catalogue. The simple meanings are paraphrases; follow the linked source when a concept's scope matters.

| Concept | Simple meaning | Source |
| --- | --- | --- |
| Task-based mental models | Use the user's goals and familiar language to organise actions, rather than exposing the implementation's structure. | [Nielsen: match between system and real world](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Proximity | Put related controls and their feedback near each other so their relationship is easier to see. | [NN/g: Gestalt principles](https://www.nngroup.com/articles/principles-visual-design/) |
| Common region | A shared container can communicate a group; unnecessary boxes can also add clutter. | [NN/g: common region](https://www.nngroup.com/articles/common-region/) |
| Visual hierarchy | Use spacing, size, placement, and contrast to make important information easier to find. | [NN/g: visual hierarchy](https://www.nngroup.com/articles/principles-visual-design/) |
| Progressive disclosure | Keep frequent or essential choices accessible; reveal specialised options through clearly labelled secondary controls. | [Nielsen: progressive disclosure](https://www.nngroup.com/articles/progressive-disclosure/) |
| Recognition rather than recall | Show meaningful labels, choices, and current state so people need to remember less. | [Nielsen: recognition rather than recall](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Consistency and standards | Familiar labels and behaviours help people reuse what they already know. | [Nielsen: consistency and standards](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Visibility of system status | Give timely, understandable feedback about progress, results, readiness, and failures. | [Nielsen: visibility of system status](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| User control and mode awareness | Make the current operating state clear; support leaving, cancelling, or undoing actions where appropriate. | [Nielsen: user control and freedom](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Error prevention and recovery | Reduce likely mistakes and provide useful ways to diagnose and recover when they occur. | [Nielsen: error prevention and recovery](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Frequency-based access | Keep frequent actions efficient while allowing people with different experience levels to work comfortably. | [Nielsen: flexibility and efficiency](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Pointing effort: Fitts's law | Larger or nearer targets generally take less time to select in pointing tasks. | [MacKenzie, 1992](https://www.yorku.ca/mack/hci1992.html) |
| Choice effort: Hick's law | Selecting among uncertain alternatives takes time; understandable choices and grouping can help. | [Hick, 1952](https://doi.org/10.1080/17470215208416600) |
| Overview and details on demand | Offer useful context, then support zooming, filtering, and inspecting relevant details. | [Shneiderman, 1996](https://www.cs.umd.edu/~ben/papers/Shneiderman1996eyes.pdf) |
| Direct manipulation and coordinated views | Let people act on visible objects and see related information respond consistently. | [Shneiderman, 1996](https://www.cs.umd.edu/~ben/papers/Shneiderman1996eyes.pdf) |
| Inspectable animation | Motion can show change; precise comparisons may also need pause, step, and stable views. | [Robertson et al., 2008](https://www.microsoft.com/en-us/research/publication/effectiveness-of-animation-in-trend-visualization/) |
| Accessible operation | Consider keyboard input, focus, alternatives to gestures, motion preferences, and comfortable target sizes. | [W3C: WCAG 2.2](https://www.w3.org/TR/WCAG22/) |
| Legibility and redundant encoding | Use readable content and convey meaning through labels, patterns, or shape as well as colour. | [W3C: use of colour](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html) and [contrast](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) |
| Understandable and correctable AI | Explain relevant capabilities and behaviour; make correction, dismissal, and useful explanations accessible. | [Amershi et al., CHI 2019](https://www.microsoft.com/en-us/research/publication/guidelines-for-human-ai-interaction/) |
| Mixed initiative | Combine human direction and useful automation while considering uncertainty and interruption costs. | [Horvitz, CHI 1999](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/11/chi99horvitz.pdf) |
| Task-based evaluation | Observe representative tasks to find problems; a plausible rationale alone does not establish usability. | [NN/g: usability testing](https://www.nngroup.com/articles/usability-testing-101/) |

## Exercise judgement

- Heuristics guide a choice; they do not prove it will work for this audience. Distinguish a recommendation from a measured outcome. Research involving charts, desktop pointing, or simple choices may not transfer directly to maps, XR, or complex missions.
- Fitts's law does not prescribe one universal button size. Hick's law does not mean "always remove choices" or "always nest menus." There is no blanket maximum number of buttons, tabs, disclosure levels, or concepts. Consider familiarity, search effort, reach, safety, accessibility, and the task together.
- A clean screen can still be difficult to use if important actions are hidden. Prefer a useful hierarchy over minimalism for its own sake. Grouping and nesting are options, not goals.
- Keep real state and user-facing feedback consistent. Do not present pending, stale, estimated, decorative, or simulated information as an authoritative current result. For AI, preserve the distinction between suggestions, executed actions, and verified outcomes.
- Flexible design guidance does not make applicable accessibility, ethical, contractual, or domain requirements optional. Conversely, citing a guideline is not evidence that compliance was tested.
- Reuse the sources here for ordinary design reasoning. Browse when a task needs current standards, exact quotations, new research, or claims beyond these sources; do not turn every small edit into a literature review. Add a new concept when it is genuinely useful and can be sourced.

## End-of-workflow note

At the end of a relevant workflow, briefly name the concepts actually used and connect them to concrete changes or decisions. Usually one sentence or a few short bullets is enough. Do not print the whole reference table or list concepts that had no effect.

Example: **HCI applied:** Proximity - grouped paired controls; progressive disclosure - moved rarely used settings behind a labelled expansion; system status - added clear loading and completion feedback.

For a design discussion without implementation, use **HCI recommended** and describe proposed choices. For a review, identify the concepts used to assess the interface without claiming changes were made. Report validation separately and truthfully; do not imply user testing took place when only code or an expert walkthrough was checked. If no meaningful HCI change was needed after explicit invocation, say so briefly rather than inventing one.

Respect a user-requested exact output format or stricter brevity limit. When several skills apply, combine their application notes with the normal outcome summary rather than adding separate checklists or appendices.
