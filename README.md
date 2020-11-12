# Zenith Finance Vault (ZFV) Technical White Paper (v1)

## Abstract

Zenith Finance Vault is developed to provide an extra level of security based on an Anti-reentrance attack protection structure. It features all the convenience of a secured blockchain wallet while adding important features allowing user transparency and freedom. Zenith Finance Vault is our answer to issues faced by the crypto community over the last decade.


## 1. Introduction

Zenith Finance Vault is built on Zenith Finance Network a permissionless secured network, which is built to drive the next generation of global commerce by unlocking the decentralized applications and digital assets of tomorrow. Zenith Finance Network enables a secure and interoperable flow of assets and data across protocols & applications to create an internet of value for all.


## 2 Zenith Finance Network (ZFN)

## 2.1.1 Consensus Engine
- ZFN will have two consensus engines on launch:

- ZETA: A DAG-optimized consensus protocol–high-throughput, parallelizable, and simple to prune.

- XANDER: A chain-optimized consensus protocol–high-throughput, totally-ordered, and great for smart contracts.

### 2.1.2 Virtual Machines (VMs)
Virtual Machines (VMs) in ZETA are code that uses consensus to produce a database. This database can be in the form of a chain, a DAG, a log file, or some other data structure that requires synchronization across multiple machines. The VM logic can be deployed many times across many subnets.

### 2.1.2 ZenithVault-Wallet
A wallet and faucet server will be open-sourced to enable developers to interact with ZETA. Using the wallet, funds can be sent and received throughout the network. When using private shared testing environments, the faucet is useful for developers in need of funds for their own testing purposes.

### 2.1.3 ZetaJs
The Javascript library for interacting with Zeta APIs. ZetaJS integrates with existing decentralized applications to enable Zeta integration. It has a modular library architecture, allowing for custom VMs to write plugins to extend ZetaJS functionality.

## 2.2 Shortcomings of Centralized Crypto Wallets

### 2.2.1 The Problem of Theft
The key requirement from a store of value is to be nonperishable. Theft is one of the primary risks of loss when dealing with anything of value. Gold performs rather well in this regard. Physical theft of gold is significantly riskier to execute than any virtual attack on an electronic asset. In addition, a thief would have a hard time hiding a sizable cargo of stolen gold from the authorities, especially across borders. Laundering and liquidating stolen gold in large quantities while remaining anonymous is no simple task either.

Unfortunately, Most crpto assets like Bitcoin fares poorly by comparison. Funds are protected by the protocol with sets of cryptographic private keys. Gaining electronic access to these keys allows an attacker to seize all funds remotely, immediately and irrevocably. Laundering stolen funds is also significantly easier since transactions are pseudonymous, traceability can be disrupted by use of mixers and Sybil identities can be created in bulk. As a result, cryptocurrency theft is on the rise with over $1 billion stolen in 2018. Community-curated lists of major incidents show that even professional institutions well-versed in the latest security practices are prone to attack. Secure management of private keys by end-users is proving to be one of the major challenges of Bitcoin.

Since keys must be regularly used to interact with funds and the signed transactions must be transmitted over the Internet, every key eventually becomes vulnerable. Security-conscious practices like splitting funds between “hot” and “cold” wallets are cumbersome and fail to solve the problem at the root.
Incidents show that hot wallets unavoidably hold significant amounts and use of cold wallets only reduces interaction with keys but does not eliminate it completely.

### 2.2.2. Ownership

Most tools and services on the internet support a single owner account architecture. An architecture that recognises and grants ownership and authority to one person identified by their email or phone number. Some of the motivation for this is the need to maintain security and to determine who pays the bills.
Crypto holding platforms are among these service providers built on this single-owner structure. All assets must be owned and managed by one person who is granted full privileges receive, approve, transfer or blacklist associated with their account without notice.  

The consequence of this is that complicated, sovereign and community-led organisations cannot build software in a trust-less manner since these collaborators must trust the root account owner. One approach employed to remedy this problem involves the creation of committees and other secondary structures. However, we argue that these structures do not deliver real ownership and governance since there is a root password managed by an individual or organisation.

