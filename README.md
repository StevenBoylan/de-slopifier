# AI De-Slopifier Test Suite

These tests are behavioural checks for the AI De-Slopifier specification.

They are not intended to have one exact "correct" output. Instead, each test describes the behaviour expected from an implementation and the behaviours that should be treated as failures.

## How to use the tests

For each test:

1. Give the implementation the content under **Input**.
2. Do not provide the expected behaviour or failure conditions to the implementation.
3. Observe what it does before writing or rewriting.
4. Compare its behaviour with **Expected behaviour** and **Failure conditions**.
5. Record anything surprising. A useful failure may indicate that the core specification needs to change.

The same tests can be run against different implementations (for example Claude, ChatGPT and Gemini) to compare whether they follow the same editorial methodology.

## Tests

- `01-generic-ai-newsletter.md` — Can it remove generic AI-style writing without replacing it with different slop?
- `02-rough-human-notes.md` — Can it develop messy but interesting human material without professionalising away the author's voice?
- `03-good-writing.md` — Can it recognise when writing is already good and avoid unnecessary intervention?
- `04-missing-context.md` — Does it ask for an important missing piece rather than inventing it?
- `05-narrative-trap.md` — Does the Narrative Checkpoint catch a plausible but incorrect interpretation before drafting?

## What these tests are testing

Across the suite, pay particular attention to whether the implementation:

- separates understanding from writing;
- asks only questions that are actually needed;
- makes assumptions on the author's behalf;
- performs the Narrative Checkpoint before substantial drafting or rewriting;
- preserves useful specificity and voice;
- removes repetition, abstraction and manufactured significance;
- avoids formulaic rhetorical substitutions;
- knows when not to edit;
- audits its own revised output.

These tests should evolve as real-world failures are discovered.
