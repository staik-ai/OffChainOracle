## StaikOracle
Oracle to pull price information from multiple DEX sources

# step 1
Deploy MultiWrapper first:

This requires an array ["address"] of existing Wrappers on deployment  

For example 'WETH' contract on Ethereum or 'WXDAI' contract on Gnosis

# step 2 (optional)
Create your own "Per DEX" Oracle Contract (see the StaikSushiSwapV2Oracle.sol & StaikUniswapV3Oracle.sol contracts) if you don't have any already to use.  

To deploy the file, you'll need the FACTORY smart contract address of the DEX on which you are making the oracle (e.g. UniswapV2Factory) as well as the 'pairCodeHash' which can be obtained from the READ of the factory contract. This is used as the _INITCODEHASH value when deploying.

# step 3
Deploy StaikOracle:

This requires all of the following:

_MULTIWRAPPER: use address of contract deployed in step 1  

EXISTINGORACLES: use addresses [] of already deployed oracles (or deploy your own oracle based on a DEX (see step 2)  

ORACLETYPES: an array of oracle types [0 = uniswap v2 oracles]  

EXISTINGCONNECTORS: an array of addresses [] of token addresses for primary tokens such as WETH, WXDAI, USDC, WBTC, USDT  

WBASE: the primary wrapped token on the chain (e.g. WETH, WXDAI, WBNB)  


# Deployed contracts (Arbiscan)
Multiwrapper - https://arbiscan.io/address/0xe7c979982112175a81ced1f21004815c988c2300  
StaikSushiswapV2Oracle - https://arbiscan.io/address/0xb4008a9162a5427d6b142928b4e78ad09753c006  
StaikUniswapV3Oracle - https://arbiscan.io/address/0x84ac745e50e3b4440dc7479ad55044ae7d3d32ac  
StaikOracle - https://arbiscan.io/address/0x75256775f58105bfebb5ec1838e2e82352604561