In the crypto industry, they say “If you do not own your private keys, you do not own the coins”. It is essential that contributors to community-led platforms can honestly and provably share ownership of a crypto asset without needing to trust a central authority such as the owner or maintainer of a wallet service or the platform operator. Real ownership of a community-owned software cannot be granted based on faith that the authority will always act in the best interest of holders.

### 2.2.3. Governance

For a community based crypto holding platform to succeed in creating and managing decentralised organisations, they must first figure out governance, otherwise what would be obtainable is chaos, uncertainty, indecision, and unaccountability. These communities need to be able to formulate a governance system that is acceptable to all parties and enables them to make decisions quickly and fairly.


## 3. Anti-Theft Solution
As a means to eliminate theft, we propose a solution based on a new, sophisticated locking script and protocol modification. A transaction performed using the new locking script will by default be delayed by 24 hours. When a miner adds a transaction to a new block, the transaction will no longer be committed
immediately. Instead, it will be added on-chain as an alert for the duration of 144 blocks (assuming blocktime of 10 minutes). If left undisturbed for 144 blocks, the transaction will change from alert state to“confirmed”. The benefit of on-chain alerts is that coin owners will receive uncensorable advance notifications
whenever their coins are moved. The owner will have 24 hours to act upon the alert and will be able to override the transfer if unauthorized. Delayed withdrawals are a proven anti-theft industry standard in custodial wallets and the traditional banking system. Coinbase Vault [12], for example, has a wait time of
48 hours. Our proposed solution provides the same protection without a trusted third party. Emergency override of a transaction in alert state requires a special recovery transaction and is carried out immediately without being subject to the 24 hour delay. The recovery transaction requires a special recovery key that must be incorporated into the locking script during the wallet creation. Once a recovery key has been registered for a given wallet, it cannot be changed. 

The private recovery key used for the emergency override is intended to be a fresh key that has never been used before. This key can be generated offline and should never be connected to the Internet or inputed to any device. The registration process only requires the public part of this key, ensuring that the private key can remain unused. Unlike cold wallet keys that must be used occasionally and are thus vulnerable to theft, the recovery key will be used for the first time only in the emergency override itself, and therefore can be completely theft resistant. Once the recovery key has been used, it is to be
considered compromised and all funds should be immediately transferred to a new wallet protected by a new unused recovery key.

The original Bitcoin Royale concept of digital gold assumed delaying all the transactions in the system by 24 hours, making the coin a secure, slow-moving store of value. We would like to expand this concept to take the best of two worlds – the digital gold and digital cash, without any compromise on security Alongside the slow-moving alerts we conditionally keep the fast-moving, “instant” transactions. To provide the highest security, sending such a transaction will require a user to perform a blockchain-based 2FA, using the 3rd key provided during wallet creation.

## 4. Bitcoin

In this section, we briefly discuss bitcoin, its consensus mechanism and particularly its inability to process enough transactions per second to meet mainstream users’ needs.

### 4.1. Introduction

Bitcoin is a form of electronic cash. It is a decentralised digital currency that does not have a central bank or a trusted authority. It can be sent from person-to-person faster and cheaper without restrictions. With cryptography, transactions are verified and transmitted through a peer-to-peer network of computers that update account balances and record changes in a public distributed ledger known as a blockchain[7]. Bitcoin was invented by Satoshi Nakamoto[8] and released to the public as an open source software in 2009.

### 4.2. Consensus Mechanism

Blockchain networks require a means to reach an agreement on a single value. Consensus algorithms define the rules that must be followed by computers on the network in other to reach an agreement. The process of agreeing with other computers is known as the consensus problem, and it is a well-researched field in computer science.
Bitcoin uses a consensus algorithm known as Proof of Work[9](PoW). It is used to process blocks of transactions and append them to a chain of blocks — the blockchain. In Bitcoin, the process of appending a block to the blockchain is known as “mining”, and the individuals who take part in the mining process are known as “miners”. PoW requires miners to solve complex cryptographic puzzles to gain the right to add a block.

Miners receive newly created Bitcoin as a reward for solving the puzzle. This reward is known as the block reward. Before the reward is issued, the generated block must follow the consensus rules. All other nodes on the network are responsible for verifying the block and enforcing the consensus rules. Once a miner discovers a valid block they did not create, they immediately stop and start mining the next block. There is a network difficulty that ensures that blocks are created within 10 minutes. It determines how hard it is for the miners to mine a block and is adjusted dynamically to maintain the 10 minutes window.

