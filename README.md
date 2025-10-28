# EVM Prediction Market Contracts
==================================

EVM Prediction Market Smart Contract: Collection of smart contracts for the prediction market platform support for EVM compatable chains like BASE.


Install
-------
### Install requirements with npm:
```bash
npm install @gnosis.pm/pm-contracts
```

Testing and Linting
-------------------
### Run all tests (requires Node version >=7 for `async/await`, and will automatically run TestRPC in the background):

```bash
npm test
```

### Run all tests matching a regexp pattern by setting the `TEST_GREP` environment variable

```bash
TEST_GREP='short selling' npm test
```

### Lint the JS

```bash
npm run lint
```

Compile and Deploy
------------------
These commands apply to the RPC provider running on port 8545. You may want to have TestRPC running in the background. They are really wrappers around the [corresponding Truffle commands](http://truffleframework.com/docs/advanced/commands).

### Compile all contracts to obtain ABI and bytecode:

```bash
npm run compile
```

### Migrate all contracts required for the basic framework onto network associated with RPC provider:

```bash
npm run migrate
```

Network Artifacts
-----------------

### Show the deployed addresses of all contracts on all networks:

```bash
npm run networks
```

Command line options for `truffle` can be passed down through NPM by preceding the options list with `--`. For example:

### Clean network artifacts:

```bash
npm run networks -- --clean
```

Network artifacts from running migrations will contain addresses of deployed contracts on the Kovan and Rinkeby testnets.

### Take network info from `networks.json` and inject it into contract build artifacts. This is done prepublish as well.

```bash
npm run injectnetinfo
```

### Extract all network information into `networks.json`.

Be aware that this will clobber `networks.json`, so be careful with this command:

```bash
npm run extractnetinfo
```

Gas Measurements
----------------

### Log gas measurements into `build/gas-stats.json`

```bash
npm run measuregasstats
```

Documentation
-------------

There is a copy version hosted online at https://gnosis-pm-contracts.readthedocs.io/en/latest/

### Locally build docs for readthedocs

Will install [Sphinx](http://www.sphinx-doc.org/en/stable/) and [Solidity Domain for Sphinx](https://github.com/cag/sphinxcontrib-soliditydomain/):

```bash
cd docs
pip install -r requirements.txt
make html
```

