# Contract Interaction

## **Deployed Contract Address**

<table><thead><tr><th width="288">Contract</th><th>Address</th></tr></thead><tbody><tr><td>PooledStakingManagerProxy</td><td><a href="https://etherscan.io/address/0x1AAa3D9f104117f06eD815cEcc9ef0C6a831c67F">0x1AAa3D9f104117f06eD815cEcc9ef0C6a831c67F</a></td></tr><tr><td>PooledStakingManagerLogic</td><td><a href="https://etherscan.io/address/0xd08b01d2e68D293DDaf6341E1b3BAd8eAa1F1530">0xd08b01d2e68D293DDaf6341E1b3BAd8eAa1F1530</a></td></tr><tr><td>PooledStakingWalletProxy</td><td><a href="https://etherscan.io/address/0xbf3B82a68631fB85e611c57eB6F0d75bEae12765">0xbf3B82a68631fB85e611c57eB6F0d75bEae12765</a></td></tr><tr><td>PooledStakingWalletLogic</td><td><a href="https://etherscan.io/address/0xb06e11d487845ed780702cd87125efc4cf518fec">0xb06e11d487845ed780702cd87125efc4cf518fec</a></td></tr></tbody></table>

## **Deposit**

1. call the `depositETH(bytes32 tag)` function with a specific tag to deposit ETH into the pool
2. call the `userStatusMap(address user)` view function to query user status
3. wait for the rewards

## Exit

1. ensure that 7 days have passed since last deposit
2. call the `userStatusMap(address user)` view function to query how many points could be used to redeem ETH
3. call the `withdrawETH(uint256 point)` function to withdraw ETH (**note:** the maximum of the input is the `userStatus.point` in step.2)
4. if the balance in **PooledStakingWallet Contract** is sufficient, the corresponding ETH will be sent to user wallet directly after waiting for a maximum of seven days

## Query

call the `calcPoint(uint256 ethAmount)` / `calcETH(uint256 point)` view function to calculate how many points/ETHs could change from a specific quantity of ETHs/points

