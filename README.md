# DLT and Blockchain Knowledge Hub

> **A practical introduction to Distributed Ledger Technology (DLT), blockchain, cryptocurrencies, stablecoins, programmable money, tokenization and institutional digital finance.**

This repository is a personal learning and reference hub designed for readers who may be new to DLT and blockchain, as well as recruiters, hiring managers and executives who want a concise view of how these technologies are changing financial services.

The content moves in a deliberate order:

**DLT fundamentals → Blockchain → Network models → Cryptocurrencies → Stablecoins → Smart contracts → Tokens → Tokenization → Tokenized deposits → Institutional adoption → Solidity / ERC hands-on examples**

---

## Table of Contents

1. [Purpose of this Repository](#1-purpose-of-this-repository)
2. [Distributed Ledger Technology (DLT)](#2-distributed-ledger-technology-dlt)
   - [2.1 What is DLT?](#21-what-is-dlt)
   - [2.2 Why is DLT useful?](#22-why-is-dlt-useful)
   - [2.3 Main DLT architectures](#23-main-dlt-architectures)
   - [2.4 How DLT enables cryptocurrencies](#24-how-dlt-enables-cryptocurrencies)
3. [Blockchain Fundamentals](#3-blockchain-fundamentals)
   - [3.1 What is blockchain?](#31-what-is-blockchain)
   - [3.2 How a blockchain transaction works](#32-how-a-blockchain-transaction-works)
   - [3.3 Benefits of blockchain](#33-benefits-of-blockchain)
   - [3.4 Limitations and considerations](#34-limitations-and-considerations)
4. [Blockchain Network Models](#4-blockchain-network-models)
   - [4.1 Permissionless / public blockchain](#41-permissionless--public-blockchain)
   - [4.2 Permissioned / private blockchain](#42-permissioned--private-blockchain)
   - [4.3 Consortium / federated blockchain](#43-consortium--federated-blockchain)
   - [4.4 Hybrid models](#44-hybrid-models)
5. [Cryptocurrencies](#5-cryptocurrencies)
   - [5.1 What is a cryptocurrency?](#51-what-is-a-cryptocurrency)
   - [5.2 How cryptocurrency transactions work](#52-how-cryptocurrency-transactions-work)
   - [5.3 Cryptocurrency vs traditional bank money](#53-cryptocurrency-vs-traditional-bank-money)
6. [Stablecoins](#6-stablecoins)
   - [6.1 What is a stablecoin?](#61-what-is-a-stablecoin)
   - [6.2 How stablecoins work](#62-how-stablecoins-work)
   - [6.3 Main stablecoin models](#63-main-stablecoin-models)
   - [6.4 Stablecoins vs cryptocurrencies](#64-stablecoins-vs-cryptocurrencies)
7. [Programmable Money and Smart Contracts](#7-programmable-money-and-smart-contracts)
   - [7.1 What is programmable money?](#71-what-is-programmable-money)
   - [7.2 What is a smart contract?](#72-what-is-a-smart-contract)
   - [7.3 Atomicity, DvP and PvP](#73-atomicity-dvp-and-pvp)
8. [Tokens and Token Standards](#8-tokens-and-token-standards)
   - [8.1 What is a token?](#81-what-is-a-token)
   - [8.2 Fungible tokens](#82-fungible-tokens)
   - [8.3 Non-fungible tokens (NFTs)](#83-non-fungible-tokens-nfts)
   - [8.4 Semi-fungible / multi-token models](#84-semi-fungible--multi-token-models)
   - [8.5 ERC-20](#85-erc-20)
   - [8.6 ERC-721](#86-erc-721)
   - [8.7 ERC-1155](#87-erc-1155)
9. [Asset Tokenization and Real-World Assets (RWAs)](#9-asset-tokenization-and-real-world-assets-rwas)
   - [9.1 What is tokenization?](#91-what-is-tokenization)
   - [9.2 What can be tokenized?](#92-what-can-be-tokenized)
   - [9.3 Tokenization lifecycle](#93-tokenization-lifecycle)
   - [9.4 Benefits of RWA tokenization](#94-benefits-of-rwa-tokenization)
   - [9.5 Important legal distinction](#95-important-legal-distinction)
10. [Tokenized Deposits](#10-tokenized-deposits)
    - [10.1 What is a tokenized deposit?](#101-what-is-a-tokenized-deposit)
    - [10.2 How tokenized deposits work](#102-how-tokenized-deposits-work)
    - [10.3 Benefits](#103-benefits)
    - [10.4 Where they can be used](#104-where-they-can-be-used)
    - [10.5 Tokenized deposits vs stablecoins](#105-tokenized-deposits-vs-stablecoins)
11. [Tokenized Financial System and Settlement](#11-tokenized-financial-system-and-settlement)
    - [11.1 Tokenized money and tokenized assets](#111-tokenized-money-and-tokenized-assets)
    - [11.2 Simple tokenized bond DvP example](#112-simple-tokenized-bond-dvp-example)
12. [How Financial Institutions are Adopting DLT](#12-how-financial-institutions-are-adopting-dlt)
    - [12.1 Why regulated institutions often prefer controlled networks](#121-why-regulated-institutions-often-prefer-controlled-networks)
    - [12.2 Selected institutional examples](#122-selected-institutional-examples)
13. [Solidity Basics](#13-solidity-basics)
    - [13.1 What is Solidity?](#131-what-is-solidity)
    - [13.2 Basic Solidity concepts](#132-basic-solidity-concepts)
    - [13.3 ERC-20 educational example](#133-erc-20-educational-example)
    - [13.4 ERC-721 educational example](#134-erc-721-educational-example)
    - [13.5 ERC-1155 educational example](#135-erc-1155-educational-example)
14. [Hands-on Learning Environment](#14-hands-on-learning-environment)
15. [Key Takeaways](#15-key-takeaways)
16. [Official References](#16-official-references)
17. [Disclaimer](#17-disclaimer)

---

# 1. Purpose of this Repository

The purpose of this repository is to explain the foundations of DLT and blockchain in simple financial-services language.

By the end of the page, a reader should understand:

- What DLT and blockchain are.
- Why distributed ledgers can be useful.
- The difference between permissionless, permissioned and consortium networks.
- How cryptocurrencies and stablecoins work.
- What programmable money and smart contracts mean.
- The difference between fungible and non-fungible tokens.
- What tokenization and Real-World Assets (RWAs) mean.
- What tokenized deposits are and how they differ from stablecoins.
- Why financial institutions are experimenting with or deploying DLT.
- How ERC-20, ERC-721 and ERC-1155 tokens can be represented in Solidity.

[Back to top](#table-of-contents)

---

# 2. Distributed Ledger Technology (DLT)

## 2.1 What is DLT?

**Distributed Ledger Technology (DLT)** is a way for multiple participants to maintain and share a synchronized record of transactions or data.

In a conventional system, one organisation may own and operate the central database. In a distributed-ledger model, multiple authorised or participating nodes can hold and validate copies of the ledger according to agreed rules.

DLT is therefore a broader technology category. **Blockchain is one type of DLT, but not every DLT is a blockchain.**

### Simple comparison

```text
Traditional model

Bank A ──► Central Database ◄── Bank B
                  ▲
                  │
                Bank C
```

```text
DLT model

Bank A Node ◄────► Bank B Node
     ▲                 ▲
     │   Shared /      │
     │ synchronized    │
     │     ledger      │
     ▼                 ▼
Bank C Node ◄────► Bank D Node
```

## 2.2 Why is DLT useful?

DLT can be useful where several organisations need to coordinate around the same transaction or asset.

| Benefit | Simple meaning | Financial example |
|---|---|---|
| **Shared ledger** | Participants work from a common or synchronized record | Banks sharing settlement information |
| **Reduced reconciliation** | Fewer independent databases need to be matched | Securities settlement |
| **Immutability / integrity** | Confirmed records are difficult to alter without detection | Audit trail |
| **Traceability** | Transactions can be followed through their lifecycle | Asset provenance |
| **Programmability** | Business rules can execute automatically | Conditional payment |
| **Atomicity** | Linked transaction legs can complete together | Bond versus cash settlement |
| **Availability** | Some networks can operate continuously | 24/7 digital-value transfer |
| **Tokenization** | Assets and money can be represented digitally | Tokenized bonds or deposits |

DLT does **not** automatically make every process faster, cheaper or safer. Legal design, privacy, governance, interoperability, scalability, cyber security and operating models remain critical.

## 2.3 Main DLT architectures

### 2.3.A Blockchain

Blockchain records transactions in blocks that are cryptographically linked in sequence.

**Most useful in:** digital assets, payments, tokenization, securities, settlement, supply chain and situations where a strong shared audit trail is useful.

Examples include public blockchains such as **Bitcoin and Ethereum**, as well as enterprise blockchain implementations.

### 2.3.B Directed Acyclic Graph (DAG)

A DAG can allow transactions to reference other transactions without requiring all activity to be grouped into a single sequential chain of blocks.

**Most useful in:** high-volume transaction environments, Internet of Things (IoT), machine-to-machine interactions and micropayment-style use cases.

Different DAG implementations use different validation and consensus approaches.

### 2.3.C Hashgraph

Hashgraph is a distributed-consensus architecture that does not use the conventional sequential block structure of a blockchain.

It aims to support fast consensus and high transaction throughput.

**Most useful in:** enterprise applications, payments, tokenization, identity, supply-chain and high-throughput distributed applications.

### 2.3.D Holochain

Holochain uses an **agent-centric** design. Each participant maintains their own activity history and shares relevant data according to application rules rather than relying on one global ledger.

**Most useful in:** peer-to-peer applications, community platforms, distributed identity and user-controlled data-sharing ecosystems.

It is generally less associated with institutional financial settlement than blockchain-based DLTs.

## 2.4 How DLT enables cryptocurrencies

DLT provides much of the infrastructure that allows cryptocurrencies to operate without a conventional central account database.

A typical crypto network uses:

1. **A distributed ledger** to record balances or transactions.
2. **Cryptography** to protect ownership and authorize transactions.
3. **Wallet addresses** to identify destinations.
4. **Private keys / digital signatures** to prove authority to spend.
5. **Consensus** so network participants agree on valid transactions.
6. **Network nodes / validators / miners** to process and confirm activity.

```text
Alice's Wallet
      │
      │ Signed transaction
      ▼
Blockchain Network
      │
      │ Validation + consensus
      ▼
Shared Ledger Updated
      │
      ▼
Bob's Wallet
```

DLT is therefore the **underlying record-keeping and consensus environment**, while cryptocurrency is a **digital asset that operates within that environment**.

[Back to top](#table-of-contents)

---

# 3. Blockchain Fundamentals

## 3.1 What is blockchain?

A blockchain is a type of distributed ledger in which validated transactions are grouped into blocks.

Each block contains information that cryptographically links it to an earlier block, producing a chain of historical records.

Changing historical information would affect the cryptographic relationships between blocks, making unauthorized alteration difficult to conceal.

Blockchain can be used for much more than cryptocurrency. It can also record asset ownership, financial transactions, identity information, contractual events and settlement instructions.

## 3.2 How a blockchain transaction works

```text
1. User creates transaction
          ↓
2. Transaction is digitally signed
          ↓
3. Transaction is broadcast / submitted
          ↓
4. Network validates transaction
          ↓
5. Consensus / ordering occurs
          ↓
6. Transaction is recorded
          ↓
7. Ledger state is updated
```

For a token transfer, the blockchain may record:

```text
From:       0xAlice...
To:         0xBob...
Token:      Example Token
Amount:     100
Tx Hash:    0x123ABC...
Block:      123456
Status:     Successful
```

## 3.3 Benefits of blockchain

### A. Shared transaction record
Multiple parties can rely on a common ledger instead of maintaining completely separate records.

### B. Traceability
Transfers can be followed through an auditable transaction history.

### C. Integrity
Cryptographic mechanisms protect the relationship between transactions and ledger state.

### D. Programmability
Smart contracts can automatically execute predefined rules.

### E. Tokenization
Money, financial instruments and other assets can be represented digitally.

### F. Atomic settlement
Blockchain can help coordinate the simultaneous exchange of tokenized money and tokenized assets.

### G. Extended operating availability
Some blockchain networks can process activity continuously rather than being restricted to traditional processing windows.

## 3.4 Limitations and considerations

Blockchain is not automatically the best architecture for every business problem.

Key considerations include:

- Privacy and data confidentiality.
- Regulatory and legal recognition.
- Governance.
- Scalability and transaction throughput.
- Cyber security and key management.
- Operational resilience.
- Interoperability with existing systems.
- Transaction costs.
- Data-quality responsibility.
- Smart-contract risk.
- Settlement finality.
- Identity and access management.

For regulated finance, technology must operate together with **legal rights, governance, compliance and operational controls**.

[Back to top](#table-of-contents)

---

# 4. Blockchain Network Models

The terms **public/private**, **permissionless/permissioned** and **consortium** describe how a network is accessed and governed. They are not separate forms of cryptography.

## 4.1 Permissionless / public blockchain

Anyone can generally access the network, submit transactions and inspect public ledger activity. Participation in validation depends on the protocol.

**Examples:** Bitcoin and Ethereum.

### Typical strengths

- Open participation.
- Large developer ecosystems.
- Public verifiability.
- Composability between applications.

### Typical challenges for financial institutions

- Privacy.
- Regulatory controls.
- Identity.
- Transaction governance.
- Public visibility of activity.
- Dependence on public-network economics and technical rules.

## 4.2 Permissioned / private blockchain

Access is restricted to approved organisations, users or validator nodes.

The operator or governance body can define:

- Who can connect.
- Who can transact.
- Who can validate.
- Who can see particular data.
- What compliance controls must apply.

**Common use cases:** institutional payments, digital securities, collateral, trade finance and regulated tokenized assets.

## 4.3 Consortium / federated blockchain

A consortium blockchain is governed collectively by a group of organisations rather than by a single company.

```text
Bank A ─┐
Bank B ─┼──► Shared Institutional DLT
Bank C ─┤
FMI    ─┘
```

Each institution operates under common network rules, technical standards and governance.

**Common use cases:** interbank settlement, cross-border payments, securities markets, shared KYC processes and collateral mobility.

## 4.4 Hybrid models

Institutional finance does not always fit neatly into "public" or "private".

A hybrid architecture may use:

- A public blockchain for token records.
- Permissioning for eligible investors.
- Private data channels for confidential information.
- Off-chain systems for KYC and compliance.
- Traditional payment rails for the cash leg.
- DLT for asset settlement.

The future financial ecosystem is therefore likely to be **multi-ledger and interoperable**, rather than based on one universal blockchain.

[Back to top](#table-of-contents)

---

# 5. Cryptocurrencies

## 5.1 What is a cryptocurrency?

A cryptocurrency is a digital asset whose ownership and transfer are normally recorded using blockchain or another distributed-ledger network.

Examples include **Bitcoin (BTC)** and **Ether (ETH)**.

Unlike normal bank deposits, many cryptocurrencies are not liabilities of a commercial bank or central bank.

Their market value can therefore move significantly based on supply, demand and market conditions.

## 5.2 How cryptocurrency transactions work

```text
Alice Wallet
    │
    │ Create + sign transaction
    ▼
Blockchain
    │
    │ Validators confirm
    ▼
Ledger Updated
    │
    ▼
Bob Wallet
```

Typical blockchain transaction information includes:

- Sender wallet address.
- Receiver wallet address.
- Amount.
- Network.
- Transaction hash.
- Network fee.
- Block number.
- Confirmation / finality status.

## 5.3 Cryptocurrency vs traditional bank money

| Characteristic | Traditional Bank Deposit | Cryptocurrency |
|---|---|---|
| Issuer / liability | Commercial bank | Usually protocol/native digital asset |
| Unit | GBP, EUR, USD etc. | BTC, ETH etc. |
| Record | Bank ledger | Blockchain / DLT |
| Transfer authority | Bank/payment system | Network protocol |
| Price stability | Fiat-denominated | Can be highly volatile |
| Identity model | Account + regulated KYC | Wallet/address model, with regulation varying by service |
| Settlement | Banking/payment infrastructure | Blockchain network |

[Back to top](#table-of-contents)

---

# 6. Stablecoins

## 6.1 What is a stablecoin?

A stablecoin is a digital token designed to maintain a relatively stable value against a reference asset, most commonly a fiat currency such as USD, EUR or GBP.

```text
1 USD-referenced stablecoin
            ≈
          USD 1
```

Stablecoins are generally designed to provide blockchain-based transferability without the price volatility associated with unbacked cryptocurrencies such as Bitcoin.

## 6.2 How stablecoins work

A simplified fiat-backed model is:

```text
Customer provides $1,000
          ↓
Stablecoin Issuer
          ↓
Backing assets / reserves
          ↓
Issuer creates 1,000 tokens
          ↓
Customer Wallet
```

For redemption:

```text
Customer returns 1,000 tokens
          ↓
Tokens redeemed / burned
          ↓
Issuer returns $1,000
```

The strength of the stablecoin depends on factors such as the quality of backing assets, legal claim, liquidity, redemption arrangements, governance and regulation.

## 6.3 Main stablecoin models

### 6.3.A Fiat / reserve-backed
Backed by assets such as cash, bank deposits or high-quality short-term securities.

### 6.3.B Crypto-collateralised
Backed by cryptocurrency or other digital assets, commonly with over-collateralisation.

### 6.3.C Algorithmic
Attempts to maintain price stability using protocol rules and incentives rather than full reserve backing.

These designs can carry materially different risk profiles.

## 6.4 Stablecoins vs cryptocurrencies

| Topic | Stablecoin | Unbacked Cryptocurrency |
|---|---|---|
| Main objective | Stable digital value | Native digital asset |
| Typical reference | USD / EUR / GBP | No fiat peg |
| Backing | Often reserve assets | Typically no external backing |
| Price volatility | Designed to be limited | Can be high |
| Typical uses | Payments, settlement, crypto liquidity | Investment, transfer, network usage |
| Example concept | 1 token ≈ $1 | 1 BTC = market price |

A stablecoin is therefore a **type of cryptoasset / digital token**, but not every cryptocurrency is a stablecoin.

[Back to top](#table-of-contents)

---

# 7. Programmable Money and Smart Contracts

## 7.1 What is programmable money?

Programmable money is digital money that can interact with software-based conditions.

Instead of only saying:

> "Transfer £1,000 from A to B"

A programmable transaction can say:

> "Transfer £1,000 from A to B **only if agreed conditions are satisfied**."

Potential conditions include successful delivery of an asset, completion of KYC, approval by multiple parties, a particular date/time, availability of collateral, or completion of another transaction leg.

## 7.2 What is a smart contract?

A **smart contract** is software deployed on a programmable ledger that automatically applies predefined rules.

```text
Buyer has £1,000?                YES
Seller owns 10 bond tokens?      YES
Buyer is eligible investor?      YES
Transaction permitted?           YES
                │
                ▼
        Execute settlement
```

Smart contracts can support token creation, transfers, balance checks, investor restrictions, asset locking, escrow, coupon/dividend logic, redemption and atomic settlement.

A smart contract does not replace legal agreements, regulation or governance. It automates parts of the business logic.

## 7.3 Atomicity, DvP and PvP

**Atomicity** means that linked actions complete together or fail together.

### Delivery versus Payment (DvP)

```text
Tokenized Bond ───────► Buyer
       AND
Tokenized Money ──────► Seller
```

Either both legs settle or neither settles.

### Payment versus Payment (PvP)

```text
GBP ─────► Party B
 AND
EUR ─────► Party A
```

This can reduce principal risk in securities and FX settlement.

[Back to top](#table-of-contents)

---

# 8. Tokens and Token Standards

## 8.1 What is a token?

A token is a digital representation of value, ownership, rights or access recorded on a programmable ledger.

A token may represent a cryptocurrency, money, a share, a bond, a fund unit, gold, a unique physical asset or access to a service.

The **technology creates the digital representation**, while legal and contractual arrangements determine what rights the token actually gives its holder.

## 8.2 Fungible tokens

Fungible tokens are interchangeable.

```text
1 Token A = another 1 Token A
```

Potential examples include stablecoins, tokenized deposits, tokenized grams of pooled gold and reward points.

On Ethereum-compatible networks, **ERC-20** is the common fungible-token interface.

## 8.3 Non-fungible tokens (NFTs)

A non-fungible token represents a distinct item or record.

```text
Token ID 101 = Gold Bar Serial GB-001
Token ID 102 = Gold Bar Serial GB-002
```

The two token IDs are not interchangeable because they identify different assets.

**ERC-721** is the standard Ethereum interface most associated with NFTs.

## 8.4 Semi-fungible / multi-token models

A single smart contract may need to manage multiple token types.

```text
Token ID 1 = Gold Units
Token ID 2 = Silver Units
Token ID 3 = Unique Certificate
Token ID 4 = Membership Pass
```

**ERC-1155** supports multiple token types in one contract and can represent fungible, non-fungible or semi-fungible structures.

## 8.5 ERC-20

**ERC-20** defines a standard interface for fungible tokens.

Common functions/concepts include `totalSupply()`, `balanceOf()`, `transfer()`, `approve()`, `transferFrom()`, the `Transfer` event and the `Approval` event.

Simple use case:

> **1 token = 1 gram of gold from a pooled reserve**

## 8.6 ERC-721

**ERC-721** is designed for individually distinguishable tokens. Each token has a unique `tokenId`.

Simple use case:

> **Token ID 1 = one specific 1 kg gold bar with a unique serial number**

Other potential use cases include certificates, collectibles and unique asset records.

## 8.7 ERC-1155

**ERC-1155** is a multi-token standard.

One contract can manage many token IDs with different supplies and characteristics.

It supports efficient batch transfers and can combine fungible and non-fungible token models.

Simple use case:

> A single luxury-asset contract manages multiple product types, certificates or editions.

[Back to top](#table-of-contents)

---

# 9. Asset Tokenization and Real-World Assets (RWAs)

## 9.1 What is tokenization?

Tokenization is the process of creating a digital representation of an asset, claim or right on a programmable ledger.

The Bank for International Settlements describes tokenisation as the digital representation of assets on programmable platforms.

```text
Traditional Government Bond
             ↓
      Legal / Asset Link
             ↓
       Digital Token
             ↓
     DLT / Blockchain
```

Tokenization can apply to digitally native financial instruments or to existing real-world / traditional financial assets.

## 9.2 What can be tokenized?

| Asset class | Tokenized representation |
|---|---|
| Government bonds | Bond/security token |
| Corporate bonds | Debt token |
| Equities | Tokenized share |
| Investment funds | Tokenized fund unit |
| Money-market funds | Tokenized fund share |
| Gold | Gold-backed token |
| Real estate | Ownership/investment token |
| Private credit | Tokenized credit exposure |
| Collateral | Tokenized entitlement / collateral record |

## 9.3 Tokenization lifecycle

```text
1. Identify asset
       ↓
2. Verify ownership / value
       ↓
3. Define legal rights
       ↓
4. Arrange custody
       ↓
5. Design token model
       ↓
6. Deploy smart contract / ledger logic
       ↓
7. Mint / issue tokens
       ↓
8. Distribute to eligible holders
       ↓
9. Transfer / trade / settle
       ↓
10. Service asset
       ↓
11. Redeem / mature / burn token
```

## 9.4 Benefits of RWA tokenization

Potential benefits include:

- Faster issuance and settlement.
- More automation.
- Improved transparency and traceability.
- Reduced reconciliation.
- Fractionalisation where legally permitted.
- Extended market operating hours.
- Programmable compliance.
- Improved collateral mobility.
- Atomic DvP.
- Potential access to new distribution channels.

Actual benefits depend on regulation, market structure, liquidity, interoperability and legal enforceability.

## 9.5 Important legal distinction

Creating a blockchain token **does not automatically create legal ownership of the real-world asset**.

For a valid financial or RWA tokenization model, the ecosystem must define:

- What legal right the token represents.
- Who owns or safeguards the underlying asset.
- How the token maps to the legal register.
- Who may hold or transfer the token.
- What happens during redemption.
- What happens if the issuer/custodian fails.

Technology and legal rights must therefore be designed together.

[Back to top](#table-of-contents)

---

# 10. Tokenized Deposits

## 10.1 What is a tokenized deposit?

A **tokenized deposit** is a commercial-bank deposit represented on a programmable or tokenized ledger.

It remains a **liability of the issuing commercial bank** and is designed to be redeemable or transferable at par with ordinary deposits.

```text
Traditional bank account
Santosh: GBP 10,000
          ↓
Tokenized representation
          ↓
GBP 10,000 tokenized bank deposit
```

It is therefore different from Bitcoin and structurally different from many non-bank stablecoins.

## 10.2 How tokenized deposits work

```text
Customer deposits / holds GBP
          ↓
Commercial Bank
          ↓
Bank issues / represents value
as tokenized deposits
          ↓
Programmable DLT
          ↓
Transfer / payment / settlement
          ↓
Receiver / another participant
```

Depending on the design, transfers between different banks may also require an interbank settlement mechanism using central-bank money, tokenized reserves or another agreed settlement asset.

## 10.3 Benefits

### A. 24/7 value transfer
Programmable infrastructure can support continuous technical availability.

### B. Programmability
Payment can depend on predefined business conditions.

### C. Atomic settlement
Tokenized deposits can potentially settle simultaneously against tokenized securities.

### D. Reduced reconciliation
Money and transaction information can be coordinated on shared infrastructure.

### E. Cross-border innovation
Tokenized deposits are being explored for faster and more efficient international payments.

### F. Compatibility with commercial-bank money
The instrument remains a claim against the issuing bank rather than becoming an unbacked cryptocurrency.

## 10.4 Where they can be used

Potential and emerging uses include:

- Domestic payments.
- Cross-border payments.
- Corporate treasury.
- Securities settlement.
- Tokenized bond purchases.
- Tokenized fund settlement.
- Collateral transactions.
- Conditional / programmable payments.
- Wholesale financial-market transactions.

Tokenized deposits remain an emerging form of money. Their use is currently much more concentrated in institutional pilots and wholesale settings than in everyday consumer payments.

## 10.5 Tokenized deposits vs stablecoins

| Characteristic | Tokenized Deposit | Stablecoin |
|---|---|---|
| Issuer | Commercial bank | Stablecoin issuer; structure varies |
| Holder's claim | Deposit claim on bank | Depends on issuer/legal structure |
| Economic basis | Commercial-bank money | Token referencing an asset/currency |
| Typical backing | Bank balance sheet / deposit framework | Reserve assets under issuer model |
| Ledger | Programmable ledger / DLT | Commonly blockchain |
| Main emerging use | Institutional payments and settlement | Crypto markets, payments, settlement |
| Regulatory treatment | Banking/deposit framework + digital rules | Stablecoin/payment/crypto framework varies by jurisdiction |

[Back to top](#table-of-contents)

---

# 11. Tokenized Financial System and Settlement

## 11.1 Tokenized money and tokenized assets

A tokenized financial ecosystem needs both:

```text
TOKENIZED MONEY
Tokenized deposit / central-bank money / stablecoin
                  +
TOKENIZED ASSET
Bond / fund / share / Treasury / RWA
                  ↓
             SETTLEMENT
```

Tokenization becomes most powerful when **money, assets and business rules can interact on interoperable programmable infrastructure**.

The BIS has described a future architecture combining tokenized central-bank reserves, tokenized commercial-bank money and tokenized government bonds on programmable infrastructure.

## 11.2 Simple tokenized bond DvP example

Suppose a buyer purchases a tokenized bond for £10,000.

```text
BUYER                         SELLER
  │                              │
  │ £10,000 Tokenized Deposit    │ Bond Token
  │                              │
  └─────────┐            ┌───────┘
            ▼            ▼
        Smart Contract /
       Settlement Engine
              │
       Check conditions
              │
        Atomic DvP
              │
      ┌───────┴─────────┐
      ▼                 ▼
Buyer receives       Seller receives
Bond Token           £10,000
```

If one side cannot complete, the other side should not complete either.

This is one of the clearest practical examples of how DLT, smart contracts, tokenized money and tokenized assets can work together.

[Back to top](#table-of-contents)

---

# 12. How Financial Institutions are Adopting DLT

## 12.1 Why regulated institutions often prefer controlled networks

Central banks, commercial banks, investment banks, custodians and market infrastructures need requirements that public crypto networks were not originally designed around.

These include:

- Known legal entities.
- KYC / AML.
- Sanctions screening.
- Confidentiality.
- Access control.
- Governance.
- Transaction finality.
- Operational resilience.
- Regulatory oversight.
- Recovery and dispute processes.
- Data-location and privacy requirements.

For this reason, many institutional implementations use **permissioned, consortium, privacy-enabled or hybrid architectures**.

At the same time, some regulated financial products are also being issued on public blockchains with **whitelisting, identity and transfer controls**. Institutional adoption is therefore not exclusively private-chain based.

## 12.2 Selected institutional examples

### A. Project Agorá - BIS and central banks

Project Agorá explores how **tokenized commercial-bank deposits and tokenized wholesale central-bank money** could operate together on a programmable public-private financial platform.

Its focus includes improving cross-border payments while preserving the two-tier monetary system.

### B. Swift blockchain-based shared ledger

In July 2026, Swift announced that its blockchain-based ledger was ready for initial use, with **17 banks from six continents** preparing to pilot live transactions using tokenized deposits.

The use case focuses on **24/7 cross-border payments, liquidity efficiency and regulated digital value**.

### C. DTCC Tokenization Service

DTCC has demonstrated tokenization of DTC-held securities in live production transactions.

Its Tokenization Service is designed to connect traditional market infrastructure to approved blockchain networks and support use cases such as collateral, repo, securities lending and DvP.

DTCC states that initial network connectivity includes **Canton Network and Hyperledger Besu**.

### D. Broader market direction

The trend is not simply:

> "Banks are replacing traditional systems with blockchain."

A more accurate description is:

> **Financial institutions are progressively integrating DLT into selected payment, settlement, securities, collateral and asset-servicing workflows while preserving regulatory controls and interoperability with existing infrastructure.**

```text
Traditional Core Banking
          │
      ISO 20022 / APIs
          │
          ▼
Interoperability / Orchestration
          │
   ┌──────┴─────────┐
   ▼                ▼
Traditional       DLT / Blockchain
Payment Rails     Tokenized Networks
   │                │
   └──────┬─────────┘
          ▼
Integrated Financial Ecosystem
```

[Back to top](#table-of-contents)

---

# 13. Solidity Basics

## 13.1 What is Solidity?

**Solidity** is a programming language used to create smart contracts, particularly on Ethereum and Ethereum-compatible networks.

A Solidity contract can contain state/data, functions, access controls, events, token logic and business rules.

A smart contract is deployed to a blockchain address and users/applications interact with its functions through blockchain transactions or read-only calls.

## 13.2 Basic Solidity concepts

| Concept | Simple meaning |
|---|---|
| `contract` | Defines a smart contract |
| `address` | Blockchain account/contract address |
| `uint256` | Unsigned integer |
| `mapping` | Key-value storage |
| `constructor` | Runs when contract is deployed |
| `function` | Executable contract logic |
| `view` | Reads state without changing it |
| `event` | Creates an on-chain log |
| `require` | Checks a condition |
| `msg.sender` | Address calling the function |
| `_mint()` | Creates tokens in many token implementations |
| `_burn()` | Destroys tokens in many token implementations |

For learning, established libraries such as **OpenZeppelin Contracts** are preferable to recreating token standards from scratch.

## 13.3 ERC-20 educational example

Use case:

> Represent **1 kg of pooled gold as 1,000 fungible tokens**, where **1 token = 1 gram**.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract TokenizedGoldGram is ERC20 {

    constructor() ERC20("Tokenized Gold Gram", "TGLD") {
        _mint(msg.sender, 1000);
    }

    function decimals() public pure override returns (uint8) {
        return 0;
    }
}
```

### What happens?

```text
Deploy contract
      ↓
Mint 1,000 TGLD
      ↓
Wallet A = 1,000 TGLD
      ↓
Transfer 500
      ↓
Wallet A = 500
Wallet B = 500
```

This demonstrates the **technical token model only**. It does not by itself prove ownership of 1 kg of real gold. A real product would also require legal rights, custody, verification, insurance, controls and redemption arrangements.

## 13.4 ERC-721 educational example

Use case:

> Represent **one specific 1 kg gold bar** identified by a unique serial number.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract TokenizedGoldBar is ERC721 {

    uint256 public constant GOLD_BAR_TOKEN_ID = 1;

    constructor() ERC721("Tokenized Gold Bar", "TGB") {
        _safeMint(msg.sender, GOLD_BAR_TOKEN_ID);
    }
}
```

Conceptually:

```text
Contract: Tokenized Gold Bar
Token ID: 1
          ↓
Represents
          ↓
Gold Bar Serial: GOLD-001
Weight: 1 kg
Purity: 24K
```

In a more realistic educational implementation, metadata could point to information describing the asset, while hashes can help prove that supporting documentation has not changed.

## 13.5 ERC-1155 educational example

Use case:

> Manage several asset/token types from one smart contract.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

import "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";

contract MultiAssetTokens is ERC1155 {

    uint256 public constant GOLD = 1;
    uint256 public constant SILVER = 2;
    uint256 public constant CERTIFICATE = 3;

    constructor()
        ERC1155("https://example.com/metadata/{id}.json")
    {
        _mint(msg.sender, GOLD, 1000, "");
        _mint(msg.sender, SILVER, 5000, "");
        _mint(msg.sender, CERTIFICATE, 1, "");
    }
}
```

Conceptually:

```text
One Contract
   │
   ├── Token ID 1 = Gold units
   ├── Token ID 2 = Silver units
   └── Token ID 3 = Unique certificate
```

ERC-1155 is useful when one application needs to manage multiple token types efficiently.

[Back to top](#table-of-contents)

---

# 14. Hands-on Learning Environment

A simple educational environment for experimenting with Ethereum-compatible token contracts is:

| Tool | Purpose |
|---|---|
| **Remix IDE** | Write, compile and deploy Solidity contracts |
| **Solidity** | Smart-contract programming language |
| **OpenZeppelin** | Reusable token/security contract libraries |
| **MetaMask** | Wallet for interacting with test networks |
| **Sepolia** | Ethereum test network |
| **Sepolia ETH** | Test-network gas token |
| **Etherscan** | Blockchain explorer / transaction verification |
| **IPFS** | Decentralised content-addressed file storage for suitable metadata |
| **GitHub / GitHub Pages** | Code, documentation and learning portfolio |

### Suggested learning sequence

```text
1. Create ERC-20 token
        ↓
2. Deploy to Sepolia
        ↓
3. Verify transaction on explorer
        ↓
4. Import token into wallet
        ↓
5. Transfer token to another wallet
        ↓
6. Create ERC-721
        ↓
7. Add metadata
        ↓
8. Create ERC-1155
        ↓
9. Compare token models
        ↓
10. Model a financial/RWA use case
```

Never use real money or production assets for basic learning experiments.

[Back to top](#table-of-contents)

---

# 15. Key Takeaways

A first-time reader should leave this repository with the following mental model:

```text
DLT
│
├── Distributed record-keeping technology
│
└── Blockchain is one DLT architecture
        │
        ├── Permissionless
        ├── Permissioned
        ├── Consortium
        └── Hybrid
              │
              ▼
        Programmable Ledger
              │
        ┌─────┴─────────┐
        ▼               ▼
 Cryptocurrency      Smart Contracts
        │               │
        ▼               ▼
 Stablecoins         Tokens
                        │
                ┌───────┼────────┐
                ▼       ▼        ▼
              ERC-20  ERC-721  ERC-1155
                │
                ▼
           Tokenization
                │
        ┌───────┴─────────────┐
        ▼                     ▼
 Tokenized Money        Tokenized Assets
        │                     │
 Tokenized Deposits       Bonds / Funds /
 Stablecoins              Equities / RWAs
        │                     │
        └──────────┬──────────┘
                   ▼
          Programmable Settlement
                   │
              DvP / PvP
```

The major financial transformation is therefore **not simply "crypto replacing banking"**.

It is the gradual convergence of:

> **Traditional financial infrastructure + ISO 20022/APIs + DLT + tokenized money + tokenized assets + programmable settlement.**

[Back to top](#table-of-contents)

---

# 16. Official References

### DLT, Tokenization and Tokenized Money

- **Bank for International Settlements - Tokenised monetary and financial system**  
  <https://www.bis.org/media-releases/20250624-next-generation-monetary-and-financial-system-takes-shape-based-tokenised-unified-ledger-bis>

- **BIS - Project Agorá**  
  <https://www.bis.org/about/bisih/topics/fmis/agora.htm>

- **BIS - Blueprint for the future monetary system**  
  <https://www.bis.org/publications/aer-2023/blueprint-future-monetary-system-improving-old-enabling-new>

### Stablecoins

- **Bank of England - What are stablecoins and how do they work?**  
  <https://www.bankofengland.co.uk/explainers/what-are-stablecoins-and-how-do-they-work>

### Institutional Adoption

- **Swift - Blockchain-based ledger and tokenized-deposit payments**  
  <https://www.swift.com/about-us/media-centre/press-releases/swifts-blockchain-ledger-ready-use-17-banks-set-pioneer-tokenised-cross-border-payments-trusted-global-infrastructure>

- **DTCC - Tokenization Hub**  
  <https://www.dtcc.com/products-and-services/digital-assets/tokenization/hub>

### Ethereum Token Standards

- **ERC-20 Token Standard**  
  <https://eips.ethereum.org/EIPS/eip-20>

- **ERC-721 Non-Fungible Token Standard**  
  <https://eips.ethereum.org/EIPS/eip-721>

- **ERC-1155 Multi Token Standard**  
  <https://eips.ethereum.org/EIPS/eip-1155>

### Solidity and OpenZeppelin

- **Solidity Documentation**  
  <https://docs.soliditylang.org/>

- **OpenZeppelin Contracts**  
  <https://docs.openzeppelin.com/contracts/>

[Back to top](#table-of-contents)

---

# 17. Disclaimer

This repository is an **educational and personal learning resource**.

The Solidity examples are intentionally simplified demonstrations and are **not production-ready smart contracts**. Tokenizing a financial or real-world asset requires much more than deploying code, including legal structuring, regulatory compliance, asset custody, identity/KYC controls, cyber security, operational resilience, governance and redemption arrangements.

Nothing in this repository should be considered investment, legal, regulatory or financial advice.

---

## Repository Topics

`DLT` · `Blockchain` · `Cryptocurrency` · `Stablecoins` · `Smart-Contracts` · `Programmable-Money` · `Tokenization` · `Tokenized-Deposits` · `RWA` · `Digital-Assets` · `ERC-20` · `ERC-721` · `ERC-1155` · `Solidity` · `Institutional-DLT` · `Financial-Markets`

---

### Learning Goal

> **Understand how traditional financial infrastructure is evolving toward programmable, interoperable and tokenized financial ecosystems while retaining the trust, regulation and controls required in institutional finance.**
