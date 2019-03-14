# Ellcrys: A Decentralized Collaboration Network
## Abstract
A decentralized system for storing source code would allow collaborators build open, transparent, community-governed software products and  organizations without a centralized authority providing coordination services. Git source control tool provides the ability for people building software to collaborate decentrally, but the unease and requirement need to host a repository server makes it unattractive for many. We propose a system that leverages on digital signatures, git and blockchain technology to enable people create, contribute and manage the ownership, accounting and governance of objects associated with a software project.

## 1. Introduction
Open-source development began as a revolution against the unfair profits and often sub-par products that closed-sourced software development companies created. These companies were known to monopolize certain areas in IT, producing software products that had slow release circles, buggy, less interoperable and expensive. Developers across the world began to collaborate, working asynchronous at times suitable for them to create alternatives that were more user-friendly, highly performant, free to use softwares that have the backing of a huge community — This was a game changer.

## 1.1 Open Source, Today
Today, open source software products run the world — Everyone uses open source software products and the movement has forced once closed-source companies who were anti-open-source to begin to release open-source projects as well as contribute to existing open projects. 
	But, companies are increasingly becoming irresponsible with the way they manage users’ data and experiences, we believe it is time for open source to move towards a new phase where open source communities provide competing and innovative services that are open, transparent and driven by a user-first philosophy. 
	Right now, open source communities mostly rally to build static products that form part of a larger product or service offered by closed-source, equity-driven companies who rarely contribute back to open source or have questionable ethics. These open communities have little power to effect philosophical changes upon the misbehaving companies that use their product. It is for the same ethical shortcomings of companies, regulators and government that motivated the creation or sustainability of Bitcoin[1] — A peer-to-peer electronic cash system that allows people to send, receive and control money without any intermediary. Bitcoin is an example of a service designed to be open, transparent and pro-users. 

## 1.2 Open Source, Tomorrow
Open source communities organizing to build services is already happening — The cryptocurrency industry is worth over $100 billion as at the time of this writing and it is the biggest pioneer in the creation, incentivization and governance of systems that are built in the open with publicly disclosed vision and ethical standards. Projects like Bitcoin and Ethereum have a large community of participants that constantly hold maintainers accountable to the standards they were founded on. 
	If we intend to experience the benefits we can derive from open source services quickly, then the tools and ideologies that make these communities successful, must be adapted for communities building centralized applications which are undoubtable the most accessible, convenient and richer that their decentralized versions. 
	By adapting the open and collaborative structure of open source to centralized systems, we will move to a time where communities composed of mutually distrusting collaborators can build all kinds of applications (desktop, mobile, VR etc) apps together and integrate any type of business model like centrally-run organizations. 
	However, for us to realize a future where open source services compete with centrally-led services, we need to find and fix the challenges and obstacles would cause failures. 
	
# 2. Obstacles Of Open Source Services	
The dream of community-led open source software applications and services directly solving end-user problems in the same way centrally-governed organizations is challenged by a host of infrastructural inadequacies. In this section, we describes some of the major issues we believe to be most threatening. 

## 2.1 Collaboration Tools & Platforms
Open source developers are spread across the world. They speak different languages, have different believes and live in different timezones but this differences have not slowed down the progress of the OSS community. One the reasons for this can be traced to the tool that has made sharing, tracking and versioning of code possible; This tool provides a common development “language” that collaborators use to contribute and manage any software project irrespective of the differences outlined earlier — This tool is known as Git[2]. 
	Git is a distributed version control system developed in 2015 by Linus Torvalds to aid the development of the Linux kernel. Ever since, it has grown to be one of the most important tools utilized by developers and enterprises across the world. Git allows developers to work in a decentralized approach where they manage replicated source code repositories and sync up with the repositories of other developers.
	Unfortunately, running and maintaining uptime of an independent git servers is challenging for most users. For this reason, cloud-based code hosting services like Github[3] emerged to provide users with a central servers that hosting repositories and eliminating the need for users to run their own servers. These services also provide collaboration tools like issue tracking, reviews, pull request that allow users communicate problems and manage new releases of their software.
	Millions of developers use Github and other code sharing platforms to build great software but the central ownership, governance and execution of the service makes it unfit to host teams building open source services. 

