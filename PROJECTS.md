# Project catalog

**80 repositories · 6 CV projects · 74 focused engineering labs**

[Profile overview](./README.md) · [Download the complete package archive](./portfolio-80.zip) · [Verification notes](./VERIFICATION.md)

The portfolio editions were created in **October 2026 with AI coding assistance** and use synthetic examples. The baseline histories across 77 repositories contain **1,108 disclosed reconstructed milestones** dated between January 2023 and October 2026. RagKit has separate disclosed enhancement milestones with synthetic 2025 author and committer dates, also prepared in October 2026. These recorded dates do not establish past development or employment; The profile introduction centralizes the timeline disclosure.

VoiceDesk and DataTalk retain their original 24 October 2026 commit timestamps; their current documentation has been updated. RagKit preserves its exact original 24 October 2026 root commit as an ancestor of its enhanced history.

## Find a track

| Track | Repositories |
| --- | ---: |
| [CV projects](#cv-projects) | 6 |
| [Retrieval and agents](#retrieval-and-agents) | 15 |
| [Voice and audio](#voice-and-audio) | 15 |
| [Evaluation and ML operations](#evaluation-and-ml-operations) | 15 |
| [Backend services](#backend-services) | 14 |
| [Systems patterns](#systems-patterns) | 15 |

## Run a project

Use Python 3.10 or later for the collection's documented baseline. The original standalone demos use only Python's standard library. RagKit’s web UI, semantic retrieval, reranker, and integrations use optional dependencies; each repository documents its requirements and boundaries.

```sh
git clone https://github.com/sunilkumar123ss/VoiceDesk.git
cd VoiceDesk
python3 main.py
python3 verify.py
```

For a standalone demo, extract the archive, open its folder under `repositories/`, and run its documented per-project verifier. For enhanced RagKit, follow its setup and test commands, including the required development dependencies. From the archive root, `python3 verify_all.py` checks the original standalone reference tests, demos and help across all 80 packages.

The original collection check passed **472 unit tests, 80 default-demo checks, and 80 CLI help checks**. RagKit’s enhanced application has separate tests and verification notes; its additional checks are not included in those original totals. The leakage demo intentionally returns status 1 for its supplied fixture; its verifier expects that result. These checks use synthetic inputs and do not establish deployment or production performance.

For RagKit’s persistent document workspace, follow its [local quickstart](https://github.com/sunilkumar123ss/RagKit#start-locally). The default lexical/extractive workflow needs no API key. Semantic indexing uses real downloaded models; optional answer providers require configuration.

## CV projects

| Repository | Focus |
| --- | --- |
| [VoiceDesk](https://github.com/sunilkumar123ss/VoiceDesk) | Offline voice-session state with transcript updates, interruption handling, and stale-reply fencing. |
| [RagKit](https://github.com/sunilkumar123ss/RagKit) | Persistent SQLite document library and web UI; BM25 + Sentence-Transformers/Qdrant hybrid retrieval, CrossEncoder reranking, cited answers, and FastAPI/MCP/LangChain interfaces. |
| [DataTalk](https://github.com/sunilkumar123ss/DataTalk) | A constrained question-to-SQL grammar with parameterized queries and read-only SQLite controls. |
| [TripMind](https://github.com/sunilkumar123ss/TripMind) | Exact itinerary optimization with daily constraints, integer budgets, and transparent preference scores. |
| [HireRank](https://github.com/sunilkumar123ss/HireRank) | Explainable technical-skill evidence coverage for human review; no automated hiring decisions. |
| [AlertFlow](https://github.com/sunilkumar123ss/AlertFlow) | A SQLite outbox with idempotency, fenced leases, retry backoff, crash recovery, and dead letters. |

## Retrieval and agents

| Repository | Focus |
| --- | --- |
| [bm25-retriever](https://github.com/sunilkumar123ss/bm25-retriever) | Rank a small text corpus with lexical BM25 scoring; no embeddings or model calls. |
| [bounded-retries](https://github.com/sunilkumar123ss/bounded-retries) | Bound transient-error retries by attempt count, exponential backoff, and total scheduled delay. |
| [checkpoint-workflow](https://github.com/sunilkumar123ss/checkpoint-workflow) | Resume a deterministic document workflow from validated, atomically written checkpoints. |
| [citation-integrity](https://github.com/sunilkumar123ss/citation-integrity) | Check source IDs and quotation text against supplied evidence; no factual-entailment claim. |
| [context-budgeter](https://github.com/sunilkumar123ss/context-budgeter) | Pack required and optional evidence within a documented word/punctuation estimate. |
| [evidence-isolation](https://github.com/sunilkumar123ss/evidence-isolation) | Separate untrusted evidence from instructions and gate tool proposals by trusted provenance. |
| [explicit-query-expansion](https://github.com/sunilkumar123ss/explicit-query-expansion) | Apply reviewed phrase-to-alias rules with provenance, a one-hop limit, and an expansion cap. |
| [extractive-qa-abstention](https://github.com/sunilkumar123ss/extractive-qa-abstention) | Return a cited source sentence when lexical coverage meets a threshold; otherwise abstain. |
| [incremental-document-index](https://github.com/sunilkumar123ss/incremental-document-index) | Detect text-file changes with hashes and update a persistent lexical inverted index. |
| [offset-aware-chunker](https://github.com/sunilkumar123ss/offset-aware-chunker) | Build overlapping whitespace-token windows while retaining exact source character offsets. |
| [prompt-template-guard](https://github.com/sunilkumar123ss/prompt-template-guard) | Validate declared placeholders and reject traversal or nested formatting in text templates. |
| [readonly-sqlite-sandbox](https://github.com/sunilkumar123ss/readonly-sqlite-sandbox) | Limit SQLite reads with table/function allowlists, an authorizer, row caps, and VM-step budgets. |
| [reciprocal-rank-fusion](https://github.com/sunilkumar123ss/reciprocal-rank-fusion) | Combine weighted ranked lists with reciprocal rank fusion and duplicate-ID handling. |
| [scoped-tool-gateway](https://github.com/sunilkumar123ss/scoped-tool-gateway) | Gate local tool calls with allowlists, caller-supplied trusted scopes, expiry, and parameter schemas. |
| [structured-output-validator](https://github.com/sunilkumar123ss/structured-output-validator) | Validate a documented JSON Schema-inspired subset and reject duplicate keys or non-finite numbers. |

## Voice and audio

| Repository | Focus |
| --- | --- |
| [audio-quality](https://github.com/sunilkumar123ss/audio-quality) | Measure RMS, dBFS, peak, DC offset, clipping, quiet fraction, zero crossings and crest factor. |
| [barge-in-controller](https://github.com/sunilkumar123ss/barge-in-controller) | Cancel assistant playback only after supplied user-activity events persist beyond a debounce threshold. |
| [command-router](https://github.com/sunilkumar123ss/command-router) | Route a small explicit command grammar while refusing ambiguity, negation and low supplied confidence. |
| [dtmf-router](https://github.com/sunilkumar123ss/dtmf-router) | Route supplied keypad symbols through a small IVR with retry limits, timeouts and human handoff. |
| [energy-vad](https://github.com/sunilkumar123ss/energy-vad) | Locate sustained high-energy intervals with minimum onset duration and a silence hangover. |
| [jitter-buffer](https://github.com/sunilkumar123ss/jitter-buffer) | Reorder packet arrivals into timed playout and explicitly track missing, late and duplicate packets. |
| [latency-budget](https://github.com/sunilkumar123ss/latency-budget) | Build an earliest-start schedule and critical path for a dependency graph of voice pipeline stages. |
| [linear-resampler](https://github.com/sunilkumar123ss/linear-resampler) | Convert a normalized waveform to another sample rate using explicit linear interpolation. |
| [pcm-converter](https://github.com/sunilkumar123ss/pcm-converter) | Convert normalized interleaved frames to signed PCM16 little-endian bytes and decode them back. |
| [session-replay](https://github.com/sunilkumar123ss/session-replay) | Validate a voice-session lifecycle and produce an auditable transition log. |
| [speaker-segment-merge](https://github.com/sunilkumar123ss/speaker-segment-merge) | Merge adjacent same-label time segments and report overlaps between different supplied speaker labels. |
| [ssml-renderer](https://github.com/sunilkumar123ss/ssml-renderer) | Render escaped SSML from structured text, emphasis and pause segments. |
| [transcript-stabilizer](https://github.com/sunilkumar123ss/transcript-stabilizer) | Commit token prefixes shared by consecutive hypotheses while leaving changing text provisional. |
| [wav-segmenter](https://github.com/sunilkumar123ss/wav-segmenter) | Split a real PCM WAV container into independently playable chunks while preserving frame boundaries, sample rate and channel layout. |
| [word-error-rate](https://github.com/sunilkumar123ss/word-error-rate) | Compute word-level substitution, deletion and insertion counts with a reproducible edit alignment. |

## Evaluation and ML operations

| Repository | Focus |
| --- | --- |
| [budget-routing](https://github.com/sunilkumar123ss/budget-routing) | Simulate model routing under configured capability, context, latency, and batch-cost limits. |
| [classification-metrics](https://github.com/sunilkumar123ss/classification-metrics) | Compute multiclass confusion matrices, accuracy, precision, recall, and F1 from supplied predictions. |
| [confidence-calibration](https://github.com/sunilkumar123ss/confidence-calibration) | Inspect binary probabilities with Brier score, log loss, reliability bins, and calibration error. |
| [distribution-drift](https://github.com/sunilkumar123ss/distribution-drift) | Compare numeric samples with population stability index, empirical KS distance, and mean shift. |
| [model-registry-check](https://github.com/sunilkumar123ss/model-registry-check) | Validate artifact hashes, confined paths, unique versions, stage rules, and evaluation metadata. |
| [paired-experiment-comparison](https://github.com/sunilkumar123ss/paired-experiment-comparison) | Compare matched-seed experiments with directional improvements and reproducible bootstrap intervals. |
| [release-gate](https://github.com/sunilkumar123ss/release-gate) | Apply fail-closed metric thresholds and sample-count rules with explicit outcome codes. |
| [retrieval-metrics](https://github.com/sunilkumar123ss/retrieval-metrics) | Calculate precision, recall, reciprocal rank, average precision, and nDCG from relevance judgments. |
| [robustness-perturbations](https://github.com/sunilkumar123ss/robustness-perturbations) | Generate text variations and measure exact output stability from supplied responses. |
| [split-leakage-guard](https://github.com/sunilkumar123ss/split-leakage-guard) | Find duplicate IDs, cross-split text/groups, and token-overlap near-duplicate candidates. |
| [synthetic-pii-redaction](https://github.com/sunilkumar123ss/synthetic-pii-redaction) | Measure a limited email/phone redactor against synthetic annotated character spans. |
| [token-batch-scheduler](https://github.com/sunilkumar123ss/token-batch-scheduler) | Simulate FIFO microbatches with token, item-count, and maximum-wait limits. |
| [token-cost-accounting](https://github.com/sunilkumar123ss/token-cost-accounting) | Calculate decimal token costs, cached-input billing, and budget usage from supplied prices. |
| [trace-span-analytics](https://github.com/sunilkumar123ss/trace-span-analytics) | Validate nested spans and compute latency, errors, and exclusive durations with overlap handling. |
| [ttl-prompt-cache](https://github.com/sunilkumar123ss/ttl-prompt-cache) | Cache responses in SQLite using contextual request hashes, TTL expiry, and local hit/miss counts. |

## Backend services

| Repository | Focus |
| --- | --- |
| [canonical-json-digest](https://github.com/sunilkumar123ss/canonical-json-digest) | Produce consistent local JSON bytes and content hashes from strict input. |
| [circuit-breaker](https://github.com/sunilkumar123ss/circuit-breaker) | Explore failure thresholds, short-circuiting, and recovery probes. |
| [configuration-validator](https://github.com/sunilkumar123ss/configuration-validator) | Validate application settings together and keep database credentials out of summaries. |
| [csv-stream-validator](https://github.com/sunilkumar123ss/csv-stream-validator) | Validate order imports one record at a time and keep precise decimal totals. |
| [cursor-pagination](https://github.com/sunilkumar123ss/cursor-pagination) | Page through records using a stable compound key and opaque cursors. |
| [dependency-health-rollup](https://github.com/sunilkumar123ss/dependency-health-rollup) | Summarize dependency status using criticality and observation freshness. |
| [etag-concurrency](https://github.com/sunilkumar123ss/etag-concurrency) | Prevent stale JSON updates with atomic compare-and-replace. |
| [idempotency-key-store](https://github.com/sunilkumar123ss/idempotency-key-store) | Replay successful byte responses while detecting conflicting key reuse. |
| [ndjson-event-reader](https://github.com/sunilkumar123ss/ndjson-event-reader) | Process bounded event lines while isolating malformed records. |
| [sliding-window-limiter](https://github.com/sunilkumar123ss/sliding-window-limiter) | Enforce exact request counts over a moving time window. |
| [token-bucket-limiter](https://github.com/sunilkumar123ss/token-bucket-limiter) | Model burst capacity and gradual token refill with a deterministic clock. |
| [trace-context-parser](https://github.com/sunilkumar123ss/trace-context-parser) | Inspect version-00 traceparent headers and derive synthetic child contexts. |
| [ttl-lru-cache](https://github.com/sunilkumar123ss/ttl-lru-cache) | Combine recency-based eviction with per-entry time limits. |
| [webhook-signature-check](https://github.com/sunilkumar123ss/webhook-signature-check) | Validate raw payload integrity and a bounded timestamp window using HMAC. |

## Systems patterns

| Repository | Focus |
| --- | --- |
| [audit-hash-chain](https://github.com/sunilkumar123ss/audit-hash-chain) | Detect changes and reordering in canonical JSON records, with optional trusted head anchoring. |
| [bloom-filter](https://github.com/sunilkumar123ss/bloom-filter) | Provide bounded approximate membership with mergeable bit arrays. |
| [bounded-task-queue](https://github.com/sunilkumar123ss/bounded-task-queue) | Apply backpressure and reject stale completion after an expired task lease. |
| [consistent-hash-ring](https://github.com/sunilkumar123ss/consistent-hash-ring) | Assign keys to a deterministic virtual-node ring and measure membership remapping. |
| [dead-letter-queue](https://github.com/sunilkumar123ss/dead-letter-queue) | Bound retries and move repeatedly failed jobs into a reviewable dead-letter state. |
| [event-deduplicator](https://github.com/sunilkumar123ss/event-deduplicator) | Reject repeated event IDs within a bounded first-seen retention window. |
| [event-time-watermarks](https://github.com/sunilkumar123ss/event-time-watermarks) | Finalize tumbling event-time windows under an explicit bounded-disorder policy. |
| [feature-flag-evaluator](https://github.com/sunilkumar123ss/feature-flag-evaluator) | Evaluate explicit targeting rules and reproducible percentage rollouts. |
| [merkle-file-manifest](https://github.com/sunilkumar123ss/merkle-file-manifest) | Detect directory changes using canonical file leaves and a reproducible Merkle root. |
| [rendezvous-hashing](https://github.com/sunilkumar123ss/rendezvous-hashing) | Choose stable primary and replica candidates by ranking node-specific hashes. |
| [retry-budget](https://github.com/sunilkumar123ss/retry-budget) | Limit retry amplification using a fractional token budget earned by original requests. |
| [saga-compensation](https://github.com/sunilkumar123ss/saga-compensation) | Compensate completed steps in reverse order after a later operation fails. |
| [sql-migration-runner](https://github.com/sunilkumar123ss/sql-migration-runner) | Apply ordered SQLite migrations atomically while detecting checksum drift. |
| [topological-job-planner](https://github.com/sunilkumar123ss/topological-job-planner) | Calculate dependency-safe earliest schedules and a critical path for a job DAG. |
| [transactional-outbox](https://github.com/sunilkumar123ss/transactional-outbox) | Commit business records and publishable events in one SQLite transaction. |

Each linked README documents implemented behavior, setup, examples, and limitations. RagKit includes offline extractive answers and configurable OpenAI, Anthropic, and Ollama adapters; its verification notes distinguish implemented adapters from live service tests. Historical CV stars, adoption, deployment results, and benchmark figures are not claimed for these portfolio editions.
