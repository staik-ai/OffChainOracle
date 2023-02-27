# OffChainOracle
Oracle to pull price information

#step 1
Deploy MultiWrapper first:

This requires an array ["address"] of existing Wrappers on deployment
For example 'WETH' contract on Ethereum or 'WXDAI' contract on Gnosis

#step 2
Deploy OffChainOracle second:

This requires all of the following:

_MULTIWRAPPER: use address of contract deployed in step 1
EXISTINGORACLES: use addresses [] of deployed oracles (or deploy your own oracle based on a DEX (see below)
ORACLETYPES: an array of oracle types [0 = uniswap v2 oracles]
EXISTINGCONNECTORS: an array of addresses [] of token addresses for primary tokens such as WETH, WXDAI, USDC, WBTC, USDT
WBASE: the primary wrapped token on the chain (e.g. WETH, WXDAI, WBNB)


# extra step (optional)
Create your own Oracle Contract (see the SushiSwapV2Oracle.sol contract



