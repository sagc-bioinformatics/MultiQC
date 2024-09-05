---
name: Iso-Seq
urls: ["https://github.com/PacificBiosciences/IsoSeq"]
summary: >
  Identifies transcripts in PacBio single-molecule sequencing data (HiFi reads)
---

<!--
~~~~~ DO NOT EDIT ~~~~~
This file is autogenerated from the MultiQC module python docstring.
Do not edit the markdown, it will be overwritten.

File path for the source of this content: multiqc/modules/isoseq/isoseq.py
~~~~~~~~~~~~~~~~~~~~~~~
-->

Supports outputs generated by two commands:

- [IsoSeq `refine`](https://github.com/PacificBiosciences/IsoSeq/blob/master/isoseq-clustering.md#step-3---refine)
  trims poly(A) tails and removes concatemers.

- [IsoSeq `cluster`](https://github.com/PacificBiosciences/IsoSeq/blob/master/isoseq-clustering.md#step-4---clustering)
  performs clustering using hierarchical n\*log(n) alignment and iterative cluster merging.

### File search patterns

```yaml
isoseq/cluster-csv:
  contents: cluster_id
  fn: "*cluster_report.csv"
  num_lines: 1
isoseq/refine-csv:
  contents: id,strand,fivelen,threelen,polyAlen,insertlen,primer
  fn: "*.csv"
isoseq/refine-json:
  contents: '"num_reads_fl"'
  fn: "*.json"
```