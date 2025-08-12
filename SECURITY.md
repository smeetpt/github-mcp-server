Thanks for helping make GitHub safe for everyone.

# Security

GitHub takes the security of our software products and services seriously, including all of the open source code repositories managed through our GitHub organizations, such as [GitHub](https://github.com/GitHub).

Even though [open source repositories are outside of the scope of our bug bounty program](https://bounty.github.com/index.html#scope) and therefore not eligible for bounty rewards, we will ensure that your finding gets passed along to the appropriate maintainers for remediation. 

## Reporting Security Issues

If you believe you have found a security vulnerability in any GitHub-owned repository, please report it to us through coordinated disclosure.

**Please do not report security vulnerabilities through public GitHub issues, discussions, or pull requests.**

Instead, please send an email to opensource-security[@]github.com.

Please include as much of the information listed below as you can to help us better understand and resolve the issue:

  * The type of issue (e.g., buffer overflow, SQL injection, or cross-site scripting)
  * Full paths of source file(s) related to the manifestation of the issue
  * The location of the affected source code (tag/branch/commit or direct URL)
  * Any special configuration required to reproduce the issue
  * Step-by-step instructions to reproduce the issue
  * Proof-of-concept or exploit code (if possible)
  * Impact of the issue, including how an attacker might exploit the issue

This information will help us triage your report more quickly.

## Policy

See [GitHub's Safe Harbor Policy](https://docs.github.com/en/site-policy/security-policies/github-bug-bounty-program-legal-safe-harbor#1-safe-harbor-terms)

## Supported Versions and Update Policy

- Unless otherwise stated in a repository’s README or SECURITY.md, GitHub maintains security fixes on a best-effort basis for the latest published release and any current container image tags. Older releases may not receive patches.
- Where applicable, supported distribution formats and architectures are documented in the repository (for example, downloadable binaries, source archives, or container images on GitHub Container Registry). In production, pin to a specific version tag or image digest.

## Security-Relevant Versions

For each GitHub-owned repository, consult the repository for authoritative version information:
- Toolchain and minimum versions: check language/tool manifests (for example, go.mod for Go, package.json for JavaScript, pyproject.toml for Python).
- Dependency versions: review the repository’s dependency manifest and any third-party license or SBOM files (for example, THIRD_PARTY_NOTICES or third-party-licenses.*).
- Container images (if published): use the repository’s Releases page or container registry page for available tags; in CI/production, prefer pinning by immutable digests.

Examples (adjust to the repository’s language/tooling):
- List the declared Go version: `grep '^go ' go.mod`
- List pinned Go modules: `go list -m -mod=mod all | sort`
- Inspect a container image: `docker pull <registry>/<image>:<tag>` and `docker inspect <registry>/<image>:<tag>`

## Model Providers Used by This Project

Unless explicitly documented in the repository, GitHub-owned open source projects do not embed or directly call proprietary AI/LLM model providers. Any AI/model usage typically occurs in downstream tools or hosts that integrate with the project and is outside the scope of the repository itself. If a project integrates with a model provider, the repository will document the provider(s), configuration, and data flow.

## Keeping This Document Up To Date

For maintainers, when cutting a new release:
- Review and update any Supported Versions statements in the repository.
- Confirm minimum toolchain versions from the project’s manifest.
- Review major versions of security-relevant dependencies.
- Verify published container image tags/digests (if applicable).
- Ensure links in this document remain valid.