Bitcoin’s PoW has a disadvantage of being very slow. It has been described as a consensus system that wastes energy and is causing harm to the planet. However, it is the most battle- tested and well understood trustless consensus system in the cryptocurrency industry.

### 4.3. Low Transaction Throughput

Bitcoin pioneered the blockchain industry and made it attractive for different categories of people who believed in its vision. Developers have created clones and alternative implementations intending to improve on the capabilities of Bitcoin. One of the primary motivation fueling the creation of Bitcoin alternatives is the inability of the Bitcoin network to process large amounts of transactions sufficient to handle the needs of mainstream users. It takes 10 minutes for the bitcoin network to create a new block and even more to attain minimum confirmation of a transactions finality. Most people agree that for cryptocurrency to go mainstream and be capable of competing centralised incumbent, blockchains must be able to handle thousands of transaction per second.

### 4.4. Alternative Consensus Mechanisms

Since the introduction of Bitcoin, developers and researches have been working on alternative consensus algorithms that are more efficient and performant than proof-of-work. The most popular of these alternatives is Proof of Stake (PoS).  
 In Proof-of-Stake consensus, the blocks are not created by miners solving computationally hard math puzzles, but by participants who stake their money to bet on the validity of a block. These participants take on the role of block forgers and validators. Proof of Stake is a faster and more energy efficient alternative to Proof of Work, but it suffers from a severe problem known as “Nothing at Stake”.
The concern behind “Nothing at Stake” is that since it cost next to nothing to create blocks that support a fork, validators can vote for every fork that happens without any severe consequence; This is unlike proof-of-work where a computationally hard problem must be solved to extend the main branch or a forked branch. Modern PoS systems employ a strategy that punishes misbehaving participants who failed to follow the consensus rules by slashing their stake.

#### 4.4.1. Bitcoin-NG

The performance of blockchain protocols is limited by two factors — block size and block interval. Increasing the block size correlates to an increase in transaction throughput. However, bigger blocks take more time to propagate to nodes on the network and can lead to an increase in forks if these blocks arrive late. Decreasing the block size reduces the time it takes for blocks to propagate to nodes, but doing so rapidly leads to forks and frequent reorganisation. The Bitcoin system traded transaction throughput for latency by using a small block of 1MB with a 10 minutes block time: Blocks are sufficiently propagated throughout the network due to the block time, but minimal transactions are processed.

Bitcoin-NG[10] is a scalable blockchain protocol designed to improve the throughput of Bitcoin without affecting the same trust model that exists in Bitcoin. It achieves performance improvement by introducing the concept of a leader election and transaction serialisation. In BitcoinNG, time is divided into periods known as “epoch” where every epoch has a leader. Once a node becomes a leader, it is expected to produce blocks until a new leader is discovered. Leader election is performed randomly in the same way miners in Bitcoin find blocks infrequently.
BitcoinNG ensures that the system can process transactions even when the network works to find a new leader unlike Nakamoto Consensus in Bitcoin where no transaction is processed during the 10 minutes block interval.

## 5. ZFV Protocol

In this section, we describe the engineering direction of our protocol. Existing knowledge of blockchain technology is essential. Please note that some concepts described below are not final and may be subject to change as we continue to execute on the journey to deliver our vision.

### 5.1. Consensus Model

#### 5.1.1. Hybrid Protocol

The ZFV consensus mechanism is a hybrid consensus algorithm of both Proof-of-Work and Proof-of-Stake. Our consensus model is based on concepts described in the Proof of Activity[11] protocol by Iddo Bentov et al. They described a process of extending Nakamoto Proof of Work via Proof of Stake to increase the security of the network while reducing the dependence on miners as the only contributor to network security. Iddo Bentov et al. questioned the capability of Bitcoin miners to sustain the security of the system when PoW is no longer subsidised via the block reward. We agree with their assertion that a cryptocurrency protocol should be designed in such a way that its incentive structure encourages different participants in the system to sustain its health.

#### 5.1.2. Bitcoin-NG — Leader-based Block Creation

