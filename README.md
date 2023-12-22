# A simplified Rust-Audit-Roadmap

Before delving into the Alphas, I invite you to explore this brief article detailing the current status of Rust in the Web3 industry: [Rust in the Web3 industry](https://daniejjimenez.medium.com/ewasm-where-we-are-and-where-we-are-going-c5b0d80a0e5e).

Presently, eWASM in Ethereum appears to be largely inactive. However, it's worth noting that WASM is thriving in various other blockchain ecosystems.

Here's a straightforward recommendation:
1. Acquire a solid understanding of blockchain and smart contract fundamentals.
2. Familiarize yourself with Rust programming language.

The popularity of the following frameworks and protocols is as follows (as of Dec 2023):
1. !ink
2. CosmWasm
3. CosmWasm Security
4. Astar


## Blockchain and smart contracts basics

You first need to be familiar with the basic concepts of blockchain technologies and smart contracts in general. I came from Solidity and Ethereum auditing myself, so I'm not very sure which ones to recommend if you don't have any experience and don't want to get much into it… For readers [Mastering Ethereum](https://github.com/ethereumbook/ethereumbook), the most popular would be Patrick Collins blockchain elaborations.

:information_desk_person: You can probably find a lot of recommendations for this already :)

###  Patrick Collins Blockchain for Beginners 

