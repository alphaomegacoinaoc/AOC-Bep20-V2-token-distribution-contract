## BulkOperations

# overview:
The BulkOperations contract enables bulk token transfers and distribution requests for Alpha Omega Coin (AOC) Bep20-V2 token, interacting with the Alpha Omega Coin (AOC) Distribution contract. 
This Contract contains only write functions and all are owner-only.

## Key Features:

## Write Functions
# Function: initialize(address _aoc)
What it does: Initializes the contract with the Alpha Omega Coin (AOC) Bep20-V2 tokens address and sets up ownership and pausability.
Purpose: Configures the contract to interact with the AOC Bep20-V2 tokens and enables secure operations.

# Function: _authorizeUpgrade(address newImplementation)
What it does: Authorizes a contract upgrade (owner-only).
Purpose: Enables future improvements to the contract securely.

# Function: bulkTransfer(address[] calldata recipients, uint256[] calldata amounts)
What It Does: Allows the owner to transfer AOC Bep20-V2 tokens to multiple recipients in a single transaction, ensuring the sender has sufficient balance and arrays match.
Purpose: Facilitates efficient bulk token distribution from the owner's wallet.
Simple Example: The owner provides a list of 10 recipients and corresponding amounts (e.g., 100 AOC Bep20-V2 tokens each); the function transfers them using transferFrom, emitting a BulkTransfer event.
Why It Matters: Reduces gas costs and simplifies large-scale AOC Bep20-V2 token distributions.

# Function: bulkDistribution(string calldata date, uint256 count)
What It Does: Emits an event requesting AOC Bep20-V2 token distribution for a specified count on a given date (no actual transfer).
Purpose: Signals external systems to handle distributions based on the request.
Simple Example: The owner calls with date "2025-08-13" and count 50; it emits BulkDistributionRequested, which off-chain tools can use to process.
Why It Matters: Enables coordinated, event-driven distributions without on-chain transfers.

## How It Works
The owner provides arrays of recipients and amounts for bulk transfers, which are processed using the Alpha Omega Coin (AOC) Bep20-V2 token contract’s transferFrom function.
The bulk distribution function emits an event for external systems to handle distribution logic.

# Deploy BulkOperations:
Pass the Alpha Omega Coin (AOC) Bep20-V2 token contract address during initialization.

