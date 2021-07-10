# Predeploy-Contracts
Predeploy `Setheum Ethereum Virtual Machine` (SEVM) Contracts
Generate bytecode for predeployment of ERC20 smart contracts in Setheum.

## 1. Build

Run `yarn` to install dependencies.

## 2. Generate bytecode

Generate bytecode for predeployment of ERC20 smart contracts in Setheum.

To generate bytecode, run `yarn run generate-bytecode`.

The generated bytecode JSON file would be `./resources/bytecodes.json`. The contracts are in `./contracts/tmp/` directory.

It can also be generated from the specified file, run `yarn run generate-bytecode [tokens.json path] [bytecodes.json output path]`

## 3. Development

The token list for ERC20 smart contracts is in `./resources/example_tokens.json`. Symbol and address are needed for each token, for instance:

```
{
  "symbol": "DNAR",
  "address": "0x0000000000000000000000000000000001000000"
}
```

# Predeployed System Contracts

## ERC20 Contracts
These ERC20 contracts make native and cross-chain tokens available inside SetheumEVM (SEVM).

- DNAR contract address: `0x0000000000000000000000000000000001000000`.
- DRAM contract address: `0x0000000000000000000000000000000001000001`.
- SETT contract address: `0x0000000000000000000000000000000001000002`.
- USDJ contract address: `0x0000000000000000000000000000000001000003`.
- EURJ contract address: `0x0000000000000000000000000000000001000004`.
- JPYJ contract address: `0x0000000000000000000000000000000001000005`.
- GBPJ contract address: `0x0000000000000000000000000000000001000006`.
- AUDJ contract address: `0x0000000000000000000000000000000001000007`.
- CADJ contract address: `0x0000000000000000000000000000000001000008`.
- CHFJ contract address: `0x0000000000000000000000000000000001000009`.
- SGDJ contract address: `0x0000000000000000000000000000000001000010`.
- BRLJ contract address: `0x0000000000000000000000000000000001000011`.
- SARJ contract address: `0x0000000000000000000000000000000001000012`.

- NEOM contract address: `0x0000000000000000000000000000000001000080`.
- MENA contract address:`0x0000000000000000000000000000000001000081`.
- NSETT contract address:`0x0000000000000000000000000000000001000082`.
- JUSD contract address: `0x0000000000000000000000000000000001000083`.
- JEUR contract address: `0x0000000000000000000000000000000001000084`.
- JJPY contract address: `0x0000000000000000000000000000000001000085`.
- JGBP contract address: `0x0000000000000000000000000000000001000086`.
- JAUD contract address: `0x0000000000000000000000000000000001000087`.
- JCAD contract address: `0x0000000000000000000000000000000001000088`.
- JCHF contract address: `0x0000000000000000000000000000000001000089`.
- JSGD contract address: `0x0000000000000000000000000000000001000090`.
- JBRL contract address: `0x0000000000000000000000000000000001000091`.
- JSAR contract address: `0x0000000000000000000000000000000001000092`.

- RENBTC contract address:  `0x0000000000000000000000000000000001000121`.

- LP_DNAR_SETT contract address: `0x0000000000000000000000010000000000000002`.
- LP_DRAM_SETT contract address: `0x0000000000000000000000010000000100000002`.
- LP_USDJ_SETT contract address: `0x0000000000000000000000010000000300000002`.
- LP_EURJ_SETT contract address: `0x0000000000000000000000010000000400000002`
- LP_JPYJ_SETT contract address: `0x0000000000000000000000010000000500000002`..
- LP_GBPJ_SETT contract address: `0x0000000000000000000000010000000600000002`.
- LP_AUDJ_SETT contract address: `0x0000000000000000000000010000000700000002`.
- LP_CADJ_SETT contract address: `0x0000000000000000000000010000000800000002`.
- LP_CHFJ_SETT contract address: `0x0000000000000000000000010000000900000002`.
- LP_SGDJ_SETT contract address: `0x0000000000000000000000010000001000000002`.
- LP_BRLJ_SETT contract address: `0x0000000000000000000000010000001100000002`.
- LP_SARJ_SETT contract address: `0x0000000000000000000000010000001200000002`.
- LP_RENBTC_SETT contract address: `0x0000000000000000000000010000012100000002`.

- LP_NEOM_NSETT contract address:   `0x0000000000000000000000010000008000000082`.
- LP_MENA_NSETT contract address:  `0x0000000000000000000000010000008100000082`.
- LP_JUSD_NSETT contract address:   `0x0000000000000000000000010000008300000082`.
- LP_JEUR_NSETT contract address:   `0x0000000000000000000000010000008400000082`.
- LP_JJPY_NSETT contract address:   `0x0000000000000000000000010000008500000082`.
- LP_JGBP_NSETT contract address:   `0x0000000000000000000000010000008600000082`.
- LP_JAUD_NSETT contract address:   `0x0000000000000000000000010000008700000082`.
- LP_JCAD_NSETT contract address:   `0x0000000000000000000000010000008800000082`.
- LP_JCHF_NSETT contract address:   `0x0000000000000000000000010000008900000082`.
- LP_JSGD_NSETT contract address:   `0x0000000000000000000000010000009000000082`.
- LP_JBRL_NSETT contract address:   `0x0000000000000000000000010000009100000082`.
- LP_JSAR_NSETT contract address:   `0x0000000000000000000000010000009200000082`.
- LP_RENBTC_NSETT contract address: `0x0000000000000000000000010000012100000082`.

