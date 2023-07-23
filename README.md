## Ehtereum Proof Beginner
This project is based on the ethereum basics. 
## Descriotion
I have created this project on the platform (remix.ethereum.org) by using solidity. In this project I have created a my very own token. 
## Getting Started
### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol).
Copy and paste the following code into the file:

     // SPDX-License-Identifier: MIT
     pragma solidity 0.8.18;
    contract MyToken {
  
      // public variables here
      string public tokenName ="Data";
      string public tokenAbbrv ="Dt";
      uint public totalSupply = 0;
  
      // mapping variable here
      mapping (address=> uint) public balances;
  
  
      // mint function
      function mint (address _address, uint _value) public{
          totalSupply += _value;
          balances[_address] += _value;
      }
  
      // burn function
       function burn (address _address, uint _value) public{
           if (balances[_address] >= _value){
          totalSupply += _value;
          balances[_address] += _value;
           }
      }
     }

### How to run the program
* On the remix.ethereum.org, first go to the solidity image
* Here, click on the compile[YOUR_FILENAME]
* Then in the deploy function, click on deploy.
* Then copy the address from the address given in the address section.
* Paste that address to mint,burn, and balance sections.
* Now by entering token amount you can call your functions.

## Authors
Kajal Raj Chauhan
kajalrajchauhan

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
