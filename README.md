# Escrow-Service

This contract allows a user (depositor) to deposit any amount of tokens (depositToken) and:
1. assign an ID to the deposit
2. assign the deposit a whitelisted address. 
3. assign a 'purchase' amount
4. designate what token the purchase must be completed with (purchaseToken)
5. all done in one function

The whitelisted address can then use the claim function using the appropriate ID, which does:

2. transfers the required amount of 'purchaseToken' to the contract
3. transfers the total amount of 'depositToken' to the caller

The 'depositor' can now use the completeClaim() function, which then:
1. sends the total amount of 'purchaseToken' to the depositor
2. marks the escrow transaction as complete
