## OffChainOracle
Oracle to pull price information

# step 1
Deploy MultiWrapper first:

This requires an array ["address"] of existing Wrappers on deployment  

For example 'WETH' contract on Ethereum or 'WXDAI' contract on Gnosis

# step 2 (optional)
Create your own Oracle Contract (see the SushiSwapV2Oracle.sol contract) if you don't have one already to use.  

To deploy the file, you'll need the FACTORY smart contract address of the DEX on which you are making the oracle (e.g. UniswapV2Factory) as well as the 'pairCodeHash' which can be obtained from the READ of the factory contract. This is used as the _INITCODEHASH value when deploying.

# step 3
Deploy OffChainOracle second:

This requires all of the following:

_MULTIWRAPPER: use address of contract deployed in step 1  

EXISTINGORACLES: use addresses [] of already deployed oracles (or deploy your own oracle based on a DEX (see step 2)  

ORACLETYPES: an array of oracle types [0 = uniswap v2 oracles]  

EXISTINGCONNECTORS: an array of addresses [] of token addresses for primary tokens such as WETH, WXDAI, USDC, WBTC, USDT  

WBASE: the primary wrapped token on the chain (e.g. WETH, WXDAI, WBNB)  





