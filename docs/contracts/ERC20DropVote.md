---
slug: /ERC20DropVote
title: ERC20DropVote
hide_title: true
displayed_sidebar: contracts
---

# ERC20DropVote

BASE: ERC20Votes EXTENSION: DropSinglePhase The `ERC20Drop` contract uses the `DropSinglePhase` extensions, along with `ERC20Votes`. It implements the ERC20 standard, along with the following additions to standard ERC20 logic: - Ownership of the contract, with the ability to restrict certain functions to only be called by the contract&#39;s owner. - Multicall capability to perform multiple actions atomically - EIP 2612 compliance: See {ERC20-permit} method, which can be used to change an account&#39;s ERC20 allowance by presenting a message signed by the account. The `drop` mechanism in the `DropSinglePhase` extension is a distribution mechanism tokens. It lets you set restrictions such as a price to charge, an allowlist etc. when an address attempts to mint tokens.

## Methods

### DOMAIN_SEPARATOR

```solidity
function DOMAIN_SEPARATOR() external view returns (bytes32)
```

_See {IERC20Permit-DOMAIN_SEPARATOR}._

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | bytes32 | undefined   |

### allowance

```solidity
function allowance(address owner, address spender) external view returns (uint256)
```

_See {IERC20-allowance}._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| owner   | address | undefined   |
| spender | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### approve

```solidity
function approve(address spender, uint256 amount) external nonpayable returns (bool)
```

_See {IERC20-approve}. NOTE: If `amount` is the maximum `uint256`, the allowance is not updated on `transferFrom`. This is semantically equivalent to an infinite approval. Requirements: - `spender` cannot be the zero address._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| spender | address | undefined   |
| amount  | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### balanceOf

```solidity
function balanceOf(address account) external view returns (uint256)
```

_See {IERC20-balanceOf}._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### burn

```solidity
function burn(uint256 _amount) external nonpayable
```

Lets an owner a given amount of their tokens.

_Caller should own the `_amount` of tokens._

#### Parameters

| Name     | Type    | Description                   |
| -------- | ------- | ----------------------------- |
| \_amount | uint256 | The number of tokens to burn. |

### checkpoints

```solidity
function checkpoints(address account, uint32 pos) external view returns (struct ERC20Votes.Checkpoint)
```

_Get the `pos`-th checkpoint for `account`._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |
| pos     | uint32  | undefined   |

#### Returns

| Name | Type                  | Description |
| ---- | --------------------- | ----------- |
| \_0  | ERC20Votes.Checkpoint | undefined   |

### claim

```solidity
function claim(address _receiver, uint256 _quantity, address _currency, uint256 _pricePerToken, IDropSinglePhase.AllowlistProof _allowlistProof, bytes _data) external payable
```

#### Parameters

| Name             | Type                            | Description |
| ---------------- | ------------------------------- | ----------- |
| \_receiver       | address                         | undefined   |
| \_quantity       | uint256                         | undefined   |
| \_currency       | address                         | undefined   |
| \_pricePerToken  | uint256                         | undefined   |
| \_allowlistProof | IDropSinglePhase.AllowlistProof | undefined   |
| \_data           | bytes                           | undefined   |

### claimCondition

```solidity
function claimCondition() external view returns (uint256 startTimestamp, uint256 maxClaimableSupply, uint256 supplyClaimed, uint256 quantityLimitPerWallet, bytes32 merkleRoot, uint256 pricePerToken, address currency, string metadata)
```

#### Returns

| Name                   | Type    | Description |
| ---------------------- | ------- | ----------- |
| startTimestamp         | uint256 | undefined   |
| maxClaimableSupply     | uint256 | undefined   |
| supplyClaimed          | uint256 | undefined   |
| quantityLimitPerWallet | uint256 | undefined   |
| merkleRoot             | bytes32 | undefined   |
| pricePerToken          | uint256 | undefined   |
| currency               | address | undefined   |
| metadata               | string  | undefined   |

### contractURI

```solidity
function contractURI() external view returns (string)
```

Returns the contract metadata URI.

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | string | undefined   |

### decimals

