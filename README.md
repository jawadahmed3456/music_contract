# MusicContract 
## Overview

This is a simple Ethereum smart contract written in Solidity that represents a basic music sharing contract. The contract allows the owner to share ownership with another address, pause and resume music playback.

## Smart Contract Details

### Owner

The contract has an `owner` variable initialized with the address of the deployer (creator) of the contract. This `owner` address has special privileges and is the only entity allowed to share ownership.

### Pausing and Resuming

The contract features a `bool` variable called `isPaused` that determines the state of music playback. The owner can pause and resume music playback through the `pauseMusic` and `resumeMusic` functions, respectively.

- `pauseMusic`: This function is used to pause music playback. It uses the `assert` statement to ensure that music is not already paused.

- `resumeMusic`: This function is used to resume music playback. It utilizes the `revert` statement to handle the case where music is not currently paused.

### Sharing Ownership

The contract provides a function called `shareMusic` that allows the owner to share ownership with another address. The function checks the sender's address against the current owner's address using the `require` statement, ensuring that only the owner can initiate the ownership transfer.


To use this contract, deploy it to an Ethereum-compatible blockchain network. The contract can be interacted with through transactions, with the owner having the ability to share ownership and control the music playback state.

## Author

This contract was authored by Jawad Ahmed.
