# Contributing

Thank you for your interest in improving *Mathematical Methods for Machine Learning*.
This is a student-authored, living document, and careful readers are its most valuable resource.

## Ways to contribute

### 1. Report errors (most valuable)
Open an [issue](../../issues) and include:
- **Location:** chapter, section, and page number (and the version or date of the PDF).
- **What is wrong:** a typo, an incorrect statement, a gap in a proof, inconsistent notation, or an unclear passage.
- **Suggested fix**, if you have one.

### 2. Propose mathematical corrections
For substantive changes (a flawed proof, a missing hypothesis, an incorrect formula):
- Explain *why* the current version is wrong, ideally with a short argument or a reference.
- Cite a source (textbook, paper, lecture notes) where possible.

### 3. Improve explanations
Suggestions to make a derivation clearer, add a worked example, or add a figure are welcome. Please keep the tone and level of rigor consistent with the surrounding text.

### 4. Suggest additions
Missing topics or recommended references are welcome. Open an issue to discuss before writing anything large.

## Pull request workflow

1. Fork the repository and create a branch: `fix/ch06-svd-typo` or `improve/ch10-distributions`.
2. Edit the relevant file in `src/chapters/`.
3. Compile locally to confirm it builds cleanly:

```bash
cd src && latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```
4. Commit with a clear message (e.g., `Fix sign error in Ch. 9 KKT example`).
5. Open a pull request describing what changed and why.

Please **do not commit the compiled PDF** in pull requests. The maintainer regenerates it for each release.

## Style guidelines

- Follow the existing notation and macros defined in `src/main.tex`. Do not introduce new symbols for existing concepts.
- Keep the definition, theorem, proof, and example environments consistent with the rest of the document.
- One logical change per pull request.
- Use British or American English consistently within a passage, matching the surrounding text.
- Figures go in `src/figures/`, preferably as TikZ or other vector graphics.

## Licensing of contributions

By contributing, you agree that your contributions will be licensed under the same
[CC BY-NC-SA 4.0](LICENSE) license as the project.

## Code of conduct

Be kind, be constructive, and assume good faith. This is a learning resource, and every question or correction is welcome regardless of the contributor's background.