```solidity
function decimals() external view returns (uint8)
```

_Returns the number of decimals used to get its user representation. For example, if `decimals` equals `2`, a balance of `505` tokens should be displayed to a user as `5.05` (`505 / 10 ** 2`). Tokens usually opt for a value of 18, imitating the relationship between Ether and Wei. This is the value {ERC20} uses, unless this function is overridden; NOTE: This information is only used for *display* purposes: it in no way affects any of the arithmetic of the contract, including {IERC20-balanceOf} and {IERC20-transfer}._

#### Returns

| Name | Type  | Description |
| ---- | ----- | ----------- |
| \_0  | uint8 | undefined   |

### decreaseAllowance

```solidity
function decreaseAllowance(address spender, uint256 subtractedValue) external nonpayable returns (bool)
```

_Atomically decreases the allowance granted to `spender` by the caller. This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}. Emits an {Approval} event indicating the updated allowance. Requirements: - `spender` cannot be the zero address. - `spender` must have allowance for the caller of at least `subtractedValue`._

#### Parameters

| Name            | Type    | Description |
| --------------- | ------- | ----------- |
| spender         | address | undefined   |
| subtractedValue | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### delegate

```solidity
function delegate(address delegatee) external nonpayable
```

_Delegate votes from the sender to `delegatee`._

#### Parameters

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| delegatee | address | undefined   |

### delegateBySig

```solidity
function delegateBySig(address delegatee, uint256 nonce, uint256 expiry, uint8 v, bytes32 r, bytes32 s) external nonpayable
```

_Delegates votes from signer to `delegatee`_

#### Parameters

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| delegatee | address | undefined   |
| nonce     | uint256 | undefined   |
| expiry    | uint256 | undefined   |
| v         | uint8   | undefined   |
| r         | bytes32 | undefined   |
| s         | bytes32 | undefined   |

### delegates

```solidity
function delegates(address account) external view returns (address)
```

_Get the address `account` is currently delegating to._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

### getPastTotalSupply

```solidity
function getPastTotalSupply(uint256 blockNumber) external view returns (uint256)
```

_Retrieve the `totalSupply` at the end of `blockNumber`. Note, this value is the sum of all balances. It is but NOT the sum of all the delegated votes! Requirements: - `blockNumber` must have been already mined_

#### Parameters

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| blockNumber | uint256 | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### getPastVotes

```solidity
function getPastVotes(address account, uint256 blockNumber) external view returns (uint256)
```

_Retrieve the number of votes for `account` at the end of `blockNumber`. Requirements: - `blockNumber` must have been already mined_

#### Parameters

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| account     | address | undefined   |
| blockNumber | uint256 | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### getSupplyClaimedByWallet

```solidity
function getSupplyClaimedByWallet(address _claimer) external view returns (uint256)
```

_Returns the supply claimed by claimer for active conditionId._

#### Parameters

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| \_claimer | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### getVotes

```solidity
function getVotes(address account) external view returns (uint256)
```

_Gets the current votes balance for `account`_

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### increaseAllowance

```solidity
function increaseAllowance(address spender, uint256 addedValue) external nonpayable returns (bool)
```

_Atomically increases the allowance granted to `spender` by the caller. This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}. Emits an {Approval} event indicating the updated allowance. Requirements: - `spender` cannot be the zero address._

#### Parameters

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| spender    | address | undefined   |
| addedValue | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### multicall

```solidity
function multicall(bytes[] data) external nonpayable returns (bytes[] results)
```

Receives and executes a batch of function calls on this contract.

_Receives and executes a batch of function calls on this contract._

#### Parameters

| Name | Type    | Description                                                          |
| ---- | ------- | -------------------------------------------------------------------- |
| data | bytes[] | The bytes data that makes up the batch of function calls to execute. |

#### Returns

| Name    | Type    | Description                                                                      |
| ------- | ------- | -------------------------------------------------------------------------------- |
| results | bytes[] | The bytes data that makes up the result of the batch of function calls executed. |

### name

```solidity
function name() external view returns (string)
```

_Returns the name of the token._

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | string | undefined   |

### nonces