Bitcoin-NG extends Nakamoto consensus into a protocol that is capable of processing more transactions than Bitcoin. It does this by introducing a leader-based block creation scheme where a miner is entitled to create several more blocks at faster intervals after they mined a block known as a “key block”. ZFV PoW implementation is based on Bitcoin-NG to improve transaction throughput through improved latency and bandwidth.

### 5.2 Coin

In most public blockchain systems with a native cryptocurrency, new coins are generated when a new block is mined. The generated coins are shared to the miner and any other network participants who contributed to the creation or validation of the new block at a predetermined ratio. In Bitcoin and other similar proof-of-work blockchains, the miner of the block receives all newly generated coins.

We believe a system built on a coin generation model where a single participant receives all rewards is unfair and does not promote equitable distribution of wealth generated by the network. Centralization of rewards within a wealthy minority further replicates and increases the existing gap between the rich and poor. In matured proof-of-work blockchains like Bitcoin, a user needs specialised equipments to compete with well-funded corporate organisations. Although, one might argue that these networks provide security to the network, but they may also become future adversaries when incentives falling below their cost of operation due to low block rewards.

#### Against Miner Centralization & Unfair Distribution

PeopleMint creates a symbiotic relationship between a global population of users and miners working together to sustain the system while also discouraging miner centralisation by diversifying the participants and processes involved in coin creation. In Bitcoin, PoW mining is the only mechanism through which new coins are introduced. Miners do not need any other party and are incentivised to invest more in superior hardware and infrastructure to outcompete other miners which further makes mining increasingly inaccessible to smaller miners. PeopleMint provides a fair coin generation model as well as a chain security mechanism to keep miners in check through a human-driven process of observing and implicitly voting of blocks on the main chain.

#### 5.2.1 Coin Basics & Supply

The ZFV native coin is called /Ell/ (plural: /Ellies/) . It is divisible to 18 decimal places. Its official Unicode character is ȅ (U+0205). At the launch of the main network, the initial supply cannot exceed a total of 1,500,000,000 coins.

#### 5.2.2 Initial Supply Allocation - 30,000 ZFV

The initial supply is allocated in the following ratio:

- Presale — 43.33%
- Marketing - 16.67%
- Advisors — 10%
- Exchanges — 20%
- Team - 10%

#### 5.2.4 Public Distribution Method

We will distribute the supply allocated to the public through a combination of public sale sessions and a distribution network designed to allow millions the chance to claim a share of the initial supply.

#### Presale Session

**Session** (Pre-Sale)

- Start Date: 
- End Date: 
- Duration: 1 Month
- Distributed Supply: 13,000 ZFV (includes bonuses)
- Price: 1 ETH - 50 ZFV


#### Distribution Network

**Introduction**

As a hybrid consensus system composed of both proof-of-work and proof-of-stake, there is a need to ensure the fair and widespread distribution of the initial coin supply to as many people as possible. When a few individuals own enough coins to launch an attack, the security of the system is weakened.

The vast majority of ICOs have distributed their initial or total coin supply within a month, leading to a situation where large amounts of coins end up in the control of a few individuals or entities. More so, short-lived ICOs prevent a sufficient amount of people from getting to learn about the project and understanding enough to acquire a stake in the system. Ideally, for a blockchain network to be sufficiently decentralised, its coin supply must also be well distributed.

**The Network**

To ensure broad and fair distribution of the native coin, we are going to run a temporary network known as the “Distribution Network”. The network is going to serve a singular purpose of allowing anyone in the world to exchange banknotes for the native coin through the PeopleMint mechanism. Once the public allocation is distributed, a snapshot of the blockchain state is collected and used to seed the genesis block of the main network.

The network is to run the full consensus specification which allows anyone to participate (as a miner, endorser, validator and scanner) and earn regular network rewards. We can test the protocol, plan upgrades and onboard more network participants into our community in preparation for our main network launch.


### 5.3. Network Participants

We now describe the types of network participants working together to sustain the system.

### 5.3.1. Miners

