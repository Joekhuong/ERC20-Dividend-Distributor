# ERC20-Dividend-Distributor
ERC20 Dividend Distributor
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Dividend {
    mapping(address => uint256) public shares;

    function deposit() public payable {}

    function distribute(address user) public {
        payable(user).transfer(address(this).balance);
    }
}
