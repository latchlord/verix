# Verix 🔬

**Open-source verification workflow engine for RISC-V and ASIC/FPGA teams.**

Verix wraps the best open-source simulators (Verilator, Icarus Verilog, GHDL) into a single, clean CLI — so you spend time closing coverage, not fighting toolchains.

> Built by a VLSI/EDA engineer, for the India chip design community and the global RISC-V ecosystem.

---

## The Problem

Running functional verification with open-source tools today looks like this:

```bash
# compile
verilator --cc --exe --build -Wall my_dut.sv tb.cpp

# run
./obj_dir/Vmy_dut

# coverage? figure it out yourself.
# regressions? shell scripts held together with hope.
# CI integration? good luck.
```

Every team reinvents the same plumbing. Verix fixes that.

---

## What Verix Does

```bash
verix init              # scaffold a verification project in seconds
verix run               # compile + simulate (Verilator / Icarus / GHDL)
verix coverage          # parse and display coverage report
verix regress           # run full regression suite in parallel
verix report            # export a clean HTML coverage dashboard
verix ai analyze        # AI-powered coverage gap advisor (coming soon)
verix ai testbench      # generate cocotb testbench from your DUT interface (coming soon)
```

One tool. Any simulator backend. Clean output. Readable errors.

---

## Supported Simulators

| Simulator | Languages | Status |
|---|---|---|
| Verilator | SystemVerilog, Verilog | ✅ Planned |
| Icarus Verilog | Verilog, SystemVerilog (subset) | ✅ Planned |
| GHDL | VHDL | ✅ Planned |
| cocotb | Python testbenches (any backend) | ✅ Planned |

---

## Who This Is For

- **RISC-V chip teams** — open hardware deserves open, great tooling
- **ASIC/FPGA students and researchers** — IIT, IISc, NIT labs doing real chip work
- **India Semiconductor Mission startups** — teams that need serious verification flows without $100K/seat licenses
- **Open-source chip contributors** — OpenLane, OpenHW, SHAKTI ecosystem
- **Anyone tired of duct-taping Makefile regressions together**

---

## Roadmap

### Phase 1 — Core CLI (current focus)
- [ ] `verix init` — project scaffolding
- [ ] `verix run` — unified simulation runner
- [ ] `verix coverage` — coverage parsing and terminal display
- [ ] `verix regress` — parallel regression runner
- [ ] `verix report` — HTML dashboard export
- [ ] pip installable (`pip install verix`)
- [ ] cocotb-native support

### Phase 2 — AI Layer
- [ ] `verix ai analyze` — LLM-powered coverage gap analysis
- [ ] `verix ai testbench` — cocotb testbench generator from DUT interface
- [ ] Regression pruning suggestions

### Phase 3 — Cloud & CI
- [ ] GitHub Actions integration (`uses: verix-dev/verix-action@v1`)
- [ ] Web dashboard for team coverage tracking
- [ ] Cloud compute tier (pay-per-use simulation)

---

## Getting Started (once v0.1 is out)

```bash
pip install verix

cd my_riscv_project
verix init
verix run --sim verilator
verix coverage
```

---

## Contributing

Verix is in early development. If you're a verification engineer and you have opinions about what this tool should do — **open an issue, I want to hear from you.**

Especially interested in:
- What does your current regression flow look like?
- What output formats do you need (UCDB, VCD, XML)?
- What would make you switch from your current setup?

---

## Why Verix?

The semiconductor industry in India is at an inflection point. Dozens of new chip design teams are spinning up. They have the talent. They shouldn't have to spend their time fighting open-source toolchain friction or begging for enterprise EDA licenses.

Verix is an attempt to give India's chip design community — and the global RISC-V ecosystem — the verification workflow they deserve. Free, fast, and smart.

---

## Status

🚧 **Pre-release — actively building v0.1**

Star the repo to follow progress. Issues and feedback welcome.

---
