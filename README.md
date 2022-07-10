
Weekend Project - 1
•	Form groups of 3 to 5 students
•	Structure scripts to
o	Deploy
o	Query proposals
o	Give vote right passing an address as input
o	Cast a vote to a ballot passing contract address and proposal as input and using the wallet in environment
o	Delegate my vote passing user address as input and using the wallet in environment
o	Query voting result and print to console


•	Publish the project in Github
•	Run the scripts with a set of proposals, cast and delegate votes and inspect results
•	Write a report detailing the addresses, transaction hashes, description of the operation script being executed and console output from script execution for each step (Deployment, giving voting rights, casting/delegating and querying results).
•	(Extra) Use TDD methodology


Scripts
•	1_deploy.ts
•	2_quey_proposals.ts
•	3_give_vote_rights.ts
•	4_cast_vote.ts
•	5_delegate_vote.ts
•	6_query_voting_results.ts
How to use
Deploy
script: 1_deploy.ts {list_of_proposals}
yarn ts-node --files scripts\Ballot\1_deploy.ts Proposal_1 Proposal_2


 

Contract deployed at 0xEa23cfe91Ff470096238bC68939f380dC9e6b62F
Query Proposals
script: 2_quey_proposals.ts {address_contract_ballot} {index_proposal}
yarn ts-node --files scripts\Ballot\2_quey_proposals.ts 0x15a5076D0e42eb7F3C2a6d0f510cb5ff41897c9a 1 ts-node --files scripts\Ballot\2_quey_proposals.ts 0xEa23cfe91Ff470096238bC68939f380dC9e6b62F 1

 

Attaching ballot contract interface to address 0xEa23cfe91Ff470096238bC68939f380dC9e6b62F
Give vote right passing an address as input
script: 3_give_vote_rights.ts {address_contract_ballot} {address_to_give_rights}
ts-node --files scripts\Ballot\3_give_vote_rights.ts  0xEa23cfe91Ff470096238bC68939f380dC9e6b62F 0xe328a3D1bC7C20AA851Bc85897262bD37364a7D4
 

Transaction completed. Hash: 0x02d70bc03f1066d15074dad8a118416fec71a132d4b0430135231fc7eb409402
Cast a vote to a ballot passing contract address and proposal as input and using the wallet in environment
script: 4_cast_vote.ts {address_contract_ballot} {index_proposal}
ts-node --files scripts\Ballot\4_cast_vote.ts 0xEa23cfe91Ff470096238bC68939f380dC9e6b62F 0




 
Transaction completed. Hash: 0x26ebe8d5ad504ce4c16667691238fd1eec814c5393fc88390e084d2662f50675
Delegate my vote passing user address as input and using the wallet in environment
script: 5_delegate_vote.ts {address_contract_ballot} {address_to_delegate}
ts-node --files scripts\Ballot\5_delegate_vote.ts 0x56D21d44F1C4c1ae0a5FF5d589CC344292A1E9c2 0xdFB228Bc7e07ce5869e0339f4B67504fc79C573f


 

Transaction completed. Hash: 0x37b2409c53277d7b5d87c295825936e3a0bb3ff1f5efde81f47f24cb7c15061a

Query voting result and print to console
script: 6_query_voting_results.ts {address_contract_ballot}

yarn ts-node --files scripts\Ballot\6_query_voting_results.ts 0xEa23cfe91Ff470096238bC68939f380dC9e6b62F

 

Using address 0x56D21d44F1C4c1ae0a5FF5d589CC344292A1E9c2
Wallet balance 54.96122197337613
Attaching ballot contract interface to address 0xEa23cfe91Ff470096238bC68939f380dC9e6b62F
Winning proposal is: Proposal_1
Winning proposal votes: 1
Done in 7.58s.

