# Klaster Gateway - Easily manage assets across multiple blockchains

Blockchain is moving in an increasingly multi-chain future, where multiple independent L1s & L2s serve as infrastructure for an ever-increasing ecosystem of dApps. Many leading blockchain ecosystems, including Ethereum, Polkadot, Cosmos & Polygon - are moving in an "Internet of Blockchains" direction, whether through App-Chains, Rollups or other mechanisms. 

While this increases throughput & reduces execution prices significantly, it introduces a lot of operational complexities for teams who want to manage assets on multiple blockchains. This relationship is usually linear with every new supported blockchain adding additional operational complexity.

Some of the key problems we observed were:

* **Managing multisig wallets on multiple networks**
    * Adding or removing signers on one chain doesn't add or remove signers on other blockchains, which makes updating permissions for multisigs very difficult for teams handing assets on many chains.
    * Multisigs on different networks have different addresses, leading to a possible loss of funds if funds are sent on the wrong network.
    * Adding a new network is an operationally lengthy process of creating a new multisig, adding all permissions & acquiring gas tokens on the new chain.
* **Single DAO controlling treasuries on multiple networks**
    * A DAO can nativelly only call contracts on its "home" network, all other actions must be done off-chain, reducing trustlessness of the system.
    * Synchronizing DAO holders who hold tokens on non-native chains is very complicated for on-chain voting.
    * Cross-chain governance is almost always done off-chain.
    * No standardized way for a DAO to hold assets on multiple blockchains.
* **Users or DAOs holding gas on new networks or networks they use rarely**
    * One of the biggest UX hurdles for users using multiple blockchains is acquiring gas tokens on all networks.
* **Account abstractions / smart contract wallets managing assets on multiple blockchains**
    * Some smart contract wallet solutions offer gas relaying for gasless transactions, but this usually only works for a limited set of "supported" blockchains.

These and other problems are the reason we're working on building **Klaster Gateway**, an easy & standardized way for EOAs and smart contracts to control assets & addresses on multiple blockchains.

Key features:
* Interact with DeFi on all blockchains, while signing transactions & paying for gas on only one.
* Use multisig wallets, such as Gnosis Safe - to control assets on multiple blockchains.
* Compatible with all EOA wallets & smart contract wallets.
* Enable DAOs to execute actions on multiple blockchains, while voting on their "home" chain.
* No-code, user-friendly frontend for upgrading your multisigs & EOAs with multichain capabilities
* Composability guarantees - Klaster will notify the source chain whether the operations on the destination chain have been sucessfull or not.
* Automation - Execute multiple transactions on multiple blockchains with just one signature.

Architecture
![Untitled Diagram drawio(49)](https://github.com/0xPolycode/klaster-gateway-docs/assets/129866940/2b9d92e8-3ced-43ce-a6fb-38ab56392812)

Frontend preview:
<img width="1512" alt="Screenshot 2023-09-18 at 14 00 14" src="https://github.com/0xPolycode/klaster-gateway-docs/assets/129866940/87030596-a63c-4192-9ac1-6e1599e28fac">


