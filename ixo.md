# IXO  

## Rationale
IXO is a protocol which combines several blockchain technologies (including Ethereum) to track and measure the impact of 
sustainable projects. In particular, it provides a mechanism that, through data collecting, allows projects to prove the reaching 
of promised targets. As a side effect, it also enables the implementation of “smart” impact bonds, since, on the reaching of those 
targets, a smart contract can be configured to transfer money.

The platform supports several types of social data and impact projects; however, they must belong to the [ 16 Sustainable Development 
Goals](https://www.un.org/sustainabledevelopment/sustainable-development-goals/)  agreed on by the United Nations General Assembly in
2015. These goals aim at, ending poverty and hunger, improving health and education, making cities more sustainable, combating climate
change, and protecting oceans and forests. Each goal has specific targets to be achieved by 2030.

## Use cases
The protocol follows several steps, orchestrated through different parties. First, an organization creates an “impact claim”, i.e. a 
target to be fulfilled (i.e., improving health for children under three years, providing attendance to schools). That claim is usually
fulfilled through a service (i.e., administering vaccinations, teaching lessons): every time the service is provided, some data is 
collected (i.e., the barcode of the vaccination, the fingerprint of the child attending class). Over time, claims are evaluated to know
whether they have been satisfied. The assessment of claims can be monitored by all the involved parties. 

Several claims can be gathered together in a project, and managed through an “impact contract”, i.e. a smart contract running on
Ethereum. Once sufficient claims have been processed successfully, the contract completes automatically. Using the smart contract, 
it is possible to trigger actions to pay out the participant in a project on the fulfillment of claims. Payments are distributed as 
IXO tokens. 

So far, the  projects  [Amply](amply.md) and  [Educate Girls](educategirls.md) have been implemented over IXO protocol. 

## Architecture
The IXO protocol combines different blockchain technologies. The IXO network is a permissioned Cosmos blockchain, which features a
Byzantine fault tolerance consensus protocol. The nodes have the purpose of validating the data coming from users, and reaching 
consensus. They also interact with smart contracts run on Ethereum (a public permissionless blockchain based on Proof-of-Work), 
since the achieving of claims can trigger calls to smart contract.

For privacy concerns, part of the data are stored off-chain from the IXO network or any other public blockchain. Instead, the proofs 
of the data submissions are stored on the IXO public ledger (called “Global Impact Ledger”), together with some metadata that are 
needed for tracking the performance of projects. Anyone can access the Global Impact Ledger (GIL) through the IXO Portal. Impact data
remains under the full private control and ownership of the project creator, who decides what is stored (in a large off-chain database),
what is public, and who can read/write the data. To gain access to the data, one must ask the owner. A proprietary application 
(called “Social Suite”) is used to insert data, configure claims, and track them.

## Discussion
The IXO project is the soundest among the ones we have investigated. In particular, it is the only one which solves the problem of
assessing targets. The achievement of targets is a crucial point, both to measure the impact of a project and to trigger payout for
investors, in case of bonds. IXO deals with several aspects and actors, from collecting data to verifying claims. To manage all these
aspects, IXO mixes different blockchains. This mix allows to handle separately private, public and off-chain data, satisfying both
privacy and transparency requirements. We remark that, while Ethereum is a well-known technology, Cosmos is an emerging one. According 
to the documentation, IXO adopts machine-learning and predictive analytics for deciding whether a claim is true. Anyhow, not all claims
can be automatically verified, so trusted authorities are still needed.

The source code of the project is public. However, the code and details linked to the Amply and DIB projects were not made available 
online, hence, there was no smart contract to investigate.

## Online Resources
* IXO network http://ixo.network 
* IXO short presentation https://vimeo.com/243097715 
* IXO technical pages https://ixofoundation.github.io/mkdocs/  
* IXO whitepaper http://ixo.foundation/wp-content/uploads/2017/12/The-ixo-Protocol-Draft-White-Paper-3.0-for-technical-review-12_8_2017.pdf 
* IXO blog https://medium.com/ixo-blog  
* How the ixo protocol works https://medium.com/ixo-blog/introduction-to-the-ixo-protocol-55f98e34de01 
* How the IXO network works https://medium.com/ixo-blog/using-dapp-tools-dsgroup-to-control-consensus-of-calls-on-ethereum-d423dc6ef1f 
* Source code for the IXO protocol https://github.com/ixofoundation
* IXO presentation https://www.fastcompany.com/40513028/this-new-blockchain-protocol-wants-to-create-accountability-for-social-impact
* IXO promotional video https://www.facebook.com/ixofoundation/videos/318871981976567/
*  Smart Impact Bonds https://medium.com/ixo-blog/smart-impact-bonds-420324ac720f
* SocialSuite and SIB https://finfeed.com/features/blockchain-measuring-social-impact-socialsuite-first-mover/
* SocialSuite https://socialsuitehq.com/
* Cosmos website https://cosmos.network/
* Tendermint website https://tendermint.com/

