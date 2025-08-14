# `codespaces-llm`

This repository provides a GitHub Codespaces environment with:
- [LLM](https://llm.datasette.io/)
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

## Related Posts

- [Prompting with LLM](https://building-with-llms-pycon-2025.readthedocs.io/en/latest/prompting.html)
- [Using AI Without Leaving the Terminal: A Guide to llm](https://kashw1n.com/blog/llm-cli/)

## Usage Examples

- `llm "Describe this image" -a screenshot.png`
- `llm "Extract all text" -a image.png -u`

```bash
# Generate commit messages
git diff --cached | llm -s "Generate a conventional commit message"

# Code reviews
git diff HEAD~1 | llm -s "Review these changes for potential issues"
```