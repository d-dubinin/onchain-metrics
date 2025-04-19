# On-Chain Metrics

A Python-based simple analytics project that fetches and analyzes the on chain data.

---

## Project Structure

### `alchemy_eth/alchemy.ipynb`
This Jupyter Notebook retrieves and analyzes Ethereum mainnet data using Alchemy's JSON-RPC endpoints.
### `pruned_node_btc/analysis.ipynb`
In this notebook we compute the basic metrics of bitcoin blockchain. In particular, we anaylyze the on chain activity during one day.

---

## TODO / Future Improvements

### alchemy_eth/alchemy.ipynb

1. **Explore Additional Data Providers**  
   Investigate alternative platforms to Alchemy as frequent requests can quickly exhaust the free tier. Some platforms may offer more cost effective or scalable options for accessing real-time data. For historical data and analytics we can consider using platforms like [Dune](https://dune.com/).

2. **Expand Historical Analysis**  
   Currently, the notebook focuses on analyzing a single block. We would like to extend the analysis to multiple blocks over time.

### Pruned_node_btc/analysis.ipynb

1. **Full node setup**
   In this project we used a pruned bitcoin node, which doesn't allow us to do a complete analysis of transactions. Indeed, we cannot access the transactions by theirs txid's. Once the full node is setup, we will to the following:
   
    - Get the exact number of active addresses
    - Clusters of addresses
    - Economic volume of BTC
    - Expand the analysis for all blocks
   



