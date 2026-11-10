# HFT Engine

**A C++ High-Frequency Trading Engine focused on market microstructure, quantitative market-making strategies, and low-latency system design.**

![Language](https://img.shields.io/badge/Language-C++-blue)
![Build](https://img.shields.io/badge/Build-CMake-green)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)
![Domain](https://img.shields.io/badge/Domain-Quantitative%20Finance-purple)

## Overview

HFT Engine is a C++ project aimed at developing a modular high-frequency trading system with a focus on limit order book simulation, quantitative trading strategies, and efficient order execution.

The project explores the intersection of computer science, financial mathematics, and market microstructure by implementing and evaluating market-making models in a simulated trading environment.

The primary objective is to understand how trading strategies interact with market dynamics and how system architecture and execution efficiency influence trading performance.

## Objectives

- Develop a limit order book and market simulation environment.
- Implement quantitative market-making strategies.
- Explore mathematical models used in high-frequency trading.
- Develop modular trading infrastructure.
- Evaluate strategies using PnL after transaction costs.
- Study latency, execution quality, and inventory risk.
- Build a testable and extensible C++ trading system.

## Architecture

The engine is designed around modular components:

| Component | Responsibility |
|---|---|
| Market Data | Receives and processes market information |
| Limit Order Book | Maintains bid and ask order levels |
| Strategy Engine | Generates trading decisions and quotes |
| Risk Management | Monitors inventory and trading risk |
| Order Management System | Handles order lifecycle and execution |
| Execution Simulator | Simulates order fills and market interactions |
| Performance Analytics | Evaluates PnL and strategy performance |

The architecture will evolve as additional components are implemented.

## Quantitative Strategies

The strategy development process follows an incremental approach.

### 1. Avellaneda-Stoikov (A-S)

The baseline market-making strategy.

Explores:
- Optimal bid-ask spread.
- Reservation price.
- Inventory management.
- Market-making under inventory risk.

### 2. Microprice Integration

Extends the baseline strategy using order book information.

Explores:
- Order book imbalance.
- Microprice estimation.
- Short-term price direction.
- Information contained in the limit order book.

### 3. GLFT Market-Making Model

An extension towards more advanced market-making and inventory control.

Explores:
- Optimal quoting.
- Inventory-sensitive pricing.
- Stochastic control.
- Market-making under different execution assumptions.

### Future Extensions

- Fill-probability modelling.
- Queue-position awareness.
- More realistic execution simulation.
- Additional market microstructure signals.

Each strategy will be evaluated against its predecessor, with particular attention to net PnL after transaction costs.

## Technology Stack

- **Language:** C++
- **Build System:** CMake
- **Testing:** C++ unit testing
- **Version Control:** Git
- **Development Environment:** VS Code

Additional tools and libraries will be introduced as the project evolves.

## Development Roadmap

- [x] Core Foundation
- [x] Simulated Exchange Core
- [x] Order Life Cycle Management
- [x] Execution Reports
- [x] Clock and Event Foundation
- [x] Order Management System
- [x] Market Data Infrastructure (Live Market Data Feed, Synthetic Market Data & Historical MArket Data Replay)
- [x] Risk Management
- [x] Kill Switch
- [x] Avellaneda-Stoikov baseline strategy
- [ ] Microprice integration
- [ ] GLFT strategy
- [x] Execution Venue Interface
- [x] Portfolio and P&L
- [ ] Backtesting Engine
- [ ] Execution Realism
- [ ] Performance optimization
- [ ] Observation and Analytics
- [ ] Persistance and Recovery
- [ ] Reconciliation
- [ ] Deployment and Operations

*Roadmap items are updated as development progresses.*

## Performance Evaluation

Strategies will be evaluated using quantitative metrics, including:

- Net Profit and Loss (PnL).
- PnL after transaction costs.
- Inventory exposure.
- Bid-ask spread capture.
- Fill rate.
- Drawdown.
- Execution performance.

The goal is to understand not just whether a strategy is profitable, but why it performs the way it does under different market conditions.

## Building the Project

### Prerequisites

- C++ compiler
- CMake
- Git

### Build

```bash
git clone <repository-url>
cd HFT_Engine

cmake -S . -B build
cmake --build build
```

### Run Tests

```bash
ctest --test-dir build --output-on-failure
```

## Learning Objectives

This project provides practical exposure to:

- Advanced C++ programming.
- Data structures and algorithm optimization.
- Concurrent and low-latency system design.
- Financial mathematics.
- Stochastic processes and optimal control.
- Market microstructure.
- Quantitative strategy development.
- Software architecture and testing.

## Disclaimer

This project is intended for educational and research purposes. It is not connected to a live exchange (yet) and should not be considered a production-ready trading system or financial advice.

---

**Built as an exploration of quantitative finance, market microstructure, and high-performance C++ engineering.**
