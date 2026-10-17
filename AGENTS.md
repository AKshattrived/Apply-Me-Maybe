# Agent Instructions

## Principles
- Follow YAGNI (You Aren't Gonna Need It) and KISS (Keep It Simple, Stupid).
- Implement only what is explicitly requested.
- Prefer the smallest working solution over extensibility or future-proofing.
- Do not overengineer or introduce unnecessary abstractions.

## Scope
- Do not create files, directories, dependencies, or scaffolding unless required for the current task.
- Do not implement planned features proactively.
- Do not modify unrelated files.
- Ask before making any decision not already resolved by the user's instructions.

## User decisions and approval
- The user makes all decisions. Do not choose on the user's behalf or treat assumptions as approval.
- Whenever a decision is needed, explain the choice and ask the user before taking dependent action.
- Proceed with the proposed action only after the user explicitly permits it. Silence or elapsed time is not permission.
- If permission is withheld or the user gives different instructions, follow those instructions and do not proceed with the original proposal.
- Carry out decisions the user has already explicitly authorized without asking for the same approval again.

## Execution
- Make minimal, targeted changes.
- Prefer existing tools and patterns over introducing new ones.
- Keep documentation concise and factual.
- Briefly summarize changes without lengthy explanations.

## Restrictions
- No speculative features, placeholder directories, or boilerplate.
- No unsolicited refactoring or improvements.
- Treat README plans as context, not implementation instructions.

## Git signing and sandbox access
- Preserve configured commit signing. Do not use `--no-gpg-sign`, `commit.gpgsign=false`, or change signing settings without explicit user approval.
- If signing fails, check SSH agent access. A sandbox denial does not mean the key is missing or needs unlocking; request approval to retry outside the sandbox when supported.
- For sandbox-related network failures, request approval to retry outside the sandbox before concluding GitHub is unreachable or asking the user to run commands locally.
- Do not conclude credentials are invalid from sandboxed authentication checks alone. Verify with network access before asking the user to authenticate again.
- If signing remains blocked, report the blocker and ask how to proceed instead of creating an unsigned commit. Do not rewrite published commits without explicit approval.

## Contribution workflow
- `main` is protected. Never commit or push directly to `main`, or bypass its ruleset.
- Before making changes, fetch the latest `origin/main` and create a branch from it named `feature/<github-username>/<feature-branch-name>`.
- Make the requested changes and signed commits on that feature branch, then push the branch and open a pull request targeting `main`.
- Include a concise description of the changes and validation in the pull request, and share its link with the user.
- The repository owner reviews and merges pull requests. Do not merge pull requests or enable auto-merge; wait for review and address requested changes on the same branch.
