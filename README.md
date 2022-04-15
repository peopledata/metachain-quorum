
Metachain-quorum is a fork of [Goquorum](www.goquorum.com) and tailored to [PeopleData Community](www.peopledata.org.cn).

GoQuorum is an Ethereum-based distributed ledger protocol with transaction/contract privacy and new consensus mechanisms.

## Key features

### Inherit features from GoQuorum

Metachain-quorum inherit key enhancements from GoQuorum over go-ethereum:

* [__Privacy__](https://consensys.net/docs/goquorum//en/latest/concepts/privacy/privacy/) - GoQuorum supports private transactions and private contracts through public/private state separation, and utilises peer-to-peer encrypted message exchanges (see [Tessera](https://github.com/consensys/tessera)) for directed transfer of private data to network participants
* [__Alternative Consensus Mechanisms__](https://consensys.net/docs/goquorum//en/latest/concepts/consensus/overview/) - with no need for POW/POS in a permissioned network, GoQuorum instead offers multiple consensus mechanisms that are more appropriate for consortium chains:
    * [__QBFT__](https://consensys.net/docs/goquorum/en/latest/configure-and-manage/configure/consensus-protocols/qbft/) - Improved version of IBFT that is interoperable with Hyperledger Besu
    * [__Istanbul BFT__](https://consensys.net/docs/goquorum/en/latest/configure-and-manage/configure/consensus-protocols/ibft/) - a PBFT-inspired consensus algorithm with transaction finality, by AMIS.
    * [__Clique POA Consensus__](https://github.com/ethereum/EIPs/issues/225) - a default POA consensus algorithm bundled with Go Ethereum.
    * [__Raft-based Consensus__](https://consensys.net/docs/goquorum/en/latest/configure-and-manage/configure/consensus-protocols/raft/) - a consensus model for faster blocktimes, transaction finality, and on-demand block creation
* [__Peer Permissioning__](https://consensys.net/docs/goquorum/en/latest/concepts/permissions-overview/) - node/peer permissioning, ensuring only known parties can join the network
* [__Account Management__](https://consensys.net/docs/goquorum/en/latest/concepts/account-management/) - GoQuorum introduced account plugins, which allows GoQuorum or clef to be extended with alternative methods of managing accounts including external vaults.
* [__Pluggable Architecture__](https://consensys.net/docs/goquorum/en/latest/concepts/plugins/) -  allows adding additional features as plugins to the core `geth`, providing extensibility, flexibility, and distinct isolation of GoQuorum features.
* __Higher Performance__ - GoQuorum offers significantly higher performance throughput than public geth

Metachain-quorum keep the same architecture with GoQuorum:

### Architecture

![metachain-quorum](https://github.com/peopledata/metachain-quorum/blob/1893c9a004c00c2838ccda9981a1dbcaa88a5ccc/metachain-quorum%E6%9E%B6%E6%9E%84%E7%A4%BA%E6%84%8F%E5%9B%BE.png)

The above diagram is very high-level overview of component architecture used by GoQuorum. For more in-depth discussion of the components and how they interact, please refer to [lifecycle of a private transaction](https://consensys.net/docs/goquorum/en/latest/concepts/privacy/private-transaction-lifecycle/).

### Key Enhancements over GoQuorum
[todo]


## Quickstart 
The easiest way to get started is to use * [metachain-quickstart](https://www.peopledata.org.cn/metachain-quickstart) - a command line tool that allows users to set up a development Metachain-quorum network on their local machine in *few minutes*.

## Official Docker Containers
The official docker containers can be found under https://hub.docker.com/atomsbeijing

## Third Party Tools/Libraries
[todo]

## Contributing
Metachain-quorum is built on open source and we invite you to contribute enhancements. Upon review you will be required to complete a Contributor License Agreement (CLA) before we are able to merge. If you have any questions about the contribution process, please feel free to send an email to info@peopledata.org.cn](mailto:info@peopledata.org.cn). Please see the [Contributors guide](.github/CONTRIBUTING.md) for more information about the process.

## Reporting Security Bugs
Security is part of our commitment to our users. At GoQuorum we have a close relationship with the security community, we understand the realm, and encourage security researchers to become part of our mission of building secure reliable software. This section explains how to submit security bugs, and what to expect in return.

If you have not received a reply to your email or you have not heard from the security team please contact any team member through GoQuorum slack security channel. **Please note that GoQuorum discord channels are public discussion forum**. When escalating to this medium, please do not disclose the details of the issue. Simply state that you're trying to reach a member of the security team.

#### Responsible Disclosure Process
Metachain-quorum project uses the following responsible disclosure process:

- Once the security report is received it is assigned a primary handler. This person coordinates the fix and release process.
- The issue is confirmed and a list of affected software is determined.
- Code is audited to find any potential similar problems.
- If it is determined, in consultation with the submitter, that a CVE-ID is required, the primary handler will trigger the process.
- Fixes are applied to the public repository and a new release is issued.
- On the date that the fixes are applied, announcements are sent to Quorum-announce.
- At this point you would be able to disclose publicly your finding.

**Note:** This process can take some time. Every effort will be made to handle the security bug in as timely a manner as possible, however it's important that we follow the process described above to ensure that disclosures are handled consistently.

#### Receiving Security Updates
The best way to receive security announcements is to subscribe to the metachain-announce mailing list/channel. Any messages pertaining to a security issue will be prefixed with **[security]**.

## License

The go-ethereum library (i.e. all code outside of the `cmd` directory) is licensed under the
[GNU Lesser General Public License v3.0](https://www.gnu.org/licenses/lgpl-3.0.en.html), also
included in our repository in the `COPYING.LESSER` file.

The go-ethereum binaries (i.e. all code inside of the `cmd` directory) is licensed under the
[GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html), also included
in our repository in the `COPYING` file.

Any project planning to use the `crypto/secp256k1` sub-module must use the specific [secp256k1 standalone library](https://github.com/ConsenSys/goquorum-crypto-secp256k1) licensed under 3-clause BSD.
