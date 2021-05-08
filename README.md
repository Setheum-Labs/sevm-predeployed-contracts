# S-EVM-Predeployed-Contracts
`Setheum Ethereum Virtual Machine` (SEVM) Contracts

## 1. Build

Run `yarn` to install dependencies.

## 2. Generate bytecode

Generate bytecode for predeployment of ERC20 smart contracts in Setheum.

To generate bytecode, run `yarn run generate-bytecode`.

The generated bytecode JSON file would be `./resources/bytecodes.json`. The contracts are in `./contracts/tmp/` directory.

It can also be generated from the specified file, run `yarn run generate-bytecode [tokens.json path] [bytecodes.json output path]`

## 3. Development

The token list for ERC20 smart contracts is in `./resources/example_tokens.json`. Name, symbol and Currency ID bytes are needed for each token, for instance:

```
{
  "name": "DNAR",
  "symbol": "DNAR",
  "currencyId": "0x0000"
}
```
