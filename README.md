# Awesome-Business-Benchmark

Awesome list of business-operation benchmarks for LLM agents.

## Content

- [Keywords Convention](#keywords-convention)
- [Benchmarks](#benchmarks)
  - [Core](#core)
  - [Adjacent](#adjacent)
  - [Real Deploy](#real-deploy)
  - [Simulators](#simulators)
- [Contributing](#contributing)

## Keywords Convention

![](https://img.shields.io/badge/Retail-blue) The business domain / setting.

![](https://img.shields.io/badge/Rules-green) How the environment dynamics are built.

![](https://img.shields.io/badge/Open_Code-orange) Code availability, replay support, or other practical notes.

## Benchmarks

### Core

End-to-end benchmarks where an agent runs a business over a long horizon.

- **Vending-Bench,** arXiv:2502.15840. One vending machine; inventory, pricing, supplier email, daily fees. ![](https://img.shields.io/badge/Vending-blue) ![](https://img.shields.io/badge/LLM_Counterpart-green) ![](https://img.shields.io/badge/Closed-orange)

  [[Paper](https://arxiv.org/abs/2502.15840)][[Leaderboard](https://andonlabs.com/evals/vending-bench)]

- **Vending-Bench 2.** Year-long vending business with adversarial suppliers; scored by final balance. ![](https://img.shields.io/badge/Vending-blue) ![](https://img.shields.io/badge/LLM_Counterpart-green) ![](https://img.shields.io/badge/Closed-orange) ![](https://img.shields.io/badge/Living_Leaderboard-orange)

  [[Leaderboard](https://andonlabs.com/evals/vending-bench-2)]

- **Vending-Bench Arena.** Several agents run machines at one site; trading, rivalry, and sabotage. ![](https://img.shields.io/badge/Vending-blue) ![](https://img.shields.io/badge/Multi_Agent-green) ![](https://img.shields.io/badge/Closed-orange)

  [[Leaderboard](https://andonlabs.com/evals/vending-bench-arena)]

- **RetailBench,** arXiv:2603.16453. Single-store supermarket over 180 days; pricing, replenishment, supplier quality. ![](https://img.shields.io/badge/Retail-blue) ![](https://img.shields.io/badge/Data_Grounded-green) ![](https://img.shields.io/badge/Open_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Paper](https://arxiv.org/abs/2603.16453)][[Code](https://github.com/linghuazhang01/RetailBench)]

- **YC-Bench.** AI start-up for one year; payroll, contracts, adversarial clients. ![](https://img.shields.io/badge/Startup-blue) ![](https://img.shields.io/badge/Rules-green) ![](https://img.shields.io/badge/Open_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Code](https://github.com/collinear-ai/yc-bench)][[Website](https://collinear-ai.github.io/yc-bench/)]

- **CoffeeBench,** arXiv:2606.16613. Coffee roaster in a 6-firm supply chain over 90 days. ![](https://img.shields.io/badge/Supply_Chain-blue) ![](https://img.shields.io/badge/Multi_Agent-green) ![](https://img.shields.io/badge/Open_Code-orange)

  [[Paper](https://arxiv.org/abs/2606.16613)][[Code](https://github.com/SakanaAI/CoffeeBench)]

- **CEO-Bench,** arXiv:2606.18543. SaaS company for 500 days via Python API and SQL; weekly cash forecast. ![](https://img.shields.io/badge/SaaS-blue) ![](https://img.shields.io/badge/Rules-green) ![](https://img.shields.io/badge/Open_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Paper](https://arxiv.org/abs/2606.18543)][[Code](https://github.com/zlab-princeton/ceobench-src)][[Website](https://ceobench.com)]

- **MerchantBench,** arXiv:2607.28956. Drop-shipping store over 365 days; sourcing, listing, delayed order outcomes. ![](https://img.shields.io/badge/E_Commerce-blue) ![](https://img.shields.io/badge/Data_Grounded-green) ![](https://img.shields.io/badge/Partial_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Paper](https://arxiv.org/abs/2607.28956)][[Code](https://github.com/KhanCold/merchantbench)]

- **Business Arena,** arXiv (Accio). Cross-border B2B shop over 30 simulated days; sourcing, compliance, competition. ![](https://img.shields.io/badge/B2B-blue) ![](https://img.shields.io/badge/Data_Grounded-green) ![](https://img.shields.io/badge/Partial_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Code](https://github.com/Accio-org/BusinessArena)][[Website](https://business-arena.site.accio.ai)]

- **FM-Bench,** arXiv:2608.18423. Football club over 20 seasons; transfers, tactics, hidden player ability. ![](https://img.shields.io/badge/Sports_Club-blue) ![](https://img.shields.io/badge/Rules-green) ![](https://img.shields.io/badge/Open_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Paper](https://arxiv.org/abs/2608.18423)]

- **E-Commerce Bench,** arXiv:2608.30730. Up to 4 online stores over 365 days; negotiation, fraud, fulfillment, cash flow. ![](https://img.shields.io/badge/E_Commerce-blue) ![](https://img.shields.io/badge/Data_Grounded-green) ![](https://img.shields.io/badge/Open_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Paper](https://arxiv.org/abs/2608.30730)][[Code](https://github.com/QwenLM/E-CommerceBench)]

- **ERPBench,** arXiv:2609.04667. Cereal manufacturer over 6 rounds; pricing, production, Solo vs Arena. ![](https://img.shields.io/badge/Manufacturing-blue) ![](https://img.shields.io/badge/Multi_Agent-green) ![](https://img.shields.io/badge/Open_Code-orange)

  [[Paper](https://arxiv.org/abs/2609.04667)]

- **StoreBench,** arXiv:2610.10942. Apparel store on Medusa v2; production-grade tools, market shocks. ![](https://img.shields.io/badge/E_Commerce-blue) ![](https://img.shields.io/badge/Rules-green) ![](https://img.shields.io/badge/Partial_Code-orange) ![](https://img.shields.io/badge/Replayable-orange)

  [[Paper](https://arxiv.org/abs/2610.10942)]

- **EcoGym,** arXiv:2602.09514. Unified suite: Vending, Freelance, and Operation over long horizons. ![](https://img.shields.io/badge/Multi_Scenario-blue) ![](https://img.shields.io/badge/Rules-green) ![](https://img.shields.io/badge/Open_Code-orange)

  [[Paper](https://arxiv.org/abs/2602.09514)]

- **AutoVend,** arXiv:2610.36980. 20 vending machines across 5 site types for 180 days. ![](https://img.shields.io/badge/Vending-blue) ![](https://img.shields.io/badge/Data_Grounded-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2610.36980)]

### Adjacent

Narrower economic tasks or analyses related to business agents.

- **Can LLMs Be CEOs?,** arXiv:2606.17459. Capital reallocation across units from conflicting advisors. ![](https://img.shields.io/badge/Strategy-blue) ![](https://img.shields.io/badge/Rules-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2606.17459)]

- **Market-Bench,** arXiv:2604.05523. LLM retailers bid for stock, price it, and write slogans. ![](https://img.shields.io/badge/Retail-blue) ![](https://img.shields.io/badge/Multi_Agent-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2604.05523)]

- **AIM-Bench,** arXiv:2508.11416. Inventory decisions from newsvendor to supply-chain network. ![](https://img.shields.io/badge/Inventory-blue) ![](https://img.shields.io/badge/Rules-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2508.11416)]

- **Magentic Marketplace,** arXiv:2510.25779. Two-sided market of LLM consumers and merchants. ![](https://img.shields.io/badge/Marketplace-blue) ![](https://img.shields.io/badge/Multi_Agent-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2510.25779)]

- **GLEE,** arXiv:2410.05254. Language-based bargaining, negotiation, and persuasion. ![](https://img.shields.io/badge/Negotiation-blue) ![](https://img.shields.io/badge/Game_Theory-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2410.05254)]

### Real Deploy

- **Project Vend.** Claude runs a real office shop; inventory, pricing, sourcing, Slack customers. ![](https://img.shields.io/badge/Retail-blue) ![](https://img.shields.io/badge/Real_World-green) ![](https://img.shields.io/badge/Closed-orange)

  [[Phase 1](https://www.anthropic.com/research/project-vend-1)][[Phase 2](https://www.anthropic.com/research/project-vend-2)]

### Simulators

Data-driven market and customer simulators used for training or offline evaluation.

- **Virtual-Taobao,** arXiv:1805.10000. Learned Taobao customer simulator for ranking / policy training. ![](https://img.shields.io/badge/E_Commerce-blue) ![](https://img.shields.io/badge/Learned-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/1805.10000)]

- **M3,** arXiv:2608.19227. Generative market microstructure model over large equity order-event corpora. ![](https://img.shields.io/badge/Finance-blue) ![](https://img.shields.io/badge/Learned-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2608.19227)]

- **RetailSynth,** arXiv:2405.10469. Calibrated grocery customer choice model for promotion / coupon RL. ![](https://img.shields.io/badge/Retail-blue) ![](https://img.shields.io/badge/Calibrated-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2405.10469)]

- **Agent4Rec,** arXiv:2310.10108. LLM-agent users for recommender evaluation. ![](https://img.shields.io/badge/Recommender-blue) ![](https://img.shields.io/badge/LLM_Counterpart-green) ![](https://img.shields.io/badge/Code_Unknown-orange)

  [[Paper](https://arxiv.org/abs/2310.10108)]

## Contributing

PRs welcome for new benchmarks, corrected metadata, or better links.
