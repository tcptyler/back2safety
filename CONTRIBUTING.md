# Contributing to back2safety

Thanks for helping make back2safety better. This guide explains how to contribute and what we expect.

## Ways to contribute

- **Report bugs:** open an issue describing what happened and what you expected.
- **Report missed or wrong verdicts:** if back2safety called a dangerous email safe, or a safe email dangerous, open an issue with a redacted sample (see [Samples and personal data](#samples-and-personal-data)).
- **Suggest features:** open an issue to discuss the idea first.
- **Improve detection:** new checks, better rules, new free threat-intelligence sources.
- **Improve docs:** fixes and clarifications are always welcome.

For anything larger than a small fix, **open an issue first** so we can agree on the approach before you spend time on it.

## Contributor License Agreement (required)

Before we can accept your first pull request, you must accept the [back2safety Contributor License Agreement (CLA)](CLA.md).

- It is a one-time step. When you open your first pull request, a bot will comment with a link. Sign in with GitHub and click **I agree**.
- In short, it confirms that your contribution is your own work and gives Blake Business Solutions, LLC the right to use it in back2safety, including in paid editions. You keep ownership of your contribution.
- Pull requests cannot be merged until the CLA is accepted.

## How changes are reviewed

1. Fork the repository and create a branch for your change.
2. Open a pull request against `main` with a clear description of what it changes and why.
3. A maintainer will review it. We may ask for changes.
4. Once approved and the CLA check passes, a maintainer merges it.

All changes go through review, including those from maintainers. Not every pull request will be accepted, and review times vary since this is a community project.

## Rules for contributions

### Licensing of third-party code

back2safety is licensed under the [PolyForm Shield License 1.0.0](LICENSE). Any third-party code, library, data set, or rule set you add must be under a license compatible with that, such as **MIT, Apache-2.0, BSD, ISC, or CC0**.

- **Do not add GPL, AGPL, or LGPL code or dependencies.**
- For anything else, ask in an issue first.
- Note the source and license of any third-party material in your pull request.

### Threat-intelligence sources

- Integrations must use **the user's own API key**. Never commit or hardcode API keys.
- Respect each provider's terms of service and rate limits.
- **Privacy first:** never upload a user's email or attachments to a third-party service by default. Prefer lookups (URL, domain, IP, or file hash) over submissions, and make any submission or scan an explicit opt-in.

### Samples and personal data

Real phishing samples are valuable, but they often contain personal information.

- **Redact** names, email addresses, phone numbers, account numbers, and personal links before sharing a sample in an issue, pull request, or test.
- Never include samples containing someone else's private information without their permission.
- Do not include live malware. Reference malicious files by their SHA-256 hash instead.

### Secrets

Never commit API keys, passwords, tokens, or `.env` files. If you accidentally commit a secret, revoke it immediately and tell a maintainer.

## Security issues

Do **not** report security vulnerabilities in public issues or pull requests. Follow [SECURITY.md](SECURITY.md) instead.

## Trademark

Contributing does not grant rights to the "back2safety" name or logo. See the [Trademark](README.md#trademark) section of the README.