```solidity
function nonces(address owner) external view returns (uint256)
```

_See {IERC20Permit-nonces}._

#### Parameters

| Name  | Type    | Description |
| ----- | ------- | ----------- |
| owner | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### numCheckpoints

```solidity
function numCheckpoints(address account) external view returns (uint32)
```

_Get number of checkpoints for `account`._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | uint32 | undefined   |

### owner

```solidity
function owner() external view returns (address)
```

Returns the owner of the contract.

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

### permit

```solidity
function permit(address owner, address spender, uint256 value, uint256 deadline, uint8 v, bytes32 r, bytes32 s) external nonpayable
```

_See {IERC20Permit-permit}._

#### Parameters

| Name     | Type    | Description |
| -------- | ------- | ----------- |
| owner    | address | undefined   |
| spender  | address | undefined   |
| value    | uint256 | undefined   |
| deadline | uint256 | undefined   |
| v        | uint8   | undefined   |
| r        | bytes32 | undefined   |
| s        | bytes32 | undefined   |

### primarySaleRecipient

```solidity
function primarySaleRecipient() external view returns (address)
```

_Returns primary sale recipient address._

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

### setClaimConditions

```solidity
function setClaimConditions(IClaimCondition.ClaimCondition _condition, bool _resetClaimEligibility) external nonpayable
```

#### Parameters

| Name                    | Type                           | Description |
| ----------------------- | ------------------------------ | ----------- |
| \_condition             | IClaimCondition.ClaimCondition | undefined   |
| \_resetClaimEligibility | bool                           | undefined   |

### setContractURI

```solidity
function setContractURI(string _uri) external nonpayable
```

Lets a contract admin set the URI for contract-level metadata.

_Caller should be authorized to setup contractURI, e.g. contract admin. See {\_canSetContractURI}. Emits {ContractURIUpdated Event}._

#### Parameters

| Name  | Type   | Description                                                           |
| ----- | ------ | --------------------------------------------------------------------- |
| \_uri | string | keccak256 hash of the role. e.g. keccak256(&quot;TRANSFER_ROLE&quot;) |

### setOwner

```solidity
function setOwner(address _newOwner) external nonpayable
```

Lets an authorized wallet set a new owner for the contract.

#### Parameters

| Name       | Type    | Description                                          |
| ---------- | ------- | ---------------------------------------------------- |
| \_newOwner | address | The address to set as the new owner of the contract. |

### setPrimarySaleRecipient

```solidity
function setPrimarySaleRecipient(address _saleRecipient) external nonpayable
```

Updates primary sale recipient.

_Caller should be authorized to set primary sales info. See {\_canSetPrimarySaleRecipient}. Emits {PrimarySaleRecipientUpdated Event}; See {\_setupPrimarySaleRecipient}._

#### Parameters

| Name            | Type    | Description                                          |
| --------------- | ------- | ---------------------------------------------------- |
| \_saleRecipient | address | Address to be set as new recipient of primary sales. |

### symbol

```solidity
function symbol() external view returns (string)
```

_Returns the symbol of the token, usually a shorter version of the name._

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | string | undefined   |

### totalSupply

```solidity
function totalSupply() external view returns (uint256)
```

_See {IERC20-totalSupply}._

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### transfer

```solidity
function transfer(address to, uint256 amount) external nonpayable returns (bool)
```

_See {IERC20-transfer}. Requirements: - `to` cannot be the zero address. - the caller must have a balance of at least `amount`._

#### Parameters

| Name   | Type    | Description |
| ------ | ------- | ----------- |
| to     | address | undefined   |
| amount | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### transferFrom

```solidity
function transferFrom(address from, address to, uint256 amount) external nonpayable returns (bool)
```

_See {IERC20-transferFrom}. Emits an {Approval} event indicating the updated allowance. This is not required by the EIP. See the note at the beginning of {ERC20}. NOTE: Does not update the allowance if the current allowance is the maximum `uint256`. Requirements: - `from` and `to` cannot be the zero address. - `from` must have a balance of at least `amount`. - the caller must have allowance for `from`&#39;s tokens of at least `amount`._

