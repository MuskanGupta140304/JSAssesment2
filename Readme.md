
# ErrorHandlerContract

## Description

This project is a Solidity smart contract designed to handle errors related to insufficient balances. The contract, `ErrorHandlerContract`, includes a custom error `InsufficientBalanceError` that is triggered when an account's balance is lower than the required amount for a transaction.

## Getting Started

### Installing

To get started with this project using Remix IDE:

1. **Open Remix IDE**:
   - Go to [Remix IDE](https://remix.ethereum.org).

2. **Create a new file**:
   - In the Remix IDE, create a new file named `ErrorHandlerContract.sol`.

3. **Copy the contract code**:
   - Copy and paste the following code into the new file:

     ```solidity
     // SPDX-License-Identifier: MIT
     pragma solidity ^0.8.4;

     contract ErrorHandlerContract {
         error InsufficientBalanceError(uint requiredAmount);

         string public tokenName = "MYTOKEN";
         uint256 public totalSupply = 100;
         mapping(address => uint256) public balances;

         function customRevertCondition(uint _balance, uint _amount) public pure {
             if (_balance < _amount) {
                 revert InsufficientBalanceError(_amount);
             }
         }
     }
     ```

### Executing program

To compile and deploy the smart contract using Remix:

1. **Compile the contract**:
   - In the Remix IDE, navigate to the "Solidity Compiler" tab.
   - Select the appropriate Solidity version (e.g., 0.8.4) and click on the "Compile ErrorHandlerContract.sol" button.

2. **Deploy the contract**:
   - Navigate to the "Deploy & Run Transactions" tab.
   - Ensure the environment is set to "JavaScript VM" for local testing.
   - Click on the "Deploy" button under the "Deploy & Run Transactions" tab.

3. **Interact with the contract**:
   - After deployment, you can interact with the contract's functions directly from the "Deploy & Run Transactions" tab.

## Help

For common problems or issues:

- **Compilation errors**: Ensure you are using the correct Solidity version (e.g., 0.8.4).
- **Deployment errors**: Make sure you have selected the "JavaScript VM" environment for local deployment.
- **Function call errors**: Ensure you are passing the correct parameters when calling the functions.

## Authors

- Muskan Gupta
  - GitHub: MuskanGupta140304
  - Email: 22BCS16747@cuchd.in

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
