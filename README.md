## Getting started

### Install packages
```
npm install
```

### Verify a vesting account (only relevant for locked tokens)

To verify a vesting account has been setup properly you need 3 things : 
- A positions account address. This is the account's unique identifier.
- The expected owner (the public key you expect to be the beneficiary of the account).
- The expected balance (the balance you expect the owner to be entitled to).

Run the following command from the root directory: 
```
npm run cli verify -- -p ${POSITION_ACCOUNT} -o ${EXPECTED_OWNER_PUBKEY} -b ${EXPECTED_BALANCE}
```

If successful the output will be something like this: 

```
npm run cli verify -- -p BPXPkj7WLAxUrotGNkC9bNnTTqPJsJD4QLDKuRhjBoAj -o ADBD8FKZXbHLTbJqJYNYPkiKqZp9AXg9EFU43oxZKeD2 -b 600000000

Succesfully verified vesting account : BPXPkj7WLAxUrotGNkC9bNnTTqPJsJD4QLDKuRhjBoAj
With owner ADBD8FKZXbHLTbJqJYNYPkiKqZp9AXg9EFU43oxZKeD2 and balance 600000000 PYTH
Tokens must be sent to: 61YcP8msC5F3ZTLy99VWM2oom6y47UzNmSQQdXMmdCG1
```

You can then transfer the tokens to the address printed.