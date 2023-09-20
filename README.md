# Euphoria Final Redemption

## Final redemption data

- Number of successful redemptions during the initial phase: 2,225 + 3 accounts for testing = 2,228 addresses in total that can claim during the final phase.
- Total remaining assets (USDC): 4,607,712.974 USDC - 100 USDC (safety margin for math + testing) = 4,607,612.974 USDC
- Total redeemable wsWAGMI: 34827.125448241370056726
- Redemption rate per wsWAGMI for the final phase: $132.3 per wsWAGMI

## Redemption instructions using Avalanche's Snowtrace Explorer:

1. You need AVAX in your wallet in order to interact with the redemption contract. You can purchase AVAX on most CEX:es.

2. To interact with the contract you usually only need a couple of cents worth of AVAX, but we recommend funding your wallet with at least 0.03 - 0.05 AVAX to perform the redemption and then having sufficient AVAX for gas to send the native USDC to a CEX or performing additional onchain activities.

3. Open the [claims.json](https://raw.githubusercontent.com/VenomProtocol/euphoria-manual-final-redemption/main/claims.json) file in a separate tab/window and search for your wallet address.

4. Pay attention to the `"amountIn"`, `"account"`, `"amount"`, and `"merkleProof"` variables and their respective values next your address / within the same surrounding `{}` block. You will need these values for the next steps.

5. [Open the redemption contract on Snowtrace](https://snowtrace.io/address/0x0b2E90054444D35f78E9134F018E7642525b56f2#writeContract) in a separate tab or window.

6. Click on `"Connect to Web3"` and connect MetaMask or your wallet of choice to Snowtrace. 

7. Click on `"2. exchangeForAssets"`

8. Now enter the values for the `"amountIn"`, `"account"`, `"amount"`, and `"merkleProof"` variables that matches your wallet in [claims.json](https://raw.githubusercontent.com/VenomProtocol/euphoria-manual-final-redemption/main/claims.json). **IMPORTANT: Enter the values without quotes.**

9. For the `"merkleProof"` field you need to combine the entire array/list into a single long string where every array/list member is separated by a comma. **IMPORTANT: Enter the values without quotes.**

10. Click on `"Write"` and sign the transaction using MetaMask or your wallet of choice.

11. If the redemption was successful you should now have received native USDC in your wallet on Avalanche. You can add native USDC to your MetaMask by going to [TraderJoe](https://traderjoexyz.com/trade), selecting `"USDC"` as the `"To"` token, then clicking on the `"Add USDC to Wallet"` link below the `"Enter an amount"` button. You can also add it directly in MetaMask as a custom token using the contract address `0xB97EF9Ef8734C71904D8002F8b6Bc66Dd9c48a6E`.

12. USDC is not the same as USDC.e which is the bridged version of USDC from Ethereum. Avalanche's native version of USDC is unfortunately not widely available on all CEX:es and you will have to pay attention to this when depositing. Otherwise you can end up losing your funds if you deposit to a CEX that does not support native Avalanche USDC.
