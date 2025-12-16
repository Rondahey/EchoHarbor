# EchoHarbor

Built for Base

EchoHarbor is a small Base-aligned repository intended for quick verification of wallet onboarding and read-only onchain access on Base networks. The goal is to keep things simple while still being explicit about chain selection, chainId expectations, and explorer visibility.

## What This Repo Is For

- Base network sanity checks (RPC chainId, latest block)
- Basic account reads (native ETH balance)
- Wallet connection UX via OnchainKit
- Clear Basescan references for deployments and verification

## Libraries

OnchainKit  
https://github.com/coinbase/onchainkit  

Viem  
EVM client used for Base JSON-RPC reads

## Project Layout

app/  
- echoHarbor.ts  
  React component that wires OnchainKit wallet UI to Viem reads on Base.

Typical supporting files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

## Networks

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

## Running

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run with a standard React/Vite or Next.js dev server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

Usage:
- Select Base Sepolia (84532) for test reads or Base Mainnet (8453) for mainnet reads
- Connect a wallet using the OnchainKit Wallet UI
- Paste an address to query balance
- Run the probe and review chainId + block + balance outputs

## License

MIT License

## Author

GitHub: https://github.com/Rondahey

Public contact (email): neater-caustic.0j@icloud.com

Public contact (X): https://x.com//medonader2002

## References

createBaseAccount reference:  
https://docs.base.org/base-account/reference/core/createBaseAccount?utm_source=chatgpt.com

Account Abstraction on Base:  
https://docs.base.org/base-chain/tools/account-abstraction?utm_source=chatgpt.com

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0x81466cb4df625e41957602ee4ca7d8fba344c19a 

Deployment and verification:
- https://sepolia.basescan.org/address/0x81466cb4df625e41957602ee4ca7d8fba344c19a 
- https://sepolia.basescan.org/0x81466cb4df625e41957602ee4ca7d8fba344c19a /0#code  

Contract #2 address:  
0x201f4a7776c719545fb4fad48876e9c7ae413fa0

Deployment and verification:
- https://sepolia.basescan.org/address/0x201f4a7776c719545fb4fad48876e9c7ae413fa0
- https://sepolia.basescan.org/0x201f4a7776c719545fb4fad48876e9c7ae413fa0/0#code  

Contract #3 address:  
0x2bff962343a9094f6021535311f6436059677a33

Deployment and verification:
- https://sepolia.basescan.org/address/0x2bff962343a9094f6021535311f6436059677a33
- https://sepolia.basescan.org/0x2bff962343a9094f6021535311f6436059677a33/0#code 
These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.

