# Cartoon Motion

A reusable agent skill for turning 2D cartoon characters into expressive screen assets and working animation. It works with Codex and Claude Code, using the art tools and runtime available in your project.

Start from a character reference, refine useful poses and expressions, prepare genuine separate parts when needed, and choose a practical path to tested animation. The skill distinguishes a pose sheet, separable artwork, a working rig and animation verified in an app, so the handoff says what is actually ready.

## Install locally

Clone the repository somewhere you intend to keep it:

```sh
git clone https://github.com/Griff2325/cartoon-motion.git
cd cartoon-motion
```

For **Codex**, link the skill into the personal skills directory:

```sh
mkdir -p "$HOME/.agents/skills"
ln -s "$PWD/skills/cartoon-motion" "$HOME/.agents/skills/cartoon-motion"
```

For **Claude Code**, link the same source into its personal skills directory:

```sh
mkdir -p "$HOME/.claude/skills"
ln -s "$PWD/skills/cartoon-motion" "$HOME/.claude/skills/cartoon-motion"
```

These shell commands are for macOS/Linux. If a destination already exists, inspect it before replacing it. You can copy the complete `skills/cartoon-motion` folder instead of linking it; copied installations need to be updated separately. For project-scoped installation, copy it into the project's `.agents/skills/` for Codex or `.claude/skills/` for Claude Code.

Start a new local session after installation. Invoke `$cartoon-motion` in Codex or `/cartoon-motion` in Claude Code, or describe a matching task and let the agent select it. Local installation does not install cloud/account skills.

Installation locations and invocation follow the official [Codex skills documentation](https://learn.chatgpt.com/docs/build-skills) and [Claude Code skills documentation](https://code.claude.com/docs/en/skills).

## Use

Give the agent the reference, target screen size/platform, required actions, and desired finish line. For example:

> Use cartoon-motion with this character reference. Make three readable success, thinking and disappointed reactions for a 64-point character in an iOS app. Start with complete pose sprites and show them on the actual background. Keep the same proportions and line style.

> Use cartoon-motion to prepare this existing character for a small head turn, blink and wave. Use our existing web animation stack. Deliver clean separate parts, measured pivots and layer order, plus an assembled motion preview. Avoid a new runtime unless the current stack cannot do it.

> Use cartoon-motion to integrate these approved layered assets into the app's existing state machine. Test repeated and interrupted reactions, return to rest, clipping and reduced motion. Report which checks ran in the app.

The skill does not include an image generator, art editor, rigging application or runtime. It uses tools actually available to the agent; Claude Code is not assumed to have Codex's image-generation tools. Art generation, paid services, editor licenses and runtime dependencies are selected for the task, not installed by this repository.

## Contents

- [`SKILL.md`](skills/cartoon-motion/SKILL.md): the workflow and acceptance checks.
- [`rig-and-runtime.md`](skills/cartoon-motion/references/rig-and-runtime.md): conditional guidance for parts, authoring tools and runtime integration.
- [`agents/openai.yaml`](skills/cartoon-motion/agents/openai.yaml): optional Codex display metadata; the core instructions remain portable.

No sample character art or third-party artwork is bundled. The [MIT license](LICENSE) covers this repository's instructions and metadata; separately supplied or generated assets have their own provenance and terms.
