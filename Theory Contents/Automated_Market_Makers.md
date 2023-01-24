# Automated Market Maker

An automated market maker (AMM) allows digital assets to be bought and sold automatically at market price on a decentralized exchange (DEX), without an intermediary. This can happen with liquidity from a liquidity pool on an AMM, where trades are secured by smart contracts on a peer-to-contract basis.

#

Include return parameters in NatSpec comments

If Return parameters are declared, you must prefix them with "/// @return".
Some code analysis programs do analysis by reading NatSpec details, if they can't see the "@return" tag, they do incomplete analysis.
Recommendation: Include return parameters in NatSpec comments
/// @notice information about what a function does
/// @param pageId The id of the page to get the URI for.
/// @return Returns a page's URI if it has been minted