## 2.2. Shortcomings of Centralized Code Sharing Platforms
In this section, we will highlight the reasons why we believe the future of community-led open source services cannot be built on centralised code sharing platforms like Github, Gitlab and others. 

### 2.2.1 Censorship

“Code” is free speech; similar to human languages, it is a form of expression used to communicate ideas. This has been proven in a U.S court [4] in the case between Bernstein v. United States where Bernstein wanted to publish a paper and source code of his encryption system [5] but the government	required him to submit his ideas for review and register to acquire a license as an arms dealer and failure to do so would result criminal penalties. Bernstein sued the government and won when it was ruled that software source code was protected by the First Amendment. 
	However, not many countries have laws that recognize code as free speech. As a result, code sharing platforms will continue face request from these governments to censor codes created and shared by individuals of interests. It is not news that Github continues to face threats and attacks from government[6] who want repositories removed.  
	While code sharing platforms face real threat from external and hostile actors, they can also exert censorship actions upon users and their projects according to pre-determined or arbitrary terms. 
	Additionally, not only are users exposed to censorship behaviours instigated by external agents and the code sharing platform, they are also vulnerable to censorship by project admins and maintainers. Project maintainers are free to prevent access and use of their repositories at any time and by their own terms.  
	The various levels of censorship threats make centralized code sharing platform unsuitable for hosting communities building innovative, competitive and possibly contentious applications and services. They will be able to remove any repository, selectively mute, block or prevent people from contributing, expressing themselves or accessing content. 
	
### 2.2.2. Ownership

Most services on the web are built with an account system them grants ownership and authority to one person identified by their email or phone number. Some of the motivation for this is the need to maintain security and to determine who pays the bills. 
	Code sharing platforms are among the service providers built on this single owner structure. All repositories must be owner and managed by one person who is granted complete privileges to create, access and destroy any resource associated to their account. 
	The consequence of this is that complex, sovereign and community-led organizations cannot build softwares in a trust-less manner as these collaborators must trust the root account owner. One popular approach  employed to remedying this problem involves the creation of committees and other secondary structures. But we argue that these structures do not deliver true ownership and governance since there is a root password managed by an individual or organization. 
	In the crypto industry, they say “If you do not own your private keys, you do not own the coins”.  Likewise for open source projects on code sharing platform, “If you do not own the password, you do not own the project”. It is important that contributors of community-led platforms have the ability to truly share ownership of a project without needing to trust a central authority such as the owner or maintainer of a repository or the platform operator. True ownership of a community software cannot be granted based on faith that the authority will always act in the best interest of collaborators, it must be enforced. 

### 2.2.3. Immutability

The concept of immutability in computing refers to the unchanging, unalterable state of data. It refers to the inability of a piece of data to be altered. Immutable data is easy to reason about; We can make assumptions and build on top of them with certainty that their state will never change unexpectedly. 
	Interestingly, the Git version control system used my millions of collaborators and supported by most code sharing platforms utilizes an immutable data structure. Git includes concepts like branches and commits; Commits are backward linked collections of changes that exists inside a branch. Collaborators can begin working from any commit and never have to worry that future commits will alter the state of the commits they are extending. 
	However, code sharing platforms do not guarantee immutability of an entire repository. Repositories as a whole are not immutable; They can be deleted by their owners or the platform operators. It is important to node that the ability to delete repository can serve as a tool for censorship. An account owner or platform operator can prevent people from collaborating by remove a repository from existence. 
	The lack of guaranteed immutability on code sharing websites makes them unappealing for hosting community-led services. It will be devastating for a community to one day to find their shared repository deleted by the account owner or platform operator. 

### 2.2.4. Governance

