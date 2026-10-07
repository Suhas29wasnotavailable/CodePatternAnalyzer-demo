# CodePatternAnalyzer — demo UI

The browser front-end for **[CodePatternAnalyzer](https://github.com/Suhas29wasnotavailable/CodePatternAnalyzer)**,
a stylometric tool that identifies the author of a Python file from coding style alone.

**[Live demo →](https://code-pattern-analyzer.vercel.app)**

Paste a Python file, and the UI calls the analyzer's `/analyze` endpoint and renders the
predicted author, the runner-up candidates with their confidences, and the structural
metrics behind the call — AST depth, cyclomatic complexity and function density.

## Structure

| File | Purpose |
|:--|:--|
| `index.html` | Input view — code editor and submit |
| `results.html` | Results view — prediction, confidences, metrics |

Static HTML with inline CSS and JS, no build step. Open `index.html` directly, or serve it:

```bash
python3 -m http.server 8080
```

The model, feature extraction and API live in the
**[main repository](https://github.com/Suhas29wasnotavailable/CodePatternAnalyzer)**.