Miners are individuals who participate in Proof-of-Work attempting to create blocks by solving hard cryptographic puzzles which require the consumption of energy. In Bitcoin, a miner is responsible for finding a solution to the puzzle for the next block. They use the result of the puzzle to create a new block containing transactions and broadcast it to the network. Likewise in ZFV, miners are responsible for creating /key/ and /microblocks/. Key blocks are similar to Bitcoin’s block in that they are created by expending energy, while microblocks are created at a predetermined interval and do not require energy investment.

### 5.3.2. Witness

Witnesses are stakeholders who validate key blocks, microblocks and extend microblocks with additional transactions. Witnesses serve as validators that audit the work of miners. They enable power dynamics with PoW miners where they continuously ensure these miners abide by the rules.

When a block is received, every witness online checks whether the block’s header is valid; It checks if the header contains a previous block’s hash, if the difficulty matches the expected current difficulty and whether the block remuneration is valid. Once validated, the witness checks whether it was one of the /N/ witnesses selected to verify this block. It does this by running a pseudo-random operation to determine the N witnesses, and when it finds that it was selected, the witness signs the hash of the block and broadcast the signature to the network.

When the /Nth/ witness see that it was derived by the block, it creates a wrapped block that extends it. If the block is a microblock, it includes as many transactions as the remaining block capacity can support, the signatures of the other selected witnesses and its signature of this wrapped block. The Nth witness broadcasts the wrapped block to the network, and when other nodes see that it is valid, they append it to their main chain.

### 5.3.3. Transaction Endorser

One of our core mission is to make it convenient for collaborators to create blockchain applications written in standard, general-purpose programming languages. Current blockchains that provide an application execution environment require these programs to be written in domain-specific languages. The requirement to use domain-specific language limits widespread adoption and may lead to buggy or insecure applications.

A major reason for DSLs (Domain Specific Languages) is that blockchain applications written in general-purpose languages can produce non-deterministic code that can lead to the creation of forks; This can be exploited by bad actors to prevent the network from reaching consensus on the validity of a block, thereby halting the system. Many programming languages include standard features that produce non-deterministic behaviour (e.g. Go map keys are randomised).

Hyperledger Fabric, which is the first blockchain system to support the use of multiple, well-established languages solved this problem of non-determinism by separating transaction execution, ordering and validation using a novel approach known as /execute-order-validate/ architecture. In this model, a client sends a transaction to peers specified in an endorsement policy. Each transaction is then individually executed by the peers and its output recorded. This process is called /endorsement/. The client must collect /N/ endorsements up to the amount specified in the endorsement policy. After collecting enough endorsement, it creates a transaction and broadcasts it to the ordering service for inclusion into a block, after which the ordering service broadcast the block to the rest of the network to perform the validation phase. During validation, transactions that failed to pass the endorsement policy or have non-deterministic outputs are ignored.

Our execution model is based on similar pre-consensus transaction execution and endorsement strategy. On ZFV, endorsers are stakeholders who are responsible for executing and endorsing transactions based on a global endorsement policy. Endorsers are former witnesses of the previous epoch. When a client broadcasts a transaction, a node X checks whether it was a witness in the last epoch. If it was, it is required to endorse the transaction and broadcast a signed endorsement report to its peers. Node X collects endorsements, creates a wrapped transaction which includes the endorsements, adds it to its pool and broadcast it. During block validation, nodes will use the endorsement to ensure only deterministic transactions are processed.

### 5.4. Block Creation

The protocol divides time into /epochs/. In each epoch, a single leader is chosen to extend the blockchain by creating blocks known as /key/ and /microblock/ blocks. Key blocks indicate the beginning of an epoch after which the key block creator is entitled to create microblocks at faster intervals.

#### 5.4.1 Key Blocks

Miners are free to start an epoch by creating a /key/ block via the same Proof of Work computation performed in Bitcoin. A /key/ block header includes the unique reference of its predecessor, the current time, the public key of its creator to payout the reward, difficulty information and coin generation transactions. Unlike Bitcoin, the public key of the key block creator is added to the header and used to verify subsequent microblocks. Similar to Bitcoin, Key blocks creation time are determined by the network difficulty. For example, Bitcoin’s difficulty dynamically adjusts to target a 10 minutes block creation interval.

#### 5.4.2 Microblocks