For open source communities to succeed at creating and managing decentralized organizations, they must first figure out governance, otherwise what would be obtainable is chaos and uncertainty. These communities need to be able to formulate a governance system that is acceptable to all parties. 
	On centralized code sharing platforms, there is only one kind of governance system — One where the account owner dictates how and when collaborators interact with and contribute to the project. As a remedy, popular projects delegate control to reputable, structured open source organizations like Apache Software Foundation or the Linux Foundation. 
	Unfortunately, governance built on systems where the rules are enforced by humans can not be absolutely trusted to be consistent and fair at all times. These organizations are not flexible enough to accommodate different governance models or support frequently changing governance rules and as such, they are not suitable for decentralized organizations. 
	The ideal collaboration framework for decentralized organizations must provide vendor-neutral governance tools. Instead of dedicating the governance scheme, it should provide tools that allow communities to construct, install and upgrade governance configurations with the ability to enforce them. 

### 2.2.5. Economic Incentives

People do not contribute to open source software in an irrational manner. They do it because there is something to gain. Many people contribute because they want to learn or be members of a community of like-minded individuals. There are those who do it to improve their reputation so that prospective employers may be interested in their abilities. Companies whose business model depends on an open source software are also incentivized to contribute to it. 
	A popular misconception in open source is the idea that open source contributions should attract no financial incentive and remain a free and voluntary activity. But the truth is, most open source contributions impose time and financial commitments on contributors who need to develop, test, document, evangelize and fix bugs to ensure the product is suitable for both individual developers and enterprises. It is unrealistic to expect contributors to consistently offer their time and money to a project that gets used by others for commercial purposes and expect no form of financial compensation as incentives to continue to remain committed to the project.  If the quality of open source software is to be maintained or improved, the best way to guarantee it is by bringing financial incentives to the table. 
	Today, there are two major channels by which open source collaboration may receive financial incentives — Through code sharing platforms or open source foundations. Code sharing platforms have the ability to create mechanisms that allow open source developers receive financial incentives, but they do not do this. These platforms do a lot to enable collaboration but not enough to allow contributors receive financial incentives. Open source foundations such as Apache Software Foundation are able to receive donations and generate income through sponsorship, merchandise sales, support and hosting conferences but those funds are for the day-to-day running of the foundation of which none of it go down to non-employee contributors. There needs to be a trusted, transparent and automated mechanism for creating, verifying and transferring value between users and developers of open source software. The introduction of such mechanism will create many types of open source economies (such as bounty, bug hunting, support services, etc). 
	In the era of community-led services, collaborators will need to be able to generate or receive financial rewards to support continuous development and execution of their services. While centralized code sharing platforms are unsuitable to provide the needed infrastructure, blockchain technology can allow collaborators created shared software products, formulate protocol enforceable governance structure, vote and authorize actions and receive and distribute financial incentives without intermediaries. 


### 2.2.6 Execution Environment

To go beyond projects like libraries, frameworks, CLI tools to community-led services, we need to begin to consider program execution environments that are suitable for running shared applications in the form of dApp, SaaS, API and other user-facing software. This execution model must lend itself to be deployed, operated and governed according to the governance structure instituted by the community. Collaborators will need an environment to run tests, stage and deploy their applications. 
	Most code sharing platforms only provide continuous integration environments with the configuration of this environment still subjected to the authorization of the single account owner. There is need for a mechanism that allows a community to collectively decide what kind of execution environment and configuration they want for their projects.			A deployment environment include a tool that runs an application and makes it accessible to target users. The ideal deployment environment must be unalterable, autonomous and can only allow itself to be upgraded according the governance rules of the community. 
	Historically, consumer applications have been executed in a centralized, managed environment but with the emergence of blockchain platforms like Ethereum, applications can now be executed decentrally on thousands of nodes in a trust-less and autonomous manner.  Decentralized applications are immutable, they cannot be altered or destroyed once deployed.   
	While many believe blockchain applications should replace all centralized applications, we believe community-led services can leverage on both types of service deployment environments according to their goals; This way they are better positioned to directly compete with centralized services providers on all fronts. 

## 3. The Ideal Platform for Open Source Service

In section 2, we discussed the reasons why centralized code sharing platforms are unsuitable for leading the charge towards a future of community-led software products and organizations. These changes range from censorship, ownership and governance to execution models. We can see that the major obstacle is the inability to enforce ownership, transparency and accountability. 

