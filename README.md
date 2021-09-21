# FreaksCatalog-Blockchain

To run this project you need to install [Openzeppelin contracts]

    npm install @openzeppelin/contracts

 Create an ERC1155 FreakTeam-contract and ProfitSharing-contract with following functions:
 
  add, delete and modifity a freak ```these functions can only be called by hr```;
  
    Each freak should have the following attributes:
     name (string)
     start date and end date (uint)
     employeeNumber (uint)      ```Risk: [it iscalculated according to the employee number, for example if the freak was hired between 1-50 the risk is 100, otherwise it is 75]```
     role (enum Role)           ```Role: [IT, Support]```
     skill level (enum Skill)   ```Skill:[Novice, Advanced, Competent, Proficient, Expert, Master]```
     norm ( enum Norm)          ```Norm: [Part time, Full time]```
     score (uint)      ```The score represents the arithmetic mean between: [role, skill, norm, risk]```
 
 displaying all freaks ```[this function can be called by any freak]```;
 
 allocate profit for each freak  ```[this function can only be called by financial]```:
 
    Before this, Financial should 'approve' this contract to spend the USDC for Profit Sharing
    Contract should interact with USDC and transfer the amount from Financial wallet to this contract.
    Interact with the Freaks smart contract and calculate the share for each freak that participated to the profit in the specified period of time (take into account freak's startDate endDate).
    Approve each freak to withdraw the allocated amount from the Profit Sharing smart contract.
    Take into consideration that freaks might have unspent allocations. These should be added to the current allocation.
 
 withdrow profit ```[this function can only be called by a freak]```
   
    Should use the freaks' allowed profit sharing bonus from the Safe and send it to the withdrawal address.
    Extra parameters:
    Amount - specify how much from the allowed amount you want to withdraw
    WithdrawalAddress - if not set, should be sent to the freaks' wallet adddress. If set, amount should be sent to the specified address.
 
