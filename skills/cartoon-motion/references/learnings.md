# Learnings

General lessons from real character work, kept so the next agent starts ahead. Read this before starting a new character or motion task, and add to it at the end of one (see "Record what you learned" in `SKILL.md`).

Only general lessons belong here. Nothing about a specific project: no character names, no project file paths or commands, no record of what one user approved. Those go in that project's own handoff file.

## How to add a learning

Add an entry under the closest heading, newest last, in this shape:

```md
### <The lesson in one line>
<What happened, in general terms, and what to do instead.>
**Applies when:** <the situations where this matters>
```

Before adding, check whether an existing entry already says it; if so, sharpen that entry instead of adding a near-duplicate. If an entry turns out to be wrong, fix or remove it. Keep each entry short; move long technique into the relevant reference file and link it.

## Design

### Users reject "code-drawn" characters fast
Characters built from easy-to-compute shapes (ellipses, one-width strokes, uniform black outlines, flat fills) read as icons or clip art, and users describe them as "vibe-coded" or "a napkin sketch". Adding props or swapping styles doesn't fix it. What fixed it was finish: painted shading, tinted inner lines, tapered limbs and individually drawn texture. See `code-drawn-svg.md`.
**Applies when:** drawing a character in SVG, canvas or another code medium.

### Cute is not a safe default
When asked to "explore looks", cute toy proportions (dot eyes, blush, stubby limbs) got rejected as worse than the original. Explore along the user's named references instead.
**Applies when:** exploring design directions without a style reference.

### References are usually about style, not props
When a user names a reference character, they usually want its art style, attitude or acting. Copying its accessories (a hat, a cane, an eyepiece) added noise and was rejected.
**Applies when:** a user names reference characters or shows.

### Going back is a valid answer
After several rounds that moved away from an earlier direction, the user picked the earlier direction and asked for it polished. Keep earlier rounds renderable so you can return to one cheaply.
**Applies when:** a user rejects several rounds in a row.

## Construction

### Check hands and limb joints visually on every pose
Glove thumbs on the wrong side and limbs that visibly start at the wrong place (near a mouth, not touching the body) were the most repeated complaints. Math alone didn't catch them; looking at each pose did. Start limbs inside the body, draw them behind it, and parametrise the thumb side.
**Applies when:** any character with articulated limbs or hands.

## Motion and review

### Prove the design in motion before integrating
One short animated moment with sound got approval faster than further stills, and exposed construction problems the stills hid.
**Applies when:** a design is approved as a still but hasn't moved yet.

### Characters should host, not react like a laugh track
Users noticed when characters only popped in to react to events. Giving them a role in the flow (introducing rounds, driving transitions) read as real animation.
**Applies when:** placing a mascot in an app or game.

## Handoff

### Keep project state out of the skill
Project-specific notes (approved looks, rejections, paths, commands) belong in a handoff file in that project's repository. This skill is shared across projects and public.
**Applies when:** finishing any session with work another agent may continue.
