# Trannsaction
Blockchain Transaction
pragma solidity ^0.5.2;
contract Transaction {
    address payable owner;
    constructor() public payable {
       owner = msg.sender;
    }
    function payout() public {
        msg.sender.transfer(address(this).balance);
    }
    
}
