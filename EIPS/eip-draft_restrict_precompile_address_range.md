---
eip: <to be assigned>
title: Specify restricted address range for precompiles/system contracts
author: Alex Beregszaszi (@axic)
discussions-to: <URL>
status: Draft
type: Standards Track
category: Core
created: 2018-07-27
---

## Simple Summary
Specify an Ethereum address range occupied by precompiles and future system contracts. Regular accounts and contracts cannot obtain such an address.

## Abstract
The address range between 0x0000000000000000000000000000000000000000 and 0x00000000000000000000000000000000000000ff is reserved for precompiles and system contracts.

## Motivation
This will simplify certain future features where unless this is implemented, several exceptions must be specified.

## Specification
The address range between 0x0000000000000000000000000000000000000000 and 0x00000000000000000000000000000000000000ff is reserved for precompiles and system contracts.

If a contract creation (as a result of a create transaction or a `CREATE` opcode) results in an address within this range, then it is rejected.

## Rationale
N/A

## Backwards Compatibility
No contracts on the main network have been created at the specified addresses. As a result it should pose no backwards compatibility problems.

## Test Cases
N/A

## Implementation
N/A

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).