We will take the following approaches to solve the issues:

	* Ellcrys will use blockchain technology to eliminate censorship concerns by creating a new type of decentralized collaboration framework that is open to anyone, anywhere and cannot be destroyed. There will be no entity to receive and carry out censorship requests. 
	
	* The use of public key cryptography as the primary mechanism to derive an identity and to authorize actions, will allow projects to have multiple owners or signatories who are able to partake in the day-to-day governance of the project through their ability to create and vote for or against on-chain proposals.

	* By the very nature of blockchains, repositories will remain immutable and always accessible to everyone. Although, owners of the repositories may enable the ability to apply access level rules to prevent unauthorized write operations.  
	
	* The introduction of autonomous procedures (a.k.a smart contracts) will allow communities to create indestructible applications to enforce ownership, governance, incentive structure and disbursement and business rules. Autonomous procedures run an a blockchain-enabled execution environment (or virtual machine).

	* The use of Git will make it easy for millions of developers who are already familiar with the tool to easily create repositories, contribute, import their existing projects and integrate with other git compatible tools they already use. 

	* With a well defined ownership and governance structure, external service providers can deliver value based on just the governance history of a project. For instance, a community may create and vote for a well detailed proposal to run ads on Google Adwords, upon the approval, a designated service creates a campaign on Google Adwords using the information provided in the proposal. 
	

## 4. Bitcoin
In this section we will briefly discuss bitcoin, its consensus mechanism and particularly its inability to process enough transactions per second to meet mainstream users’ needs.    

### 4.1. Introduction

Bitcoin is a form of electronic cash. It is a decentralized digital currency that does not have a central bank or a trusted authority. It can be sent from person-to-person faster and cheaper without restrictions. Using cryptography, transactions are verified and transmitted through a peer-to-peer network of computers that update account balances and record changes in a public distributed ledger known as a blockchain[8]. Bitcoin was invented by Satoshi Nakamoto[9] and released to the public as an open source software in 2009. 

###  4.2. Consensus Mechanism
	
Blockchain networks require a means to reach an agreement on a single value. Consensus algorithms define the rules that must be followed by computers on the network in other to reach agreement. The process of arriving at an agreement with other computers is known as the consensus problem and it is well researched field in computer science.
	Bitcoin uses a consensus algorithm known as Proof of Work[9] (PoW). It is used to process blocks of transactions and append them to a chain of blocks — the blockchain. In Bitcoin,  the process of appending a block to the blockchain is known as “mining” and the individuals who take part in the mining process are known as “miners”. PoW requires miners to solve complex cryptographic puzzles to gain the right add a block. 
	Miners are rewarded with Bitcoin for solving the puzzle. This reward is known as the block reward. Before the reward is issued, the generated block must follow the consensus rule. All other nodes on the network are responsible for verifying the block and enforcing the consensus rule. Once a miner discovers a valid block they did not create, they immediately stop and restart mining the next block. There is a network difficulty that ensure blocks are created within 10 minutes. It determines how hard it is for the miners to miner a block and adjusted dynamically to maintain the 10 minutes window.  
	Bitcoin’s PoW has a disadvantage of being very slow. It has so been described a consensus system that wastes energy and is causing harm to the planet. However, it is the most battled tested and well understood trust-less consensus system for cryptocurrency. 

### 4.3. Low Transaction Through-put 

Bitcoin pioneered the blockchain industry and made it attractive for different categories of people who believed in its vision. Developers have created clones and alternative implementations intending to improve on the capabilities of Bitcoin. One of the main motivation fueling the creation of Bitcoin alternatives is the inability of the Bitcoin network to process large amounts of transactions sufficient to handle the needs of mainstream users. It takes 10 minutes for the bitcoin network to create a new block and even more to confirm the permanence of a transaction. It is widely agreed that for cryptocurrency to go mainstream, it must be able to handle thousands of transaction per second. 

