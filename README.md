# RIF Token Contracts
The RSK contracts for the RSK Infraestructure Framework token (RIF).

# Info

- [Contract @ RSK Explorer](https://explorer.rsk.co/address/0x2acc95758f8b5f583470ba265eb685a8f45fc9d5)
- [Audit report](https://github.com/riflabs/RIF-Token/blob/master/RIF2018v2006.pdf)
- [Documentation](https://developers.rsk.co/rif)

# Fork Modifications for DAO Contracts Testing

This fork contains necessary modifications to integrate with the [RootstockCollective/dao-contracts](https://github.com/RootstockCollective/dao-contracts) repository for testing purposes.

## Required Changes


### 1. Added package.json
**Issue:** Repository compilation failed when referenced in dao-contracts' package.json.

**Cause:** Missing package.json file prevented proper repository integration.

**Solution:** Added package.json file to enable proper package management and dependency resolution.


### 2. Modified Method Visibility
**Issue:** RIF-Token compilation failed with "Bytecode is not a valid hex string" error.

**Cause:** Compiler incompatibility with method visibility settings in AddressLinker and AddressHelper libraries.

**Solution:** Changed method visibility from `public` to `internal` in affected libraries.

## Important Note
This RIF Token repository is used solely for testing the DAO contracts. The production RIF Token was deployed long ago and remains unaffected by these modifications.