# Report


## Medium Issues


| |Issue|Instances|
|-|:-|:-:|
| [M-1](#M-1) | Strings should use double quotes rather than single quotes | 1 |
| [M-2](#M-2) | Avoid using ecrecover() | 2 |
| [M-3](#M-3) | Centralization Risk for trusted owners | 14 |
| [M-4](#M-4) | Unsafe use of ERC20 transferFrom() | 7 |
| [M-5](#M-5) | Unsafe use of ERC20 transfer() | 8 |
| [M-6](#M-6) | Timestamp may be manipulation | 8 |

## Low Issues


| |Issue|Instances|
|-|:-|:-:|
| [L-1](#L-1) |  `abi.encodePacked()` should not be used with dynamic types when passing the result to a hash function such as `keccak256()` | 1 |
| [L-2](#L-2) | Do not use deprecated library functions | 2 |
| [L-3](#L-3) | Empty function body | 1 |
| [L-4](#L-4) | Initializers could be front-run | 1 |
| [L-5](#L-5) | Missing contract existence checks before low-level calls | 8 |
| [L-6](#L-6) | State variables not capped at reasonable values | 39 |
| [L-7](#L-7) | Some tokens may revert when zero value transfers are made | 8 |
| [L-8](#L-8) |  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard   | 8 |
| [L-9](#L-9) | Some tokens may revert when large transfers are made | 8 |
| [L-10](#L-10) | Unsafe ERC20 operation(s) | 11 |

## Non Critical Issues


| |Issue|Instances|
|-|:-|:-:|
| [NC-1](#NC-1) | assert() should be replaced with require() or revert() | 1 |
| [NC-2](#NC-2) | Variables without visibility specifier | 18 |
| [NC-3](#NC-3) | Constants in comparisons should appear on the left side | 31 |
| [NC-4](#NC-4) | Contract declarations should have NatSpec @author annotations | 3 |
| [NC-5](#NC-5) | Contract declarations should have NatSpec @Title annotations | 3 |
| [NC-6](#NC-6) | Consider using delete rather than assigning zero to clear value | 15 |
| [NC-7](#NC-7) | Consider using delete rather than assigning false to clear value | 2 |
| [NC-8](#NC-8) | Consider adding a block/deny-list" | 17 |
| [NC-9](#NC-9) | Events are missing sender information | 56 |
| [NC-10](#NC-10) | Events should use parameters to convey information | 2 |
| [NC-11](#NC-11) | If-statement can be converted to a ternary | 36 |
| [NC-12](#NC-12) | Variable names for immutables should use CONSTANT_CASE | 16 |
| [NC-13](#NC-13) | Contract should expose an interface | 3 |
| [NC-14](#NC-14) | Consider using named mappings | 3 |
| [NC-15](#NC-15) | Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct | 11 |
| [NC-16](#NC-16) | Use of override is unnecessary | 4 |
| [NC-17](#NC-17) | Consider using descriptive constants when passing zero as a function argument | 22 |
| [NC-18](#NC-18) | Non-external/public variable names should begin with an underscore | 24 |
| [NC-19](#NC-19) | Return values of `approve()` not checked | 3 |
| [NC-20](#NC-20) | Use the latest solidity version for deployment   | 18 |
| [NC-21](#NC-21) | Constants should be defined rather than using magic numbers | 1 |
| [NC-22](#NC-22) | Consider moving msg.sender checks to modifiers | 65 |
| [NC-23](#NC-23) | Owner can renounce while system is paused | 3 |
| [NC-24](#NC-24) | Array indices should be referenced via enums rather than numeric literals | 4 |

## Gas Optimizations


| |Issue|Instances|
|-|:-|:-:|
| [GAS-1](#GAS-1) | Use scientific notation (e.g. 1e18) rather than exponentiation (e.g. 10**18) | 11 |
| [GAS-2](#GAS-2) | Nesting if-statements is cheaper than using && | 12 |
| [GAS-3](#GAS-3) | Consider using = instead of += and -= for gas efficiency | 2 |
| [GAS-4](#GAS-4) | Use >= instead of > for gas efficiency | 1 |
| [GAS-5](#GAS-5) | Dont use _msgSender() if not supporting EIP-2771 | 5 |
| [GAS-6](#GAS-6) | <array>.length should not be looked up in every loop of a for-loop | 4 |
| [GAS-7](#GAS-7) | Use assembly to emit events, in order to save gas | 60 |
| [GAS-8](#GAS-8) | Using bools for storage incurs overhead | 4 |
| [GAS-9](#GAS-9) | Cache array length outside of loop | 4 |
| [GAS-10](#GAS-10) | Consider using assembly for simple zero checks to save gas | 6 |
| [GAS-11](#GAS-11) | Consider using constant rather than immutable to save gas | 16 |
| [GAS-12](#GAS-12) | Constructors can be marked payable | 14 |
| [GAS-13](#GAS-13) | Use Custom Errors | 75 |
| [GAS-14](#GAS-14) | Don't initialize variables with default value | 10 |
| [GAS-15](#GAS-15) | Initializers can be marked as payable to save deployment gas | 1 |
| [GAS-16](#GAS-16) | Use assembly for small keccak256 hashes, in order to save gas | 1 |
| [GAS-17](#GAS-17) | Long revert strings | 33 |
| [GAS-18](#GAS-18) | Reduce gas usage by moving to Solidity 0.8.19 or later | 18 |
| [GAS-19](#GAS-19) | Functions guaranteed to revert when called by normal users can be marked `payable` | 7 |
| [GAS-20](#GAS-20) | `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too) | 10 |
| [GAS-21](#GAS-21) | Using `private` rather than `public` for constants, saves gas | 5 |
| [GAS-22](#GAS-22) | require()/revert() strings longer than 32 bytes cost extra gas | 94 |
| [GAS-23](#GAS-23) | Splitting require() statements that use && saves gas | 3 |
| [GAS-24](#GAS-24) | Structs can be packed into fewer storage slots | 5 |
| [GAS-25](#GAS-25) | Use storage instead of memory for structs/arrays | 3 |
| [GAS-26](#GAS-26) | Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency | 13 |
| [GAS-27](#GAS-27) | Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead | 72 |
| [GAS-28](#GAS-28) | Use != 0 instead of > 0 for unsigned integer comparison | 1 |
| [GAS-29](#GAS-29) | Optimize names to save gas | 199 |

##################################################################### 
 
 DETAILED REPORT:: 


##################################################################### 


## Medium Issues


 ### <a name="M-1"></a>[M-1] Strings should use double quotes rather than single quotes

#### Impact:
Using consistent double quotes for strings improves code readability and maintainability. Also see it here https://docs.soliditylang.org/en/v0.8.20/style-guide.html#other-recommendations

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/PoolManager.sol

26:         keccak256(bytes memory data)= abi.encode(keccak256('transferTrancheTokensToEVM(uint64,bytes16,address,uint64,address,uint128)'))

```

</details> 
 


 ### <a name="M-2"></a>[M-2] Avoid using ecrecover()
Using ecrecover() to verify signatures can be dangerous and should be replaced with a safer alternative such as OpenZeppelin’s ECDSA library.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

79:         return signer == ecrecover(hash, v, r, s);

```

```solidity
File: example/UserEscrow.sol

89:         return signer == ecrecover(digest, v+1, r, signature);

```

</details> 
 


 ### <a name="M-3"></a>[M-3] Centralization Risk for trusted owners

#### Impact:
Contracts have owners with privileged rights to perform admin tasks and need to be trusted to not perform malicious updates or drain funds.

*Instances (14)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

7: contract Auth {

```

```solidity
File: example/DelayedAdmin.sol

12: contract DelayedAdmin is Auth {

```

```solidity
File: example/Escrow.sol

14: contract Escrow is Auth {

```

```solidity
File: example/Factory.sol

26: contract LiquidityPoolFactory is Auth {

98: contract TrancheTokenFactory is Auth {

```

```solidity
File: example/Gateway.sol

84: contract Gateway is Auth {

```

```solidity
File: example/InvestmentManager.sol

69: contract InvestmentManager is Auth {

```

```solidity
File: example/LiquidityPool.sol

52: contract LiquidityPool is Auth, IERC4626 {

```

```solidity
File: example/PauseAdmin.sol

10: contract PauseAdmin is Auth {

```

```solidity
File: example/PoolManager.sol

83: contract PoolManager is Auth {

```

```solidity
File: example/RestrictionManager.sol

14: contract RestrictionManager is Auth {

```

```solidity
File: example/Root.sol

15: contract Root is Auth {

```

```solidity
File: example/Router.sol

24: contract AxelarRouter is Auth {

```

```solidity
File: example/UserEscrow.sol

15: contract UserEscrow is Auth {

```

</details> 
 


 ### <a name="M-4"></a>[M-4] Unsafe use of ERC20 transferFrom()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transferFrom() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransferFrom() from OpenZeppelin instead.

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

25:     function transferFrom(address from, address to, uint256 amount) external returns (bool);

167:         lPool.transferFrom(user, address(escrow), _trancheTokenAmount);

313:             LiquidityPoolLike(liquidityPool).transferFrom(address(escrow), user, trancheTokenPayout),

475:             lPool.transferFrom(address(escrow), user, trancheTokenAmount),

```

```solidity
File: example/LiquidityPool.sol

295:     function transferFrom(address, address, uint256) public returns (bool) {

```

```solidity
File: example/Tranche.sol

63:     function transferFrom(address from, address to, uint256 value)

69:         return super.transferFrom(from, to, value);

```

</details> 
 


 ### <a name="M-5"></a>[M-5] Unsafe use of ERC20 transfer()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transfer() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransfer() from OpenZeppelin instead.

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

15: function transfer(address _to, uint256 _value) public returns (bool success) {

```

```solidity
File: example/Gateway.sol

192:     function transfer(uint128 token, address sender, bytes32 receiver, uint128 amount)

```

```solidity
File: example/LiquidityPool.sol

301:     function transfer(address, uint256) public returns (bool) {

```

```solidity
File: example/PoolManager.sol

28:     function transfer(uint128 currency, address sender, bytes32 recipient, uint128 amount) external;

136:     function transfer(address currencyAddress, bytes32 recipient, uint128 amount) public {

141:         gateway.transfer(currency, msg.sender, recipient, amount);

```

```solidity
File: example/Tranche.sol

59:     function transfer(address to, uint256 value) public override restricted(_msgSender(), to, value) returns (bool) {

60:         return super.transfer(to, value);

```

</details> 
 


 ### <a name="M-6"></a>[M-6] Timestamp may be manipulation
The block.timestamp can be manipulated by miners to perform MEV profiting or other time-based attacks.

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/LiquidityPool.sol

326:         lastPriceUpdate = block.timestamp;

```

```solidity
File: example/PoolManager.sol

180:         pool.createdAt = block.timestamp;

217:         tranche.createdAt = block.timestamp;

```

```solidity
File: example/RestrictionManager.sol

46:         require((members[user] >= block.timestamp), "RestrictionManager/destination-not-a-member");

50:         if (members[user] >= block.timestamp) {

58:         require(block.timestamp <= validUntil, "RestrictionManager/invalid-valid-until");

```

```solidity
File: example/Root.sol

66:         schedule[target] = block.timestamp + delay;

77:         require(schedule[target] < block.timestamp, "Root/target-not-ready");

```

</details> 
 


## Low Issues


 ### <a name="L-1"></a>[L-1]  `abi.encodePacked()` should not be used with dynamic types when passing the result to a hash function such as `keccak256()`
Use `abi.encode()` instead which will pad items to 32 bytes, which will [prevent hash collisions](https://docs.soliditylang.org/en/v0.8.13/abi-spec.html#non-standard-packed-mode) (e.g. `abi.encodePacked(0x123,0x456)` => `0x123456` => `abi.encodePacked(0x1,0x23456)`, but `abi.encode(0x123,0x456)` => `0x0...1230...456`). "Unless there is a compelling reason, `abi.encode` should be preferred". If there is only one argument to `abi.encodePacked()` it can often be cast to `bytes()` or `bytes32()` [instead](https://ethereum.stackexchange.com/questions/30912/how-to-compare-strings-in-solidity#answer-82739).
If all arguments are strings and or bytes, `bytes.concat()` should be used instead

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

121:         bytes32 salt = keccak256(abi.encodePacked(poolId, trancheId));

```

</details> 
 


 ### <a name="L-2"></a>[L-2] Do not use deprecated library functions

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Escrow.sol

24:         SafeTransferLib.safeApprove(token, spender, value);

```

```solidity
File: example/SafeTransferLib.sol

36:     function safeApprove(address token, address to, uint256 value) internal {

```

</details> 
 


 ### <a name="L-3"></a>[L-3] Empty function body
Consider adding a comment about why the function body is empty

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Tranche.sol

33:     constructor(uint8 decimals_) ERC20(decimals_) {}

```

</details> 
 


 ### <a name="L-4"></a>[L-4] Initializers could be front-run
Initializers could be front-run, allowing an attacker to either set their own values, take ownership of the contract, and in the best case forcing a re-deployment

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/UserEscrow.sol

62:     function initialize(address _root) external {

```

</details> 
 


 ### <a name="L-5"></a>[L-5] Missing contract existence checks before low-level calls
Low-level calls return success if there is no code present at the specified address. In addition to the zero-address checks, add a check to verify that `<address>.code.length > 0`.

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/LiquidityPool.sol

296:         (bool success, bytes memory data) = address(share).call(bytes.concat(msg.data, bytes20(msg.sender)));

302:         (bool success, bytes memory data) = address(share).call(bytes.concat(msg.data, bytes20(msg.sender)));

308:         (bool success, bytes memory data) = address(share).call(bytes.concat(msg.data, bytes20(msg.sender)));

314:         (bool success,) = address(share).call(bytes.concat(msg.data, bytes20(address(this))));

319:         (bool success,) = address(share).call(bytes.concat(msg.data, bytes20(address(this))));

```

```solidity
File: example/SafeTransferLib.sol

17:             token.call(abi.encodeWithSelector(IERC20.transferFrom.selector, from, to, value));

27:         (bool success, bytes memory data) = token.call(abi.encodeWithSelector(IERC20.transfer.selector, to, value));

37:         (bool success, bytes memory data) = token.call(abi.encodeWithSelector(IERC20.approve.selector, to, value));

```

</details> 
 


 ### <a name="L-6"></a>[L-6] State variables not capped at reasonable values
Consider adding minimum/maximum value checks to ensure that the state variables below can never be used to excessively harm users, including via griefing

*Instances (39)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

10:     uint32 h;

11:     uint add;

```

```solidity
File: example/Factory.sol

62: 

64:         bytes32 s;

65:         uint8 v;

```

```solidity
File: example/InvestmentManager.sol

60:     uint128 maxDeposit; // denominated in currency

61:     uint128 maxMint; // denominated in tranche tokens

62:     uint128 maxWithdraw; // denominated in currency

63:     uint128 maxRedeem; // denominated in tranche tokens

554:             return 0;

563:             return 0;

661:         return true;

```

```solidity
File: example/LiquidityPool.sol

183:         return sharesRedeemed;

207:         return currencyPayout;

```

```solidity
File: example/Messages.sol

855: 

879:             return 0x0;

```

```solidity
File: example/PoolManager.sol

57:     uint64 poolId;

58:     uint256 createdAt;

67:     address token;

68:     uint64 poolId;

69:     bytes16 trancheId;

71:     uint8 decimals;

72:     uint256 createdAt;

73:     string tokenName;

74:     string tokenSymbol;

312:         return token;

340:         return liquidityPool;

357:         return true;

```

```solidity
File: example/RestrictionManager.sol

30:             return DESTINATION_NOT_A_MEMBER_RESTRICTION_CODE;

32: 

38:             return DESTINATION_NOT_A_MEMBER_RESTRICTION_MESSAGE;

40: 

51:             return true;

53:         return false;

```

```solidity
File: example/UserEscrow.sol

21:         string name;

22:         string symbol;

72: 

74:         bytes32 s;

75:         uint8 v;

```

</details> 
 


 ### <a name="L-7"></a>[L-7] Some tokens may revert when zero value transfers are made
Despite the fact that [EIP-20](https://github.com/ethereum/EIPs/blob/7500ac4fc1bbdfaf684e7ef851f798f6b667b2fe/EIPS/eip-20.md?plain=1#L116) states that zero-value transfers must be accepted, some tokens, such as LEND, will revert if this is attempted, which may cause transactions that involve other tokens (such as batch operations) to fully revert. Consider skipping the transfer if the amount is zero, which will also save gas.

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

15: function transfer(address _to, uint256 _value) public returns (bool success) {

```

```solidity
File: example/Gateway.sol

192:     function transfer(uint128 token, address sender, bytes32 receiver, uint128 amount)

```

```solidity
File: example/LiquidityPool.sol

301:     function transfer(address, uint256) public returns (bool) {

```

```solidity
File: example/PoolManager.sol

28:     function transfer(uint128 currency, address sender, bytes32 recipient, uint128 amount) external;

136:     function transfer(address currencyAddress, bytes32 recipient, uint128 amount) public {

141:         gateway.transfer(currency, msg.sender, recipient, amount);

```

```solidity
File: example/Tranche.sol

59:     function transfer(address to, uint256 value) public override restricted(_msgSender(), to, value) returns (bool) {

60:         return super.transfer(to, value);

```

</details> 
 


 ### <a name="L-8"></a>[L-8]  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard  
Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks opens the users of this protocol up to [read-only reentrancy](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) vulnerability with no way to protect them except by block-listing the entire protocol.

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

15: function transfer(address _to, uint256 _value) public returns (bool success) {

```

```solidity
File: example/Gateway.sol

192:     function transfer(uint128 token, address sender, bytes32 receiver, uint128 amount)

```

```solidity
File: example/LiquidityPool.sol

301:     function transfer(address, uint256) public returns (bool) {

```

```solidity
File: example/PoolManager.sol

28:     function transfer(uint128 currency, address sender, bytes32 recipient, uint128 amount) external;

136:     function transfer(address currencyAddress, bytes32 recipient, uint128 amount) public {

141:         gateway.transfer(currency, msg.sender, recipient, amount);

```

```solidity
File: example/Tranche.sol

59:     function transfer(address to, uint256 value) public override restricted(_msgSender(), to, value) returns (bool) {

60:         return super.transfer(to, value);

```

</details> 
 


 ### <a name="L-9"></a>[L-9] Some tokens may revert when large transfers are made
Tokens such as COMP or UNI will revert when an address balance reaches type(uint96).max. Ensure that the calls below can be broken up into smaller batches if necessary.  

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

15: function transfer(address _to, uint256 _value) public returns (bool success) {

```

```solidity
File: example/Gateway.sol

192:     function transfer(uint128 token, address sender, bytes32 receiver, uint128 amount)

```

```solidity
File: example/LiquidityPool.sol

301:     function transfer(address, uint256) public returns (bool) {

```

```solidity
File: example/PoolManager.sol

28:     function transfer(uint128 currency, address sender, bytes32 recipient, uint128 amount) external;

136:     function transfer(address currencyAddress, bytes32 recipient, uint128 amount) public {

141:         gateway.transfer(currency, msg.sender, recipient, amount);

```

```solidity
File: example/Tranche.sol

59:     function transfer(address to, uint256 value) public override restricted(_msgSender(), to, value) returns (bool) {

60:         return super.transfer(to, value);

```

</details> 
 


 ### <a name="L-10"></a>[L-10] Unsafe ERC20 operation(s)

*Instances (11)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

167:         lPool.transferFrom(user, address(escrow), _trancheTokenAmount);

313:             LiquidityPoolLike(liquidityPool).transferFrom(address(escrow), user, trancheTokenPayout),

475:             lPool.transferFrom(address(escrow), user, trancheTokenAmount),

```

```solidity
File: example/PoolManager.sol

141:         gateway.transfer(currency, msg.sender, recipient, amount);

257:         EscrowLike(escrow).approve(currencyAddress, investmentManager.userEscrow(), type(uint256).max);

260:         EscrowLike(escrow).approve(currencyAddress, address(investmentManager), type(uint256).max);

269:         EscrowLike(escrow).approve(currencyAddress, address(this), amount);

336:         EscrowLike(escrow).approve(liquidityPool, address(investmentManager), type(uint256).max); // Approve investment manager on tranche token for coordinating transfers

337:         EscrowLike(escrow).approve(liquidityPool, liquidityPool, type(uint256).max); // Approve liquidityPool on tranche token to be able to burn

```

```solidity
File: example/Tranche.sol

60:         return super.transfer(to, value);

69:         return super.transferFrom(from, to, value);

```

</details> 
 


## Non Critical Issues


 ### <a name="NC-1"></a>[NC-1] assert() should be replaced with require() or revert()
In versions of Solidity prior to 0.8.0, when encountering an assert all the remaining gas will be consumed. Even after Solidity 0.8.0, the assert function is still not recommended, as described in the [documentation:](https://docs.soliditylang.org/en/v0.8.20/control-structures.html#panic-via-assert-and-error-via-require)

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/PoolManager.sol

130:         assert(gateway != GatewayLike(0) && investmentManager != InvestmentManagerLike(0));

```

</details> 
 


 ### <a name="NC-2"></a>[NC-2] Variables without visibility specifier

#### Impact:
Specifying visibility for variables can improve code readability and maintainability.

*Instances (18)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

10:     uint32 h;

11:     uint add;

```

```solidity
File: example/Factory.sol

65:         uint8 v;

```

```solidity
File: example/InvestmentManager.sol

60:     uint128 maxDeposit; // denominated in currency

61:     uint128 maxMint; // denominated in tranche tokens

62:     uint128 maxWithdraw; // denominated in currency

63:     uint128 maxRedeem; // denominated in tranche tokens

```

```solidity
File: example/PoolManager.sol

57:     uint64 poolId;

58:     uint256 createdAt;

67:     address token;

68:     uint64 poolId;

71:     uint8 decimals;

72:     uint256 createdAt;

73:     string tokenName;

74:     string tokenSymbol;

```

```solidity
File: example/UserEscrow.sol

21:         string name;

22:         string symbol;

75:         uint8 v;

```

</details> 
 


 ### <a name="NC-3"></a>[NC-3] Constants in comparisons should appear on the left side

#### Impact:
Placing constants on the left side of comparisons can improve code readability and prevent accidental assignment. Doing so will prevent typo [bugs](https://www.moserware.com/2008/01/constants-on-left-are-better-but-this.html)

*Instances (31)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

73:         if (v < 27) {

```

```solidity
File: example/Gateway.sol

131:         if (what == "poolManager") poolManager = PoolManagerLike(data);

132:         else if (what == "investmentManager") investmentManager = InvestmentManagerLike(data);

```

```solidity
File: example/InvestmentManager.sol

104:         if (what == "gateway") gateway = GatewayLike(data);

105:         else if (what == "poolManager") poolManager = PoolManagerLike(data);

127:         if (_currencyAmount == 0) {

159:         if (_trancheTokenAmount == 0) {

377:         if (depositPrice == 0) return 0;

390:         if (depositPrice == 0) return 0;

403:         if (redeemPrice == 0) return 0;

416:         if (redeemPrice == 0) return 0;

553:         if (lpValues.maxMint == 0) {

562:         if (lpValues.maxRedeem == 0) {

623:         if (lpValues.maxDeposit < _currency) {

628:         if (lpValues.maxMint < trancheTokens) {

639:         if (lpValues.maxWithdraw < _currency) {

644:         if (lpValues.maxRedeem < trancheTokens) {

667:         if (_value > type(uint128).max) {

681:         if (PRICE_DECIMALS == decimals) return uint256(_value);

691:         if (PRICE_DECIMALS == decimals) return _toUint128(_value);

```

```solidity
File: example/LiquidityPool.sol

104:         if (what == "investmentManager") investmentManager = InvestmentManagerLike(data);

```

```solidity
File: example/Messages.sol

849:             if (i < temp.length) {

878:         if (tempEmptyStringTest.length == 0) {

```

```solidity
File: example/PoolManager.sol

126:         if (what == "gateway") gateway = GatewayLike(data);

127:         else if (what == "investmentManager") investmentManager = InvestmentManagerLike(data);

```

```solidity
File: example/RestrictionManager.sol

37:         if (restrictionCode == DESTINATION_NOT_A_MEMBER_RESTRICTION_CODE) {

50:         if (members[user] >= block.timestamp) {

```

```solidity
File: example/Root.sol

44:         if (what == "delay") {

```

```solidity
File: example/Router.sol

63:         if (what == "gateway") {

```

```solidity
File: example/Tranche.sol

43:         if (what == "restrictionManager") restrictionManager = ERC1404Like(data);

```

```solidity
File: example/UserEscrow.sol

83:         if (v < 27) {

```

</details> 
 


 ### <a name="NC-4"></a>[NC-4] Contract declarations should have NatSpec @author annotations

#### Impact:
Adding a NatSpec @author annotation to contract declarations can improve code documentation.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

7: contract Auth {

```

```solidity
File: example/Context.sol

12: abstract contract Context {

```

```solidity
File: example/ERC20.sol

5: contract ERC20{

```

</details> 
 


 ### <a name="NC-5"></a>[NC-5] Contract declarations should have NatSpec @Title annotations

#### Impact:
Adding a NatSpec @Title annotation to contract declarations can improve code documentation.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

7: contract Auth {

```

```solidity
File: example/Context.sol

12: abstract contract Context {

```

```solidity
File: example/ERC20.sol

5: contract ERC20{

```

</details> 
 


 ### <a name="NC-6"></a>[NC-6] Consider using delete rather than assigning zero to clear value

#### Impact:
Consider using delete rather than assigning zero to clear values. The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*Instances (15)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

16:    for (uint i = 0; i < jhh.length; i++) {

```

```solidity
File: example/Factory.sol

47:         for (uint256 i = 0; i < wards.length; i++) {

130:         for (uint256 i = 0; i < trancheTokenWards.length; i++) {

144:         for (uint256 i = 0; i < restrictionManagerWards.length; i++) {

```

```solidity
File: example/InvestmentManager.sol

624:             lpValues.maxDeposit = 0;

629:             lpValues.maxMint = 0;

640:             lpValues.maxWithdraw = 0;

645:             lpValues.maxRedeem = 0;

```

```solidity
File: example/Messages.sol

848:         for (uint256 i = 0; i < 128; i++) {

862:         uint8 i = 0;

869:         for (uint8 j = 0; j < i; j++) {

888:         uint8 i = 0;

893:         for (i = 0; i < 32 && _bytes32[i] != 0; i++) {

```

```solidity
File: example/RestrictionManager.sol

15:     uint8 public constant SUCCESS_CODE = 0;

64:         for (uint256 i = 0; i < userLength; i++) {

```

</details> 
 


 ### <a name="NC-7"></a>[NC-7] Consider using delete rather than assigning false to clear value

#### Impact:
Consider using delete rather than assigning alse to clear values. The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Root.sol

23:     bool public paused = false;

60:         paused = false;

```

</details> 
 


 ### <a name="NC-8"></a>[NC-8] Consider adding a block/deny-list"
Doing so will significantly increase centralization, but will help to prevent hackers from using stolen tokens  

*Instances (17)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

7: contract Auth {

```

```solidity
File: example/Context.sol

12: abstract contract Context {

```

```solidity
File: example/DelayedAdmin.sol

12: contract DelayedAdmin is Auth {

```

```solidity
File: example/ERC20.sol

5: contract ERC20{

```

```solidity
File: example/Escrow.sol

14: contract Escrow is Auth {

```

```solidity
File: example/Factory.sol

26: contract LiquidityPoolFactory is Auth {

98: contract TrancheTokenFactory is Auth {

```

```solidity
File: example/Gateway.sol

84: contract Gateway is Auth {

```

```solidity
File: example/InvestmentManager.sol

69: contract InvestmentManager is Auth {

```

```solidity
File: example/LiquidityPool.sol

52: contract LiquidityPool is Auth, IERC4626 {

```

```solidity
File: example/PauseAdmin.sol

10: contract PauseAdmin is Auth {

```

```solidity
File: example/PoolManager.sol

83: contract PoolManager is Auth {

```

```solidity
File: example/RestrictionManager.sol

14: contract RestrictionManager is Auth {

```

```solidity
File: example/Root.sol

15: contract Root is Auth {

```

```solidity
File: example/Router.sol

24: contract AxelarRouter is Auth {

```

```solidity
File: example/Tranche.sol

23: contract TrancheToken is ERC20, ERC1404Like {

```

```solidity
File: example/UserEscrow.sol

15: contract UserEscrow is Auth {

```

</details> 
 


 ### <a name="NC-9"></a>[NC-9] Events are missing sender information

#### Impact:
Including msg.sender in events triggered by user actions can make events more useful for end users.

*Instances (56)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

16:         emit Rely(user);

22:         emit Deny(user);

```

```solidity
File: example/DelayedAdmin.sol

22:         emit Rely(msg.sender);

```

```solidity
File: example/ERC20.sol

17:     emit transfeer(msg.sender, _to, _value);

```

```solidity
File: example/Escrow.sol

19:         emit Rely(msg.sender);

25:         emit Approve(token, spender, value);

```

```solidity
File: example/Factory.sol

33:         emit Rely(msg.sender);

105:         emit Rely(msg.sender);

```

```solidity
File: example/Gateway.sol

106:         emit Rely(msg.sender);

134:         emit File(what, data);

139:         emit AddIncomingRouter(router);

144:         emit RemoveIncomingRouter(router);

149:         emit UpdateOutgoingRouter(router);

```

```solidity
File: example/InvestmentManager.sol

93:         emit Rely(msg.sender);

107:         emit File(what, data);

479:         emit DepositProcessed(liquidityPool, user, currencyAmount);

547:         emit RedemptionProcessed(liquidityPool, user, trancheTokenAmount);

```

```solidity
File: example/LiquidityPool.sol

93:         emit Rely(msg.sender);

106:         emit File(what, data);

216:         emit DepositRequested(owner, assets);

225:         emit DepositRequested(owner, assets);

233:         emit RedeemRequested(owner, shares);

242:         emit RedeemRequested(owner, shares);

261:         emit DepositCollected(receiver);

267:         emit RedeemCollected(receiver);

327:         emit UpdatePrice(price);

```

```solidity
File: example/PauseAdmin.sol

25:         emit Rely(msg.sender);

36:         emit AddPauser(user);

41:         emit RemovePauser(user);

```

```solidity
File: example/PoolManager.sol

115:         emit Rely(msg.sender);

129:         emit File(what, data);

181:         emit PoolAdded(poolId);

195:         emit PoolCurrencyAllowed(currency, poolId);

219:         emit TrancheAdded(poolId, trancheId);

262:         emit CurrencyAdded(currency, currencyAddress);

311:         emit TrancheTokenDeployed(poolId, trancheId);

339:         emit LiquidityPoolDeployed(poolId, trancheId, liquidityPool);

```

```solidity
File: example/RestrictionManager.sol

24:         emit Rely(msg.sender);

```

```solidity
File: example/Root.sol

39:         emit Rely(msg.sender);

50:         emit File(what, data);

56:         emit Pause();

61:         emit Unpause();

67:         emit RelyScheduled(target, schedule[target]);

72:         emit RelyCancelled(target);

80:         emit Rely(target);

92:         emit RelyContract(target, user);

100:         emit DenyContract(target, user);

```

```solidity
File: example/Router.sol

40:         emit Rely(msg.sender);

69:         emit File(what, data);

```

```solidity
File: example/Tranche.sol

45:         emit File(what, data);

50:         emit AddLiquidityPool(liquidityPool);

55:         emit RemoveLiquidityPool(liquidityPool);

```

```solidity
File: example/UserEscrow.sol

33:         emit Rely(msg.sender);

42:         emit TransferIn(token, source, destination, amount);

58:         emit TransferOut(token, receiver, amount);

67:         emit Rely(msg.sender);

```

</details> 
 


 ### <a name="NC-10"></a>[NC-10] Events should use parameters to convey information

#### Impact:
Using parameters in events can provide additional information to subscribers about the event occurrence.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Root.sol

56:         emit Pause();

61:         emit Unpause();

```

</details> 
 


 ### <a name="NC-11"></a>[NC-11] If-statement can be converted to a ternary

#### Impact:
The code can be made more compact while also increasing readability by converting the following `if`-statements to ternaries (e.g. `foo += (x > y) ? a : b`)

*Instances (36)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

73:         if (v < 27) {

```

```solidity
File: example/Gateway.sol

286:         if (Messages.isAddCurrency(message)) {

289:         } else if (Messages.isAddPool(message)) {

292:         } else if (Messages.isAllowPoolCurrency(message)) {

295:         } else if (Messages.isAddTranche(message)) {

305:         } else if (Messages.isUpdateMember(message)) {

308:         } else if (Messages.isUpdateTrancheTokenPrice(message)) {

312:         } else if (Messages.isTransfer(message)) {

315:         } else if (Messages.isTransferTrancheTokens(message)) {

319:         } else if (Messages.isExecutedDecreaseInvestOrder(message)) {

323:         } else if (Messages.isExecutedDecreaseRedeemOrder(message)) {

329:         } else if (Messages.isExecutedCollectInvest(message)) {

341:         } else if (Messages.isExecutedCollectRedeem(message)) {

353:         } else if (Messages.isScheduleUpgrade(message)) {

356:         } else if (Messages.isCancelUpgrade(message)) {

359:         } else if (Messages.isUpdateTrancheTokenMetadata(message)) {

```

```solidity
File: example/InvestmentManager.sol

127:         if (_currencyAmount == 0) {

159:         if (_trancheTokenAmount == 0) {

553:         if (lpValues.maxMint == 0) {

562:         if (lpValues.maxRedeem == 0) {

623:         if (lpValues.maxDeposit < _currency) {

628:         if (lpValues.maxMint < trancheTokens) {

639:         if (lpValues.maxWithdraw < _currency) {

644:         if (lpValues.maxRedeem < trancheTokens) {

667:         if (_value > type(uint128).max) {

```

```solidity
File: example/LiquidityPool.sol

339:         if (!success) {

```

```solidity
File: example/Messages.sol

849:             if (i < temp.length) {

878:         if (tempEmptyStringTest.length == 0) {

```

```solidity
File: example/RestrictionManager.sol

29:         if (!hasMember(to)) {

37:         if (restrictionCode == DESTINATION_NOT_A_MEMBER_RESTRICTION_CODE) {

50:         if (members[user] >= block.timestamp) {

```

```solidity
File: example/Root.sol

44:         if (what == "delay") {

```

```solidity
File: example/Router.sol

63:         if (what == "gateway") {

```

```solidity
File: example/Tranche.sol

104:         if (isTrustedForwarder(msg.sender) && msg.data.length >= 20) {

110:         } else {

```

```solidity
File: example/UserEscrow.sol

83:         if (v < 27) {

```

</details> 
 


 ### <a name="NC-12"></a>[NC-12] Variable names for immutables should use CONSTANT_CASE

#### Impact:
Using CONSTANT_CASE for immutables improves code readability and maintainability.

*Instances (16)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DelayedAdmin.sol

13:     Root public immutable root;

```

```solidity
File: example/Factory.sol

27:     address immutable root;

99:     address immutable root;

```

```solidity
File: example/Gateway.sol

85:     RootLike public immutable root;

```

```solidity
File: example/InvestmentManager.sol

75:     EscrowLike public immutable escrow;

76:     UserEscrowLike public immutable userEscrow;

```

```solidity
File: example/LiquidityPool.sol

55:     uint64 public immutable poolId;

56:     bytes16 public immutable trancheId;

62:     address public immutable asset;

67:     TrancheTokenLike public immutable share;

```

```solidity
File: example/PauseAdmin.sol

11:     Root public immutable root;

```

```solidity
File: example/PoolManager.sol

86:     EscrowLike public immutable escrow;

87:     LiquidityPoolFactoryLike public immutable liquidityPoolFactory;

88:     TrancheTokenFactoryLike public immutable trancheTokenFactory;

```

```solidity
File: example/Root.sol

19:     address public immutable escrow;

```

```solidity
File: example/Router.sol

29:     AxelarGatewayLike public immutable axelarGateway;

```

</details> 
 


 ### <a name="NC-13"></a>[NC-13] Contract should expose an interface

#### Impact:
The contracts should expose an interface so that other projects can more easily integrate with it, without having to develop their own non-standard variants.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

7: contract Auth {

```

```solidity
File: example/Context.sol

12: abstract contract Context {

```

```solidity
File: example/ERC20.sol

5: contract ERC20{

```

</details> 
 


 ### <a name="NC-14"></a>[NC-14] Consider using named mappings

#### Impact:
Using named mappings can improve code readability and maintainability.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/PoolManager.sol

60:     mapping(address => bool) allowedCurrencies;

77:     mapping(address => address) liquidityPools; // currency -> liquidity pool address

```

```solidity
File: example/UserEscrow.sol

17:     mapping(address => mapping(address => uint256)) destinations;

```

</details> 
 


 ### <a name="NC-15"></a>[NC-15] Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct

#### Impact:
Combining multiple mappings into a single mapping with a struct can improve readability and maintainability of the code.

*Instances (11)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

8:     mapping(address => uint256) public wards;

```

```solidity
File: example/Gateway.sol

89:     mapping(address => bool) public incomingRouters;

```

```solidity
File: example/InvestmentManager.sol

81:     mapping(address => mapping(address => LPValues)) public orderbook;

```

```solidity
File: example/PauseAdmin.sol

13:     mapping(address => uint256) public pausers;

```

```solidity
File: example/PoolManager.sol

60:     mapping(address => bool) allowedCurrencies;

77:     mapping(address => address) liquidityPools; // currency -> liquidity pool address

97:     mapping(address => uint128) public currencyAddressToId;

```

```solidity
File: example/RestrictionManager.sol

20:     mapping(address => uint256) public members;

```

```solidity
File: example/Root.sol

21:     mapping(address => uint256) public schedule;

```

```solidity
File: example/Tranche.sol

26:     mapping(address => bool) public liquidityPools;

```

```solidity
File: example/UserEscrow.sol

17:     mapping(address => mapping(address => uint256)) destinations;

```

</details> 
 


 ### <a name="NC-16"></a>[NC-16] Use of override is unnecessary

#### Impact:
Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the override keyword when the function solely overrides an interface function, and the function doesnt exist in multiple base contracts, is unnecessary.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Tranche.sol

59:     function transfer(address to, uint256 value) public override restricted(_msgSender(), to, value) returns (bool) {

65:         override

72:     function mint(address to, uint256 value) public override restricted(_msgSender(), to, value) {

103:     function _msgSender() internal view virtual override returns (address sender) {

```

</details> 
 


 ### <a name="NC-17"></a>[NC-17] Consider using descriptive constants when passing zero as a function argument

#### Impact:
Passing zero as a function argument/Event emission can sometimes result in a security issue (e.g. passing zero as the slippage parameter). Consider using a constant variable with a descriptive name, so its clear that the 0 is intentionally being used, and for the right reasons.

*Instances (22)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

242:         require(currencyPayout != 0, "InvestmentManager/zero-invest");

263:         require(trancheTokensPayout != 0, "InvestmentManager/zero-redeem");

284:         require(currencyPayout != 0, "InvestmentManager/zero-payout");

301:         require(trancheTokenPayout != 0, "InvestmentManager/zero-payout");

436:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

460:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

502:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

528:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

579:         depositPrice = currencyAmountInPriceDecimals.mulDiv(

598:         uint256 currencyAmountInPriceDecimals = _toPriceDecimals(currencyAmount, currencyDecimals, liquidityPool).mulDiv(

614:         ).mulDiv(price, 10 ** PRICE_DECIMALS, MathLib.Rounding.Down);

```

```solidity
File: example/PoolManager.sol

138:         require(currency != 0, "PoolManager/unknown-currency");

178:         require(pool.createdAt == 0, "PoolManager/pool-already-added");

189:         require(pool.createdAt != 0, "PoolManager/invalid-pool");

208:         require(pool.createdAt != 0, "PoolManager/invalid-pool");

210:         require(tranche.createdAt == 0, "PoolManager/tranche-already-exists");

248:         require(currency != 0, "PoolManager/currency-id-has-to-be-greater-than-0");

250:         require(currencyAddressToId[currencyAddress] == 0, "PoolManager/currency-address-in-use");

291:         require(tranche.createdAt != 0, "PoolManager/tranche-not-added");

322:         require(pools[poolId].createdAt != 0, "PoolManager/pool-does-not-exist");

355:         require(currency != 0, "PoolManager/unknown-currency"); // Currency index on the Centrifuge side should start at 1

```

```solidity
File: example/Root.sol

76:         require(schedule[target] != 0, "Root/target-not-scheduled");

```

</details> 
 


 ### <a name="NC-18"></a>[NC-18] Non-external/public variable names should begin with an underscore

#### Impact:
Using an underscore at the beginning of non-external/public variable names can improve code clarity and maintainability. According to the Solidity Style Guide, non-external/public variable names should begin with an [underscore](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables)

*Instances (24)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

8:     mapping(address => uint256) public wards;

```

```solidity
File: example/Factory.sol

50:              uint public j;

```

```solidity
File: example/Gateway.sol

86:     InvestmentManagerLike public investmentManager;

87:     PoolManagerLike public poolManager;

89:     mapping(address => bool) public incomingRouters;

90:     RouterLike public outgoingRouter;

```

```solidity
File: example/InvestmentManager.sol

78:     GatewayLike public gateway;

79:     PoolManagerLike public poolManager;

81:     mapping(address => mapping(address => LPValues)) public orderbook;

```

```solidity
File: example/LiquidityPool.sol

69:     InvestmentManagerLike public investmentManager;

72:     uint128 public latestPrice;

75:     uint256 public lastPriceUpdate;

```

```solidity
File: example/PauseAdmin.sol

13:     mapping(address => uint256) public pausers;

```

```solidity
File: example/PoolManager.sol

90:     GatewayLike public gateway;

91:     InvestmentManagerLike public investmentManager;

93:     mapping(uint64 => Pool) public pools;

96:     mapping(uint128 => address) public currencyIdToAddress;

97:     mapping(address => uint128) public currencyAddressToId;

```

```solidity
File: example/RestrictionManager.sol

20:     mapping(address => uint256) public members;

```

```solidity
File: example/Root.sol

21:     mapping(address => uint256) public schedule;

22:     uint256 public delay;

```

```solidity
File: example/Router.sol

31:     GatewayLike public gateway;

```

```solidity
File: example/Tranche.sol

24:     ERC1404Like public restrictionManager;

26:     mapping(address => bool) public liquidityPools;

```

</details> 
 


 ### <a name="NC-19"></a>[NC-19] Return values of `approve()` not checked
Not all IERC20 implementations `revert()` when there's a failure in `approve()`. The function signature has a boolean return value and they indicate errors that way instead. By not checking the return value, operations that should have marked as failed, may potentially go through without actually approving anything

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/PoolManager.sol

269:         EscrowLike(escrow).approve(currencyAddress, address(this), amount);

336:         EscrowLike(escrow).approve(liquidityPool, address(investmentManager), type(uint256).max); // Approve investment manager on tranche token for coordinating transfers

337:         EscrowLike(escrow).approve(liquidityPool, liquidityPool, type(uint256).max); // Approve liquidityPool on tranche token to be able to burn

```

</details> 
 


 ### <a name="NC-20"></a>[NC-20] Use the latest solidity version for deployment  
Upgrading to a newer Solidity release can optimize gas usage, take advantage of new features and improve overall contract efficiency. Where possible, based on compatibility requirements, it is recommended to use newer/latest solidity version to take advantage of the latest optimizations and features.

*Instances (18)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

3: pragma solidity 0.8.21;

```

```solidity
File: example/Context.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/DelayedAdmin.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/ERC20.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Escrow.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Factory.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Gateway.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/InvestmentManager.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/LiquidityPool.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Messages.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/PauseAdmin.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/PoolManager.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/RestrictionManager.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Root.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Router.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/SafeTransferLib.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Tranche.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/UserEscrow.sol

2: pragma solidity 0.8.21;

```

</details> 
 


 ### <a name="NC-21"></a>[NC-21] Constants should be defined rather than using magic numbers

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Tranche.sol

108:                 sender := shr(96, calldataload(sub(calldatasize(), 20)))

```

</details> 
 


 ### <a name="NC-22"></a>[NC-22] Consider moving msg.sender checks to modifiers
If some functions are only allowed to be called by some specific users, consider using a modifier instead of checking with a require statement, especially if this check is done in multiple functions.  

*Instances (65)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

27:         require(wards[msg.sender] == 1, "Auth/not-authorized");

```

```solidity
File: example/Context.sol

14:         return msg.sender;

```

```solidity
File: example/DelayedAdmin.sol

21:         wards[msg.sender] = 1;

22:         emit Rely(msg.sender);

```

```solidity
File: example/ERC20.sol

17:     emit transfeer(msg.sender, _to, _value);

```

```solidity
File: example/Escrow.sol

18:         wards[msg.sender] = 1;

19:         emit Rely(msg.sender);

```

```solidity
File: example/Factory.sol

32:         wards[msg.sender] = 1;

33:         emit Rely(msg.sender);

104:         wards[msg.sender] = 1;

105:         emit Rely(msg.sender);

```

```solidity
File: example/Gateway.sol

105:         wards[msg.sender] = 1;

106:         emit Rely(msg.sender);

110:         require(msg.sender == address(investmentManager), "Gateway/only-investment-manager-allowed-to-call");

115:         require(msg.sender == address(poolManager), "Gateway/only-pool-manager-allowed-to-call");

120:         require(incomingRouters[msg.sender], "Gateway/only-router-allowed-to-call");

```

```solidity
File: example/InvestmentManager.sol

92:         wards[msg.sender] = 1;

93:         emit Rely(msg.sender);

98:         require(msg.sender == address(gateway), "InvestmentManager/not-the-gateway");

118:         address liquidityPool = msg.sender;

149:         address liquidityPool = msg.sender;

176:         LiquidityPoolLike liquidityPool = LiquidityPoolLike(msg.sender);

189:         LiquidityPoolLike liquidityPool = LiquidityPoolLike(msg.sender);

201:         LiquidityPoolLike liquidityPool = LiquidityPoolLike(msg.sender);

212:         LiquidityPoolLike liquidityPool = LiquidityPoolLike(msg.sender);

428:         address liquidityPool = msg.sender;

452:         address liquidityPool = msg.sender;

473:         require(lPool.checkTransferRestriction(msg.sender, user, 0), "InvestmentManager/trancheTokens-not-a-member");

494:         address liquidityPool = msg.sender;

520:         address liquidityPool = msg.sender;

```

```solidity
File: example/LiquidityPool.sol

92:         wards[msg.sender] = 1;

93:         emit Rely(msg.sender);

98:         require(msg.sender == owner, "LiquidityPool/no-approval");

136:         shares = investmentManager.previewDeposit(msg.sender, address(this), assets);

161:         assets = investmentManager.previewMint(msg.sender, address(this), shares);

171:         shares = investmentManager.previewWithdraw(msg.sender, address(this), assets);

193:         assets = investmentManager.previewRedeem(msg.sender, address(this), shares);

296:         (bool success, bytes memory data) = address(share).call(bytes.concat(msg.data, bytes20(msg.sender)));

302:         (bool success, bytes memory data) = address(share).call(bytes.concat(msg.data, bytes20(msg.sender)));

308:         (bool success, bytes memory data) = address(share).call(bytes.concat(msg.data, bytes20(msg.sender)));

```

```solidity
File: example/PauseAdmin.sol

24:         wards[msg.sender] = 1;

25:         emit Rely(msg.sender);

29:         require(pausers[msg.sender] == 1, "PauseAdmin/not-authorized-to-pause");

```

```solidity
File: example/PoolManager.sol

114:         wards[msg.sender] = 1;

115:         emit Rely(msg.sender);

120:         require(msg.sender == address(gateway), "PoolManager/not-the-gateway");

140:         SafeTransferLib.safeTransferFrom(currencyAddress, msg.sender, address(escrow), amount);

141:         gateway.transfer(currency, msg.sender, recipient, amount);

153:         trancheToken.burn(msg.sender, amount);

154:         gateway.transferTrancheTokensToCentrifuge(poolId, trancheId, msg.sender, destinationAddress, amount);

167:         trancheToken.burn(msg.sender, amount);

169:             poolId, trancheId, msg.sender, destinationChainId, destinationAddress, amount

```

```solidity
File: example/RestrictionManager.sol

23:         wards[msg.sender] = 1;

24:         emit Rely(msg.sender);

```

```solidity
File: example/Root.sol

38:         wards[msg.sender] = 1;

39:         emit Rely(msg.sender);

```

```solidity
File: example/Router.sol

39:         wards[msg.sender] = 1;

40:         emit Rely(msg.sender);

44:         require(msg.sender == address(axelarGateway), "AxelarRouter/invalid-origin");

57:         require(msg.sender == address(gateway), "AxelarRouter/only-gateway-allowed-to-call");

```

```solidity
File: example/Tranche.sol

104:         if (isTrustedForwarder(msg.sender) && msg.data.length >= 20) {

```

```solidity
File: example/UserEscrow.sol

32:         wards[msg.sender] = 1;

33:         emit Rely(msg.sender);

66:         wards[msg.sender] = 1;

67:         emit Rely(msg.sender);

```

</details> 
 


 ### <a name="NC-23"></a>[NC-23] Owner can renounce while system is paused
The contract owner or single user with a role is not prevented from renouncing the role/ownership while the contract is paused, which would cause any user assets stored in the protocol, to be locked indefinitely.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DelayedAdmin.sol

26:     function pause() public auth {

```

```solidity
File: example/PauseAdmin.sol

45:     function pause() public canPause {

```

```solidity
File: example/Root.sol

54:     function pause() external auth {

```

</details> 
 


 ### <a name="NC-24"></a>[NC-24] Array indices should be referenced via enums rather than numeric literals

#### Impact:
Referencing array indices via enums can improve code readability and maintainability.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/PoolManager.sol

294:         trancheTokenWards[0] = address(investmentManager);

295:         trancheTokenWards[1] = address(this);

298:         memberlistWards[0] = address(this);

325:         liquidityPoolWards[0] = address(investmentManager);

```

</details> 
 


## Gas Optimizations


 ### <a name="GAS-1"></a>[GAS-1] Use scientific notation (e.g. 1e18) rather than exponentiation (e.g. 10**18)
While the compiler knows to optimize away the exponentiation, its still better coding practice to use idioms that do not require compiler optimization, if they exist.

*Instances (11)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

6:       uint256 private constant ONE = 10** 27;

7:         uint256 private constant OmNE = 10 **27;

```

```solidity
File: example/InvestmentManager.sol

330:             10 ** (PRICE_DECIMALS + trancheTokenDecimals - currencyDecimals),

344:             10 ** (PRICE_DECIMALS + trancheTokenDecimals - currencyDecimals),

580:             10 ** PRICE_DECIMALS, trancheTokenAmountInPriceDecimals, MathLib.Rounding.Down

599:             10 ** PRICE_DECIMALS, price, MathLib.Rounding.Down

614:         ).mulDiv(price, 10 ** PRICE_DECIMALS, MathLib.Rounding.Down);

682:         value = uint256(_value) * 10 ** (PRICE_DECIMALS - decimals);

692:         value = _toUint128(_value / 10 ** (PRICE_DECIMALS - decimals));

```

```solidity
File: example/PoolManager.sol

51:       uint256 private constant ONE = 10**27;

131:        uint256 private constant ONE = 10 ** 27;

```

</details> 
 


 ### <a name="GAS-2"></a>[GAS-2] Nesting if-statements is cheaper than using &&
Nesting if-statements avoids the stack operations of setting up and using an extra jumpdest, and saves 6 [gas](https://gist.github.com/IllIllI000/7f3b818abecfadbef93b894481ae7d19)

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

431:             (_currencyAmount <= orderbook[user][liquidityPool].maxDeposit && _currencyAmount != 0),

455:             (_trancheTokenAmount <= orderbook[user][liquidityPool].maxMint && _trancheTokenAmount != 0),

497:             (_trancheTokenAmount <= orderbook[user][liquidityPool].maxRedeem && _trancheTokenAmount != 0),

523:             (_currencyAmount <= orderbook[user][liquidityPool].maxWithdraw && _currencyAmount != 0),

```

```solidity
File: example/Messages.sol

863:         while (i < 128 && _bytes128[i] != 0) {

889:         while (i < 32 && _bytes32[i] != 0) {

893:         for (i = 0; i < 32 && _bytes32[i] != 0; i++) {

```

```solidity
File: example/PoolManager.sol

130:         assert(gateway != GatewayLike(0) && investmentManager != InvestmentManagerLike(0));

```

```solidity
File: example/SafeTransferLib.sol

18:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-from-failed");

28:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-failed");

38:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-approve-failed");

```

```solidity
File: example/Tranche.sol

104:         if (isTrustedForwarder(msg.sender) && msg.data.length >= 20) {

```

</details> 
 


 ### <a name="GAS-3"></a>[GAS-3] Consider using = instead of += and -= for gas efficiency
Using = instead of += and -= can save gas in certain scenarios. Consider using = when appropriate.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

74:             v += 27;

```

```solidity
File: example/UserEscrow.sol

84:             v += 27;

```

</details> 
 


 ### <a name="GAS-4"></a>[GAS-4] Use >= instead of > for gas efficiency
Using >= costs less gas than >. Consider using >= when appropriate.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

667:         if (_value > type(uint128).max) {

```

</details> 
 


 ### <a name="GAS-5"></a>[GAS-5] Dont use _msgSender() if not supporting EIP-2771
Use msg.sender if the code does not implement EIP-2771 trusted forwarder support

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Context.sol

13:     function _msgSender() internal view virtual returns (address) {

```

```solidity
File: example/Tranche.sol

59:     function transfer(address to, uint256 value) public override restricted(_msgSender(), to, value) returns (bool) {

72:     function mint(address to, uint256 value) public override restricted(_msgSender(), to, value) {

103:     function _msgSender() internal view virtual override returns (address sender) {

111:             return super._msgSender();

```

</details> 
 


 ### <a name="GAS-6"></a>[GAS-6] <array>.length should not be looked up in every loop of a for-loop
The overheads outlined below are PER LOOP, excluding the first loop. Storage arrays incur a Gwarmaccess (100 gas), memory arrays use MLOAD (3 gas), calldata arrays use CALLDATALOAD (3 gas). Caching the length changes each of these to a DUP<N> (3 gas), and gets rid of the extra DUP<N> needed to store the stack offset.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

16:    for (uint i = 0; i < jhh.length; i++) {

```

```solidity
File: example/Factory.sol

47:         for (uint256 i = 0; i < wards.length; i++) {

130:         for (uint256 i = 0; i < trancheTokenWards.length; i++) {

144:         for (uint256 i = 0; i < restrictionManagerWards.length; i++) {

```

</details> 
 


 ### <a name="GAS-7"></a>[GAS-7] Use assembly to emit events, in order to save gas
Using the [scratch space](https://github.com/Vectorized/solady/blob/30558f5402f02351b96eeb6eaf32bcea29773841/src/tokens/ERC1155.sol#L501-L504) for event arguments (two words or fewer) will save gas over needing Soliditys full abi memory expansion used for emitting normally.

*Instances (60)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

16:         emit Rely(user);

22:         emit Deny(user);

```

```solidity
File: example/DelayedAdmin.sol

22:         emit Rely(msg.sender);

```

```solidity
File: example/ERC20.sol

17:     emit transfeer(msg.sender, _to, _value);

```

```solidity
File: example/Escrow.sol

19:         emit Rely(msg.sender);

25:         emit Approve(token, spender, value);

```

```solidity
File: example/Factory.sol

33:         emit Rely(msg.sender);

105:         emit Rely(msg.sender);

```

```solidity
File: example/Gateway.sol

106:         emit Rely(msg.sender);

134:         emit File(what, data);

139:         emit AddIncomingRouter(router);

144:         emit RemoveIncomingRouter(router);

149:         emit UpdateOutgoingRouter(router);

```

```solidity
File: example/InvestmentManager.sol

93:         emit Rely(msg.sender);

107:         emit File(what, data);

479:         emit DepositProcessed(liquidityPool, user, currencyAmount);

547:         emit RedemptionProcessed(liquidityPool, user, trancheTokenAmount);

```

```solidity
File: example/LiquidityPool.sol

93:         emit Rely(msg.sender);

106:         emit File(what, data);

143:         emit Deposit(address(this), receiver, assets, shares);

151:         emit Deposit(address(this), receiver, assets, shares);

182:         emit Withdraw(address(this), receiver, owner, assets, sharesRedeemed);

206:         emit Withdraw(address(this), receiver, owner, currencyPayout, shares);

216:         emit DepositRequested(owner, assets);

225:         emit DepositRequested(owner, assets);

233:         emit RedeemRequested(owner, shares);

242:         emit RedeemRequested(owner, shares);

261:         emit DepositCollected(receiver);

267:         emit RedeemCollected(receiver);

327:         emit UpdatePrice(price);

```

```solidity
File: example/PauseAdmin.sol

25:         emit Rely(msg.sender);

36:         emit AddPauser(user);

41:         emit RemovePauser(user);

```

```solidity
File: example/PoolManager.sol

115:         emit Rely(msg.sender);

129:         emit File(what, data);

181:         emit PoolAdded(poolId);

195:         emit PoolCurrencyAllowed(currency, poolId);

219:         emit TrancheAdded(poolId, trancheId);

262:         emit CurrencyAdded(currency, currencyAddress);

311:         emit TrancheTokenDeployed(poolId, trancheId);

339:         emit LiquidityPoolDeployed(poolId, trancheId, liquidityPool);

```

```solidity
File: example/RestrictionManager.sol

24:         emit Rely(msg.sender);

```

```solidity
File: example/Root.sol

39:         emit Rely(msg.sender);

50:         emit File(what, data);

56:         emit Pause();

61:         emit Unpause();

67:         emit RelyScheduled(target, schedule[target]);

72:         emit RelyCancelled(target);

80:         emit Rely(target);

92:         emit RelyContract(target, user);

100:         emit DenyContract(target, user);

```

```solidity
File: example/Router.sol

40:         emit Rely(msg.sender);

69:         emit File(what, data);

```

```solidity
File: example/Tranche.sol

45:         emit File(what, data);

50:         emit AddLiquidityPool(liquidityPool);

55:         emit RemoveLiquidityPool(liquidityPool);

```

```solidity
File: example/UserEscrow.sol

33:         emit Rely(msg.sender);

42:         emit TransferIn(token, source, destination, amount);

58:         emit TransferOut(token, receiver, amount);

67:         emit Rely(msg.sender);

```

</details> 
 


 ### <a name="GAS-8"></a>[GAS-8] Using bools for storage incurs overhead
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Gateway.sol

89:     mapping(address => bool) public incomingRouters;

```

```solidity
File: example/PoolManager.sol

60:     mapping(address => bool) allowedCurrencies;

```

```solidity
File: example/Root.sol

23:     bool public paused = false;

```

```solidity
File: example/Tranche.sol

26:     mapping(address => bool) public liquidityPools;

```

</details> 
 


 ### <a name="GAS-9"></a>[GAS-9] Cache array length outside of loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

16:    for (uint i = 0; i < jhh.length; i++) {

```

```solidity
File: example/Factory.sol

47:         for (uint256 i = 0; i < wards.length; i++) {

130:         for (uint256 i = 0; i < trancheTokenWards.length; i++) {

144:         for (uint256 i = 0; i < restrictionManagerWards.length; i++) {

```

</details> 
 


 ### <a name="GAS-10"></a>[GAS-10] Consider using assembly for simple zero checks to save gas
Using assembly for simple zero checks can save gas. Consider using assembly when appropriate.

*Instances (6)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

127:         if (_currencyAmount == 0) {

159:         if (_trancheTokenAmount == 0) {

377:         if (depositPrice == 0) return 0;

390:         if (depositPrice == 0) return 0;

403:         if (redeemPrice == 0) return 0;

416:         if (redeemPrice == 0) return 0;

```

</details> 
 


 ### <a name="GAS-11"></a>[GAS-11] Consider using constant rather than immutable to save gas

#### Impact:
Using constant variables instead of immutable can potentially save gas costs in some cases. You can see it [here](https://docs.soliditylang.org/en/v0.8.21/contracts.html#constant-and-immutable-state-variables)

*Instances (16)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DelayedAdmin.sol

13:     Root public immutable root;

```

```solidity
File: example/Factory.sol

27:     address immutable root;

99:     address immutable root;

```

```solidity
File: example/Gateway.sol

85:     RootLike public immutable root;

```

```solidity
File: example/InvestmentManager.sol

75:     EscrowLike public immutable escrow;

76:     UserEscrowLike public immutable userEscrow;

```

```solidity
File: example/LiquidityPool.sol

55:     uint64 public immutable poolId;

56:     bytes16 public immutable trancheId;

62:     address public immutable asset;

67:     TrancheTokenLike public immutable share;

```

```solidity
File: example/PauseAdmin.sol

11:     Root public immutable root;

```

```solidity
File: example/PoolManager.sol

86:     EscrowLike public immutable escrow;

87:     LiquidityPoolFactoryLike public immutable liquidityPoolFactory;

88:     TrancheTokenFactoryLike public immutable trancheTokenFactory;

```

```solidity
File: example/Root.sol

19:     address public immutable escrow;

```

```solidity
File: example/Router.sol

29:     AxelarGatewayLike public immutable axelarGateway;

```

</details> 
 


 ### <a name="GAS-12"></a>[GAS-12] Constructors can be marked payable
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn  t provided. A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

*Instances (14)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DelayedAdmin.sol

18:     constructor(address root_) {

```

```solidity
File: example/Escrow.sol

17:     constructor() {

```

```solidity
File: example/Factory.sol

29:     constructor(address _root) {

101:     constructor(address _root) {

```

```solidity
File: example/Gateway.sol

98:     constructor(address root_, address investmentManager_, address poolManager_, address router_) {

```

```solidity
File: example/InvestmentManager.sol

88:     constructor(address escrow_, address userEscrow_) {

```

```solidity
File: example/LiquidityPool.sol

85:     constructor(uint64 poolId_, bytes16 trancheId_, address asset_, address share_, address investmentManager_) {

```

```solidity
File: example/PauseAdmin.sol

21:     constructor(address root_) {

```

```solidity
File: example/PoolManager.sol

109:     constructor(address escrow_, address liquidityPoolFactory_, address trancheTokenFactory_) {

```

```solidity
File: example/RestrictionManager.sol

22:     constructor() {

```

```solidity
File: example/Root.sol

34:     constructor(address _escrow, uint256 _delay) {

```

```solidity
File: example/Router.sol

36:     constructor(address axelarGateway_) {

```

```solidity
File: example/Tranche.sol

33:     constructor(uint8 decimals_) ERC20(decimals_) {}

```

```solidity
File: example/UserEscrow.sol

31:     constructor() {

```

</details> 
 


 ### <a name="GAS-13"></a>[GAS-13] Use Custom Errors
[Source](https://blog.soliditylang.org/2021/04/21/custom-errors/)
Instead of using error strings, to reduce deployment and runtime cost, you should use Custom Errors. This would save both deployment and runtime cost.

*Instances (75)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

27:         require(wards[msg.sender] == 1, "Auth/not-authorized");

```

```solidity
File: example/Gateway.sol

110:         require(msg.sender == address(investmentManager), "Gateway/only-investment-manager-allowed-to-call");

115:         require(msg.sender == address(poolManager), "Gateway/only-pool-manager-allowed-to-call");

120:         require(incomingRouters[msg.sender], "Gateway/only-router-allowed-to-call");

125:         require(!root.paused(), "Gateway/paused");

133:         else revert("Gateway/file-unrecognized-param");

364:             revert("Gateway/invalid-message");

```

```solidity
File: example/InvestmentManager.sol

98:         require(msg.sender == address(gateway), "InvestmentManager/not-the-gateway");

106:         else revert("InvestmentManager/file-unrecognized-param");

177:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

190:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

202:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

213:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

229:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

242:         require(currencyPayout != 0, "InvestmentManager/zero-invest");

245:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

263:         require(trancheTokensPayout != 0, "InvestmentManager/zero-redeem");

266:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

284:         require(currencyPayout != 0, "InvestmentManager/zero-payout");

288:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

289:         require(_currency == LiquidityPoolLike(liquidityPool).asset(), "InvestmentManager/not-tranche-currency");

301:         require(trancheTokenPayout != 0, "InvestmentManager/zero-payout");

305:         require(address(liquidityPool) != address(0), "InvestmentManager/tranche-does-not-exist");

436:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

460:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

473:         require(lPool.checkTransferRestriction(msg.sender, user, 0), "InvestmentManager/trancheTokens-not-a-member");

502:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

528:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

656:         require(liquidityPool != address(0), "InvestmentManager/unknown-liquidity-pool");

668:             revert("InvestmentManager/uint128-overflow");

```

```solidity
File: example/LiquidityPool.sol

98:         require(msg.sender == owner, "LiquidityPool/no-approval");

105:         else revert("LiquidityPool/file-unrecognized-param");

```

```solidity
File: example/Messages.sol

860:         require(_bytes128.length == 128, "Input should be 128 bytes");

```

```solidity
File: example/PauseAdmin.sol

29:         require(pausers[msg.sender] == 1, "PauseAdmin/not-authorized-to-pause");

```

```solidity
File: example/PoolManager.sol

120:         require(msg.sender == address(gateway), "PoolManager/not-the-gateway");

128:         else revert("PoolManager/file-unrecognized-param");

138:         require(currency != 0, "PoolManager/unknown-currency");

151:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

165:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

178:         require(pool.createdAt == 0, "PoolManager/pool-already-added");

189:         require(pool.createdAt != 0, "PoolManager/invalid-pool");

192:         require(currencyAddress != address(0), "PoolManager/unknown-currency");

208:         require(pool.createdAt != 0, "PoolManager/invalid-pool");

210:         require(tranche.createdAt == 0, "PoolManager/tranche-already-exists");

229:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

237:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

248:         require(currency != 0, "PoolManager/currency-id-has-to-be-greater-than-0");

249:         require(currencyIdToAddress[currency] == address(0), "PoolManager/currency-id-in-use");

250:         require(currencyAddressToId[currencyAddress] == 0, "PoolManager/currency-address-in-use");

251:         require(IERC20(currencyAddress).decimals() <= MAX_CURRENCY_DECIMALS, "PoolManager/too-many-currency-decimals");

267:         require(currencyAddress != address(0), "PoolManager/unknown-currency");

278:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

290:         require(tranche.token == address(0), "PoolManager/tranche-already-deployed");

291:         require(tranche.createdAt != 0, "PoolManager/tranche-not-added");

317:         require(tranche.token != address(0), "PoolManager/tranche-does-not-exist"); // Tranche must have been added

318:         require(isAllowedAsPoolCurrency(poolId, currency), "PoolManager/currency-not-supported"); // Currency must be supported by pool

321:         require(liquidityPool == address(0), "PoolManager/liquidityPool-already-deployed");

322:         require(pools[poolId].createdAt != 0, "PoolManager/pool-does-not-exist");

355:         require(currency != 0, "PoolManager/unknown-currency"); // Currency index on the Centrifuge side should start at 1

356:         require(pools[poolId].allowedCurrencies[currencyAddress], "PoolManager/pool-currency-not-allowed");

```

```solidity
File: example/RestrictionManager.sol

46:         require((members[user] >= block.timestamp), "RestrictionManager/destination-not-a-member");

58:         require(block.timestamp <= validUntil, "RestrictionManager/invalid-valid-until");

```

```solidity
File: example/Root.sol

45:             require(data <= MAX_DELAY, "Root/delay-too-long");

48:             revert("Root/file-unrecognized-param");

76:         require(schedule[target] != 0, "Root/target-not-scheduled");

77:         require(schedule[target] < block.timestamp, "Root/target-not-ready");

```

```solidity
File: example/Router.sol

44:         require(msg.sender == address(axelarGateway), "AxelarRouter/invalid-origin");

57:         require(msg.sender == address(gateway), "AxelarRouter/only-gateway-allowed-to-call");

66:             revert("AxelarRouter/file-unrecognized-param");

```

```solidity
File: example/SafeTransferLib.sol

18:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-from-failed");

28:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-failed");

38:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-approve-failed");

```

```solidity
File: example/Tranche.sol

44:         else revert("TrancheToken/file-unrecognized-param");

```

```solidity
File: example/UserEscrow.sol

46:         require(destinations[token][destination] >= amount, "UserEscrow/transfer-failed");

63:         require(root == address(0), "TrancheTokenFactory/already-initialized");

```

</details> 
 


 ### <a name="GAS-14"></a>[GAS-14] Don't initialize variables with default value

*Instances (10)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

16:    for (uint i = 0; i < jhh.length; i++) {

```

```solidity
File: example/Factory.sol

47:         for (uint256 i = 0; i < wards.length; i++) {

130:         for (uint256 i = 0; i < trancheTokenWards.length; i++) {

144:         for (uint256 i = 0; i < restrictionManagerWards.length; i++) {

```

```solidity
File: example/Messages.sol

848:         for (uint256 i = 0; i < 128; i++) {

862:         uint8 i = 0;

869:         for (uint8 j = 0; j < i; j++) {

888:         uint8 i = 0;

```

```solidity
File: example/RestrictionManager.sol

15:     uint8 public constant SUCCESS_CODE = 0;

64:         for (uint256 i = 0; i < userLength; i++) {

```

</details> 
 


 ### <a name="GAS-15"></a>[GAS-15] Initializers can be marked as payable to save deployment gas
Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. Initializers can be safely marked as payable, because only the deployer or the factory contract would call the function without carrying any funds.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/UserEscrow.sol

62:     function initialize(address _root) external {

```

</details> 
 


 ### <a name="GAS-16"></a>[GAS-16] Use assembly for small keccak256 hashes, in order to save gas
If the arguments to the encode call can fit into the scratch space (two words or fewer), then its more efficient to use assembly to generate the hash (80 gas): keccak256(abi.encodePacked(x, y)) -> assembly {mstore(0x00, a); mstore(0x20, b); let hash := keccak256(0x00, 0x40); }

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

121:         bytes32 salt = keccak256(abi.encodePacked(poolId, trancheId));

```

</details> 
 


 ### <a name="GAS-17"></a>[GAS-17] Long revert strings

*Instances (33)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Gateway.sol

110:         require(msg.sender == address(investmentManager), "Gateway/only-investment-manager-allowed-to-call");

115:         require(msg.sender == address(poolManager), "Gateway/only-pool-manager-allowed-to-call");

120:         require(incomingRouters[msg.sender], "Gateway/only-router-allowed-to-call");

```

```solidity
File: example/InvestmentManager.sol

98:         require(msg.sender == address(gateway), "InvestmentManager/not-the-gateway");

229:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

245:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

266:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

288:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

289:         require(_currency == LiquidityPoolLike(liquidityPool).asset(), "InvestmentManager/not-tranche-currency");

305:         require(address(liquidityPool) != address(0), "InvestmentManager/tranche-does-not-exist");

436:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

460:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

473:         require(lPool.checkTransferRestriction(msg.sender, user, 0), "InvestmentManager/trancheTokens-not-a-member");

502:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

528:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

656:         require(liquidityPool != address(0), "InvestmentManager/unknown-liquidity-pool");

```

```solidity
File: example/PauseAdmin.sol

29:         require(pausers[msg.sender] == 1, "PauseAdmin/not-authorized-to-pause");

```

```solidity
File: example/PoolManager.sol

210:         require(tranche.createdAt == 0, "PoolManager/tranche-already-exists");

248:         require(currency != 0, "PoolManager/currency-id-has-to-be-greater-than-0");

250:         require(currencyAddressToId[currencyAddress] == 0, "PoolManager/currency-address-in-use");

251:         require(IERC20(currencyAddress).decimals() <= MAX_CURRENCY_DECIMALS, "PoolManager/too-many-currency-decimals");

290:         require(tranche.token == address(0), "PoolManager/tranche-already-deployed");

317:         require(tranche.token != address(0), "PoolManager/tranche-does-not-exist"); // Tranche must have been added

318:         require(isAllowedAsPoolCurrency(poolId, currency), "PoolManager/currency-not-supported"); // Currency must be supported by pool

321:         require(liquidityPool == address(0), "PoolManager/liquidityPool-already-deployed");

356:         require(pools[poolId].allowedCurrencies[currencyAddress], "PoolManager/pool-currency-not-allowed");

```

```solidity
File: example/RestrictionManager.sol

46:         require((members[user] >= block.timestamp), "RestrictionManager/destination-not-a-member");

58:         require(block.timestamp <= validUntil, "RestrictionManager/invalid-valid-until");

```

```solidity
File: example/Router.sol

57:         require(msg.sender == address(gateway), "AxelarRouter/only-gateway-allowed-to-call");

```

```solidity
File: example/SafeTransferLib.sol

18:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-from-failed");

28:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-failed");

38:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-approve-failed");

```

```solidity
File: example/UserEscrow.sol

63:         require(root == address(0), "TrancheTokenFactory/already-initialized");

```

</details> 
 


 ### <a name="GAS-18"></a>[GAS-18] Reduce gas usage by moving to Solidity 0.8.19 or later
Solidity version 0.8.19 introduced a number of gas optimizations, refer to the [Solidity 0.8.19 Release Announcement](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement) for details.

*Instances (18)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

3: pragma solidity 0.8.21;

```

```solidity
File: example/Context.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/DelayedAdmin.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/ERC20.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Escrow.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Factory.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Gateway.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/InvestmentManager.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/LiquidityPool.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Messages.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/PauseAdmin.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/PoolManager.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/RestrictionManager.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Root.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Router.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/SafeTransferLib.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/Tranche.sol

2: pragma solidity 0.8.21;

```

```solidity
File: example/UserEscrow.sol

2: pragma solidity 0.8.21;

```

</details> 
 


 ### <a name="GAS-19"></a>[GAS-19] Functions guaranteed to revert when called by normal users can be marked `payable`
If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Gateway.sol

285:     function handle(bytes calldata message) external onlyIncomingRouter pauseable {

```

```solidity
File: example/PoolManager.sol

176:     function addPool(uint64 poolId) public onlyGateway {

187:     function allowPoolCurrency(uint64 poolId, uint128 currency) public onlyGateway {

235:     function updateMember(uint64 poolId, bytes16 trancheId, address user, uint64 validUntil) public onlyGateway {

246:     function addCurrency(uint128 currency, address currencyAddress) public onlyGateway {

265:     function handleTransfer(uint128 currency, address recipient, uint128 amount) public onlyGateway {

```

```solidity
File: example/Router.sol

89:     function send(bytes calldata message) public onlyGateway {

```

</details> 
 


 ### <a name="GAS-20"></a>[GAS-20] `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too)
*Saves 5 gas per loop*

*Instances (10)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

16:    for (uint i = 0; i < jhh.length; i++) {

```

```solidity
File: example/Factory.sol

47:         for (uint256 i = 0; i < wards.length; i++) {

130:         for (uint256 i = 0; i < trancheTokenWards.length; i++) {

144:         for (uint256 i = 0; i < restrictionManagerWards.length; i++) {

```

```solidity
File: example/Messages.sol

848:         for (uint256 i = 0; i < 128; i++) {

864:             i++;

869:         for (uint8 j = 0; j < i; j++) {

890:             i++;

893:         for (i = 0; i < 32 && _bytes32[i] != 0; i++) {

```

```solidity
File: example/RestrictionManager.sol

64:         for (uint256 i = 0; i < userLength; i++) {

```

</details> 
 


 ### <a name="GAS-21"></a>[GAS-21] Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

74:     uint8 public constant PRICE_DECIMALS = 18;

```

```solidity
File: example/RestrictionManager.sol

15:     uint8 public constant SUCCESS_CODE = 0;

16:     uint8 public constant DESTINATION_NOT_A_MEMBER_RESTRICTION_CODE = 1;

17:     string public constant SUCCESS_MESSAGE = "RestrictionManager/transfer-allowed";

18:     string public constant DESTINATION_NOT_A_MEMBER_RESTRICTION_MESSAGE = "RestrictionManager/destination-not-a-member";

```

</details> 
 


 ### <a name="GAS-22"></a>[GAS-22] require()/revert() strings longer than 32 bytes cost extra gas
Each extra memory word of bytes past the original 32 [incurs an MSTORE](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#consider-having-short-revert-strings) which costs 3 gas.

*Instances (94)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

27:         require(wards[msg.sender] == 1, "Auth/not-authorized");

```

```solidity
File: example/Factory.sol

61:         require(signature.length == 65);

77:         require(v == 27 || v == 28);

```

```solidity
File: example/Gateway.sol

110:         require(msg.sender == address(investmentManager), "Gateway/only-investment-manager-allowed-to-call");

115:         require(msg.sender == address(poolManager), "Gateway/only-pool-manager-allowed-to-call");

120:         require(incomingRouters[msg.sender], "Gateway/only-router-allowed-to-call");

125:         require(!root.paused(), "Gateway/paused");

133:         else revert("Gateway/file-unrecognized-param");

364:             revert("Gateway/invalid-message");

```

```solidity
File: example/InvestmentManager.sol

98:         require(msg.sender == address(gateway), "InvestmentManager/not-the-gateway");

106:         else revert("InvestmentManager/file-unrecognized-param");

177:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

190:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

202:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

213:         require(liquidityPool.checkTransferRestriction(address(0), user, 0), "InvestmentManager/not-a-member");

229:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

242:         require(currencyPayout != 0, "InvestmentManager/zero-invest");

245:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

263:         require(trancheTokensPayout != 0, "InvestmentManager/zero-redeem");

266:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

284:         require(currencyPayout != 0, "InvestmentManager/zero-payout");

288:         require(liquidityPool != address(0), "InvestmentManager/tranche-does-not-exist");

289:         require(_currency == LiquidityPoolLike(liquidityPool).asset(), "InvestmentManager/not-tranche-currency");

301:         require(trancheTokenPayout != 0, "InvestmentManager/zero-payout");

305:         require(address(liquidityPool) != address(0), "InvestmentManager/tranche-does-not-exist");

307:         require(

312:         require(

430:         require(

436:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

454:         require(

460:         require(depositPrice != 0, "LiquidityPool/deposit-token-price-0");

473:         require(lPool.checkTransferRestriction(msg.sender, user, 0), "InvestmentManager/trancheTokens-not-a-member");

474:         require(

496:         require(

502:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

522:         require(

528:         require(redeemPrice != 0, "LiquidityPool/redeem-token-price-0");

656:         require(liquidityPool != address(0), "InvestmentManager/unknown-liquidity-pool");

657:         require(

668:             revert("InvestmentManager/uint128-overflow");

```

```solidity
File: example/LiquidityPool.sol

98:         require(msg.sender == owner, "LiquidityPool/no-approval");

105:         else revert("LiquidityPool/file-unrecognized-param");

344:                 revert(ptr, size)

```

```solidity
File: example/Messages.sol

860:         require(_bytes128.length == 128, "Input should be 128 bytes");

```

```solidity
File: example/PauseAdmin.sol

29:         require(pausers[msg.sender] == 1, "PauseAdmin/not-authorized-to-pause");

```

```solidity
File: example/PoolManager.sol

120:         require(msg.sender == address(gateway), "PoolManager/not-the-gateway");

128:         else revert("PoolManager/file-unrecognized-param");

138:         require(currency != 0, "PoolManager/unknown-currency");

151:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

165:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

178:         require(pool.createdAt == 0, "PoolManager/pool-already-added");

189:         require(pool.createdAt != 0, "PoolManager/invalid-pool");

192:         require(currencyAddress != address(0), "PoolManager/unknown-currency");

208:         require(pool.createdAt != 0, "PoolManager/invalid-pool");

210:         require(tranche.createdAt == 0, "PoolManager/tranche-already-exists");

229:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

237:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

248:         require(currency != 0, "PoolManager/currency-id-has-to-be-greater-than-0");

249:         require(currencyIdToAddress[currency] == address(0), "PoolManager/currency-id-in-use");

250:         require(currencyAddressToId[currencyAddress] == 0, "PoolManager/currency-address-in-use");

251:         require(IERC20(currencyAddress).decimals() <= MAX_CURRENCY_DECIMALS, "PoolManager/too-many-currency-decimals");

267:         require(currencyAddress != address(0), "PoolManager/unknown-currency");

278:         require(address(trancheToken) != address(0), "PoolManager/unknown-token");

280:         require(

290:         require(tranche.token == address(0), "PoolManager/tranche-already-deployed");

291:         require(tranche.createdAt != 0, "PoolManager/tranche-not-added");

317:         require(tranche.token != address(0), "PoolManager/tranche-does-not-exist"); // Tranche must have been added

318:         require(isAllowedAsPoolCurrency(poolId, currency), "PoolManager/currency-not-supported"); // Currency must be supported by pool

321:         require(liquidityPool == address(0), "PoolManager/liquidityPool-already-deployed");

322:         require(pools[poolId].createdAt != 0, "PoolManager/pool-does-not-exist");

355:         require(currency != 0, "PoolManager/unknown-currency"); // Currency index on the Centrifuge side should start at 1

356:         require(pools[poolId].allowedCurrencies[currencyAddress], "PoolManager/pool-currency-not-allowed");

```

```solidity
File: example/RestrictionManager.sol

46:         require((members[user] >= block.timestamp), "RestrictionManager/destination-not-a-member");

58:         require(block.timestamp <= validUntil, "RestrictionManager/invalid-valid-until");

```

```solidity
File: example/Root.sol

45:             require(data <= MAX_DELAY, "Root/delay-too-long");

48:             revert("Root/file-unrecognized-param");

76:         require(schedule[target] != 0, "Root/target-not-scheduled");

77:         require(schedule[target] < block.timestamp, "Root/target-not-ready");

```

```solidity
File: example/Router.sol

44:         require(msg.sender == address(axelarGateway), "AxelarRouter/invalid-origin");

45:         require(

49:         require(

57:         require(msg.sender == address(gateway), "AxelarRouter/only-gateway-allowed-to-call");

66:             revert("AxelarRouter/file-unrecognized-param");

80:         require(

```

```solidity
File: example/SafeTransferLib.sol

18:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-from-failed");

28:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-failed");

38:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-approve-failed");

```

```solidity
File: example/Tranche.sol

37:         require(restrictionCode == restrictionManager.SUCCESS_CODE(), messageForTransferRestriction(restrictionCode));

44:         else revert("TrancheToken/file-unrecognized-param");

```

```solidity
File: example/UserEscrow.sol

46:         require(destinations[token][destination] >= amount, "UserEscrow/transfer-failed");

47:         require(

63:         require(root == address(0), "TrancheTokenFactory/already-initialized");

71:         require(signature.length == 65);

87:         require(v == 27 || v == 28);

```

</details> 
 


 ### <a name="GAS-23"></a>[GAS-23] Splitting require() statements that use && saves gas

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/SafeTransferLib.sol

18:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-from-failed");

28:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-transfer-failed");

38:         require(success && (data.length == 0 || abi.decode(data, (bool))), "SafeTransferLib/safe-approve-failed");

```

</details> 
 


 ### <a name="GAS-24"></a>[GAS-24] Structs can be packed into fewer storage slots
Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/ERC20.sol

9: struct  jhh {

```

```solidity
File: example/InvestmentManager.sol

59: struct LPValues {

```

```solidity
File: example/PoolManager.sol

56: struct Pool {

66: struct Tranche {

```

```solidity
File: example/UserEscrow.sol

20:     struct Name {

```

</details> 
 


 ### <a name="GAS-25"></a>[GAS-25] Use storage instead of memory for structs/arrays
When fetching data from a storage location, assigning the data to a memory variable causes all fields of the struct/array to be read from storage, which incurs a Gcoldsload (2100 gas) for each field of the struct/array. If the fields are read from the new memory variable, they incur an additional MLOAD rather than a cheap stack read. Instead of declaring the variable with the memory keyword, declaring the variable with the storage keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incurring the Gcoldsload for the fields actually read. The only time it makes sense to read the whole struct/array into a memory variable, is if the full struct/array is being returned by the function, is being passed to a function that requires memory, or if the array/struct is being read from another memory array/struct.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

49:              wards memory name = names[token];

51:              j memory name = names[token];

```

```solidity
File: example/UserEscrow.sol

39:         name memory name = names[token];

```

</details> 
 


 ### <a name="GAS-26"></a>[GAS-26] Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency
Using uint256(1) and uint256(2) instead of true and false can save gas for certain changes. Consider using uint256(1)/uint256(2) when appropriate.

*Instances (13)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Gateway.sol

102:         incomingRouters[router_] = true;

138:         incomingRouters[router] = true;

143:         incomingRouters[router] = false;

```

```solidity
File: example/InvestmentManager.sol

661:         return true;

```

```solidity
File: example/PoolManager.sol

194:         pools[poolId].allowedCurrencies[currencyAddress] = true;

357:         return true;

```

```solidity
File: example/RestrictionManager.sol

51:             return true;

53:         return false;

```

```solidity
File: example/Root.sol

23:     bool public paused = false;

55:         paused = true;

60:         paused = false;

```

```solidity
File: example/Tranche.sol

49:         liquidityPools[liquidityPool] = true;

54:         liquidityPools[liquidityPool] = false;

```

</details> 
 


 ### <a name="GAS-27"></a>[GAS-27] Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead
Using uints or ints smaller than 32 bytes (256 bits) can incur overhead. Consider using uint256 or int256 to avoid potential issues.

*Instances (72)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Factory.sol

65:         uint8 v;

88:         uint8 decimals,

113:         uint8 decimals,

```

```solidity
File: example/Gateway.sol

49:         uint8 decimals

301:                 uint8 decimals,

```

```solidity
File: example/InvestmentManager.sol

26:     function decimals() external view returns (uint8);

74:     uint8 public constant PRICE_DECIMALS = 18;

326:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

326:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

339:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

339:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

574:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

574:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

596:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

596:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

610:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

610:         (uint8 currencyDecimals, uint8 trancheTokenDecimals) = _getPoolDecimals(liquidityPool);

676:     function _toPriceDecimals(uint128 _value, uint8 decimals, address liquidityPool)

686:     function _fromPriceDecimals(uint256 _value, uint8 decimals, address liquidityPool)

699:         returns (uint8 currencyDecimals, uint8 trancheTokenDecimals)

699:         returns (uint8 currencyDecimals, uint8 trancheTokenDecimals)

```

```solidity
File: example/LiquidityPool.sol

10:     function permit(address owner, address spender, uint256 value, uint256 deadline, uint8 v, bytes32 r, bytes32 s)

220:     function requestDepositWithPermit(uint256 assets, address owner, uint256 deadline, uint8 v, bytes32 r, bytes32 s)

237:     function requestRedeemWithPermit(uint256 shares, address owner, uint256 deadline, uint8 v, bytes32 r, bytes32 s)

279:     function decimals() public view returns (uint8) {

```

```solidity
File: example/Messages.sol

80:         return abi.encodePacked(uint8(Call.AddCurrency), currency, currencyAddress);

99:         return abi.encodePacked(uint8(Call.AddPool), poolId);

118:         return abi.encodePacked(uint8(Call.AllowPoolCurrency), poolId, currency);

146:         uint8 decimals,

153:             uint8(Call.AddTranche),

175:             uint8 decimals,

210:         return abi.encodePacked(uint8(Call.UpdateMember), poolId, trancheId, member, validUntil);

242:         return abi.encodePacked(uint8(Call.UpdateTrancheTokenPrice), poolId, trancheId, currencyId, price);

274:         return abi.encodePacked(uint8(Call.Transfer), currency, sender, receiver, amount);

324:             uint8(Call.TransferTrancheTokens), poolId, trancheId, sender, destinationDomain, destinationAddress, amount

381:         return abi.encodePacked(uint8(Call.IncreaseInvestOrder), poolId, trancheId, investor, currency, amount);

417:         return abi.encodePacked(uint8(Call.DecreaseInvestOrder), poolId, trancheId, investor, currency, amount);

449:         return abi.encodePacked(uint8(Call.IncreaseRedeemOrder), poolId, trancheId, investor, currency, amount);

481:         return abi.encodePacked(uint8(Call.DecreaseRedeemOrder), poolId, trancheId, investor, currency, amount);

509:         return abi.encodePacked(uint8(Call.CollectInvest), poolId, trancheId, investor, currency);

540:         return abi.encodePacked(uint8(Call.CollectRedeem), poolId, trancheId, investor, currency);

566:             uint8(Call.ExecutedDecreaseInvestOrder), poolId, trancheId, investor, currency, currencyPayout

594:             uint8(Call.ExecutedDecreaseRedeemOrder), poolId, trancheId, investor, currency, trancheTokenPayout

623:             uint8(Call.ExecutedCollectInvest),

666:             uint8(Call.ExecutedCollectRedeem),

701:         return abi.encodePacked(uint8(Call.ScheduleUpgrade), _contract);

713:         return abi.encodePacked(uint8(Call.CancelUpgrade), _contract);

743:             uint8(Call.UpdateTrancheTokenMetadata),

771:         return abi.encodePacked(uint8(Call.CancelInvestOrder), poolId, trancheId, investor, currency);

790:         return abi.encodePacked(uint8(Call.CancelRedeemOrder), poolId, trancheId, investor, currency);

817:         return abi.encodePacked(uint8(Call.UpdateTrancheInvestmentLimit), poolId, trancheId, investmentLimit);

837:         return bytes9(bytes1(uint8(domain)));

841:         return bytes9(BytesLib.slice(abi.encodePacked(uint8(domain), chainId), 0, 9));

862:         uint8 i = 0;

869:         for (uint8 j = 0; j < i; j++) {

888:         uint8 i = 0;

```

```solidity
File: example/PoolManager.sol

71:     uint8 decimals;

84:     uint8 internal constant MAX_CURRENCY_DECIMALS = 18;

205:         uint8 decimals

```

```solidity
File: example/RestrictionManager.sol

15:     uint8 public constant SUCCESS_CODE = 0;

16:     uint8 public constant DESTINATION_NOT_A_MEMBER_RESTRICTION_CODE = 1;

28:     function detectTransferRestriction(address from, address to, uint256 value) public view returns (uint8) {

36:     function messageForTransferRestriction(uint8 restrictionCode) public view returns (string memory) {

```

```solidity
File: example/Tranche.sol

13:     function detectTransferRestriction(address from, address to, uint256 value) external view returns (uint8);

14:     function messageForTransferRestriction(uint8 restrictionCode) external view returns (string memory);

15:     function SUCCESS_CODE() external view returns (uint8);

33:     constructor(uint8 decimals_) ERC20(decimals_) {}

36:         uint8 restrictionCode = detectTransferRestriction(from, to, value);

76:     function detectTransferRestriction(address from, address to, uint256 value) public view returns (uint8) {

84:     function messageForTransferRestriction(uint8 restrictionCode) public view returns (string memory) {

88:     function SUCCESS_CODE() public view returns (uint8) {

```

```solidity
File: example/UserEscrow.sol

75:         uint8 v;

```

</details> 
 


 ### <a name="GAS-28"></a>[GAS-28] Use != 0 instead of > 0 for unsigned integer comparison

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/InvestmentManager.sol

667:         if (_value > type(uint128).max) {

```

</details> 
 


 ### <a name="GAS-29"></a>[GAS-29] Optimize names to save gas
public/external function names and public member variable names can be optimized to save gas. See [this](https://gist.github.com/IllIllI000/a5d8b486a8259f9f77891a919febd1a9) link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92)

*Instances (199)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Auth.sol

8:     mapping(address => uint256) public wards;

14:     function rely(address user) external auth {

20:     function deny(address user) external auth {

```

```solidity
File: example/DelayedAdmin.sol

13:     Root public immutable root;

26:     function pause() public auth {

30:     function unpause() public auth {

34:     function scheduleRely(address target) public auth {

38:     function cancelRely(address target) public auth {

```

```solidity
File: example/Escrow.sol

23:     function approve(address token, address spender, uint256 value) external auth {

```

```solidity
File: example/Factory.sol

10:     function escrow() external view returns (address);

43:     ) public auth returns (address) {

50:              uint public j;

116:     ) public auth returns (address) {

```

```solidity
File: example/Gateway.sol

85:     RootLike public immutable root;

86:     InvestmentManagerLike public investmentManager;

87:     PoolManagerLike public poolManager;

89:     mapping(address => bool) public incomingRouters;

90:     RouterLike public outgoingRouter;

130:     function file(bytes32 what, address data) public auth {

137:     function addIncomingRouter(address router) public auth {

142:     function removeIncomingRouter(address router) public auth {

147:     function updateOutgoingRouter(address router) public auth {

159:     ) public onlyPoolManager pauseable {

179:     ) public onlyPoolManager pauseable {

193:         public

206:     ) public onlyInvestmentManager pauseable {

218:     ) public onlyInvestmentManager pauseable {

230:     ) public onlyInvestmentManager pauseable {

244:     ) public onlyInvestmentManager pauseable {

253:         public

261:         public

269:         public

277:         public

285:     function handle(bytes calldata message) external onlyIncomingRouter pauseable {

```

```solidity
File: example/InvestmentManager.sol

26:     function decimals() external view returns (uint8);

34:     function asset() external view returns (address);

37:     function checkTransferRestriction(address from, address to, uint256 value) external view returns (bool);

38:     function latestPrice() external view returns (uint128);

42:     function currencyIdToAddress(uint128 currencyId) external view returns (address);

43:     function currencyAddressToId(address addr) external view returns (uint128);

44:     function getTrancheToken(uint64 poolId, bytes16 trancheId) external view returns (address);

45:     function getLiquidityPool(uint64 poolId, bytes16 trancheId, address currency) external view returns (address);

46:     function isAllowedAsPoolCurrency(uint64 poolId, address currencyAddress) external view returns (bool);

74:     uint8 public constant PRICE_DECIMALS = 18;

75:     EscrowLike public immutable escrow;

76:     UserEscrowLike public immutable userEscrow;

78:     GatewayLike public gateway;

79:     PoolManagerLike public poolManager;

81:     mapping(address => mapping(address => LPValues)) public orderbook;

103:     function file(bytes32 what, address data) external auth {

117:     function requestDeposit(uint256 currencyAmount, address user) public auth {

148:     function requestRedeem(uint256 trancheTokenAmount, address user) public auth {

174:     function decreaseDepositRequest(uint256 _currencyAmount, address user) public auth {

187:     function decreaseRedeemRequest(uint256 _trancheTokenAmount, address user) public auth {

200:     function collectDeposit(address user) public auth {

211:     function collectRedeem(address user) public auth {

224:         public

241:     ) public onlyGateway {

262:     ) public onlyGateway {

283:     ) public onlyGateway {

300:     ) public onlyGateway {

319:     function totalAssets(uint256 totalSupply, address liquidityPool) public view returns (uint256 _totalAssets) {

325:     function convertToShares(uint256 _assets, address liquidityPool) public view auth returns (uint256 shares) {

338:     function convertToAssets(uint256 _shares, address liquidityPool) public view auth returns (uint256 assets) {

350:     function maxDeposit(address user, address liquidityPool) public view returns (uint256 currencyAmount) {

355:     function maxMint(address user, address liquidityPool) public view returns (uint256 trancheTokenAmount) {

360:     function maxWithdraw(address user, address liquidityPool) public view returns (uint256 currencyAmount) {

365:     function maxRedeem(address user, address liquidityPool) public view returns (uint256 trancheTokenAmount) {

371:         public

384:         public

397:         public

410:         public

427:     function processDeposit(address user, uint256 currencyAmount) public auth returns (uint256 trancheTokenAmount) {

451:     function processMint(address user, uint256 trancheTokenAmount) public auth returns (uint256 currencyAmount) {

490:         public

516:         public

551:     function calculateDepositPrice(address user, address liquidityPool) public view returns (uint256 depositPrice) {

560:     function calculateRedeemPrice(address user, address liquidityPool) public view returns (uint256 redeemPrice) {

570:         public

```

```solidity
File: example/LiquidityPool.sol

12:     function PERMIT_TYPEHASH() external view returns (bytes32);

13:     function DOMAIN_SEPARATOR() external view returns (bytes32);

17:     function checkTransferRestriction(address from, address to, uint256 value) external view returns (bool);

25:     function maxDeposit(address user, address _tranche) external view returns (uint256);

26:     function maxMint(address user, address _tranche) external view returns (uint256);

27:     function maxWithdraw(address user, address _tranche) external view returns (uint256);

28:     function maxRedeem(address user, address _tranche) external view returns (uint256);

29:     function totalAssets(uint256 totalSupply, address liquidityPool) external view returns (uint256);

30:     function convertToShares(uint256 assets, address liquidityPool) external view returns (uint256);

31:     function convertToAssets(uint256 shares, address liquidityPool) external view returns (uint256);

32:     function previewDeposit(address user, address liquidityPool, uint256 assets) external view returns (uint256);

33:     function previewMint(address user, address liquidityPool, uint256 shares) external view returns (uint256);

34:     function previewWithdraw(address user, address liquidityPool, uint256 assets) external view returns (uint256);

35:     function previewRedeem(address user, address liquidityPool, uint256 shares) external view returns (uint256);

55:     uint64 public immutable poolId;

56:     bytes16 public immutable trancheId;

62:     address public immutable asset;

67:     TrancheTokenLike public immutable share;

69:     InvestmentManagerLike public investmentManager;

72:     uint128 public latestPrice;

75:     uint256 public lastPriceUpdate;

103:     function file(bytes32 what, address data) public auth {

111:     function totalAssets() public view returns (uint256) {

118:     function convertToShares(uint256 assets) public view returns (uint256 shares) {

125:     function convertToAssets(uint256 shares) public view returns (uint256 assets) {

130:     function maxDeposit(address receiver) public view returns (uint256) {

135:     function previewDeposit(uint256 assets) public view returns (uint256 shares) {

155:     function maxMint(address receiver) external view returns (uint256 maxShares) {

160:     function previewMint(uint256 shares) external view returns (uint256 assets) {

165:     function maxWithdraw(address receiver) public view returns (uint256 maxAssets) {

170:     function previewWithdraw(uint256 assets) public view returns (uint256 shares) {

187:     function maxRedeem(address owner) public view returns (uint256 maxShares) {

192:     function previewRedeem(uint256 shares) public view returns (uint256 assets) {

271:     function name() public view returns (string memory) {

275:     function symbol() public view returns (string memory) {

279:     function decimals() public view returns (uint8) {

283:     function totalSupply() public view returns (uint256) {

287:     function balanceOf(address owner) public view returns (uint256) {

291:     function allowance(address owner, address spender) public view returns (uint256) {

313:     function mint(address, uint256) public auth {

318:     function burn(address, uint256) public auth {

324:     function updatePrice(uint128 price) public auth {

332:     function checkTransferRestriction(address from, address to, uint256 value) public view returns (bool) {

```

```solidity
File: example/Messages.sol

836:     function formatDomain(Domain domain) public pure returns (bytes9) {

840:     function formatDomain(Domain domain, uint64 chainId) public pure returns (bytes9) {

```

```solidity
File: example/PauseAdmin.sol

11:     Root public immutable root;

13:     mapping(address => uint256) public pausers;

34:     function addPauser(address user) external auth {

39:     function removePauser(address user) external auth {

45:     function pause() public canPause {

```

```solidity
File: example/PoolManager.sol

37:     function getTrancheToken(uint64 _poolId, bytes16 _trancheId) external view returns (address);

38:     function userEscrow() external view returns (address);

86:     EscrowLike public immutable escrow;

87:     LiquidityPoolFactoryLike public immutable liquidityPoolFactory;

88:     TrancheTokenFactoryLike public immutable trancheTokenFactory;

90:     GatewayLike public gateway;

91:     InvestmentManagerLike public investmentManager;

93:     mapping(uint64 => Pool) public pools;

96:     mapping(uint128 => address) public currencyIdToAddress;

97:     mapping(address => uint128) public currencyAddressToId;

125:     function file(bytes32 what, address data) external auth {

176:     function addPool(uint64 poolId) public onlyGateway {

187:     function allowPoolCurrency(uint64 poolId, uint128 currency) public onlyGateway {

206:     ) public onlyGateway {

227:     ) public onlyGateway {

235:     function updateMember(uint64 poolId, bytes16 trancheId, address user, uint64 validUntil) public onlyGateway {

246:     function addCurrency(uint128 currency, address currencyAddress) public onlyGateway {

265:     function handleTransfer(uint128 currency, address recipient, uint128 amount) public onlyGateway {

274:         public

344:     function getTrancheToken(uint64 poolId, bytes16 trancheId) public view returns (address) {

349:     function getLiquidityPool(uint64 poolId, bytes16 trancheId, address currency) public view returns (address) {

353:     function isAllowedAsPoolCurrency(uint64 poolId, address currencyAddress) public view returns (bool) {

```

```solidity
File: example/RestrictionManager.sol

8:     function members(address user) external view returns (uint256);

9:     function hasMember(address user) external view returns (bool);

15:     uint8 public constant SUCCESS_CODE = 0;

16:     uint8 public constant DESTINATION_NOT_A_MEMBER_RESTRICTION_CODE = 1;

17:     string public constant SUCCESS_MESSAGE = "RestrictionManager/transfer-allowed";

18:     string public constant DESTINATION_NOT_A_MEMBER_RESTRICTION_MESSAGE = "RestrictionManager/destination-not-a-member";

20:     mapping(address => uint256) public members;

28:     function detectTransferRestriction(address from, address to, uint256 value) public view returns (uint8) {

36:     function messageForTransferRestriction(uint8 restrictionCode) public view returns (string memory) {

45:     function member(address user) public view {

49:     function hasMember(address user) public view returns (bool) {

57:     function updateMember(address user, uint256 validUntil) public auth {

62:     function updateMembers(address[] memory users, uint256 validUntil) public auth {

```

```solidity
File: example/Root.sol

19:     address public immutable escrow;

21:     mapping(address => uint256) public schedule;

22:     uint256 public delay;

23:     bool public paused = false;

43:     function file(bytes32 what, uint256 data) external auth {

54:     function pause() external auth {

59:     function unpause() external auth {

65:     function scheduleRely(address target) external auth {

70:     function cancelRely(address target) external auth {

90:     function relyContract(address target, address user) public auth {

98:     function denyContract(address target, address user) public auth {

```

```solidity
File: example/Router.sol

29:     AxelarGatewayLike public immutable axelarGateway;

31:     GatewayLike public gateway;

62:     function file(bytes32 what, address data) external auth {

89:     function send(bytes calldata message) public onlyGateway {

```

```solidity
File: example/Tranche.sol

9:     function restrictionManager() external view returns (address);

13:     function detectTransferRestriction(address from, address to, uint256 value) external view returns (uint8);

14:     function messageForTransferRestriction(uint8 restrictionCode) external view returns (string memory);

15:     function SUCCESS_CODE() external view returns (uint8);

24:     ERC1404Like public restrictionManager;

26:     mapping(address => bool) public liquidityPools;

42:     function file(bytes32 what, address data) public auth {

48:     function addLiquidityPool(address liquidityPool) public auth {

53:     function removeLiquidityPool(address liquidityPool) public auth {

59:     function transfer(address to, uint256 value) public override restricted(_msgSender(), to, value) returns (bool) {

64:         public

72:     function mint(address to, uint256 value) public override restricted(_msgSender(), to, value) {

76:     function detectTransferRestriction(address from, address to, uint256 value) public view returns (uint8) {

80:     function checkTransferRestriction(address from, address to, uint256 value) public view returns (bool) {

84:     function messageForTransferRestriction(uint8 restrictionCode) public view returns (string memory) {

88:     function SUCCESS_CODE() public view returns (uint8) {

93:     function isTrustedForwarder(address forwarder) public view returns (bool) {

```

```solidity
File: example/UserEscrow.sol

8:     function allowance(address owner, address spender) external view returns (uint256);

37:     function transferIn(address token, address source, address destination, uint256 amount) external auth {

45:     function transferOut(address token, address destination, address receiver, uint256 amount) external auth {

```

</details> 
 

