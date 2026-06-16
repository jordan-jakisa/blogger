# Contributing to Blogger

Thanks for your interest in improving Blogger! This project is an open-source AI
agent that generates SEO-optimised blog posts from web references. Contributions
of all kinds are welcome — bug reports, features, docs, and tests.

## Ways to contribute

- **Report a bug** — open an issue describing what happened, what you expected,
  and steps to reproduce.
- **Suggest a feature** — open an issue describing the use case before sending a
  large change, so we can agree on the approach.
- **Improve docs** — fixes to the README, setup steps, or this guide are always
  welcome.
- **Send a fix or feature** — see the workflow below.

## Development setup

The project uses [pipenv](https://pipenv.pypa.io/) for dependency management.

```bash
git clone https://github.com/jordan-jakisa/blogger.git
cd blogger
pip install pipenv
pipenv install
```

Copy `.env.template` to `.env` and add your `OPENAI_API_KEY`, then run the app:

```bash
pipenv run streamlit run src/app.py
```

## Pull request workflow

1. Fork the repository and create a branch from `master`
   (e.g. `fix/parse-links` or `feat/export-markdown`).
2. Make your change. Keep PRs focused — one logical change per PR.
3. Run the app locally and confirm it still generates a post end to end.
4. Write a clear PR description: what changed and why. Link any related issue.
5. Open the PR against `master`. For large changes, please open an issue first
   to discuss the approach.

## Code style

- Follow the existing structure: app/UI code in `src/app.py`, agent logic in
  `src/agents/`, prompts in `src/agents/prompts.py`.
- Match the surrounding code's formatting and naming.
- Avoid committing secrets — `.env` is gitignored; never hardcode API keys.

## Reporting security issues

If a change touches how user API keys are handled, or how scraped web content is
parsed and fed into prompts, call it out explicitly in the PR — these are the
project's most sensitive areas. For sensitive security reports, contact the
maintainer directly rather than opening a public issue.

## License

By contributing, you agree that your contributions will be licensed under the
[MIT License](LICENSE) that covers this project.
