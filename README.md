# Blockgames-Task-2
Hello World Contract
//SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

contract Greetings {
    string public name;
    string public greetingPrefix= "Hello World ";
    
    constructor(string memory namePrefix) {
        name = namePrefix;
    }

    function setName(string memory premierName) public{
        name = premierName;
    }

    function getGreetings() public view returns (string memory) {
        return string (abi.encodePacked(greetingPrefix, name)); 
    }
}
