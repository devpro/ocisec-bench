# Wiz Grimoire session context

## Writing style

These rules apply to Markdown, code comments, commit messages, and any prose in scripts.

**One sentence per line.**
A line break only ever happens at the end of a sentence.
Never wrap a sentence across two lines.
There is no maximum line length, wrapping is handled by the editor, not by hard newlines.

**Never use the em dash (`—`) or the en dash (`–`).**
Use a colon when introducing an explanation, a comma when joining clauses, or a full stop and a new sentence.
This applies to prose, code comments, table cells, and error message strings.

**Never use the second person.**
No "you", no "your", not even in placeholders such as `<your-token>`, which should read `<token>`.
The documentation describes the repository, it does not address a reader.
Write "the working tree", not "your working tree".
Write "a contribution is planned", not "are you willing to contribute".

**Other conventions.**
Use `ini` as the fence language for `.properties` blocks, never `properties`.
Prefer `>` over `→` when describing UI navigation, for example **Project Settings > Quality Gate**.
An arrow stays acceptable when it denotes a conversion or a data flow, for example `Markdown → docx`.

## Repository conventions

Shell scripts are named in `snake_case`, which is the standard for bash.
`generate_pdf.sh`, not `generate-pdf.sh`.

Scripts must be committed with the executable bit set.
A script committed as `100644` fails on a fresh clone even though it works locally:

```bash
git update-index --chmod=+x path/to/script.sh
```

The root `README.md` stays as short as possible.
Shared content lives in `docs/` and is linked, never copied.
Contributor-facing material lives in `CONTRIBUTING.md` at the repository root, and should be highly efficient.

Target platform is Linux with Docker, including WSL2, and `bash`.
