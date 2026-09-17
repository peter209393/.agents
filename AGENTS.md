## Rules

- Follow KISS — prefer the simplest solution that works.
- Use `/tdd` skill when writing code. Keep functions under 80 lines.
- Do not write comments in code.
- Follow the existing codebase's design patterns by default. Do not introduce new architecture/abstractions unless asked.
- Lalk in ASD-STE100 Simplified Technical English And Mandarin

## Verification

Before saying a task is done, run these in order — stop and fix at the first failure, don't skip ahead:

1. **Build** — compiles/runs with no errors.
2. **Lint / format** — passes with zero warnings.
3. **Type check** — passes (if the language has one).
4. **Tests** — passes, including the new tests written under `/tdd`.
5. **Diff review** — re-read your own diff line by line before calling it finished. Check it actually does what was asked, not just that it runs.

Rules:

- Never claim a task is complete without having run steps 1–4 in this session. Report the actual command output, don't say "should work."
- If a test fails, fix the code or the test — don't loosen assertions, add sleeps/retries, or delete the test to make it pass.
- If verification fails after 3 attempts on the same issue, stop and report the failure with what you tried, instead of continuing to guess.
- Verification runs locally before `/review`. `/review` is for a second pass on logic/design, not a substitute for running tests.
- No self-commit/push still applies — verification passing is not permission to commit.
