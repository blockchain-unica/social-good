# ImpakCoin 

[ImpakCoin](https://mpk.impak.eco/en/) is platform that aims at offering investment opportunities, in fields/projects dedicated to impact economy.

The platform implements a tokenized economy, through a custom coin (MPK). In the platform, it will be possible:  
* to buy products and services from accredited companies;
* to do Peer to Peer (P2P) payments;
* to make profit by microlending, crowdlending, and P2P lending relationships.

The platform rewards users in MPK for some actions, such as:
* downloading the impak mobile app;
* inviting other users;
* buying products or services from an impact business.

# Technical details
The platform lays on the blockchain WAVES, which uses a PoS-consensus algorithm.
However, the blockchain is only used as a ledger to record transactions, since the coin is issued by the platform itself.
The platform decides the value for the coin, and acts as the only exchange for it. 

Users registered on the platform are subject to limited anonymity (i.e., the platform knows the identity of each user).
The platform provides each user with a pair of public-private keys, in order to let them perform transactions.
The private keys are not to be sent to the users, but instead are stored within the platform.

Some measures are possible in case of attacks to the platform.
* In case of unauthorized transactions, the amount of the transaction is directed towards a dummy account, so that the money is considered burned. After that, new coins are minted and sent to the original sender.
* In case of stealing of private keys (that are stored in clear on a central database), the platform will create a new pair of keys for each user. The new keys are then used to recreate all the history of past transactions until the point the platform was compromised.

Given the centrality of the platform in managing private keys, assessing coin ownership and performing recovering for unauthorized transactions, it seems that the current project requires strong assumption of trust towards the platform itself. With these premises, the use of a blockchain is debatable.

### Online resources
* https://mpk-ico-prod.s3.amazonaws.com/static/files/MPK_Whitepaper_en.c8bf79a6e15e.pdf
* https://www.impak.eco/en/europe/