```
// Returns the currencyId of the token.
function currencyId() public view returns (uint256);

// Returns the name of the token.
function name() public view returns (string memory);

// Returns the symbol of the token, usually a shorter version of the name.
function symbol() public view returns (string memory);

// Returns the number of decimals used to get its user representation.
function decimals() public view returns (uint8);

// Returns the amount of tokens in existence.
function totalSupply() public view returns (uint256);

// Returns the amount of tokens owned by `account`.
function balanceOf(address account) public view returns (uint256);

// Moves `amount` tokens from the caller's account to `recipient`.
// Returns a boolean value indicating whether the operation succeeded.
// Emits a {Transfer} event.
function transfer(address recipient, uint256 amount) public returns (bool);

// Returns the remaining number of tokens that `spender` will be allowed to spend on behalf of `owner` through {transferFrom}.
// This is zero by default.
function allowance(address owner, address spender) public view returns (uint256);

// Sets `amount` as the allowance of `spender` over the caller's tokens.
// Returns a boolean value indicating whether the operation succeeded.
function approve(address spender, uint256 amount) public returns (bool);

// Moves `amount` tokens from `sender` to `recipient` using the allowance mechanism. `amount` is then deducted from the caller's allowance.
// Returns a boolean value indicating whether the operation succeeded.
function transferFrom(address sender, address recipient, uint256 amount) public returns (bool);

// Atomically increases the allowance granted to `spender` by the caller.
// This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}.
// Emits an {Approval} event indicating the updated allowance.
function increaseAllowance(address spender, uint256 addedValue) public returns (bool);

// Atomically decreases the allowance granted to `spender` by the caller.
// This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}.
// Emits an {Approval} event indicating the updated allowance.
function decreaseAllowance(address spender, uint256 subtractedValue) public returns (bool);
```

## Other System Contracts:
These contracts make other chain-native functionalities available in SetheumEVM (SEVM).

### State Rent
- StateRent contract address: `0x0000000000000000000000000000000000000801`
```
// Returns the const of NewContractExtraBytes.
function newContractExtraBytes() public view returns (uint256);

// Returns the const of StorageDepositPerByte.
function storageDepositPerByte() public view returns (uint256);

// Returns the maintainer of the contract.
function maintainerOf(address contract_address) public view returns (address);

// Returns the const of DeveloperDeposit.
function developerDeposit() public view returns (uint256);

// Returns the const of DeploymentFee.
function deploymentFee() public view returns (uint256);

// Transfer the maintainer of the contract.
// Returns a boolean value indicating whether the operation succeeded.
function transferMaintainer(address contract_address, address new_maintainer) public returns (bool);
```

### Oracle Price Feed
- Oracle contract address: `0x0000000000000000000000000000000000000802`
```
// Get the price of the currency_id.
// Returns the (price, timestamp)
function getPrice(address token) public view returns (uint256, uint256);
```
### On-chain Automatic Scheduler
- ScheduleCall contract address: `0x0000000000000000000000000000000000000803`
```
// Schedule call the contract.
// Returns a boolean value indicating whether the operation succeeded.
function scheduleCall(address contract_address, uint256 value, uint256 gas_limit, uint256 storage_limit, uint256 min_delay, bytes memory input_data) public returns (bool);

// Cancel schedule call the contract.
// Returns a boolean value indicating whether the operation succeeded.
function cancelCall(bytes memory task_id) public returns (bool);

// Reschedule call the contract.
// Returns a boolean value indicating whether the operation succeeded.
function rescheduleCall(uint256 min_delay, bytes memory task_id) public returns (bool);
```

### DEX
- DEX contract address: `0x0000000000000000000000000000000000000804`
```
// Get liquidity of the currency_id_a and currency_id_b.
// Returns (liquidity_a, liquidity_b)
function getLiquidity(address tokenA, address tokenB) public view returns (uint256, uint256)

// Get swap target amount.
// Returns (target_amount)
function getSwapTargetAmount(address[] calldata path, uint256 supplyAmount) external view returns (uint256);

// Get swap supply amount.
// Returns (supply_amount)
function getSwapSupplyAmount(address[] calldata path, uint256 targetAmount) external view returns (uint256);

// Swap with exact supply.
// Returns a boolean value indicating whether the operation succeeded.
function swapWithExactSupply(address[] calldata path, uint256 supplyAmount, uint256 minTargetAmount) external returns (bool);

// Swap with exact target.
// Returns a boolean value indicating whether the operation succeeded.
function swapWithExactTarget(address[] calldata path, uint256 targetAmount, uint256 maxSupplyAmount) external returns (bool);

// Add liquidity to the trading pair.
// Returns a boolean value indicating whether the operation succeeded.
function addLiquidity(address tokenA, address tokenB, uint256 maxAmountA, uint256 maxAmountB) external returns (bool);

// Remove liquidity from the trading pair.
// Returns a boolean value indicating whether the operation succeeded.
function removeLiquidity(address tokenA, address tokenB, uint256 removeShare) external returns (bool);
```

## DeFi Contracts (Coming Soon)
These contracts will make Setheum's DeFi primitives (SettMint, SERP, SettPay) available in SetheumEVM (SEVM).
