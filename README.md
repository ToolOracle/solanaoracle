# SolanaOracle MCP Server

**12 DeFi Risk & Intelligence tools for Solana** — built for the [Solana AI Agent ecosystem](https://github.com/solana-foundation/awesome-solana-ai).

Compliance and risk intelligence that's missing from Solana's agent tooling. While Solana Agent Kit handles swaps and transfers — SolanaOracle tells agents **what's safe**.

## Live Endpoint

```
https://tooloracle.io/solana/mcp/
```

## Tools (12)

| Tool | Description |
|------|-------------|
| `sol_overview` | Ecosystem overview: SOL price, $6.6B TVL, 3,500+ TPS, epoch, supply |
| `sol_token_risk` | SPL token risk scoring — checks mint/freeze authority, CoinGecko listing. **Ideal for Pump.fun token screening.** |
| `sol_protocol_health` | Protocol health: TVL, audits, risk grade (Jupiter, Raydium, Jito, Orca, Drift…) |
| `sol_defi_yields` | Compare yields across all Solana protocols |
| `sol_protocol_list` | 372 DeFi protocols ranked by TVL |
| `sol_stablecoin_risk` | Stablecoin supply & risk (USDC, USDT, PYUSD…) |
| `sol_wallet_analysis` | Wallet analysis: SOL balance, USD value, SPL token holdings |
| `sol_dex_volume` | DEX volume across 72 exchanges ($1.6B+ daily) |
| `sol_network_stats` | Network health: TPS, slot, epoch, block height, supply |
| `sol_whale_watch` | Recent transaction monitoring for any address |
| `sol_bridge_flows` | Bridge flow monitoring |
| `sol_validator_info` | 774 validators, stake distribution, top 10 concentration (23%) |

## Quick Start

### Claude Desktop / Claude Code
```json
{
  "mcpServers": {
    "solanaoracle": {
      "url": "https://tooloracle.io/solana/mcp/"
    }
  }
}
```

### Use with Solana Agent Kit
```
Agent: "Is this token safe to swap?"
→ sol_token_risk (check mint/freeze authority)
→ sol_dex_volume (check liquidity exists)
→ sol_protocol_health (check DEX protocol is healthy)
→ Risk-informed swap decision
```

### Pump.fun Token Screening
```
Agent: "Screen this new Pump.fun token before buying"
→ sol_token_risk with mint address
→ Checks: mint authority revoked? freeze authority? CoinGecko listed? supply reasonable?
→ PASS / WARN / BLOCK verdict
```

## Why This Matters

Solana processes **15M+ on-chain agent payments** and handles **77% of x402 transaction volume**. As AI agents increasingly trade on Solana, they need risk intelligence:

- Is the token's mint authority revoked (or can someone mint infinite supply)?
- Does the protocol have audits and meaningful TVL?
- Is there enough DEX liquidity to exit the position?
- Which stablecoins on Solana are safe to hold?

## Data Sources

- **Solana RPC** (public mainnet) — On-chain data, token info, validators, transactions
- **DeFiLlama** — TVL, protocol health, yields, stablecoins, DEX volumes, bridges
- **CoinGecko** — Token prices, market data, listing verification

## Part of ToolOracle

One of 55+ MCP servers in [ToolOracle](https://tooloracle.io), built by [FeedOracle Technologies](https://feedoracle.io).

## License

MIT
