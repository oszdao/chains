# 🔍 Pre-Merge Checklist for Chain PRs

Before merging a chain PR, please verify the following:

- [ ] **Explorer Compliance**  
  - If the PR includes explorers, ensure they adhere to [EIP-3091](https://eips.ethereum.org/EIPS/eip-3091).  
  - Double-check that the explorer URLs actually follow the specification.

- [ ] **Icon Verification**  
  - For any new icons in the PR:  
    - Run `ipfs get` on all icon CIDs.  
    - Confirm that the size of the downloaded icons matches the size specified in the PR.

- [ ] **Chain Removal Rules**  
  - PRs cannot remove chains.  
  - Chains can only be deprecated, to protect users from potential replay attacks.

- [ ] **Chain ID Assignment**  
  - Ensure the PR does not assign an existing chainID to a new chain.  
  - Example to avoid: [PR #1750](https://github.com/ethereum-lists/chains/pull/1750)

- [ ] **Automation Ideas**  
  - If you have ideas on automating these checks in CI, PRs are welcome!  
  - Automated validation could include: EIP-3091 URL checks, IPFS icon validation, chain removal/deprecation checks, chainID conflicts.
