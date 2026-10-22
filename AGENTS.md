# Organization profile (public)

The public profile of the `MaxMofid` organization: `profile/README.md` is shown to everyone on https://github.com/MaxMofid. The members-only profile, with the Blueprint, is `MaxMofid/.github-private`. Git rules: the repository `MaxMofid/engineering`, `git-delivery.md`.

## Working here

- Cards are issues of `MaxMofid/.github-private` on the roadmap project of the work (https://github.com/orgs/MaxMofid/projects).
- Branch `<type>/<short-description>`, Conventional Commits in English, a PR that closes its card (or refs it when it only advances it), squash merge (`git-delivery.md` §1, §3, §4).
- Review: an independent review approves the exact head commit, recorded as a PR comment beginning with "Approve:", before merge (`testing.md` §12). The secret scan (`.github/workflows/gitleaks.yml`) is a required check.
- Hooks: run `lefthook install` once per clone (`lefthook` and `gitleaks` on PATH); they scan staged changes before a commit and unpushed commits before a push. CI is the authority; a false positive goes into `.gitleaksignore` by its fingerprint, with the reason.
