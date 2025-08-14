# `codespaces-llm`

This repository provides a GitHub Codespaces environment with:
- [LLM](https://llm.datasette.io/), `strip-tags`, `ttok`
- Python 3.13
- `uv`
- GitHub CLI
- GitHub Copilot VS Code extension.

**[Launch Codespace](https://codespaces.new/hazadus/codespaces-llm?quickstart=1)**

Then try running this in a terminal:
```bash
llm "Fun facts about pelicans"
```
LLM is configured using the [llm-github-models](https://github.com/tonybaloney/llm-github-models) plugin.

## Documentation

- [LLM docs](https://llm.datasette.io/en/stable/)

## Related Posts

- [Prompting with LLM](https://building-with-llms-pycon-2025.readthedocs.io/en/latest/prompting.html)
- [Using AI Without Leaving the Terminal: A Guide to llm](https://kashw1n.com/blog/llm-cli/)

## Usage Examples

- `llm "Describe this image" -a screenshot.png`
- `llm "Extract all text" -a image.png -u`
- `curl "https://raw.githubusercontent.com/hazadus/bluesky-reader/refs/heads/main/feeds/2025-08-13.md" | llm "Составь обзор, о чем писали в ленте за день" -u`
- `curl -Ls "https://llm.datasette.io/en/stable/" | strip-tags | ttok -t 8000 | llm -s "Расскажи коротко о содержании страницы" -u`

```bash
# Generate commit messages
git diff --cached | llm -s "Generate a conventional commit message"

# Code reviews
git diff HEAD~1 | llm -s "Review these changes for potential issues"
```