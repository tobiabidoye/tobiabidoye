# Hi, I'm Tobi

Software engineer at **JPMorgan Chase** (NYC), working on cloud HPC infrastructure. CS grad from **UMBC**. I like distributed systems, consensus, and infrastructure.

**Languages:** Go · C++ · Java · Python
**Tools:** Terraform · Docker · AWS · PostgreSQL · Git

## Open source

### [etcd](https://github.com/etcd-io/etcd) (CNCF, Go, 52k+ stars)
[All my merged PRs →](https://github.com/etcd-io/etcd/pulls?q=is%3Apr+author%3Atobiabidoye+is%3Amerged)

Merged PRs: [#22542](https://github.com/etcd-io/etcd/pull/22542) · [#22552](https://github.com/etcd-io/etcd/pull/22552) · [#22554](https://github.com/etcd-io/etcd/pull/22554) · [#22558](https://github.com/etcd-io/etcd/pull/22558) · [#22583](https://github.com/etcd-io/etcd/pull/22583) · [#22590](https://github.com/etcd-io/etcd/pull/22590) · [#22591](https://github.com/etcd-io/etcd/pull/22591)

- Fixed an `etcdctl txn` panic when comparing leases (value parsed as a hex lease ID), with regression test `TestParseCompare`. Backported to `release-3.6` ([PR #22542](https://github.com/etcd-io/etcd/pull/22542)).
- Remediated OpenTelemetry vulnerability GO-2026-6505 across all three supported branches (3.5, 3.6, 3.7), one PR per branch, upgrading the tracing SDK and OTLP exporters to v1.45.0 without breaking release builds.
- Tailored each backport to its branch's dependency constraints and iterated through maintainer review to approval on all 6 PRs.

## Projects

### [Distributed-Kv-Store](https://github.com/tobiabidoye/Distributed-Kv-Store)
Fault-tolerant, linearizable key-value store in Go on a from-scratch Raft implementation (leader election, log replication, persistence, snapshotting) with no external consensus or storage libraries.
- Verified linearizability with Porcupine and failure-tested leader/follower crashes and snapshot catch-up.
- Crash-safe durability via atomic write-then-rename with fsync; exactly-once client semantics through request deduplication.
- Deployed as a 3-node AWS EC2 cluster across availability zones: 111 Put ops/sec, 143 ms p50, 290 ms p99.

### [DistributedPrimeCounter](https://github.com/tobiabidoye/DistributedPrimeCounter)
MapReduce-style distributed prime counter in Go using gRPC and protobuf.

### [Campus-DoorDash](https://github.com/QBallardUMBC/Fall-2025-Campus-DoorDash)
Full-stack on-campus food delivery app built for the UMBC community.

## Find me

[LinkedIn](https://www.linkedin.com/in/oluwatobiloba-abidoye-645320282/)
