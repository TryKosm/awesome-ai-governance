# Contributing

This list aims to stay short, opinionated, and useful. Please follow these rules before opening a PR.

## Quality bar

An entry should:

- Be an actively maintained project (last meaningful commit within 12 months) **or** a foundational paper / standard.
- Have a clear connection to **governance, policy, audit, observability, orchestration, agents, or LLM safety**.
- Not duplicate an existing entry. If a project is similar to an existing entry, explain in the PR why both should be listed.

An entry should not:

- Be primarily a marketing page for a closed-source product.
- Be a thin wrapper around another listed project.
- Use vague descriptions like "AI platform" or "the future of work."

## Format

Each entry follows this exact format:

```
- [owner/repo](https://github.com/owner/repo) — One-line description focused on what it does and why it belongs.
```

Keep descriptions under ~150 characters. Avoid superlatives. State capabilities, not feelings.

## Sections

Add the entry to the most relevant section. If a project genuinely spans two sections, list it once in the most relevant one and reference it from the other only if necessary.

If you believe a new section is needed, open an issue first to discuss before sending a PR.

## Order within a section

Within a section, ordering loosely follows: foundational projects first, then breadth, then niche tooling. Pure-alphabetical is acceptable when no obvious priority exists.

## PR checklist

- [ ] Entry uses the format above.
- [ ] Project meets the quality bar.
- [ ] No duplicate of an existing entry.
- [ ] Description is one line, ≤150 characters, factual.
- [ ] Lint check: `markdownlint README.md` passes (if you have it installed).

## License

By contributing you agree that your contributions will be licensed under the same MIT terms as the rest of the project.