After a node has generated a key block to become the leader, it is allowed to generate microblocks which can include transactions. Microblocks must be generated at a deterministic rate. A microblock is considered invalid; if the difference between the timestamp of a microblock and its parent is less than a predetermined minimum or its timestamp is a future time. The constraints are put in place to prevent a malicious node from overwhelming the system with microblocks.

A microblock contains transactions and a header. The header contains the hash of the previous block, the current timestamp, the Merkle root of the transactions and the signature of the header. The signature must be created using the private key of the most recent key block in the chain.

#### 5.4.3 Block Validation

After the creation of key or microblocks, the miner broadcasts the block to the network. Upon learning about the block, witness nodes must check whether they have been selected to validate the block by running a pseudo-random, deterministic algorithm to compute a set of witnesses for the block. Every online witness checks whether the block is valid, sign the hash of the block header with the private key that controls their staking account and broadcast their signature to the network.

The /Nth/ peer in the set of eligible peers must create a wrapped block: It may include some transactions if the received block is a microblock and broadcast to the network. Upon receipt of a wrapped block, the node validates its header, any transactions it may have and appends it to its main chain. The wrapped block must contain signatures of 2/3 of the /N/ peers in the computed validation set. The fee from the transactions in the wrapped block is shared between the miner and the witnesses.

#### 5.4.4. Middleware

A middleware is a custom autonomous function that acts as a bridge between operations executed by holders and the ZFV protocol. It may be used to alter the properties of the request in question or run sub-operations. During the execution of operations, the ZFV protocol allows developers to hook autonomous functions to lifecycle events of operations which can be used to create more powerful behaviours.

## 6. Conclusion

ZFV is determined to create a system that allows networked organizations to be created, managed and flourish without concerns of The Problem of Theft, ownership, and Governance. We are particularly impressed with the work of Malte Möser et al. on Bitcoin Covenants. Their extension of the Bitcoin script language enables restrictions on the future use of coins, which can be used to implement a variety of security measures. The primary of which is vault transactions, which
resemble our proposed delayed withdrawals mechanism. We have opted for a simpler implementation that does not require a recursive array of custom scripts to be implemented by wallets. Our proposal is more than an optional extension, it is a fundamental change to the protocol with a wide mandatory effect on transactions. Shifting the burden of implementation to miners and leaving the end-user transaction experience identical to the default, enable us to better carry out our mission of creating true electronic gold.

## 7. References

1. Bitcoin - https://bitcoin.org/bitcoin.pdf
2. Snuffle - https://cr.yp.to/snuffle.html
3. Blockchain - https://en.wikipedia.org/wiki/Blockchain
4. Satoshi Nakamoto - https://en.wikipedia.org/wiki/Satoshi_Nakamoto
5. Proof of Work - https://en.bitcoin.it/wiki/Proof_of_work
6. Bitcoin-NG: A Scalable Blockchain Protocol - https://arxiv.org/abs/1510.02037
7. Proof of Activity: Extending Bitcoin’s Proof of Work via Proof of Stake - https://eprint.iacr.org/2014/452.pdf
8. PeopleMint: A Multi-Party Mining
    Protocol - https://storage.googleapis.com/ZFV-docs/PeopleMint.pdf
9. Hyperledger Fabric: A Distributed Operating System for
    Permissioned Blockchains - https://arxiv.org/pdf/1801.10228.pdf
12. Aragon Court - https://forum.aragon.org/t/aragon-court-v1/691
13. On Consensus and Humming in the IETF - https://tools.ietf.org/html/rfc7282
Ian Duoteli Fleming, https://bitcoinroyale.org/bitcoinroyale.pdf
14. S. Nakamoto, “Bitcoin: A Peer-to-Peer Electronic Cash System”,
https://www.bitcoin.org/bitcoin.pdf, 2008.
15. bitcoingold.org, “Bitcoin Gold”, https://bitcoingold.org, 2018.
16. J. H. Ziegeldorf, F. Grossmann, M. Henze, N. Inden, and K. Wehrle,
“Coinparty: Secure multi-party mixing of bitcoins”, In: CODASPY ’15, 2015.
17. CipherTrace, “Cryptocurrency Anti-Money Laundering Report, 2018 Q4”,
https://ciphertrace.com/crypto-aml-report-2018q4, 2019.


