# Poseidon

Rust-based Kraken dashboard designed for CU Quants' trading team.

## Features
- View account balances in real-time
- Place, modify, and cancel orders
- Manage subaccounts
- Track order history
- High-performance, safe, and reliable

## Setup
1. Install Rust
2. Clone repository
3. Configure Kraken API keys
4. Run `cargo run`

## Struc
```bash
poseidon/
│
├── Cargo.toml                # Rust dependencies and project metadata
├── config/
│   └── config.toml           # API keys, endpoints, default settings
│
├── src/
│   ├── main.rs               # Entry point, initializes runtime and UI
│   ├── app.rs                # Core application logic (state management)
│   ├── api/
│   │   ├── mod.rs            # API module exports
│   │   ├── kraken_rest.rs    # REST client: balances, orders, subaccounts
│   │   └── kraken_ws.rs      # WebSocket client: real-time updates
│   │
│   ├── ui/
│   │   ├── mod.rs            # UI module exports
│   │   ├── terminal.rs       # Terminal UI logic (tui-rs/crossterm)
│   │   └── gui.rs            # Optional GUI logic (egui/iced)
│   │
│   ├── models.rs             # Data structures: Orders, Balances, Positions
│   ├── errors.rs             # Custom error types and handling
│   └── utils.rs              # Helper functions (parsing, logging, etc.)
│
└── tests/                    # Integration and unit tests
    ├── api_tests.rs
    └── ui_tests.rs

```

## License
MIT