*[⌨️ (00:09:05) Lesson 1: Blockchain Basics](https://www.youtube.com/watch?v=gyMwXuJrbJQ&t=545s)*
### What is a Blockchain? What does a blockchain do? 
-   [What is a Smart Contract?](https://chain.link/education/smart-contracts)
-   [Hybrid Smart Contracts](https://blog.chain.link/hybrid-smart-contracts-explained/)
-   [Blockchain Oracles](https://betterprogramming.pub/what-is-a-blockchain-oracle-f5ccab8dbd72?source=friends_link&sk=d921a38466df8a9176ed8dd767d8c77d)
-   [Terminology](https://connect.comptia.org/content/articles/blockchain-terminology)
-   [Web3](https://en.wikipedia.org/wiki/Web3)
-   [What is a blockchain](https://www.investopedia.com/terms/b/blockchain.asp)

### The Purpose Of Smart Contracts
*[⌨️ (00:18:27) The Purpose of Smart Contracts](https://youtu.be/gyMwXuJrbJQ?t=1107)*
- 🎥 [Original Video](https://www.youtube.com/watch?v=_JeRq7Gwj5Y&feature=youtu.be)
- 🦬 [My ETH Denver Talk](https://www.youtube.com/watch?v=06hXCX_jj2E)
- 🍔 [McDonalds Scandal](https://www.chicagotribune.com/sns-mcdonalds-story.html)
- ⛓ [More on the evolution of agreements](https://www.youtube.com/watch?v=ufVyX7JDCgg)
- ✍️ [What is a Smart Contract?](https://www.youtube.com/watch?v=ZE2HxTmxfrI)
- 🧱 [How does a blockchain work?](https://www.youtube.com/watch?v=SSo_EIwHSd4)
- 🔮 [Chainlink & Oracles](https://www.youtube.com/watch?v=tIUHQ7sDoaU)

### Other Blockchain Benefits
*[⌨️ (00:30:41) Other Blockchain Benefits](https://youtu.be/gyMwXuJrbJQ?t=1841)*
- Decentralized
- Transparency & Flexibility
- Speed & Efficiency
- Security & Immutability
- Counterparty Risk Removal
- Trust Minimized Agreements

### What have Smart Contracts done so far?
*[⌨️ (00:36:36) What have Smart Contracts done so far?](https://youtu.be/gyMwXuJrbJQ?t=2196)*
- [DeFi](https://chain.link/education/defi)
  - [Defi Llama](https://defillama.com/)
  - [Why DeFi is Important](https://medium.com/the-capital/why-defi-1519cc4d4bd3)
- [DAOs](https://betterprogramming.pub/what-is-a-dao-what-is-the-architecture-of-a-dao-how-to-build-a-dao-high-level-d096a97162cc)
- [NFTs](https://www.youtube.com/watch?v=9yuHz6g_P50)


## Rust language

**Summary: Why Rust for Smart Contracts?**

The choice of Rust for smart contracts, particularly with ink!, is rooted in several compelling reasons:

1. **Ideal Contract Language:** Rust is inherently suitable for smart contracts due to its type safety, memory safety, and absence of undefined behaviors. It produces small binaries by avoiding unnecessary elements like a garbage collector, and advanced optimizations enhance efficiency by eliminating dead code. Rust can automatically guard against integer overflow through compiler flags.

2. **Robust Ecosystem:** Leveraging the Rust ecosystem comes as a bonus, with ink! automatically benefiting from ongoing language developments. This ensures continuous access to new features and functionalities, enhancing the overall capability of writing smart contracts.

3. **Comprehensive Tooling:** Being aligned with Rust standards, ink! seamlessly integrates with widely used tools such as rustfmt, clippy, and rust-analyzer. This compatibility extends to code formatting and syntax highlighting in modern text editors. Rust's integrated test and benchmark runner contribute to effective testing practices.

4. **Minimal Runtime Overhead:** Rust imposes minimal runtime overhead, contributing to the efficiency and streamlined execution of smart contracts.

5. **Safety and Efficiency:** Rust offers zero-cost and safe abstractions, prioritizing the creation of secure and efficient smart contracts.

6. **Productivity Boost:** Utilizing Cargo and the crates.io ecosystem enhances productivity, providing a robust infrastructure for managing dependencies and facilitating efficient code development.

7. **First-Class Wasm Support:** Rust ensures first-class support for WebAssembly (Wasm), aligning seamlessly with the demands of the blockchain environment.

8. **Small Code Size:** In the context of space-constrained blockchains where size is crucial, Rust's compiler aids in minimizing code size. By reordering struct fields intelligently, Rust achieves compact data structures, often surpassing the compactness achieved in C.

In essence, Rust stands out as a language for smart contracts, offering a balance of safety, efficiency, productivity, and compatibility with the broader Rust ecosystem.

Achieving a high level of proficiency in Rust programming isn't necessary when you're just starting. Instead, focus on developing a clear understanding of Rust code and the ability to create basic programs, which can be quite challenging, in my opinion. If you have any questions along the way, consider [the Rust Book](https://doc.rust-lang.org/stable/book/) as your primary reference.

There are numerous free basic courses available, such as [Udemy: Ultimate Rust Crash Course](https://www.udemy.com/course/ultimate-rust-crash-course/) and its follow-up, [Ultimate Rust 2](https://www.udemy.com/course/ultimate-rust-2/).

:bulb: Explore easy-to-follow code examples or try your hand at implementing them by visiting [Rust by Example](https://doc.rust-lang.org/rust-by-example/). 
These tutorials are a must do [Exercism's Rust path](https://exercism.org/tracks/rust), offer additional Rust exercises.

:star: Personally, I found [Rustlings](https://github.com/rust-lang/rustlings) enjoyable. It lets you learn Rust by fixing code snippets that you need to understand beforehand, akin to auditing.

For quick and ready-to-go testing of random code and behaviors, make use of [Rust Playground](https://play.rust-lang.org/).

If you want to focus soley on Solana: [Blog post by Vitto](https://vitto.cc/the-complete-solana-development-roadmap/)

## Substrate

Substrate is a Software Development Kit (SDK) that allows you to build application-specific blockchains that can run as standalone services or in parallel with other chains with the shared security provided by the Polkadot ecosystem.
**Summary: 

Substrate, in conjunction with Rust, offers a comprehensive framework for blockchain development. The process is tailored to cater to different levels of expertise and preferences. Here's a quick overview:

1. **Quick Start:**
   - **Target Audience:** New developers with no prior Substrate or FRAME experience.
   - **Objective:** Set up a development environment and initiate a blockchain node on the local computer.
   - **Steps:**
     - Brief overview of Substrate.
     - Learning to compile and start a node.
     - Exploring node template code.
     - Modifying the runtime.

2. **Developer Journey:**
   - **Structured Information:**
     - **Learn:** Core blockchain and Substrate concepts and operations.
     - **Install:** Platform-specific installation instructions and troubleshooting tips.
     - **Build:** Tools and techniques for building custom blockchain applications.
     - **Test:** Approaches for unit testing and benchmarking code.
     - **Deploy:** Options for deploying nodes, preparation, and transitioning from test to production.
     - **Maintain:** General information on network maintenance, upgrades, and infrastructure management.

3. **Tutorials:**
   - **Hands-on Learning:**
     - **Build a Blockchain Tutorials:** Focus on network basics, starting from a single node to creating private blockchains, monitoring operations, and upgrading networks.
     - **Build Application Logic Tutorials:** Implementation of application-specific logic using existing and custom pallets.
     - **Build a Parachain Tutorials:** Guidance on transitioning from a standalone chain to a parachain, connecting to a relay chain, and inter-chain messaging.

4. **Reference:**
   - **Technical Information:**
     - **Rust API:** Direct access to technical details.
     - **Command-Line Tools:** Assistance and information on command-line tools.

In essence, the integration of Rust and Substrate provides a versatile and accessible approach to blockchain development, accommodating diverse learning styles and levels of expertise. The documentation is organized into a narrative developer journey, hands-on tutorials, and a reference section for technical details.

- [Documentation](https://docs.substrate.io/quick-start/)
- [Website](https://substrate.io/)
- [Leverage Rust in Substrate](https://paritytech.github.io/substrate/master/sc_service/)
### !ink 
ink! is a programming language for smart contracts — one of several that blockchains built with the Substrate framework can choose from. It’s an opinionated language at Parity have built by extending the popular Rust programming language with functionality needed to make it smart contract compatible.

- [Blog on !ink](https://www.parity.io/blog/what-is-paritys-ink)
- [Documentation](https://use.ink/)
- [!ink vs Solidity](https://use.ink/ink-vs-solidity)
- [!ink vs CosmWasm](https://use.ink/ink-vs-cosmwasm))

## CosmWasm

By now, you should possess a basic understanding of blockchain technologies, smart contracts, and Rust. It's time to delve into CosmWasm. Ethan Frey [@ethanfrey] has curated a series of posts, albeit outdated, providing a comprehensive overview and comparison with other technologies:

- [CosmWasm for Developers](https://blog.cosmos.network/cosmwasm-for-developers-7640ee38430f)
- [CosmWasm for CTOs 0](https://medium.com/cosmwasm/cosmwasm-for-ctos-f1ffa19cccb8), [I: the architecture](https://medium.com/cosmwasm/cosmwasm-for-ctos-i-the-architecture-59a3e52d9b9c), [II: advanced usage](https://medium.com/cosmwasm/cosmwasm-for-ctos-ii-advanced-usage-ee04ce95d1d0), [IV: native integrations](https://medium.com/cosmwasm/cosmwasm-for-ctos-iv-native-integrations-713140bf75fc)

:milky_way: Since CosmWasm operates as a Cosmos SDK module, running on Cosmos chains, it's crucial to familiarize yourself with Cosmos fundamentals. Begin by reading the following Cosmos documentation:
1. [Introduction section](https://docs.cosmos.network/v0.47/intro/overview) covers a high-level overview, application-specific blockchains, blockchain architecture, and main components of the Cosmos SDK.
2. [Basics section](https://docs.cosmos.network/v0.47/basics/app-anatomy) includes the anatomy of a Cosmos SDK application, transaction lifecycle, query lifecycle, accounts, and gas and fees.

:point_right: Now, let's immerse ourselves in CosmWasm. Reading the [CosmWasm Book](https://book.cosmwasm.com/) cover to cover is an excellent starting point for grasping all the concepts before venturing into contract development. Additionally, [this resource](https://github.com/CosmWasm/cosmwasm/blob/main/SEMANTICS.md) serves as a helpful quick reference, offering details not explicitly covered in The Book.

Your next focus will be on CosmWasm smart contract programming. You should be able to write simple CosmWasm contracts, and [CW Template](https://github.com/CosmWasm/cw-template) provides a great resource for experimentation. A list of resources is provided below, and while some content may overlap, the intention is to offer multiple options rather than completing all of them:

1. [CosmWasm zero to hero](https://github.com/Callum-A/cosmwasm-zero-to-hero)
2. [CosmWasm Academy](https://academy.cosmwasm.com/)
3. [Area 52](https://area-52.io/)
4. [Terra academy: CosmWasm smart contracts I](https://academy.terra.money/courses/cosmwasm-smart-contracts-i)

:heavy_plus_sign: [CosmWasm Plus](https://github.com/CosmWasm/cw-plus) comprises publicly available base contracts, akin to [OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts). Reviewing key contracts and understanding their architecture and behavior is an excellent way to hone your Smart Contract analysis skills, a vital skill for future auditors:

- [CW20 fungible token](https://github.com/CosmWasm/cw-plus/blob/main/packages/cw20/README.md)
- [CW721 non-fungible token](https://github.com/CosmWasm/cw-nfts/blob/main/packages/cw721/README.md)
- [CW1 fixed multisig](https://github.com/CosmWasm/cw-plus/tree/main/contracts/cw3-fixed-multisig)

:100: Additionally, familiarize yourself with Smart Contract testing, as you'll craft your own PoCs using these. Refer to [Mastering CosmWasm Multi-Test](https://medium.com/obi-money/learn-cosmwasm-multi-test-easy-rust-smart-contract-apps-96818550ba3d) for a practical crash course. Further documentation on the most used libraries can be found at:

- [Module cosmwasm_std::testing](https://docs.rs/cosmwasm-std/latest/cosmwasm_std/testing/index.html)
- [Crate cw_multi_test](https://docs.rs/cw-multi-test/latest/cw_multi_test/), with a [chapter in the CW Book](https://book.cosmwasm.com/basics/multitest-intro.html)

Getting acquainted with [IBC in CosmWasm](https://github.com/CosmWasm/cosmwasm/blob/main/IBC.md) is a valuable addition, as it will likely become more common in CosmWasm contracts. While not mandatory initially, understanding IBC is crucial for your development journey.

An alternative framework for building CosmWasm smart contracts is [the Sylvia Framework](https://medium.com/cosmwasm/the-sylvia-framework-release-b4ffbb74fe3d). However, its community traction is uncertain at the moment, as I haven't encountered requests for audits related to it.


## CosmWasm Security

Now that you've covered all the prerequisites, it's time to delve into the audit and security specifics of CosmWasm. If you're transitioning from Solidity auditing, you'll likely notice a scarcity of resources compared to the abundance of beginner security material available for Sol/EVM.

:scroll: Begin with the [CosmWasm Security Spotlight posts](https://github.com/jcsec-security/cosmwasm-security-spotlight), and keep an eye out for future posts on [Medium (@jcsec-audits)](https://medium.com/@jcsec-audits). Additionally, DAO DAO's [CosmWasm security best practices](https://github.com/DA0-DA0/dao-contracts/wiki/CosmWasm-security-best-practices) offer valuable insights.

:muscle: The next step involves practical examples:

1. [Oak's CosmWasm Security Dojo](https://github.com/oak-security/cosmwasm-security-dojo): This resource not only provides challenges but also includes an `EXPLANATION.md` in each directory, offering further details and concepts that prove highly beneficial.

2. [Oak Security CTF](https://github.com/oak-security/cosmwasm-ctf): This CosmWasm Capture The Flag (CTF), created by Oak Security for Awesomwasm 2023, offers a comprehensive overview of various security issues in CW contracts, with a medium difficulty level.

3. [DeFiVulnLabsCosmWasm](https://github.com/punishell/DeFiVulnLabsCosmWasm)

Given the limited availability of additional resources, the next step involves reading CosmWasm audit reports. This is the most effective way to familiarize yourself with the types of security issues identified during security reviews by auditors.

Three companies known for publishing multiple public reports on CosmWasm audits are:

1. [Oak Security](https://github.com/oak-security/audit-reports)
2. [SCV Security](https://github.com/SCV-Security/PublicReports/tree/main/CW)
3. [Halborn](https://github.com/HalbornSecurity/PublicReports/tree/master/CosmWasm%20Smart%20Contract%20Audits)

## Astar
Astar Network functions as a smart contract platform that accommodates both EVM and WebAssembly (Wasm) environments. As a parachain of Polkadot, it places emphasis on fostering corporate adoption and capturing consumer interest in web3 technologies. It's important to note that The Block is an autonomous media outlet, providing news, research, and data.
- [What is Astar?](https://astar.network/developers)
- [Audit Reports](https://github.com/AstarNetwork/Audits)

#### Tooling

I prefer using a VM instead of Windows WSL. It's faster, trust me. Learnt the hard way when participating hackathons.
- [Rust analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)
- [Better TOML](https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml)
- [Inline Bookmarks](https://marketplace.visualstudio.com/items?itemName=tintinweb.vscode-inline-bookmarks) - audit is just not the same without this one, MVP
- [CodeLLDB](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb) - Do you know you can debug rust unit tests for CW smart contracts? I may write a Medium post in the future
- [Coverage Gutters](https://marketplace.visualstudio.com/items?itemName=ryanluker.vscode-coverage-gutters) - easily displays test coverage from a `lcov` file
- [Line Note](https://marketplace.visualstudio.com/items?itemName=tkrkt.linenote) - I sometimes like to add 2/3 lines of additional info without breaking the total number of lines and not creating very large one-line comments
- [Cosmy Wasmy](https://marketplace.visualstudio.com/items?itemName=spoorthi.cosmy-wasmy) - To be honest this has not been helpful to me at the moment, but I keep it in check as it will probably be a nice addition soon when they further polish some of the features.

#### Side Note:
Whenever you use Rust or any frameworks. Ensure that different frameworks supports the same Rust Version. Once interfered, the debugging can be days....
