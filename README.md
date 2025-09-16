# DDoS Regression Testbed

Small Linux-based pytest harness to simulate common DDoS patterns and validate mitigations.

## Why
Aligned to DDoS Mitigation QA: automated test cases (pytest), Linux regression environment, TCP/IP attacks (SYN/UDP/ICMP/slowloris), and artifacted debugging.

## Quickstart (minimum)
1. `git clone ... && cd ddos-regression`
2. `make up`      # docker-compose up -d
3. `make baseline`# apply baseline iptables
4. `make test`    # run pytest (small smoke)
5. `make down`

## What to show in interview
- `pytest --html=reports/report.html`
- `reports/capture.pcap` and `reports/compose.log`
- `git log --oneline` showing small incremental commits

## Optional: SR Linux integration
See `examples/srl/` branch for porting tests to Nokia SR Linux container image.
