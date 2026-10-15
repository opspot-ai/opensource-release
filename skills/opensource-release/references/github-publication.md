# Optional GitHub publication reference

This is a GitHub-specific reference for an owner-authorized repository transition. Current owner instructions and platform behavior control. Do not run these steps merely because this document is installed.

## Prepare the reviewed candidate

Inspect the intended account and repository, current permissions, and any existing destination. Preserve authentication. Do not overwrite, rename, or repurpose a private original. If a separate staging repository is needed, create it only when authorized and keep its visibility private until the public transition is explicitly authorized.

Create a new Git repository from the final allowlisted candidate with one clean root commit. Use an approved public or noreply author identity. Do not copy `.git`, branches, tags, or private history. Capture the commit, tree, metadata, and exact file list; scan the intended history and have the reviewer inspect only the approved files. Recheck candidate hashes before pushing. A post-review source change requires review of the changed bytes.

Push only the reviewed branch to the intended new repository with an ordinary non-force push. Read back the remote branch and tree and compare them with the reviewed local commit. Verify that the original remains private and unchanged. A repository release does not imply tags, downloadable assets, or package-registry publication.

## Optional platform features

Hosted CI, private vulnerability reporting, packages, and release assets are outside a repository-only sanitation scope unless the owner separately requests them. Each needs applicable authority and current platform readback. Do not add workflows or activate services as an assumed release gate. If an enabled reporting channel is documented, verify the actual repository setting and accurately state access requirements; never submit a fabricated report.

## Public transition and readback

Only when current owner authority covers the exact public transition, change visibility on the new repository. For example, a GitHub CLI workflow may use:

```sh
gh repo edit OWNER/NEW --visibility public --accept-visibility-change-consequences
```

Read back repository visibility and the default branch revision. Do not treat a successful command exit as proof of the resulting state.

If publication is authorized, fetch the public repository from a fresh unauthenticated process and compare its files and revision with the reviewed manifest. This proves public source access and content identity only; it does not prove a clean install, product behavior, security, customer use, or support on another platform.

Keep failed attempts and exact outputs in private evidence. If a new disclosure or rights issue appears, stop the affected transition, preserve evidence, and report the concrete issue to the owner.