#### Parameters

| Name   | Type    | Description |
| ------ | ------- | ----------- |
| from   | address | undefined   |
| to     | address | undefined   |
| amount | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### verifyClaim

```solidity
function verifyClaim(address _claimer, uint256 _quantity, address _currency, uint256 _pricePerToken, IDropSinglePhase.AllowlistProof _allowlistProof) external view returns (bool isOverride)
```

#### Parameters

| Name             | Type                            | Description |
| ---------------- | ------------------------------- | ----------- |
| \_claimer        | address                         | undefined   |
| \_quantity       | uint256                         | undefined   |
| \_currency       | address                         | undefined   |
| \_pricePerToken  | uint256                         | undefined   |
| \_allowlistProof | IDropSinglePhase.AllowlistProof | undefined   |

#### Returns

| Name       | Type | Description |
| ---------- | ---- | ----------- |
| isOverride | bool | undefined   |

## Events

### Approval

```solidity
event Approval(address indexed owner, address indexed spender, uint256 value)
```

#### Parameters

| Name              | Type    | Description |
| ----------------- | ------- | ----------- |
| owner `indexed`   | address | undefined   |
| spender `indexed` | address | undefined   |
| value             | uint256 | undefined   |

### ClaimConditionUpdated

```solidity
event ClaimConditionUpdated(IClaimCondition.ClaimCondition condition, bool resetEligibility)
```

Emitted when the contract&#39;s claim conditions are updated.

#### Parameters

| Name             | Type                           | Description |
| ---------------- | ------------------------------ | ----------- |
| condition        | IClaimCondition.ClaimCondition | undefined   |
| resetEligibility | bool                           | undefined   |

### ContractURIUpdated

```solidity
event ContractURIUpdated(string prevURI, string newURI)
```

#### Parameters

| Name    | Type   | Description |
| ------- | ------ | ----------- |
| prevURI | string | undefined   |
| newURI  | string | undefined   |

### DelegateChanged

```solidity
event DelegateChanged(address indexed delegator, address indexed fromDelegate, address indexed toDelegate)
```

#### Parameters

| Name                   | Type    | Description |
| ---------------------- | ------- | ----------- |
| delegator `indexed`    | address | undefined   |
| fromDelegate `indexed` | address | undefined   |
| toDelegate `indexed`   | address | undefined   |

### DelegateVotesChanged

```solidity
event DelegateVotesChanged(address indexed delegate, uint256 previousBalance, uint256 newBalance)
```

#### Parameters

| Name               | Type    | Description |
| ------------------ | ------- | ----------- |
| delegate `indexed` | address | undefined   |
| previousBalance    | uint256 | undefined   |
| newBalance         | uint256 | undefined   |

### OwnerUpdated

```solidity
event OwnerUpdated(address indexed prevOwner, address indexed newOwner)
```

#### Parameters

| Name                | Type    | Description |
| ------------------- | ------- | ----------- |
| prevOwner `indexed` | address | undefined   |
| newOwner `indexed`  | address | undefined   |

### PrimarySaleRecipientUpdated

```solidity
event PrimarySaleRecipientUpdated(address indexed recipient)
```

#### Parameters

| Name                | Type    | Description |
| ------------------- | ------- | ----------- |
| recipient `indexed` | address | undefined   |

### TokensClaimed

```solidity
event TokensClaimed(address indexed claimer, address indexed receiver, uint256 indexed startTokenId, uint256 quantityClaimed)
```

Emitted when tokens are claimed via `claim`.

#### Parameters

| Name                   | Type    | Description |
| ---------------------- | ------- | ----------- |
| claimer `indexed`      | address | undefined   |
| receiver `indexed`     | address | undefined   |
| startTokenId `indexed` | uint256 | undefined   |
| quantityClaimed        | uint256 | undefined   |

### Transfer

```solidity
event Transfer(address indexed from, address indexed to, uint256 value)
```

#### Parameters

| Name           | Type    | Description |
| -------------- | ------- | ----------- |
| from `indexed` | address | undefined   |
| to `indexed`   | address | undefined   |
| value          | uint256 | undefined   |