### 4.4. Alternative Consensus Mechanisms

 Since the introduction of Bitcoin, developers and researches have been working on alternative consensus algorithms that are more efficient and performant than proof of work. The most popular of these alternatives is Proof of Stake (PoS).  
	In Proof of Stake, the blocks are not created by miners solving difficult math puzzles, but by forgers or minters staking their money to bet on the validity of a block. When a majority vote on the correct chain of blocks, those who voted for the wrong chain may lose their stake. 
	Proof of Stake is faster and more energy efficient than Proof of Work, but it suffers from a serious problem known as “Nothing at Stake”. The concern behind “Nothing at Stake” is that since it cost next to nothing to support a fork, validators can vote for every fork that happens without any serious consequence; This is unlike proof-of-work where a computational hard problem must be solve to extend a chain. 

#### 4.4.1. Bitcoin-NG

The performance of blockchain protocols are limited by two factors — block size and block interval. Increasing the block size, correlates to an increase in transaction throughput, but requires bigger blocks that take more time to propagate to nodes on the network. Decreasing the block size, reduces the time it takes for blocks to propagate to nodes, leading to frequent reorganization. The Bitcoin system traded transaction through-put for latency by using a small block of 1MB which amounts to 1 to 3.5 transactions per second.  
	Bitcoin-NG[10] is a scalable blockchain protocol designed to improve the through-put of Bitcoin without affecting the same trust model that exists in Bitcoin. It achieves performance improvement by introducing the concept of leader election and transaction serialization. In BitcoinNG, time is divided into periods known as “epoch”, where every epoch has a leader. Once a node becomes a leader, it is expected to produce blocks until a new leader is discovered. Leader election is performed randomly in the same way miners in Bitcoin find blocks infrequently. 
	BitcoinNG ensures that the system is able to process transactions even when the network works to find a new leader unlike the Nakamoto Consensus in Bitcoin where no transaction is processed during the 10 minutes block interval. 

## 5. Ellcrys Protocol
In this section describes the engineering direction of our protocol.  Existing knowledge of blockchain technology is essential. Please note that some concepts described below are not final and may be subject to change.
 
### 5.1. Consensus Model

#### 5.1.1. Hybrid Protocol

The Ellcrys consensus mechanism is an hybrid consensus algorithm of both Proof of Work and Proof of Stake. Our consensus model is based on concepts described in the Proof of Activity[11]  protocol by Iddo Bentov et al.  They described a process of extending Nakamoto Proof of Work via Proof of Stake to increase the security of the network while reducing the dependence on miners as the only contributor to network security. Iddo Bentov et al questioned the capability of Bitcoin miners to sustain the security of the system when PoW is no longer subsidized via the block reward. We agree with their assertion that a cryptocurrency protocol should be designed in such a way that its incentive structure encourages different participants in the system to sustain its health. 

#### 5.1.2. Bitcoin-NG — Leader-based Block Creation 
	
Bitcoin-NG extends Nakamoto consensus into a protocol that is capable of processing more transactions than Bitcoin. It does this by introducing a leader-based block creation scheme where a miner is entitled to create several more blocks at faster intervals after they mined a block known as a “key block”.  Ellcrys PoW implementation will be based on Bitcoin-NG to improve transaction through-put through improved latency and bandwidth.  

### 5.2 Coin Generation

In most public blockchain systems with a native cryptocurrency, new coins are generated when a new block is mined. The generated coins are shared to the miner and any other network participants who contributed to the creation or validation of the new block at a pre-determined ratio. In Bitcoin and other similar proof of work blockchain, the miner of the block receives all the newly generated coins. 
	We believe a system built on a coin generation model where a single participant receives all rewards is unfair and does not promote equitable distribution of wealth generated by the network. In matured proof-of-work blockchains like Bitcoin, a user must be able to afford specialized equipments to be able to compete with well-funded, corporate organizations. The inability for small miners to compete fosters a system that is only centralized between to a few individuals, pools and mining companies. 

#### 5.2.1 PeopleMint

