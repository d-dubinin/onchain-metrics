# On-Chain Metrics

A Python-based simple analytics project that fetches and analyzes Ethereum on-chain metrics using [Alchemy](https://www.alchemy.com/) API endpoints. It aims to provide insight into blocks, validator withdrawals, and specific transactions (including ERC-20 transfer events) on the Ethereum blockchain.

---

## Project Structure

### `alchemy_eth/alchemy.ipynb`
This Jupyter Notebook retrieves and analyzes Ethereum mainnet data using Alchemy's JSON-RPC endpoints.

---

## Features & Analysis

### Block-Level Metrics
Fetch and display the following data about the latest Ethereum block:

- Miner address  
- Block number  
- Number of uncles (post-merge, these are deprecated)  
- Number of transactions  
- Gas metrics:  
  - Gas limit, gas used, gas target  
  - Percent over target  
- Base fee per gas  
- Burnt ETH in the block  
- Miners' rewards (fee-only, no consensus layer rewards)  
- Number of validator withdrawals  

### Validators Withdrawals
Extracts and presents validator withdrawal data for a given block:

- Validator index  
- Withdrawal address  
- Withdrawal amount (in ETH)  

### Transaction Analysis
Analyzes a specific Ethereum transaction:

- Transaction hash  
- From/To addresses (high-level contract names if applicable)  
- Base fee and effective gas price  
- Gas used, priority tip, total fees paid  
- Burnt ETH from the transaction  

### ERC-20 Event Log Parsing
Parses ERC-20 `Transfer` logs from the transaction receipt:

- Detects and decodes only logs matching the ERC-20 Transfer event signature  
- Fetches token metadata (name, symbol, decimals)  
- Outputs sender, receiver, token type, quantity, and removal status  

---

## TODO / Future Improvements

1. **Explore Additional Data Providers**  
   Investigate alternative platforms to Alchemy, as frequent requests can quickly exhaust the free tier. Some platforms may offer more cost-effective or scalable options for accessing real-time data. For historical and aggregated analytics, consider using platforms like [Dune](https://dune.com/), which provide queryable archives of on-chain data.

2. **Expand Historical Analysis**  
   Currently, the notebook focuses on analyzing a single block. Extending the analysis to cover multiple blocks over time would allow for more meaningful historical insights, trend analysis, and metric comparisons.

