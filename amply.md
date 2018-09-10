
# IXO Foundation for Amply and Educated Girls projects 



## Rationale
IXO is a protocol which combines several blockchain technologies (including Ethereum) to track and measure the impact of sustainable projects. In particular, it provides a mechanism that, through data collecting, allows projects to prove the reaching of promised targets. As a side effect, it also enables the implementation of “smart” impact bonds, since, on the reaching of those targets, a smart contract can be configured to transfer money.

The platform supports several types of social data and impact projects; however, they must belong to the [ 16 Sustainable Development Goals](https://www.un.org/sustainabledevelopment/sustainable-development-goals/)  agreed on by the United Nations General Assembly in 2015. These goals aim at, ending poverty and hunger, improving health and education, making cities more sustainable, combating climate change, and protecting oceans and forests. Each goal has specific targets to be achieved by 2030.

## Use cases
The protocol follows several steps, orchestrated through different parties. First, an organization creates an “impact claim”, i.e. a target to be fulfilled (i.e., improving health for children under three years, providing attendance to schools). That claim is usually fulfilled through a service (i.e., administering vaccinations, teaching lessons): every time the service is provided, some data is collected (i.e., the barcode of the vaccination, the fingerprint of the child attending class). Over time, claims are evaluated to know whether they have been satisfied. The assessment of claims can be monitored by all the involved parties. 

Several claims can be gathered together in a project, and managed through an “impact contract”, i.e. a smart contract running on Ethereum. Once sufficient claims have been processed successfully, the contract completes automatically. Using the smart contract, it is possible to trigger actions to pay out the participant in a project on the fulfillment of claims. Payments are distributed as IXO tokens. 

So far, the following projects have been implemented over IXO protocol: 
* The [Amply](http://amply.tech/) project (of 2016), supported by UNICEF and Innovation Edge, consists of a  mobile app that uses the IXO protocol to track attendance in pre-schools in South Africa. There, many parents cannot afford to send their children to preschool. To rectify this, the South African government has a subsidy programme to support over 800,000 children. To access these subsidies, teachers must track attendance through a paper-based system, which is slow to be checked. Through the Amply project, a mobile application built upon the IXO protocol enables teachers to track attendance. With each positive attendance record, an impact claim is made, allowing access to government subsidies. The program serves about 700,000 kids aged two to five across thousands of small centers around the country; the project has saved about  than 4,000 hours every month.

* The [Educate Girls Development Impact Bonds (DIB)](https://www.educategirls.ngo/) project of 2015, is funding a three-year education program implemented by Indian NGO Educate Girls in a remote rural district of Rajasthan. The project measures progress against agreed targets (attendance and learning results) for the number of out-of-school girls enrolled into primary education and the progress of girls and boys in English, Hindi and mathematics. The mechanism of the DIB works like this:   a socially-motivated investor – in this case the UBS Optimus Foundation (UBSOF) - puts in the working capital so the service provider – Educate Girls - can carry out its work on the ground. An outcome payer, in this case the [Children’s Investment Fund Foundation](https://ciff.org/), promises to pay back the investor (UBSOF) the original amount plus extra returns as long as agreed enrolment, literacy and numeracy targets are met. The targets are assessed regularly by an independent evaluator over the course of the program. Actually, the program has reached the second (out of three)  year, and results are considered good. 
Reportedly,  Phyllis Costanza, CEO of the [UBS Optimus Foundation](https://www.ubs.com/microsites/optimus-foundation/en/home.html)  said: “Progress has been strong, particularly against enrolment targets, and, just as important, the DIB is demonstrating its potential to attract much need funding as donors are increasingly seeing that they can achieve real social impact and results-based financial returns. And we at the UBS Optimus Foundation are working on the next generation of DIBs, which will be announced later this year.” ( from https://www.ubs.com/microsites/optimus-foundation/en/stories/development-impact-bond-in-education.html )
Also: “The Educate Girls Development Impact Bond (DIB) is a pioneering new way to encourage private investors to fund international development projects that is 100% focused on the outcomes achieved. It aims to help improve education for 18,000 children in Rajasthan, India. But more than this, this first-ever development impact bond aims to create a ‘proof of concept’, showing potential donors and investors how DIBs could contribute to societal gains while also offering financial returns”. (from http://instiglio.org/educategirlsdib/ )
At the end of the DIB program, if all the  targets are met, the initial investment will be paid back to UBS Optimus Foundation by the outcome payer, with interests up to 15 per cent, depending on how far the children’s learning targets are reached. Educate Girls will also receive part of this payment if it achieves its targets.

Further info: 
* http://instiglio.org/educategirlsdib/educate-girls-development-impact-bond-delivers-robust-second-year-results-valuable-lessons/ 
* https://www.ubs.com/microsites/optimus-foundation/en/home.html
* http://instiglio.org/educategirlsdib/  

## Architecture
The IXO protocol combines different blockchain technologies. The IXO network is a permissioned Cosmos blockchain, which features a Byzantine fault tolerance consensus protocol. The nodes have the purpose of validating the data coming from users, and reaching consensus. They also interact with smart contracts run on Ethereum (a public permissionless blockchain based on Proof-of-Work), since the achieving of claims can trigger calls to smart contract.

For privacy concerns, part of the data are stored off-chain from the IXO network or any other public blockchain. Instead, the proofs of the data submissions are stored on the IXO public ledger (called “Global Impact Ledger”), together with some metadata that are needed for tracking the performance of projects. Anyone can access the Global Impact Ledger (GIL) through the IXO Portal. Impact data remains under the full private control and ownership of the project creator, who decides what is stored (in a large off-chain database), what is public, and who can read/write the data. To gain access to the data, one must ask the owner. A proprietary application (called “Social Suite”) is used to insert data, configure claims, and track them.

## Discussion
The IXO project is the soundest among the ones we have investigated. In particular, it is the only one which solves the problem of assessing targets. The achievement of targets is a crucial point, both to measure the impact of a project and to trigger payout for investors, in case of bonds. IXO deals with several aspects and actors, from collecting data to verifying claims. To manage all these aspects, IXO mixes different blockchains. This mix allows to handle separately private, public and off-chain data, satisfying both privacy and transparency requirements. We remark that, while Ethereum is a well-known technology, Cosmos is an emerging one. According to the documentation, IXO adopts machine-learning and predictive analytics for deciding whether a claim is true. Anyhow, not all claims can be automatically verified, so trusted authorities are still needed.

The source code of the project is public. However, the code and details linked to the Amply and DIB projects were not made available online, hence, there was no smart contract to investigate.

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
*  Amply in press: https://bitcoinmagazine.com/articles/ixo-foundation-blockchain-based-response-un-call-data-revolution/ 
*  Amply Project repository: https://github.com/TrustlabTech
* Amply project discussed: https://medium.com/@Paul.Haas/blockchain-for-social-good-revolutionizing-pre-school-funding-in-south-africa-f0c7c63ee2ee 

