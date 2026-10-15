---
name: opensource-release
description: "Prepare sanitized open-source repositories from existing projects under explicit owner authority. Supports sanitation-only releases and optional product-readiness work."
---

# Open-source Release

Use this skill to prepare a useful public repository from existing work while preserving the private original and publishing only the reviewed release surface. This is process guidance: it does not confer rights, authorize external changes, create a team, run checks, or publish by itself. Follow the current owner instruction and the target project's rules.

## Choose the requested release scope

When the owner accepts existing code with known gaps, use **sanitation-only**. Preserve the original and dirty work, create a separate candidate without private history, inspect every intended file, run a redacted secret scan, resolve concrete rights and attribution questions, write a concise truthful README, and obtain independent hash-bound sanitation review. Bugs, incomplete features, old dependencies, and unrun behavior checks are limitations to report; they are not sanitation failures by themselves. Do not add feature work, dependency upgrades, demonstrations, hosted CI, broad runtime matrices, or security-hardening gates to this scope.

A fuller product-readiness release is optional and must be requested. Use the product's existing acceptance guidance to define any additional clean-install, runtime, behavior, or security checks; agree on new acceptance criteria with the owner when that guidance is absent. Keep product readiness evidence separate from sanitation findings. This skill does not depend on a separate readiness package.

Preserve public package names, commands, configuration keys, and API fields. Remove concrete private values without renaming interfaces or turning sanitation into a migration.

## Establish scope and authority

Read the current project instructions and only the source, receipts, and decisions relevant to the named project. Record the exact projects, source revision and dirty state, candidate path, allowed files, selected license, rights confirmation, intended destination, chosen mode, owner, and required checks. Authorization for one named project does not extend to another. Preserve existing authentication and settings; do not infer permission to change them.

Keep the following decisions explicit and distinct: rights to distribute the source, delegation, license, candidate preparation, any external staging, and public visibility. A template field or successful check is not approval. Respect a newer hold or restriction over an earlier instruction.

The owner may choose either supported mode:

- `prepare-private`: complete the requested local preparation and review, then stop before a public visibility change.
- `publish-approved`: continue to the public transition only when current owner authority explicitly covers that exact repository and action.

Neither mode is a default. Hosted CI, security reporting, packages, release assets, and other platform features are separate optional scopes; they are not implied by a repository release.

Use [the batch input template](assets/batch-template.json) and [the project assignment template](assets/project-job.md) only as records. Replace their placeholders with verified project facts; never manufacture authorization from them.

## Assign and preserve the work

Use the existing accountable owners and coordination path. If delegation is authorized and useful, assign one lead, one snapshot writer, and an independent reviewer with disjoint responsibilities. The reviewer inspects and reports; the reviewer does not fix source. Name a single publisher for the external repository change. Do not create workers, change model settings, spend money, contact others, or bypass an ownership or permission boundary because this skill describes a workflow.

Before editing, record a file inventory and cryptographic hashes for the source and preserved copy. Preserve original files, history, references, remotes, and unfinished work. Create a fresh candidate containing only an explicit allowlist; never copy source `.git` data, branches, tags, or private history. An exclusion from the candidate is not authority to delete the original.

Remove concrete private identifiers, personal contacts, absolute workstation paths, credentials, customer data, internal operations, and employee records from retained files. Keep required upstream notices and attribution. Classify scan matches individually: common operating-system paths, clearly synthetic examples, public package names, and required attribution are not private merely because a scanner matched them.

Create the selected license, a concise README, and any supporting reference or template needed by this skill. The [README template](assets/public-readme.md) and [security-policy template](assets/security-policy.md) contain authoring guidance; fill them with verified facts before use. A reporting policy is optional and must describe a channel only after it is enabled and verified. Do not invent a contact, response time, or account authority. The MIT license text in this repository is based on the standard text at <https://opensource.org/license/mit>.

## Verify the exact candidate

For sanitation-only work, review the exact payload files, intended Git history if one is part of the authorized deliverable, metadata, license notices, links, and planned repository metadata. Run a redacted secret scan and manually inspect every intended file. Preserve exact commands, tool versions, exits, redacted logs, scan findings, and the reason for each classified match in private evidence. Do not publish evidence logs or use broad scanner suppressions.

Freeze a complete file manifest with relative paths, hashes, sizes, and executable bits. Ensure the final-byte scan and manual review refer to those same bytes. The independent reviewer compares the candidate with the preserved original and binds the verdict to the manifest. The writer's checks are not an independent verdict. Sanitation review does not prove runtime behavior, security, usability, host compatibility, or product readiness.

If fuller readiness was requested, add only the checks in the agreed product acceptance scope and report their evidence separately. Do not reuse another product's runtime matrix or acceptance claims.

## Publish only with current authority

Use [the GitHub publication reference](references/github-publication.md) for optional GitHub-specific mechanics. Before any external mutation, recheck the exact owner authority, rights, destination, reviewed manifest, candidate hashes, and unresolved findings. Publish only the new reviewed history to the intended destination; never force-push, rename, or repurpose the private original. Do not treat a reviewer verdict as publication authority.

Any hosted CI, vulnerability-reporting setup, package upload, or release asset is optional and requires its own applicable authority and readback. Do not report an optional platform feature as enabled without checking it. If the repository is published, verify public access and the intended content from a fresh unauthenticated fetch. Keep publication separate from customer use or runtime acceptance.

## Close with evidence

Record the candidate path, exact manifest and its hash, source deltas, files excluded or added, checks and logs, manual inspection inventory, classified findings, limitations, and any pending owner action. Preserve failed attempts. Report the real state as prepared, reviewed, published, or blocked; a finished candidate is not a published release.
