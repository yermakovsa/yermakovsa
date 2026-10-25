**Senior Backend Engineer | Go · Distributed Systems · EVM/RPC Infrastructure**

I've spent 6+ years building distributed systems across fintech, telecom, and Web3. My work includes Kafka services processing **20M+ events/day**.

I also independently built and operated a low-latency Go trading system that identified price differences across decentralized exchanges and executed trades on Base, an Ethereum Layer 2.

## Featured Projects

### Low-Latency Trading Infrastructure on Base

*Independent production system · 2025–2026*

The Go backend monitored Base Flashblocks, fetched pool state in batches, and evaluated trade routes locally before signing and submitting transactions. Custom Solidity contracts executed trades atomically, supporting 10+ decentralized exchanges.

- Operated in production for **365+ consecutive days**, handling **300k+ transaction submissions**.
- Achieved **sub-100ms p95 end-to-end latency** (Flashblock receipt → first transaction hash returned).
- Executed **200k+ successful on-chain transactions**, totaling **~$200M in swap volume**.

![BaseScan Analytics](basescan-activity-2026-09-30.png)

*BaseScan Analytics · September 30, 2026*

### [failnext](https://github.com/yermakovsa/failnext) · HTTP/RPC Failover for Go

`failnext` provides ordered client-side failover across HTTP/RPC providers directly in Go applications, without a separate proxy. Built on Go's `http.RoundTripper`, it handles provider selection, cooldowns, and per-request routing controls while leaving decisions about failover safety and provider eligibility to the application.

## Other Open-Source Projects

- **RPC reliability and measurement:** [failnext-blocklag](https://github.com/yermakovsa/failnext-blocklag) (Ethereum RPC block-lag detection) · [rpclat](https://github.com/yermakovsa/rpclat) (RPC latency and reliability benchmarking).
- **Ethereum signatures:** [erc6492-go](https://github.com/yermakovsa/erc6492-go) (EOA, EIP-1271, and ERC-6492 signature verification) · [example-eip1271-wallet](https://github.com/yermakovsa/example-eip1271-wallet) (Solidity EIP-1271 example wallet).

## Distributed Systems in Production

- Built Kafka-backed services processing **20M+ telecom events/day**, using batching and PostgreSQL transactions to atomically persist offsets, business state, and outbox events for replay-safe processing.
- Built long-running financial workflows with Temporal, using idempotent payouts and compensating actions to handle failures.
- Created a shared distributed tracing library adopted across **10+ services**.

**Backend & Data:** Go · Java · REST/gRPC · PostgreSQL · Redis · Kafka · Temporal

**Infrastructure & Observability:** AWS (S3/SQS) · GCP · Kubernetes · Docker · Terraform · Prometheus · Grafana

**EVM & RPC:** Ethereum · Base · JSON-RPC · go-ethereum · Solidity
