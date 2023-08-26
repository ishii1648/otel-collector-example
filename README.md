# otel-collector-example

## log output example

notSampled

```console
2023-08-26T17:47:11.349Z        debug   tailsamplingprocessor@v0.83.0/processor.go:171  Sampling Policy Evaluation ticked       {"kind": "processor", "name": "tail_sampling", "pipeline": "traces"}
2023-08-26T17:47:11.349Z        debug   sampling/latency.go:32  Evaluating spans in latency filter      {"kind": "processor", "name": "tail_sampling", "pipeline": "traces", "policy": "latency"}
2023-08-26T17:47:11.349Z        debug   sampling/string_tag_filter.go:95        Evaluting spans in string-tag filter    {"kind": "processor", "name": "tail_sampling", "pipeline": "traces", "policy": "string_attribute"}
2023-08-26T17:47:11.349Z        debug   tailsamplingprocessor@v0.83.0/processor.go:201  Sampling policy evaluation completed    {"kind": "processor", "name": "tail_sampling", "pipeline": "traces", "batch.len": 1, "sampled": 0, "notSampled": 2, "droppedPriorToEvaluation": 0, "policyEvaluationErrors": 0}
```

sampled

```console
2023-08-26T17:47:16.345Z        debug   tailsamplingprocessor@v0.83.0/processor.go:171  Sampling Policy Evaluation ticked       {"kind": "processor", "name": "tail_sampling", "pipeline": "traces"}
2023-08-26T17:47:16.345Z        debug   sampling/latency.go:32  Evaluating spans in latency filter      {"kind": "processor", "name": "tail_sampling", "pipeline": "traces", "policy": "latency"}
2023-08-26T17:47:16.345Z        debug   sampling/string_tag_filter.go:95        Evaluting spans in string-tag filter    {"kind": "processor", "name": "tail_sampling", "pipeline": "traces", "policy": "string_attribute"}
2023-08-26T17:47:16.345Z        debug   tailsamplingprocessor@v0.83.0/processor.go:201  Sampling policy evaluation completed    {"kind": "processor", "name": "tail_sampling", "pipeline": "traces", "batch.len": 1, "sampled": 2, "notSampled": 0, "droppedPriorToEvaluation": 0, "policyEvaluationErrors": 0}
```
