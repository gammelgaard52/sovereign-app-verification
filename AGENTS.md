# Repository Agent Instructions

## Scope

- Follow the user's requested scope. Do not add related documentation, workflows,
  integrations, or infrastructure unless requested.
- Preserve existing files and resources. Do not modify unrelated repositories.
- Read applicable repository instructions before making changes.

## Branch workflow

- Create feature branches from `main`; keep unrelated work on separate branches.
- Do not work or commit directly on `main` without explicit instruction.
- Use `main` for integration and `release` for stable releases.
- Promote releases only from validated `main` to `release`.
- Obtain explicit instruction before promoting application or workflow changes
  to `main`.

## Validation

- Inspect Git status and diffs; include only changes within the requested scope.
- Run `git diff --check` and the applicable documented checks before committing.
- Report when no automated check exists. Fix failures before committing or pushing.
- After pushing, verify the workflow, commit, and job results with `gh run list`
  and `gh run view`. Explain when workflow filters mean no run is expected.
- Report software tests, deployments, attestation, and key release separately.
  Do not present sample results as live verification.

## Public content

- Publish only content explicitly approved for this public repository.
- Keep private source, executable packages, credentials, environment files,
  deployment identifiers, internal configuration, and raw logs outside it.
- Review the complete proposed content before publication, including filenames,
  commit messages, pull-request text, and workflow output.

## Security

- Use supported tools and standard libraries. Do not implement custom attestation
  verifiers, brokers, or replacement protocols; report unsupported integrations.
- Keep required verification fail-closed. A successful build or command does not
  by itself prove application integrity, hardware attestation, or key release.
- Never log plaintext uploads, access tokens, private keys, or released keys.
- Perform cloud operations only within an explicitly authorized scope, after
  verifying the active context and resource ownership.
- Do not purge resources or rotate keys without explicit instruction.

## Parallel work

- Delegate independent workstreams when useful; avoid delegation for trivial or
  strictly sequential tasks.
- Coordinate ownership, prevent conflicting edits, await relevant results, and
  validate findings before reporting completion.
