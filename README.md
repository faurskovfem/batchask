# batchask

Batch prompt runner with retries and progress

Small but I use it weekly.

## Installation

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Features

- JSONL in, JSONL out: stream-safe for huge inputs
- Idempotent: skips ids already present in the output
- Retries failed items with backoff, logs them aside
- Concurrent workers with a rate ceiling

## Usage

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── dependabot.yml
│   └── pull_request_template.md
├── docs/
│   ├── configuration.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .editorconfig
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── Makefile
├── SECURITY.md
├── batch.py
├── prompts.sample.jsonl
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## Development

```bash
# run the test suite
pytest -q   # or npm test / go test ./...
```

## License

MIT - see [LICENSE](LICENSE).
