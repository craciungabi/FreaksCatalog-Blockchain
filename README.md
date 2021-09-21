# FreaksCatalog-Blockchain

To run this project you need to install [Openzeppelin contracts] [npm install @openzeppelin/contracts]

 Create an ERC1155 FreakTeam-contract and ProfitSharing-contract with following functions:
 
  -add, delete and modifity a freak [these functions can only be called by hr];
  
    Each freak should have the following attributes:
     name (string)
     start date and end date (uint)
     employeeNumber (uint)      Risk: [it iscalculated according to the employee number, for example if the freak was hired between 1-50 the risk is 100, otherwise it is 75]
     role (enum Role)           Role: [IT, Support]
     skill level (enum Skill)   Skill:[Novice, Advanced, Competent, Proficient, Expert, Master]
     norm ( enum Norm)          Norm: [Part time, Full time]
     score (uint)      The score represents the arithmetic mean between: [role, skill, norm, risk]
 
 - displaying all freaks [ this function can be called by any freak];
 - 
 - 
 
