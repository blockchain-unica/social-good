
# SmartSib
## Rationale
[Pan-Impact Korea](https://avpn.asia/organisation/pan-impact-korea/) is a Korean society founded in 2015 to realize social 
value by impact investments. In particular, one of their projects aims at providing child welfare services over three years 
for a total of 10 billion won (~USD $9 M). According to the online documentation, these services will work with children and 
young people in group homes to improve their social outcomes and build capacity for long-term independence and wellbeing. 
The project was commissioned by the Seoul Metropolitan Government, and was funded by 3 societies (People & Peace Link - 
[Merry Year Social Company](https://avpn.asia/organisation/mysc-merry-year-social-compan) - UBS Securities Seoul Branch). 

To pay back investors, Pan-Impact Korea uses social impact bonds linked to a smart contract. These bonds specify fulfilment 
conditions which determine the interest rates. According the online documentation, a trusted third party (Sungkyunkwan  
University  Research  &  Business  Foundation)  is delegated to check that these conditions are satisfied. The publicly 
available material only specifies the minimum and maximum requirements (e.g. the minimum is that at least 40% of the children
reach a given learning target), but the way this condition is assessed is not specified. On February 7th 2018, Pan-Impact Korea 
issued 1,110,000 transferable token units, and according to investors’ shares of the first SIB in Korea, Merry Year Social Company
together with UBS Securities received 110,000 units. Reportedly, People & Peace Link was to  receive 1,000,000 units in the 
subsequent month.
Use cases
The online documentation does not detail the behaviour of the token (e.g. its issuance and trading). It is not possible to infer 
this behaviour from the smart contract associated with the token, since the source code of this smart contract is not publicly
available. 

## Architecture
Smart SIB has been implemented as an ERC20-compliant token on Ethereum. The Ethereum blockchain is public, i.e. every 
transaction on it can be observed. Tokens can be created through the deployment of a smart contract. The assembly (EVM) code 
of such a contract is always publicly readable, while the high-level code can be omitted. For the Smart SIB token, this 
high-level code is missing, so we cannot determine the token behaviour. 

The ERC20 standard only asks the smart contract to assess the ownership of the tokens, and to allow owners to transfer that 
ownership. However, according to the online documentation, the feeling is that the Smart SIB contract is far more complex,
as it should not only assess ownership, but also distribute the interests back to investors, in proportion on the token units
owned. 

The Smart SIB token can be inquired in blockchain explorers. Its full name is “[Pan-Impact Korea] Smart SIB (No.1)”, and the 
other details can be found at the following links:
* [Token transfert](https://etherscan.io/token/0xd9b242f0a54cf627418ac7918a2aeb42579d7f20)
* [Top 100 token holders](https://etherscan.io/token/tokenholderchart/0xd9b242f0a54cf627418ac7918a2aeb42579d7f20)

As we can see, the total supply amounts to 1,110,000 units, owned by just 2 stakeholders: one of them is the initial owner, 
who still controls the 90% of the total supply. The smart contract associated to the token has been created on February 5th, 
2018. From what we can see from the explorer, the token units has never been transferred again after a first initial division. 
The two stakeholders addresses do not seem to have any other tokens.

## Discussion
The declared goal of the project was to divide bonds among three original investors, who could then trade them, and redeem 
the interests. However, upon a closer investigation, the total supply of 1,110,000 token units belongs to the contract creator 
(Pan-Impact Korea) and to one of the three stakeholders. Only 5 transactions have occurred in total. 
Besides the online documents referring to the starting of the project, we have not been able to find any other document which 
attests how the project is proceeding. According to the blockchain explorer, only a single transfer was made after the tokens 
were issued. This conflicts with the declared goal of dividing the token units among the three initial funders. Our conjecture 
is that some technical problems prevented the subsequent ownership transfers. The most common reason for this is the presence of
a bug that makes the whole contract stuck. Indeed, since the code deployed on Ethereum cannot be changed, bugs cannot be fixed. 
This (mis)feature has caused huge money losses in the past: for instance, the DAO was a contract implementing a crowdfunding
platform, which raised ∼$150M before being attacked on June 18th, 2016; an attacker managed to put ∼$60M under her control, 
until the hard-fork of the blockchain nullified the effects of the transactions involved in the attack [14]. Unfortunately, 
being the smart contract code not public, we cannot know if it contain security vulnerabilities. 

## Online resources
* Roadmap of the project: https://avpn.asia/wp-content/uploads/2016/07/Pan-Impact-Korea-Leaflet.pdf
* Press release: http://panimpact.kr/first_smart_sib/
* Sibs: https://avpn.asia/blog/the-first-smart-social-impact-bond-innovative-synergies-blockchain-and-sibs/
* Detail on bureaucratic problems on Korean government: https://emmatomkinson.com/2014/08/15/seoul-social-impact-bond-sib/
