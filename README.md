## Ali_Khatami_Solidity
We have created a file ```akrkSimpleStorage.sol``` where ```.sol``` means that it is a solidity file. Solidity is the priamary coding language of smart contract.<br>
Solidity is constantly changing and updating language.<br>
Today I have have done some basic part of solidity
```
//SPDX-License-Identifier: MIT
//at the top of our code we use licensing to make our code sharing and licensing easier and MIT which is the least restrictive license
pragma solidity ^0.8.7;
//we have to tell our code which version of solidity we need to use 
//we can add version by doing pragma,solidity and version we want to use.
//we have use here a caret to tell the code any version of 0.8.7 and above is okay for this contract.
//to define our contract we write contract that tells that next piece of our code will be contract
//contract can be think of like class in OOP and and anything within the curly bracket can be content of the contract
contract akrkSimplestorage {
  // basic data types: boolean, uint,int,address,bytes
  //uint(unsigned integer only positive),int both pos and neg
  //address is the address of the account
  //string are secretly byte objects only for text
  //bytes32 is a bytes objects whre 32 represent how many bytes we want them to be
  //byte objects look like 0xsdsysydggt
  //unint256 here 256 is bit (8,16,32 upto 256 we can use)
  bool hasPreferredNumber= true;
  uint256 preferredNumberU=689;
  int256 preferredNumberI=689;
  string preferredNumberS="Six hundred eighty nine";
  address akraddress= 0x3Fe3d73B20BAc5A43D8dACb674982011ec1Db200;
}
```
