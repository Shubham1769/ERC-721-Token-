# ERC-721-Token-
Introduction: 
The ERC-721 (Ethereum Request for Comments 721), proposed by William Entriken, Dieter Shirley, Jacob Evans, Nastassia Sachs in January 2018, is a Non-Fungible Token Standard that implements an API for tokens within Smart Contracts.  
It provides functionalities like to transfer tokens from one account to another, to get the current token balance of an account, to get the owner of a specific token and also the total supply of the token available on the network. Besides these it also has some other functionalities like to approve that an amount of token from an account can be moved by a third party account.
 If a Smart Contract implements the following methods and events it can be called an ERC-721 Non-Fungible Token Contract and, once deployed, it will be responsible to keep track of the created tokens on Ethereum.

detailed explanation of each function in the code:

The code starts with SPDX-License-Identifier and pragma statement to define the Solidity version and license information. Then, the contract ERC721 is defined.

name and symbol are public string variables representing the name and symbol of the ERC721 token.

nextTokenIdToMint is a public uint256 variable representing the ID of the next token to be minted.

contractOwner is a public address variable representing the owner of the contract.

The next section defines several internal mappings used for token ownership, token approvals, operator approvals, and token URIs.

Transfer, Approval, and ApprovalForAll events are defined to emit when certain actions occur in the contract.

The constructor function initializes the name, symbol, nextTokenIdToMint, and contractOwner variables with the provided values.

The balanceOf function takes an address _owner as input and returns the number of tokens owned by that address. It checks if the address is not the zero address before returning the balance.

The ownerOf function takes a token ID _tokenId as input and returns the address of the token owner by retrieving the value from the _owners mapping.

​​The safeTransferFrom function allows the safe transfer of a token from one address _from to another address _to. It delegates the transfer to the overloaded safeTransferFrom function with an empty data parameter.


Deployed Contract Link for easy access for checking:
https://thirdweb.com/contracts/deploy/QmaGMq4FSNgZwUJLCEkK5F59eJAnpKRsE4ccbzQypNHryr