We introduced PeopleMint[12] — A novel coin generation model that allows anyone to participate in the creation of new coin by exchanging their national banknotes for new coins. PeopleMint gives everyone a chance to participate in coin creation using a material (a currency note) that is both valuable and accessible to all class of people. Banknotes are raw material a miner needs to be able to create new coins and receive reward for their work. Without it, a miner will be compensated only through transaction fees. 
	PeopleMint creates a symbiotic relationship between a global population of users and miners that work together to sustain the system while also discouraging miner centralization by diversifying the process of coin creation. In Bitcoin, PoW mining is the only mechanism through which new coins are introduced. Miners do not need any other party and are incentivized to invest more in infrastructure to outcompete other miners. The result is that mining becomes centralized within a small group who provide most of the security of the network. PeopleMint provides a fair coin generation model as well as a mechanism to keep miners in check through a human-driven process of observing and vouching for a chain. 
	In PeopleMint, a user takes a short video in which she must capture an image of a banknote that has part of the hash of a recent block engraved on it. She sends a transaction that references the short video to a node X. Node X performs preliminary image analysis operations to assert that an image of a banknote was captured. Upon correct assertion, the transaction can be included in a block. Human-driven validation process commences when the transaction is added to a block; Anyone in the world can stake money to predict the validity of the banknote. We utilize a well researched concept known as the wisdom of the crowd to determine banknote validity. When a banknote is considered valid, the owner of the banknote and validators share a part of the allocated reward in proportion to their stake.  

### 5.3. Network Participants

We now describe the types of network participants working together to sustain the system.

### 5.3.1. Miners

Miners are individuals who participate in Proof of Work attempting to create blocks by solving hard cryptographic puzzles by burning energy. In Bitcoin, miners are responsible for finding solution to the puzzle, using the result to create blocks containing transactions and broadcast to the network. Likewise in Ellcrys, miners are responsible for creating _key_ and _microblocks_. Key blocks are similar to Bitcoin’s block in that they are created by expending energy, while microblocks are created at pre-determined interval and do no require energy investment. 

### 5.3.2. Witness

Witnesses are stakeholders who validate key blocks, microblocks and extend microblocks with additional transactions. Witnesses serve as validators that audit the work of miners. They enable a power dynamics and diverse incentive structure	 where stakeholders continuously ensure miners abide by the protocol rules. 
	When a block is received, every witness online checks whether the block’s header is valid; It checks if the header contains a previous block’s hash, if the difficulty matches the expected current difficulty and whether the block renumeration is valid. Once validated, the witness checks whether it was one of N witnesses selected to verify this block. It does this by running a pseudo-random operation to determine the N witnesses and when it finds that it was selected, the witness signs the hash of the block and broadcast the signature to the network. 
	When the Nth witness sees that it was derived by the block, it creates a wrapped block that extends it. If the block is a microblock, it includes as many transactions as the remaining block capacity can support, the signatures of the other selected witnesses and its signature of this wrapped block. The Nth witness broadcasts the wrapped block to the network and when other nodes see that it is valid, they append it to their best chain. 

### 5.3.3. Endorser

One of our core mission is to make it convenient for collaborators to create blockchain applications written in standard, general-purpose programming languages. Current blockchains that provide application execution environment require these programs be written in domain-specific languages. The requirement to use domain-specific language limits wide-spread adoption and may lead to buggy, insecure applications. 
	The use of domain-specific languages is due to fact that blockchain applications written in general-purpose languages can produce non-deterministic code that can lead to the creation of forks; This can be exploited by bad actors to prevent the network from agreeing on the validity of a block, thereby halting the system. Many programming languages include standard features produce non-deterministic behaviour (e.g Go map keys are randomized). 
	Hyperledger Fabric[11], which is the first blockchain system to support the use of multiple, well established languages solved this problem of non-determinism by separate transaction execution, ordering and validation using a novel approach known as _execute-order-validate_ architecture	. In this model, a client sends a transaction to peers specified in an endorsement policy. Each transaction is then individually executed by the peers and its output recorded. This process is called _endorsement_. The client must collect N endorsements up to the amount specified in the endorsement policy. After collecting enough endorsement, it creates a transaction and broadcasts it to the ordering service for inclusion into a block, after which the ordering service broadcast the block to the rest of the network to perform the validation phase. During validation, transactions that failed to pass the endorsement policy or have non-deterministic outputs are ignored. 
	Our execution model is based on a similar pre-consensus transaction execution and endorsement strategy. On Ellcrys, endorsers are stakeholders who are responsible for executing and endorsing transactions based on a global endorsement policy. Endorsers are former witnesses of the previous epoch.  When a client broadcasts a transaction, a node X checks whether it was a witness in the last epoch. If it was, it is required to endorse the transaction and return an broadcast a signed endorsement report to its peers. Node X collects endorsements and creates and a transaction to be added in the next block.
	
