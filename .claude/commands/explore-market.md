---
name: explore-market
description: Deep dive into a specific Polymarket market
allowed-tools: Read, Bash, Grep
---

# Explore Market

Analyse: $ARGUMENTS

## Steps
1. Search: polymarket -o json markets search "$ARGUMENTS" --limit 3
2. Get midpoint price for the top result
3. Fetch price history: polymarket -o json clob price-history TOKEN --interval 1d
4. Check order book: polymarket -o json clob book TOKEN
5. Summarise: probability, trend, liquidity
