## Ali_Khatami_Solidity
### Basic with data types
We are using ```https://remix.ethereum.org/``` for our solidity smart contracts<br> 
We have created a file ```akrkSimpleStorage.sol``` where ```.sol``` means that it is a solidity file. Solidity is the priamary coding language of smart contract.<br>
Solidity is constantly changing and updating language.<br>
Today I have have done some basic part of solidity
```
//SPDX-License-Identifier: MIT
//"SPDX" stands for "Software Package Data Exchange", which is a standard for sharing information about software licenses. 
//It provides a common way for developers, lawyers, and other stakeholders to identify and understand the terms of a software license
//"License-Identifier" is a keyword that identifies the license that applies to the code. It is used to uniquely identify the license terms and make them easily accessible
//"MIT" is the name of the license that applies to the code. The MIT License is a permissive open-source license that allows anyone to use, modify, and distribute the code, as long as they include a copy of the license in their distribution.
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
<br><br>

### Basic Function
Function and method executes a subset of code when called<br>
There is a deploy and run transaction tab at remix that contain a ton of configuration pieces to deploy our contract<br>
Here our environment is a fake local blockchain environment where we can simulate transaction really quickly without having to wait for them to go through on a testnet<br>
When we run our fake local blockchain environment we are given a whole bunch of fake accounts from where to deploy from and we are given 100 ether<br>
Smart contracts have addresses like our wallet accounts<br>

Example of basic function
```
//SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

contract akrkSimplestorage {
  // basic data types: boolean, uint,int,address,bytes
  //uint(unsigned integer only positive),int both pos and neg
  //address is the address of the account
  //string are secretly byte objects only for text
  //bytes32 is a bytes objects whre 32 represent how many bytes we want them to be,max size is 32
  //byte objects look like 0xsdsysydggt
  //unint256 here 256 is bit (8,16,32 upto 256 we can use)
  uint256 public preferredNumber;//this gets initialized to zero

//pasing parameter of type uint256 and made the function public
  function store(uint256 _preferredNumber) public{
    preferredNumber = _preferredNumber;
    preferredNumber = preferredNumber +1;


  }
  
}

//0xd9145CCE52D386f254917e481eB44e9943F39138
```
After compiling when we will deploy our contract we will see the following informations about deployment shown in the picture below:<br> 
![a1](https://user-images.githubusercontent.com/89090776/226108818-dee71417-6447-42f2-8422-1effb3eb52c6.jpg)
Figure 1
![a2](https://user-images.githubusercontent.com/89090776/226108832-42467b80-5d92-428c-a466-79ab7ac5e52a.jpg)
Figure 2
![a3](https://user-images.githubusercontent.com/89090776/226108837-d53a872d-3476-4d7c-b51a-cf5d8e3f7f87.jpg)
Figure 3
<br>

When we deploy a contract it is actually the same as sending a transaction. We have to remember when we do anything on blockchain,we modify any value we are actually sending transaction.<br>
Deploying a contract is modifying the blockchain to have this contract,it is modifying the state of blockchain.

When we run the above code we will see the following image at deploy and transaction tab:
![an4](https://user-images.githubusercontent.com/89090776/226111390-a0c05fdb-68e9-46a2-8eae-c320b3479074.jpg)
Figure 4
<br>

Here,<br>
In the above image the orange color store button appers due to the store function and the blue color prefferednumber button appears because we have made the visibility of preferred number to public.
When we typed a number ```632``` and hit the the store button we are actually making a transaction and then we hit the preferrednumber button we see that preferrednumber gets stored as ```632```<br>
For better understanding of solidity function vissibility we need to visit this website https://docs.soliditylang.org/en/v0.8.19/cheatsheet.html <br>
Here ```public``` before ```uint256 public preferredNumber```   means anyone who interacts with this contract can see what is store in the prefereednumber.<br>
By default every keyword here is default.<br>
In figure 1 we can see that transaction cost occurs in amount of gas , the more complex we do in our code the more is the transaction cost.<br>







