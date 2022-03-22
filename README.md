# sudo remixd -s /home/(your VM name)/ -u https://remix.ethereum.org/
##TEST

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.4;
import
"../node_modules/@openzeppelin/contracts/token/ERC721/presets/ERC721PresetMint
erPauserAutoId.sol";
contract comp3320 is ERC721PresetMinterPauserAutoId {

 constructor()
 ERC721PresetMinterPauserAutoId("<describe yourself here>", "<your name>",
"https://ipfs.io/ipfs/<your ipfs folder address>/")
 {}

 // This allows the minter to update the tokenURI after it's been minted.
 // To disable this, delete this function.
 function setTokenURI(uint256 tokenId, string memory tokenURI) public {
 require(hasRole(MINTER_ROLE, _msgSender()), "web3 CLI: must have
minter role to update tokenURI");

 setTokenURI(tokenId, tokenURI);
 }
}
