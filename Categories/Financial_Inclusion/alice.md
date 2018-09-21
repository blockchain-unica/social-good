# Alice 

[Alice](http://alice.si/) is a platform to fund philantropy projects which aims at making donation flow transparent, and at 
assessing project results.

The platform manages two kind of funding protocols: donations and impact investments.
The funds allocated for a project  are given to it incrementally, only after the project has reached the its goals. To assess 
the reaching of goals, the platform designates entities to validate the job done.  In the absence of results, remaining money is 
returned to the project’s funders.
Alice allows projects to combine different types of funding, so that, for example, donations can be used to pay back investors,
as and when goals are achieved. In this way, social organisations to tap into both philanthropic money and impact investment.

The platform asks for some fees, which are paid in its own token (Alice). Part of these, are reinvested back
in the platform in the form of grants to help social organisations. 
These grants are managed collectively by Alice token holders via a decentralised autonomous fund (DAF).


## Tecnical details
Alice is based on the Ethereum blockchain. The blockchain is used to record almost every parameter of projects run on the network,
so that they are immutable and public. Other information are stored offchain and encrypted. In particular, in case of sensitive data, 
their access is regulated by authorizations.

Alice uses [smart contracts](https://github.com/alice-si/contracts), to automate payment flows between all stakeholders participating 
in the network. When a social organisation achieves one of its project goals, for example, it will automatically receive payment from 
the pot of escrowed donations made to the project. If any impact investors funded the project, part of these donations are 
automatically siphoned off to make their interest payments, and if these investments are managed by an intermediary fund,
then it automatically  receives it  management fee from the  interest payments.

### Alice tokens
Interacting with the Alice platform requires the use of different tokens.
* Donation tokens represents donations made to projects  within the project's donation contract. They are used to 
manage conditional payments and cannot be transferred outside the project's contract.
* Coupon tokens give the bearer the right to a specific bond's interest paymet and the reimbursement of its principal. 
They can be transferred between impact investor.  
* Data tokens represents impact facts and serve to provide information about a give project.
* Alice tokens are used to pay the interactions within the system. For instance, the following actions come to a cost: accessing 
a project's impact data; launching a fundraising project; registering a validator. 
Under some circumstances, some actions are free of charge, such accessing to impact data from funder and beneficiary or making a donation (differently from funding a project, which is subjected to a fee).
