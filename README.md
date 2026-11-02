# Awesome-Business-Benchmark

Awesome list of business-operation benchmarks for LLM agents.

## Benchmarks

| Name | Category | Setting | Horizon | Dynamics | Hidden state | Replay | Code | Models | Metric | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [Vending-Bench](https://arxiv.org/abs/2502.15840) | Core | 1 vending machine | ≤2,000 msgs | LLM + rules | delivery timing, demand | ✗ | ✗ | 10 | net worth | Closed; LLM suppliers |
| [Vending-Bench 2](https://andonlabs.com/evals/vending-bench-2) | Core | 1 vending machine | 1 year | LLM + rules | supplier honesty, demand | ✗ | ✗ | 72+ | final balance | Living leaderboard |
| [Vending-Bench Arena](https://andonlabs.com/evals/vending-bench-arena) | Core | 3–5 machines + rivals | 1 year | LLM + rules + multi-agent | rival strategy | ✗ | ✗ | 3–5 / round | final balance | Agents trade and compete |
| [RetailBench](https://arxiv.org/abs/2603.16453) | Core | supermarket, 96 SKUs | 180 days | data + rules | supplier quality, news | ✓ | ✓ | 7 | net worth | [code](https://github.com/linghuazhang01/RetailBench) |
| [YC-Bench](https://github.com/collinear-ai/yc-bench) | Core | AI start-up, 8 employees | 1 year | deterministic rules | adversarial clients | ◦ | ✓ | 12 | final funds | Open; SQLite-backed |
| [CoffeeBench](https://github.com/SakanaAI/CoffeeBench) | Core | coffee roaster in 6-firm chain | 90 days | multi-agent + rules | demand, rival prices | ✗ | ✓ | 7 | net income | Other firms are LLM agents |
| [CEO-Bench](https://github.com/zlab-princeton/ceobench-src) | Core | SaaS company | 500 days | rules (+ LLM) | willingness to pay, churn | ✓ | ✓ | 16 | final cash | Includes weekly cash forecast |
| [MerchantBench](https://github.com/KhanCold/merchantbench) | Core | drop-shipping store | 365 days | data + rules | product risk, elasticity | ✓ | ◦ | 8×2 | net assets | Synthetic catalog in public release |
| [Business Arena](https://github.com/Accio-org/BusinessArena) | Core | cross-border B2B shop | 30 days | data + rules + multi-agent | demand, supplier honesty | ✓ | ✗ | 15 | net worth | Engine not fully released |
| [FM-Bench](https://arxiv.org/abs/2608.18423) | Core | football club | 20 seasons | deterministic rules | player ability, asking prices | ✓ | ✓ | 15 | composite score | Bit-identical replay |
| [E-Commerce Bench](https://github.com/QwenLM/E-CommerceBench) | Core | ≤4 online stores | 365 days | data + deterministic rules | fraud, cost floors, elasticity | ◦ | ✓ | 18 | assets | Negotiation kernel + LLM renderer |
| [ERPBench](https://arxiv.org/abs/2609.04667) | Core | cereal manufacturer, 12 SKUs | 6×30 days | rules + multi-agent | rival strategies | ◦ | ✓ | 6 | valuation | Solo and arena settings |
| [StoreBench](https://arxiv.org/abs/2610.10942) | Core | apparel store (Medusa v2) | 30–365 days | rules + multi-agent | demand, market shocks | ✓ | ◦ | 7 | composite | Full environment withheld |
| [EcoGym](https://arxiv.org/abs/2602.09514) | Core | Vending / Freelance / Operation | 1000+ steps | interactive rules | economic mechanics | ? | ✓ | 11 | net worth / income / DAU | Open multi-scenario suite |
| [AutoVend](https://arxiv.org/abs/2610.36980) | Core | 20 machines × 5 sites | 180 days | data + rules | inventory, site coordination | ? | ? | 5 | returns | Multi-site O2O operations |
| [Can LLMs Be CEOs?](https://arxiv.org/abs/2606.17459) | Adjacent | capital reallocation | 13 scenarios | authored scenarios | advisor conflict | n/a | ? | — | scenario score | Multi-role advice setting |
| [Market-Bench](https://arxiv.org/abs/2604.05523) | Adjacent | 20 LLM retailers | auction + pricing | rules + multi-agent | buyer personas | ✗ | ? | 20 | profit | Procurement-focused |
| [AIM-Bench](https://arxiv.org/abs/2508.11416) | Adjacent | inventory manager | 5 settings | stochastic rules | demand / lead time | n/a | ? | — | inventory metrics | Classic inventory problems |
| [Magentic Marketplace](https://arxiv.org/abs/2510.25779) | Adjacent | two-sided LLM market | market episode | multi-agent | strategies | ✗ | ? | — | welfare / win rate | Consumers and merchants |
| [GLEE](https://arxiv.org/abs/2410.05254) | Adjacent | bargaining / negotiation | 1,320 configs | game theory | opponent type | n/a | ? | — | payoff | Language-based economic games |
| [Project Vend](https://www.anthropic.com/research/project-vend-1) | Real deploy | office shop | ~1 month | real world | human customers | ✗ | ✗ | — | qualitative P&L | [Phase 2](https://www.anthropic.com/research/project-vend-2) |
| [Virtual-Taobao](https://arxiv.org/abs/1805.10000) | Simulator | e-commerce customers | — | learned | customer response | n/a | ? | — | A/B revenue | Firm-level customer simulator |
| [M3](https://arxiv.org/abs/2608.19227) | Simulator | equity order books | — | learned | microstructure | n/a | ? | — | forecast / stress | Large-scale market simulator |
| [RetailSynth](https://arxiv.org/abs/2405.10469) | Simulator | grocery customers | — | calibrated choice | coupon response | n/a | ? | — | offline RL | Coupon / promotion benchmarking |
| [Agent4Rec](https://arxiv.org/abs/2310.10108) | Simulator | recommender users | — | LLM agents | user taste | n/a | ? | — | taste alignment | Simulated recommender users |

## Legend

| Field | Meaning |
| --- | --- |
| **Category** | Core = end-to-end business operation; Adjacent = narrower economic task; Real deploy = physical deployment; Simulator = market / customer simulator |
| **Dynamics** | How the environment is generated (rules, real data, LLM counterparts, multi-agent, learned) |
| **Replay** | ✓ save/restore or bit-identical replay; ◦ deterministic replay from action log; ✗ not replayable |
| **Code** | ✓ public; ◦ partial; ✗ not released |

## Contributing

PRs welcome for new benchmarks, corrected metadata, or better links.
