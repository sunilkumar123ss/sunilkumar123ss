# Verification

The source download contains **80 packages**, including RagKit’s enhanced application at `6309347ed65bbe5eb5aa8779fb10031bc5d3bcc0`. Application code, tests and fixtures are unchanged. Current README notices have been consolidated in the profile introduction, and per-project HISTORY.md files removed; RagKit’s package manifest reflects that documentation removal.

## Original standalone baseline

**472 passing tests · 80 demo runs · 80 CLI help checks.** These counts concern the original `test_main.py` reference suites and `main.py` demos. They include RagKit’s preserved eight reference tests, not its enhanced application suite.

The refreshed source archive passed that same baseline check at 2026-10-24T13:33:29.161961+00:00 with Python 3.12.14. Each suite ran in a separate process. The original Python 3.9.6 evidence from 24 October 2026 is retained as `verification-original.json`; `verification.json` records this baseline rerun.

The split-leakage-guard demo intentionally exits with status 1 because its synthetic fixture contains leakage. The verifier checks that expected result explicitly.

## Enhanced RagKit

[RagKit’s separate application evidence](https://github.com/sunilkumar123ss/RagKit/blob/main/docs/VERIFICATION.md) records **108 tests and 49 subtests**, a separate actual embedding/reranker test, and **24 isolated package-install checks**. These counts overlap the baseline because the application suite includes the original eight RagKit tests; do not add the totals together.

The evidence distinguishes actual local Sentence-Transformers/CrossEncoder, Qdrant, MCP and LangChain runs from mocked OpenAI/Anthropic transports and a local Ollama test server. External answer services were not contacted. Desktop/mobile UI checks passed; browser file-picker automation was unavailable, while multipart API upload tests passed. Docker execution was unavailable; native installation and application execution were verified.

To repeat the baseline check after extracting `portfolio-80.zip`:

```sh
python3 verify_all.py
```

For enhanced RagKit, use the dependency setup and `python verify.py` command in its README. The real model check is separate and opt-in.

These are local engineering checks and synthetic examples. They do not establish production performance, adoption or the accuracy of generated claims. Consult repository workflow results for hosted CI outcomes.

This ZIP is a source download. The separate `expanded-history-80.zip` and its audited bundles/manifests remain the baseline history snapshot; this source refresh does not alter them. All portfolio implementations were prepared in October 2026 with AI assistance, and reconstructed Git dates are disclosed in this profile introduction.