### 5.3.4. Banknote Scanners (“Scanners”)

Banknote scanners are individuals who provide short videos of banknotes required to create new coin. As described in Section 5.2.1, PeopleMint allows anyone to exchange banknotes for the native currency. Scanners  annotate the hash of a recent block, take a short video that captures the banknote and send this video to the network for analysis and validation. 
	Scanners are required to annotate their banknotes to fulfil an chain observer role. The more observers a chain has the great its chances of becoming or retaining the best chain choice. To increase the security of the network, we will be take into account the amount of banknotes a chain has received as a criteria in our fork choice rule.  


### 5.3.5. Banknote Validators (“Bettors”)

Banknote validators predict the validity of a banknote that was created by a scanner. Their opinion, along with those of other banknote validators is used to determine the correctness and validity of a banknote, as well as any other metadata associated with the node. 
	Validators perform their duties by staking a pre-determined amount of the native coin along with their response to the market’s questions such as (1) whether or not the banknote looks authentic, (2) what is the denomination of the note is, (3) the currency code of note’s native country and lastly (4) what the hash that was annotated on the note is. 
	The information provided by a validator for a given banknote is compared with the prediction of other validators who observed and predicted on the same banknote. A prediction is considered correct if it matches the outcome predicted by the majority of banknote validators. If a validator’s prediction does not match that of the majority, they lose their stake to the majority. Bettors who are part of the majority not only share the stake of the bettors who lost, but also share a fraction of the block reward.


### 5.4. Block Creation

The protocol divides time into _epochs_. In each epoch, a single leader is chosen to extend the blockchain by creating blocks known as _key_ and _microblock_ blocks. Key blocks indicate the beginning of an epoch after which the key block creator is entitled to create microblocks at faster intervals. 

#### 5.4.1 Key Blocks

Miners are free to start an epoch by creating a _key_ block via the same Proof of Work computation performed in Bitcoin. A _key_ block header includes the unique reference of its predecessor, the current time, the public key of its creator to payout the reward, difficulty information and coin generation transactions.  Unlike Bitcoin, the public key of the key block creator is added to the header and used to verify subsequent microblocks. Similar to Bitcoin, Key blocks creation time are determined by the network difficulty. For example, Bitcoin’s difficulty dynamically adjusts to target a 10 minutes block creation interval. Ellcrys will set a target of 2 minutes between each block. 

#### 5.4.2 Microblocks 

After a node has generated a key block to become the leader, it is allowed to generate microblocks which can include transactions. Microblocks must be generated at a deterministic rate. A microblock is considered invalid, if the difference between the timestamp of a microblock and its parent is less than a predetermined minimum or its timestamp is a future time. The constraints are put in place to prevent a malicious node from overwhelming the system with microblocks. 
	A microblock contains transactions and a header. The header contains the hash of the previous block, the current timestamp, the merkle root of the transactions and the signature of the header. The signature must be created using the private key of the most recent key block in the chain.

#### 5.4.3 Block Validation 

After the creation of key or microblocks, the client will broadcasts the block to its peers and soon it will reach all nodes. All witness nodes must check whether they have been selected to validate the received block by running a pseudo-random, deterministic algorithm that derives a set of eligible witnesses. Every witness who is online will check whether the block is valid, sign the hash of the block header with the private key that controls their staking account and broadcast their signature to the network. 
	One of the peers in the set of eligible peers must create a wrapped block, it may include some transactions if the received block is a microblock and broadcast to its peers. Upon receipt of a wrapped block, the node  validates its header, any transactions it may have and appends it to its chain. The wrap block must contain signatures of 2/3 of the N peers in the computed validation set. The fee from the transactions in the wrapped block will be shared between the miner and the witnesses. We have set N to be equal to 5. 

### 5.5. Transaction Execution Model



























