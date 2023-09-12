# Report


## Medium Issues


| |Issue|Instances|
|-|:-|:-:|
| [M-1](#M-1) | Strings should use double quotes rather than single quotes | 20 |
| [M-2](#M-2) | Missing storage gap for upgradable contracts | 16 |
| [M-3](#M-3) | Centralization Risk for trusted owners | 22 |
| [M-4](#M-4) | Unsafe use of ERC20 transferFrom() | 2 |
| [M-5](#M-5) | Unsafe use of ERC20 transfer() | 4 |
| [M-6](#M-6) | Timestamp may be manipulation | 4 |

## Low Issues


| |Issue|Instances|
|-|:-|:-:|
| [L-1](#L-1) | External call recipient may consume all transaction gas | 1 |
| [L-2](#L-2) | Division by zero not prevented | 5 |
| [L-3](#L-3) | Initializers could be front-run | 3 |
| [L-4](#L-4) | Unsafe solidity low-level call can cause gas grief attack | 1 |
| [L-5](#L-5) | Missing contract existence checks before low-level calls | 1 |
| [L-6](#L-6) | Use Ownable2Step instead of Ownable | 2 |
| [L-7](#L-7) | Owner can renounce while system is pausedOwner can renounce Ownership   | 2 |
| [L-8](#L-8) | Loss of precision | 5 |
| [L-9](#L-9) | State variables not capped at reasonable values | 22 |
| [L-10](#L-10) | Some tokens may revert when zero value transfers are made | 4 |
| [L-11](#L-11) |  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard   | 4 |
| [L-12](#L-12) | Some tokens may revert when large transfers are made | 4 |
| [L-13](#L-13) | Unsafe ERC20 operation(s) | 4 |

## Non Critical Issues


| |Issue|Instances|
|-|:-|:-:|
| [NC-1](#NC-1) | assert() should be replaced with require() or revert() | 1 |
| [NC-2](#NC-2) | Custom error has no error details | 13 |
| [NC-3](#NC-3) | Variables without visibility specifier | 9 |
| [NC-4](#NC-4) | Array is push()ed but not pop()ed | 1 |
| [NC-5](#NC-5) | Constants in comparisons should appear on the left side | 31 |
| [NC-6](#NC-6) | Consider using delete rather than assigning zero to clear value | 7 |
| [NC-7](#NC-7) | Consider adding a block/deny-list" | 4 |
| [NC-8](#NC-8) | Events are missing sender information | 16 |
| [NC-9](#NC-9) | If-statement can be converted to a ternary | 23 |
| [NC-10](#NC-10) | Variable names for immutables should use CONSTANT_CASE | 4 |
| [NC-11](#NC-11) | Consider using named mappings | 2 |
| [NC-12](#NC-12) | Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct | 3 |
| [NC-13](#NC-13) | Use of override is unnecessary | 5 |
| [NC-14](#NC-14) | Consider using descriptive constants when passing zero as a function argument | 3 |
| [NC-15](#NC-15) | Non-external/public variable names should begin with an underscore | 15 |
| [NC-16](#NC-16) |  `require()` / `revert()` statements should have descriptive reason strings | 1 |
| [NC-17](#NC-17) | Return values of `approve()` not checked | 6 |
| [NC-18](#NC-18) | Use the latest solidity version for deployment   | 5 |
| [NC-19](#NC-19) | Event is missing `indexed` fields | 12 |
| [NC-20](#NC-20) | Functions not used internally could be marked external | 14 |
| [NC-21](#NC-21) | Consider moving msg.sender checks to modifiers | 28 |
| [NC-22](#NC-22) | Owner can renounce while system is paused | 2 |
| [NC-23](#NC-23) | Array indices should be referenced via enums rather than numeric literals | 2 |

## Gas Optimizations


| |Issue|Instances|
|-|:-|:-:|
| [GAS-1](#GAS-1) | Use scientific notation (e.g. 1e18) rather than exponentiation (e.g. 10**18) | 1 |
| [GAS-2](#GAS-2) | Nesting if-statements is cheaper than using && | 2 |
| [GAS-3](#GAS-3) | Consider using = instead of += and -= for gas efficiency | 4 |
| [GAS-4](#GAS-4) | Use >= instead of > for gas efficiency | 7 |
| [GAS-5](#GAS-5) | Use assembly to emit events, in order to save gas | 19 |
| [GAS-6](#GAS-6) | `array[index] += amount` is cheaper than `array[index] = array[index] + amount` (or related variants) | 2 |
| [GAS-7](#GAS-7) | Using bools for storage incurs overhead | 2 |
| [GAS-8](#GAS-8) | Cache array length outside of loop | 4 |
| [GAS-9](#GAS-9) | State variables should be cached in stack variables rather than re-reading them from storage | 3 |
| [GAS-10](#GAS-10) | Consider using assembly for simple zero checks to save gas | 3 |
| [GAS-11](#GAS-11) | Consider using constant rather than immutable to save gas | 4 |
| [GAS-12](#GAS-12) | Constructors can be marked payable | 4 |
| [GAS-13](#GAS-13) | Use Custom Errors | 20 |
| [GAS-14](#GAS-14) | Don't initialize variables with default value | 7 |
| [GAS-15](#GAS-15) | Initializers can be marked as payable to save deployment gas | 1 |
| [GAS-16](#GAS-16) | Use assembly for small keccak256 hashes, in order to save gas | 2 |
| [GAS-17](#GAS-17) | Long revert strings | 7 |
| [GAS-18](#GAS-18) | Avoid fetching a low-level calls return data by using assembly | 1 |
| [GAS-19](#GAS-19) | Reduce gas usage by moving to Solidity 0.8.19 or later | 5 |
| [GAS-20](#GAS-20) | Functions guaranteed to revert when called by normal users can be marked `payable` | 12 |
| [GAS-21](#GAS-21) | Using `private` rather than `public` for constants, saves gas | 11 |
| [GAS-22](#GAS-22) | require()/revert() strings longer than 32 bytes cost extra gas | 45 |
| [GAS-23](#GAS-23) | Structs can be packed into fewer storage slots | 4 |
| [GAS-24](#GAS-24) | Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency | 11 |
| [GAS-25](#GAS-25) | Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead | 1 |
| [GAS-26](#GAS-26) | Use != 0 instead of > 0 for unsigned integer comparison | 7 |
| [GAS-27](#GAS-27) | Optimize names to save gas | 58 |

##################################################################### 
 
 DETAILED REPORT:: 


##################################################################### 


## Medium Issues


 ### <a name="M-1"></a>[M-1] Strings should use double quotes rather than single quotes

#### Impact:
Using consistent double quotes for strings improves code readability and maintainability. Also see it here https://docs.soliditylang.org/en/v0.8.20/style-guide.html#other-recommendations

*Instances (20)*:
 
 <details>
 <summary>Click to expand!</summary>



```solidity
File: example/rUSDY.sol

444:     require(_rUSDYAmount > 0, "rUSDY: can't unwrap zero rUSDY tokens");

628:       require(!_isBlocked(msg.sender), "rUSDY: 'sender' address blocked");

629:       require(!_isSanctioned(msg.sender), "rUSDY: 'sender' address sanctioned");

632:         "rUSDY: 'sender' address not on allowlist"

638:       require(!_isBlocked(from), "rUSDY: 'from' address blocked");

639:       require(!_isSanctioned(from), "rUSDY: 'from' address sanctioned");

640:       require(_isAllowed(from), "rUSDY: 'from' address not on allowlist");

645:       require(!_isBlocked(to), "rUSDY: 'to' address blocked");

646:       require(!_isSanctioned(to), "rUSDY: 'to' address sanctioned");

647:       require(_isAllowed(to), "rUSDY: 'to' address not on allowlist");

```


</details> 
 


 ### <a name="M-2"></a>[M-2] Missing storage gap for upgradable contracts
Adding a storage gap after the last state variable in your contract can help prevent storage layout collisions in upgradable contracts.

*Instances (16)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

18: import "@openzeppelin/contracts-upgradeable/token/ERC20/IERC20Upgradeable.sol";

18: import "@openzeppelin/contracts-upgradeable/token/ERC20/IERC20Upgradeable.sol";

19: import "@openzeppelin/contracts-upgradeable/utils/ContextUpgradeable.sol";

19: import "@openzeppelin/contracts-upgradeable/utils/ContextUpgradeable.sol";

20: import "@openzeppelin/contracts-upgradeable/security/PausableUpgradeable.sol";

20: import "@openzeppelin/contracts-upgradeable/security/PausableUpgradeable.sol";

21: import "@openzeppelin/contracts-upgradeable/access/AccessControlEnumerableUpgradeable.sol";

21: import "@openzeppelin/contracts-upgradeable/access/AccessControlEnumerableUpgradeable.sol";

53:   ContextUpgradeable,

54:   PausableUpgradeable,

55:   AccessControlEnumerableUpgradeable,

56:   BlocklistClientUpgradeable,

57:   AllowlistClientUpgradeable,

58:   SanctionsListClientUpgradeable,

59:   IERC20Upgradeable,

60:   IERC20MetadataUpgradeable

```

</details> 
 


 ### <a name="M-3"></a>[M-3] Centralization Risk for trusted owners

#### Impact:
Contracts have owners with privileged rights to perform admin tasks and need to be trusted to not perform malicious updates or drain funds.

*Instances (22)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

24:   Ownable,

204:   function addApprover(address approver) external onlyOwner {

214:   function removeApprover(address approver) external onlyOwner {

231:   ) external onlyOwner {

253:   ) external onlyOwner {

280:   function setMintLimit(uint256 mintLimit) external onlyOwner {

289:   function setMintLimitDuration(uint256 mintDuration) external onlyOwner {

298:   function pause() external onlyOwner {

307:   function unpause() external onlyOwner {

316:   function rescueTokens(address _token) external onlyOwner {

```

```solidity
File: example/RWADynamicOracle.sol

21: contract RWADynamicOracle is IRWAOracle, AccessControlEnumerable, Pausable {

153:   ) external onlyRole(SETTER_ROLE) {

191:   ) external onlyRole(DEFAULT_ADMIN_ROLE) {

240:   function pauseOracle() external onlyRole(PAUSER_ROLE) {

247:   function unpauseOracle() external onlyRole(DEFAULT_ADMIN_ROLE) {

```

```solidity
File: example/rUSDY.sol

656:   function setOracle(address _oracle) external onlyRole(USDY_MANAGER_ROLE) {

669:   ) external onlyRole(BURNER_ROLE) {

679:   function pause() external onlyRole(PAUSER_ROLE) {

683:   function unpause() external onlyRole(USDY_MANAGER_ROLE) {

694:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

705:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

716:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

```

</details> 
 


 ### <a name="M-4"></a>[M-4] Unsafe use of ERC20 transferFrom()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transferFrom() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransferFrom() from OpenZeppelin instead.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

295:   function transferFrom(

431:     usdy.transferFrom(msg.sender, address(this), _USDYAmount);

```

</details> 
 


 ### <a name="M-5"></a>[M-5] Unsafe use of ERC20 transfer()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transfer() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransfer() from OpenZeppelin instead.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

318:     IRWALike(_token).transfer(owner(), balance);

```

```solidity
File: example/rUSDY.sol

239:   function transfer(address _recipient, uint256 _amount) public returns (bool) {

448:     usdy.transfer(msg.sender, usdyAmount / BPS_DENOMINATOR);

674:     usdy.transfer(msg.sender, sharesAmount / BPS_DENOMINATOR);

```

</details> 
 


 ### <a name="M-6"></a>[M-6] Timestamp may be manipulation
The block.timestamp can be manipulated by miners to perform MEV profiting or other time-based attacks.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RWADynamicOracle.sol

63:     timestamp = block.timestamp;

78:       if (range.start <= block.timestamp) {

79:         if (range.end <= block.timestamp) {

82:           return derivePrice(range, block.timestamp);

```

</details> 
 


## Low Issues


 ### <a name="L-1"></a>[L-1] External call recipient may consume all transaction gas
There is no limit specified on the amount of gas used, so the recipient can use up all of the transactions gas, causing it to revert. Use addr.call{gas: <amount>}("") or this https://github.com/nomad-xyz/ExcessivelySafeCall library instead.  

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDYFactory.sol

127:       (bool success, bytes memory ret) = address(exCallData[i].target).call{

```

</details> 
 


 ### <a name="L-2"></a>[L-2] Division by zero not prevented
The divisions below take an input parameter that has no zero-value checks, which can cause the functions reverting if zero is passed.  

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RWADynamicOracle.sol

43:     uint256 trueStart = (startPrice * ONE) / dailyIR;

116:       uint256 trueStart = (rangeStartPrice * ONE) / dailyIR;

218:       uint256 trueStart = (newPrevRangeClosePrice * ONE) / newDailyIR;

265:     uint256 elapsedDays = (currentTime - currentRange.start) / DAY;

400:     z = _mul(x, y) / ONE;

```

</details> 
 


 ### <a name="L-3"></a>[L-3] Initializers could be front-run
Initializers could be front-run, allowing an attacker to either set their own values, take ownership of the contract, and in the best case forcing a re-deployment

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

103:   function initialize(

110:   ) public virtual initializer {

```

```solidity
File: example/rUSDYFactory.sol

86:     rUSDYProxied.initialize(

```

</details> 
 


 ### <a name="L-4"></a>[L-4] Unsafe solidity low-level call can cause gas grief attack
Using the low-level calls of a solidity address can leave the contract open to gas grief attacks. These attacks occur when the called contract returns a large amount of data. So when calling an external contract, it is necessary to check the length of the return data before reading/copying it (using returndatasize()).

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDYFactory.sol

127:       (bool success, bytes memory ret) = address(exCallData[i].target).call{

```

</details> 
 


 ### <a name="L-5"></a>[L-5] Missing contract existence checks before low-level calls
Low-level calls return success if there is no code present at the specified address. In addition to the zero-address checks, add a check to verify that `<address>.code.length > 0`.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDYFactory.sol

127:       (bool success, bytes memory ret) = address(exCallData[i].target).call{

```

</details> 
 


 ### <a name="L-6"></a>[L-6] Use Ownable2Step instead of Ownable
Add a description of why Ownable2Step is recommended.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

19: import "@openzeppelin/contracts/access/Ownable.sol";

24:   Ownable,

```

</details> 
 


 ### <a name="L-7"></a>[L-7] Owner can renounce while system is pausedOwner can renounce Ownership  
Each of the following contracts implements or inherits the renounceOwnership() function. This can represent a certain risk if the ownership is renounced for any other reason than by design. Renouncing ownership will leave the contract without an owner, thereby removing any functionality that is only available to the owner.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

19: import "@openzeppelin/contracts/access/Ownable.sol";

24:   Ownable,

```

</details> 
 


 ### <a name="L-8"></a>[L-8] Loss of precision
Division by large numbers or variables may result in the result being zero, due to Solidity not supporting fractions.

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RWADynamicOracle.sol

43:     uint256 trueStart = (startPrice * ONE) / dailyIR;

116:       uint256 trueStart = (rangeStartPrice * ONE) / dailyIR;

218:       uint256 trueStart = (newPrevRangeClosePrice * ONE) / newDailyIR;

265:     uint256 elapsedDays = (currentTime - currentRange.start) / DAY;

400:     z = _mul(x, y) / ONE;

```

</details> 
 


 ### <a name="L-9"></a>[L-9] State variables not capped at reasonable values
Consider adding minimum/maximum value checks to ensure that the state variables below can never be used to excessively harm users, including via griefing

*Instances (22)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

174:       return true;

176:       return false;

364:     uint256 amount;

365:     uint256 numberOfApprovalsNeeded;

369:     uint256 numberOfApprovalsNeeded;

374:     address sender;

375:     uint256 amount;

```

```solidity
File: example/RWADynamicOracle.sol

287:     return value;

295:     uint256 start;

296:     uint256 end;

297:     uint256 dailyInterestRate;

298:     uint256 prevRangeClosePrice;

```

```solidity
File: example/rUSDY.sol

204:     return 18;

241:     return true;

272:     return true;

305:     return true;

330:     return true;

357:     return true;

367:     return totalShares;

418:     return tokensAmount;

548: 

594: 

```

</details> 
 


 ### <a name="L-10"></a>[L-10] Some tokens may revert when zero value transfers are made
Despite the fact that [EIP-20](https://github.com/ethereum/EIPs/blob/7500ac4fc1bbdfaf684e7ef851f798f6b667b2fe/EIPS/eip-20.md?plain=1#L116) states that zero-value transfers must be accepted, some tokens, such as LEND, will revert if this is attempted, which may cause transactions that involve other tokens (such as batch operations) to fully revert. Consider skipping the transfer if the amount is zero, which will also save gas.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

318:     IRWALike(_token).transfer(owner(), balance);

```

```solidity
File: example/rUSDY.sol

239:   function transfer(address _recipient, uint256 _amount) public returns (bool) {

448:     usdy.transfer(msg.sender, usdyAmount / BPS_DENOMINATOR);

674:     usdy.transfer(msg.sender, sharesAmount / BPS_DENOMINATOR);

```

</details> 
 


 ### <a name="L-11"></a>[L-11]  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard  
Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks opens the users of this protocol up to [read-only reentrancy](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) vulnerability with no way to protect them except by block-listing the entire protocol.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

318:     IRWALike(_token).transfer(owner(), balance);

```

```solidity
File: example/rUSDY.sol

239:   function transfer(address _recipient, uint256 _amount) public returns (bool) {

448:     usdy.transfer(msg.sender, usdyAmount / BPS_DENOMINATOR);

674:     usdy.transfer(msg.sender, sharesAmount / BPS_DENOMINATOR);

```

</details> 
 


 ### <a name="L-12"></a>[L-12] Some tokens may revert when large transfers are made
Tokens such as COMP or UNI will revert when an address balance reaches type(uint96).max. Ensure that the calls below can be broken up into smaller batches if necessary.  

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

318:     IRWALike(_token).transfer(owner(), balance);

```

```solidity
File: example/rUSDY.sol

239:   function transfer(address _recipient, uint256 _amount) public returns (bool) {

448:     usdy.transfer(msg.sender, usdyAmount / BPS_DENOMINATOR);

674:     usdy.transfer(msg.sender, sharesAmount / BPS_DENOMINATOR);

```

</details> 
 


 ### <a name="L-13"></a>[L-13] Unsafe ERC20 operation(s)

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

318:     IRWALike(_token).transfer(owner(), balance);

```

```solidity
File: example/rUSDY.sol

431:     usdy.transferFrom(msg.sender, address(this), _USDYAmount);

448:     usdy.transfer(msg.sender, usdyAmount / BPS_DENOMINATOR);

674:     usdy.transfer(msg.sender, sharesAmount / BPS_DENOMINATOR);

```

</details> 
 


## Non Critical Issues


 ### <a name="NC-1"></a>[NC-1] assert() should be replaced with require() or revert()
In versions of Solidity prior to 0.8.0, when encountering an assert all the remaining gas will be consumed. Even after Solidity 0.8.0, the assert function is still not recommended, as described in the [documentation:](https://docs.soliditylang.org/en/v0.8.20/control-structures.html#panic-via-assert-and-error-via-require)

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDYFactory.sol

96:     assert(rUSDYProxyAdmin.owner() == guardian);

```

</details> 
 


 ### <a name="NC-2"></a>[NC-2] Custom error has no error details

#### Impact:
Defining custom errors without error details can make error messages less informative.

*Instances (13)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

433:   error NotApprover();

434:   error NoThresholdMatch();

435:   error ThresholdsNotInAscendingOrder();

437:   error ChainNotSupported();

438:   error SourceNotSupported();

439:   error NonceSpent();

440:   error AlreadyApproved();

441:   error InvalidVersion();

442:   error ArrayLengthMismatch();

```

```solidity
File: example/RWADynamicOracle.sol

333:   error InvalidPrice();

334:   error InvalidRange();

335:   error PriceNotSet();

```

```solidity
File: example/rUSDY.sol

88:   error UnwrapTooSmall();

```

</details> 
 


 ### <a name="NC-3"></a>[NC-3] Variables without visibility specifier

#### Impact:
Specifying visibility for variables can improve code readability and maintainability.

*Instances (9)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

364:     uint256 amount;

365:     uint256 numberOfApprovalsNeeded;

369:     uint256 numberOfApprovalsNeeded;

374:     address sender;

375:     uint256 amount;

```

```solidity
File: example/RWADynamicOracle.sol

295:     uint256 start;

296:     uint256 end;

297:     uint256 dailyInterestRate;

298:     uint256 prevRangeClosePrice;

```

</details> 
 


 ### <a name="NC-4"></a>[NC-4] Array is push()ed but not pop()ed

#### Impact:
Array entries are added but are never removed. Consider whether this should be the case, or whether there should be a maximum, or whether old entries should be removed.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

160:     t.approvers.push(msg.sender);

```

</details> 
 


 ### <a name="NC-5"></a>[NC-5] Constants in comparisons should appear on the left side

#### Impact:
Placing constants on the left side of comparisons can improve code readability and prevent accidental assignment. Doing so will prevent typo [bugs](https://www.moserware.com/2008/01/constants-on-left-are-better-but-this.html)

*Instances (31)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

87:     if (version != VERSION) {

90:     if (chainToApprovedSender[srcChain] == bytes32(0)) {

93:     if (chainToApprovedSender[srcChain] != keccak256(abi.encode(srcAddr))) {

130:       if (amount <= t.amount) {

138:     if (txnToThresholdSet[txnHash].numberOfApprovalsNeeded == 0) {

153:     if (t.approvers.length > 0) {

155:         if (t.approvers[i] == msg.sender) {

173:     if (t.numberOfApprovalsNeeded <= t.approvers.length) {

254:     if (amounts.length != numOfApprovers.length) {

259:       if (i == 0) {

264:         if (chainToThresholds[srcChain][i - 1].amount > amounts[i]) {

```

```solidity
File: example/RWADynamicOracle.sol

42:     if (firstRangeStart >= firstRangeEnd) revert InvalidRange();

78:       if (range.start <= block.timestamp) {

79:         if (range.end <= block.timestamp) {

115:     if (startTime == ranges[0].start) {

130:       if (range.start <= blockTimeStamp) {

131:         if (range.end <= blockTimeStamp) {

157:     if (lastRange.end >= endTimestamp) revert InvalidRange();

193:     if (newStart >= newEnd) revert InvalidRange();

197:     if (indexToModify == 0) {

200:       if (rangeLength > 1 && newEnd > ranges[indexToModify + 1].start)

204:     else if (indexToModify == rangeLength - 1) {

206:       if (newStart < ranges[indexToModify - 1].end) revert InvalidRange();

211:       if (newStart < ranges[indexToModify - 1].end) revert InvalidRange();

213:       if (newEnd > ranges[indexToModify + 1].start) revert InvalidRange();

217:     if (indexToModify == 0) {

283:     if (remainder >= 0.5e10) {

```

```solidity
File: example/rUSDY.sol

446:     if (usdyAmount < BPS_DENOMINATOR) revert UnwrapTooSmall();

627:     if (from != msg.sender && to != msg.sender) {

636:     if (from != address(0)) {

643:     if (to != address(0)) {

```

</details> 
 


 ### <a name="NC-6"></a>[NC-6] Consider using delete rather than assigning zero to clear value

#### Impact:
Consider using delete rather than assigning zero to clear values. The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

128:     for (uint256 i = 0; i < thresholds.length; ++i) {

154:       for (uint256 i = 0; i < t.approvers.length; ++i) {

258:     for (uint256 i = 0; i < amounts.length; ++i) {

```

```solidity
File: example/RWADynamicOracle.sol

76:     for (uint256 i = 0; i < length; ++i) {

112:     for (uint256 i = 0; i < length; ++i) {

128:     for (uint256 i = 0; i < length + 1; ++i) {

```

```solidity
File: example/rUSDYFactory.sol

126:     for (uint256 i = 0; i < exCallData.length; ++i) {

```

</details> 
 


 ### <a name="NC-7"></a>[NC-7] Consider adding a block/deny-list"
Doing so will significantly increase centralization, but will help to prevent hackers from using stolen tokens  

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

21: contract DestinationBridge is

```

```solidity
File: example/RWADynamicOracle.sol

21: contract RWADynamicOracle is IRWAOracle, AccessControlEnumerable, Pausable {

```

```solidity
File: example/rUSDY.sol

51: contract rUSDY is

```

```solidity
File: example/rUSDYFactory.sol

39: contract rUSDYFactory is IMulticall {

```

</details> 
 


 ### <a name="NC-8"></a>[NC-8] Events are missing sender information

#### Impact:
Including msg.sender in events triggered by user actions can make events more useful for end users.

*Instances (16)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

107:     emit MessageReceived(srcChain, srcSender, amt, nonce);

206:     emit ApproverAdded(approver);

216:     emit ApproverRemoved(approver);

233:     emit ChainIdSupported(srcChain, srcContractAddress);

272:     emit ThresholdSet(srcChain, amounts, numOfApprovers);

345:       emit BridgeCompleted(txn.sender, txn.amount);

```

```solidity
File: example/RWADynamicOracle.sol

163:     emit RangeSet(

228:     emit RangeOverriden(

```

```solidity
File: example/rUSDY.sol

415:     emit TransferShares(msg.sender, _recipient, _sharesAmount);

417:     emit Transfer(msg.sender, _recipient, tokensAmount);

449:     emit TokensBurnt(msg.sender, _rUSDYAmount);

464:     emit Transfer(_sender, _recipient, _amount);

465:     emit TransferShares(_sender, _recipient, _sharesToTransfer);

488:     emit Approval(_owner, _spender, _amount);

588:     emit SharesBurnt(

676:     emit TokensBurnt(_account, _amount);

```

</details> 
 


 ### <a name="NC-9"></a>[NC-9] If-statement can be converted to a ternary

#### Impact:
The code can be made more compact while also increasing readability by converting the following `if`-statements to ternaries (e.g. `foo += (x > y) ? a : b`)

*Instances (23)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

87:     if (version != VERSION) {

90:     if (chainToApprovedSender[srcChain] == bytes32(0)) {

93:     if (chainToApprovedSender[srcChain] != keccak256(abi.encode(srcAddr))) {

96:     if (isSpentNonce[chainToApprovedSender[srcChain]][nonce]) {

130:       if (amount <= t.amount) {

138:     if (txnToThresholdSet[txnHash].numberOfApprovalsNeeded == 0) {

153:     if (t.approvers.length > 0) {

173:     if (t.numberOfApprovalsNeeded <= t.approvers.length) {

192:     if (!approvers[msg.sender]) {

254:     if (amounts.length != numOfApprovers.length) {

259:       if (i == 0) {

334:     if (thresholdMet) {

```

```solidity
File: example/RWADynamicOracle.sol

78:       if (range.start <= block.timestamp) {

115:     if (startTime == ranges[0].start) {

130:       if (range.start <= blockTimeStamp) {

197:     if (indexToModify == 0) {

204:     else if (indexToModify == rangeLength - 1) {

209:     else {

217:     if (indexToModify == 0) {

283:     if (remainder >= 0.5e10) {

```

```solidity
File: example/rUSDY.sol

627:     if (from != msg.sender && to != msg.sender) {

636:     if (from != address(0)) {

643:     if (to != address(0)) {

```

</details> 
 


 ### <a name="NC-10"></a>[NC-10] Variable names for immutables should use CONSTANT_CASE

#### Impact:
Using CONSTANT_CASE for immutables improves code readability and maintainability.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

28:   IRWALike public immutable TOKEN;

31:   IAxelarGateway public immutable AXELAR_GATEWAY;

34:   IAllowlist public immutable ALLOWLIST;

```

```solidity
File: example/rUSDYFactory.sol

42:   address internal immutable guardian;

```

</details> 
 


 ### <a name="NC-11"></a>[NC-11] Consider using named mappings

#### Impact:
Using named mappings can improve code readability and maintainability.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

70:   mapping(address => uint256) private shares;

73:   mapping(address => mapping(address => uint256)) private allowances;

```

</details> 
 


 ### <a name="NC-12"></a>[NC-12] Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct

#### Impact:
Combining multiple mappings into a single mapping with a struct can improve readability and maintainability of the code.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

37:   mapping(address => bool) public approvers;

```

```solidity
File: example/rUSDY.sol

70:   mapping(address => uint256) private shares;

73:   mapping(address => mapping(address => uint256)) private allowances;

```

</details> 
 


 ### <a name="NC-13"></a>[NC-13] Use of override is unnecessary

#### Impact:
Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the override keyword when the function solely overrides an interface function, and the function doesnt exist in multiple base contracts, is unnecessary.

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

83:   ) internal override whenNotPaused {

```

```solidity
File: example/rUSDY.sol

694:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

705:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

716:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

```

```solidity
File: example/rUSDYFactory.sol

124:   ) external payable override onlyGuardian returns (bytes[] memory results) {

```

</details> 
 


 ### <a name="NC-14"></a>[NC-14] Consider using descriptive constants when passing zero as a function argument

#### Impact:
Passing zero as a function argument/Event emission can sometimes result in a security issue (e.g. passing zero as the slippage parameter). Consider using a constant variable with a descriptive name, so its clear that the 0 is intentionally being used, and for the right reasons.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

429:     require(_USDYAmount > 0, "rUSDY: can't wrap zero USDY tokens");

444:     require(_rUSDYAmount > 0, "rUSDY: can't unwrap zero rUSDY tokens");

```

```solidity
File: example/rUSDYFactory.sol

40:   bytes32 public constant DEFAULT_ADMIN_ROLE = bytes32(0);

```

</details> 
 


 ### <a name="NC-15"></a>[NC-15] Non-external/public variable names should begin with an underscore

#### Impact:
Using an underscore at the beginning of non-external/public variable names can improve code clarity and maintainability. According to the Solidity Style Guide, non-external/public variable names should begin with an [underscore](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables)

*Instances (15)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

37:   mapping(address => bool) public approvers;

38:   mapping(string => bytes32) public chainToApprovedSender;

39:   mapping(bytes32 => mapping(uint256 => bool)) public isSpentNonce;

45:   mapping(bytes32 => TxnThreshold) public txnToThresholdSet;

46:   mapping(string => Threshold[]) public chainToThresholds;

47:   mapping(bytes32 => Transaction) public txnHashToTransaction;

```

```solidity
File: example/RWADynamicOracle.sol

24:   Range[] public ranges;

```

```solidity
File: example/rUSDY.sol

70:   mapping(address => uint256) private shares;

73:   mapping(address => mapping(address => uint256)) private allowances;

76:   uint256 private totalShares;

79:   IRWADynamicOracle public oracle;

82:   IUSDY public usdy;

```

```solidity
File: example/rUSDYFactory.sol

43:   rUSDY public rUSDYImplementation;

44:   ProxyAdmin public rUSDYProxyAdmin;

45:   TokenProxy public rUSDYProxy;

```

</details> 
 


 


 ### <a name="NC-17"></a>[NC-17] Return values of `approve()` not checked
Not all IERC20 implementations `revert()` when there's a failure in `approve()`. The function signature has a boolean return value and they indicate errors that way instead. By not checking the return value, operations that should have marked as failed, may potentially go through without actually approving anything

*Instances (6)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

105:     _approve(txnHash);

195:     _approve(txnHash);

```

```solidity
File: example/rUSDY.sol

271:     _approve(msg.sender, _spender, _amount);

304:     _approve(_sender, msg.sender, currentAllowance - _amount);

325:     _approve(

356:     _approve(msg.sender, _spender, currentAllowance - _subtractedValue);

```

</details> 
 


 ### <a name="NC-18"></a>[NC-18] Use the latest solidity version for deployment  
Upgrading to a newer Solidity release can optimize gas usage, take advantage of new features and improve overall contract efficiency. Where possible, based on compatibility requirements, it is recommended to use newer/latest solidity version to take advantage of the latest optimizations and features.

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/IRWADynamicOracle.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/RWADynamicOracle.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/rUSDY.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/rUSDYFactory.sol

16: pragma solidity 0.8.16;

```

</details> 
 


 ### <a name="NC-19"></a>[NC-19] Event is missing `indexed` fields
Index event fields make the field more quickly accessible to off-chain tools that parse events. However, note that each index field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields). Each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three fields, all of the fields should be indexed.

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

404:    * @param chain           The chain for which the threshold was set

406:    * @param numOfApprovers  The number of approvals needed

414:    * @param amount  The amount of tokens that have been minted

423:    * @param amt       The amount of tokens being bridged

435:   error ThresholdsNotInAscendingOrder();

444: 

```

```solidity
File: example/RWADynamicOracle.sol

323:    * @param newPrevRangeClosePrice The new prevRangeClosePrice for the modified range

348:   ) internal pure returns (uint256 z) {

```

```solidity
File: example/rUSDY.sol

164:    * @param sharesAmount amount of burnt shares

188:   function name() public pure returns (string memory) {

208:    * @return the amount of tokens in existence.

```

```solidity
File: example/rUSDYFactory.sol

155: 

```

</details> 
 


 ### <a name="NC-20"></a>[NC-20] Functions not used internally could be marked external

*Instances (14)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

211:     return (totalShares * oracle.getPrice()) / (1e18 * BPS_DENOMINATOR);

218:    *      by the price of USDY

225:    * @notice Moves `_amount` tokens from the caller's account to the `_recipient` account.

227:    * @return a boolean value indicating whether the operation succeeded.

237:    * @dev The `_amount` argument is the amount of tokens, not shares.

258:    * @notice Sets `_amount` as the allowance of `_spender` over the caller's tokens.

271:     _approve(msg.sender, _spender, _amount);

288:    * - `_sender` and `_recipient` cannot be the zero addresses.

313:    * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/IERC20.sol#L42

339:    * Emits an `Approval` event indicating the updated allowance.

366:   function getTotalShares() public view returns (uint256) {

389:    * @return the amount of rUSDY that corresponds to `_shares` of usdy.

396:    * @notice Moves `_sharesAmount` token shares from the caller's account to the `_recipient` account.

428:   function wrap(uint256 _USDYAmount) external whenNotPaused {

```

</details> 
 


 ### <a name="NC-21"></a>[NC-21] Consider moving msg.sender checks to modifiers
If some functions are only allowed to be called by some specific users, consider using a modifier instead of checking with a require statement, especially if this check is done in multiple functions.  

*Instances (28)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

155:         if (t.approvers[i] == msg.sender) {

160:     t.approvers.push(msg.sender);

192:     if (!approvers[msg.sender]) {

```

```solidity
File: example/rUSDY.sol

240:     _transfer(msg.sender, _recipient, _amount);

271:     _approve(msg.sender, _spender, _amount);

300:     uint256 currentAllowance = allowances[_sender][msg.sender];

304:     _approve(_sender, msg.sender, currentAllowance - _amount);

326:       msg.sender,

328:       allowances[msg.sender][_spender] + _addedValue

351:     uint256 currentAllowance = allowances[msg.sender][_spender];

356:     _approve(msg.sender, _spender, currentAllowance - _subtractedValue);

414:     _transferShares(msg.sender, _recipient, _sharesAmount);

415:     emit TransferShares(msg.sender, _recipient, _sharesAmount);

417:     emit Transfer(msg.sender, _recipient, tokensAmount);

430:     _mintShares(msg.sender, _USDYAmount * BPS_DENOMINATOR);

431:     usdy.transferFrom(msg.sender, address(this), _USDYAmount);

432:     emit Transfer(address(0), msg.sender, getRUSDYByShares(_USDYAmount));

433:     emit TransferShares(address(0), msg.sender, _USDYAmount);

447:     _burnShares(msg.sender, usdyAmount);

448:     usdy.transfer(msg.sender, usdyAmount / BPS_DENOMINATOR);

449:     emit TokensBurnt(msg.sender, _rUSDYAmount);

627:     if (from != msg.sender && to != msg.sender) {

627:     if (from != msg.sender && to != msg.sender) {

628:       require(!_isBlocked(msg.sender), "rUSDY: 'sender' address blocked");

629:       require(!_isSanctioned(msg.sender), "rUSDY: 'sender' address sanctioned");

631:         _isAllowed(msg.sender),

674:     usdy.transfer(msg.sender, sharesAmount / BPS_DENOMINATOR);

```

```solidity
File: example/rUSDYFactory.sol

151:     require(msg.sender == guardian, "rUSDYFactory: You are not the Guardian");

```

</details> 
 


 ### <a name="NC-22"></a>[NC-22] Owner can renounce while system is paused
The contract owner or single user with a role is not prevented from renouncing the role/ownership while the contract is paused, which would cause any user assets stored in the protocol, to be locked indefinitely.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

298:   function pause() external onlyOwner {

```

```solidity
File: example/rUSDY.sol

679:   function pause() external onlyRole(PAUSER_ROLE) {

```

</details> 
 


 ### <a name="NC-23"></a>[NC-23] Array indices should be referenced via enums rather than numeric literals

#### Impact:
Referencing array indices via enums can improve code readability and maintainability.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

339:           ALLOWLIST.getValidTermIndexes()[0],

```

```solidity
File: example/RWADynamicOracle.sol

115:     if (startTime == ranges[0].start) {

```

</details> 
 


## Gas Optimizations


 ### <a name="GAS-1"></a>[GAS-1] Use scientific notation (e.g. 1e18) rather than exponentiation (e.g. 10**18)
While the compiler knows to optimize away the exponentiation, its still better coding practice to use idioms that do not require compiler optimization, if they exist.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RWADynamicOracle.sol

342:   uint256 private constant ONE = 10 ** 27;

```

</details> 
 


 ### <a name="GAS-2"></a>[GAS-2] Nesting if-statements is cheaper than using &&
Nesting if-statements avoids the stack operations of setting up and using an extra jumpdest, and saves 6 [gas](https://gist.github.com/IllIllI000/7f3b818abecfadbef93b894481ae7d19)

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RWADynamicOracle.sol

200:       if (rangeLength > 1 && newEnd > ranges[indexToModify + 1].start)

```

```solidity
File: example/rUSDY.sol

627:     if (from != msg.sender && to != msg.sender) {

```

</details> 
 


 ### <a name="GAS-3"></a>[GAS-3] Consider using = instead of += and -= for gas efficiency
Using = instead of += and -= can save gas in certain scenarios. Consider using = when appropriate.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RWADynamicOracle.sol

284:       value += 1e10;

286:     value -= remainder;

```

```solidity
File: example/rUSDY.sol

545:     totalShares += _sharesAmount;

582:     totalShares -= _sharesAmount;

```

</details> 
 


 ### <a name="GAS-4"></a>[GAS-4] Use >= instead of > for gas efficiency
Using >= costs less gas than >. Consider using >= when appropriate.

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

153:     if (t.approvers.length > 0) {

264:         if (chainToThresholds[srcChain][i - 1].amount > amounts[i]) {

```

```solidity
File: example/RWADynamicOracle.sol

200:       if (rangeLength > 1 && newEnd > ranges[indexToModify + 1].start)

200:       if (rangeLength > 1 && newEnd > ranges[indexToModify + 1].start)

213:       if (newEnd > ranges[indexToModify + 1].start) revert InvalidRange();

```

```solidity
File: example/rUSDY.sol

429:     require(_USDYAmount > 0, "rUSDY: can't wrap zero USDY tokens");

444:     require(_rUSDYAmount > 0, "rUSDY: can't unwrap zero rUSDY tokens");

```

</details> 
 


 ### <a name="GAS-5"></a>[GAS-5] Use assembly to emit events, in order to save gas
Using the [scratch space](https://github.com/Vectorized/solady/blob/30558f5402f02351b96eeb6eaf32bcea29773841/src/tokens/ERC1155.sol#L501-L504) for event arguments (two words or fewer) will save gas over needing Soliditys full abi memory expansion used for emitting normally.

*Instances (19)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

107:     emit MessageReceived(srcChain, srcSender, amt, nonce);

206:     emit ApproverAdded(approver);

216:     emit ApproverRemoved(approver);

233:     emit ChainIdSupported(srcChain, srcContractAddress);

272:     emit ThresholdSet(srcChain, amounts, numOfApprovers);

345:       emit BridgeCompleted(txn.sender, txn.amount);

```

```solidity
File: example/RWADynamicOracle.sol

163:     emit RangeSet(

228:     emit RangeOverriden(

```

```solidity
File: example/rUSDY.sol

415:     emit TransferShares(msg.sender, _recipient, _sharesAmount);

417:     emit Transfer(msg.sender, _recipient, tokensAmount);

432:     emit Transfer(address(0), msg.sender, getRUSDYByShares(_USDYAmount));

433:     emit TransferShares(address(0), msg.sender, _USDYAmount);

449:     emit TokensBurnt(msg.sender, _rUSDYAmount);

464:     emit Transfer(_sender, _recipient, _amount);

465:     emit TransferShares(_sender, _recipient, _sharesToTransfer);

488:     emit Approval(_owner, _spender, _amount);

588:     emit SharesBurnt(

676:     emit TokensBurnt(_account, _amount);

```

```solidity
File: example/rUSDYFactory.sol

97:     emit rUSDYDeployed(

```

</details> 
 


 


 ### <a name="GAS-7"></a>[GAS-7] Using bools for storage incurs overhead
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

37:   mapping(address => bool) public approvers;

39:   mapping(bytes32 => mapping(uint256 => bool)) public isSpentNonce;

```

</details> 
 


 ### <a name="GAS-8"></a>[GAS-8] Cache array length outside of loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

128:     for (uint256 i = 0; i < thresholds.length; ++i) {

154:       for (uint256 i = 0; i < t.approvers.length; ++i) {

258:     for (uint256 i = 0; i < amounts.length; ++i) {

```

```solidity
File: example/rUSDYFactory.sol

126:     for (uint256 i = 0; i < exCallData.length; ++i) {

```

</details> 
 


 ### <a name="GAS-9"></a>[GAS-9] State variables should be cached in stack variables rather than re-reading them from storage
The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

*Saves 100 gas per instance*

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDYFactory.sol

122:   function multiexcall(

123:     ExCallData[] calldata exCallData

124:   ) external payable override onlyGuardian returns (bytes[] memory results) {

```

</details> 
 


 ### <a name="GAS-10"></a>[GAS-10] Consider using assembly for simple zero checks to save gas
Using assembly for simple zero checks can save gas. Consider using assembly when appropriate.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

259:       if (i == 0) {

```

```solidity
File: example/RWADynamicOracle.sol

197:     if (indexToModify == 0) {

217:     if (indexToModify == 0) {

```

</details> 
 


 ### <a name="GAS-11"></a>[GAS-11] Consider using constant rather than immutable to save gas

#### Impact:
Using constant variables instead of immutable can potentially save gas costs in some cases. You can see it [here](https://docs.soliditylang.org/en/v0.8.21/contracts.html#constant-and-immutable-state-variables)

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

28:   IRWALike public immutable TOKEN;

31:   IAxelarGateway public immutable AXELAR_GATEWAY;

34:   IAllowlist public immutable ALLOWLIST;

```

```solidity
File: example/rUSDYFactory.sol

42:   address internal immutable guardian;

```

</details> 
 


 ### <a name="GAS-12"></a>[GAS-12] Constructors can be marked payable
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn  t provided. A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

49:   constructor(

```

```solidity
File: example/RWADynamicOracle.sol

29:   constructor(

```

```solidity
File: example/rUSDY.sol

99:   constructor() {

```

```solidity
File: example/rUSDYFactory.sol

47:   constructor(address _guardian) {

```

</details> 
 


 ### <a name="GAS-13"></a>[GAS-13] Use Custom Errors
[Source](https://blog.soliditylang.org/2021/04/21/custom-errors/)
Instead of using error strings, to reduce deployment and runtime cost, you should use Custom Errors. This would save both deployment and runtime cost.

*Instances (20)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

301:     require(currentAllowance >= _amount, "TRANSFER_AMOUNT_EXCEEDS_ALLOWANCE");

429:     require(_USDYAmount > 0, "rUSDY: can't wrap zero USDY tokens");

444:     require(_rUSDYAmount > 0, "rUSDY: can't unwrap zero rUSDY tokens");

484:     require(_owner != address(0), "APPROVE_FROM_ZERO_ADDRESS");

485:     require(_spender != address(0), "APPROVE_TO_ZERO_ADDRESS");

513:     require(_sender != address(0), "TRANSFER_FROM_THE_ZERO_ADDRESS");

514:     require(_recipient != address(0), "TRANSFER_TO_THE_ZERO_ADDRESS");

541:     require(_recipient != address(0), "MINT_TO_THE_ZERO_ADDRESS");

573:     require(_account != address(0), "BURN_FROM_THE_ZERO_ADDRESS");

578:     require(_sharesAmount <= accountShares, "BURN_AMOUNT_EXCEEDS_BALANCE");

628:       require(!_isBlocked(msg.sender), "rUSDY: 'sender' address blocked");

629:       require(!_isSanctioned(msg.sender), "rUSDY: 'sender' address sanctioned");

638:       require(!_isBlocked(from), "rUSDY: 'from' address blocked");

639:       require(!_isSanctioned(from), "rUSDY: 'from' address sanctioned");

640:       require(_isAllowed(from), "rUSDY: 'from' address not on allowlist");

645:       require(!_isBlocked(to), "rUSDY: 'to' address blocked");

646:       require(!_isSanctioned(to), "rUSDY: 'to' address sanctioned");

647:       require(_isAllowed(to), "rUSDY: 'to' address not on allowlist");

```

```solidity
File: example/rUSDYFactory.sol

130:       require(success, "Call Failed");

151:     require(msg.sender == guardian, "rUSDYFactory: You are not the Guardian");

```

</details> 
 


 ### <a name="GAS-14"></a>[GAS-14] Don't initialize variables with default value

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

128:     for (uint256 i = 0; i < thresholds.length; ++i) {

154:       for (uint256 i = 0; i < t.approvers.length; ++i) {

258:     for (uint256 i = 0; i < amounts.length; ++i) {

```

```solidity
File: example/RWADynamicOracle.sol

76:     for (uint256 i = 0; i < length; ++i) {

112:     for (uint256 i = 0; i < length; ++i) {

128:     for (uint256 i = 0; i < length + 1; ++i) {

```

```solidity
File: example/rUSDYFactory.sol

126:     for (uint256 i = 0; i < exCallData.length; ++i) {

```

</details> 
 


 ### <a name="GAS-15"></a>[GAS-15] Initializers can be marked as payable to save deployment gas
Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. Initializers can be safely marked as payable, because only the deployer or the factory contract would call the function without carrying any funds.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

103:   function initialize(

```

</details> 
 


 ### <a name="GAS-16"></a>[GAS-16] Use assembly for small keccak256 hashes, in order to save gas
If the arguments to the encode call can fit into the scratch space (two words or fewer), then its more efficient to use assembly to generate the hash (80 gas): keccak256(abi.encodePacked(x, y)) -> assembly {mstore(0x00, a); mstore(0x20, b); let hash := keccak256(0x00, 0x40); }

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

93:     if (chainToApprovedSender[srcChain] != keccak256(abi.encode(srcAddr))) {

232:     chainToApprovedSender[srcChain] = keccak256(abi.encode(srcContractAddress));

```

</details> 
 


 ### <a name="GAS-17"></a>[GAS-17] Long revert strings

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

301:     require(currentAllowance >= _amount, "TRANSFER_AMOUNT_EXCEEDS_ALLOWANCE");

429:     require(_USDYAmount > 0, "rUSDY: can't wrap zero USDY tokens");

444:     require(_rUSDYAmount > 0, "rUSDY: can't unwrap zero rUSDY tokens");

629:       require(!_isSanctioned(msg.sender), "rUSDY: 'sender' address sanctioned");

640:       require(_isAllowed(from), "rUSDY: 'from' address not on allowlist");

647:       require(_isAllowed(to), "rUSDY: 'to' address not on allowlist");

```

```solidity
File: example/rUSDYFactory.sol

151:     require(msg.sender == guardian, "rUSDYFactory: You are not the Guardian");

```

</details> 
 


 ### <a name="GAS-18"></a>[GAS-18] Avoid fetching a low-level calls return data by using assembly
Even if you dont assign the calls second return value, it still gets copied to memory. Use assembly instead to prevent this and save 159 gas: `(bool success,) = payable(receiver).call{gas: gas, value: value}("");` -> `bool success; assembly { success := call(gas, receiver, value, 0, 0, 0, 0)` }

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDYFactory.sol

127:       (bool success, bytes memory ret) = address(exCallData[i].target).call{

```

</details> 
 


 ### <a name="GAS-19"></a>[GAS-19] Reduce gas usage by moving to Solidity 0.8.19 or later
Solidity version 0.8.19 introduced a number of gas optimizations, refer to the [Solidity 0.8.19 Release Announcement](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement) for details.

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/IRWADynamicOracle.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/RWADynamicOracle.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/rUSDY.sol

16: pragma solidity 0.8.16;

```

```solidity
File: example/rUSDYFactory.sol

16: pragma solidity 0.8.16;

```

</details> 
 


 ### <a name="GAS-20"></a>[GAS-20] Functions guaranteed to revert when called by normal users can be marked `payable`
If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

204:   function addApprover(address approver) external onlyOwner {

214:   function removeApprover(address approver) external onlyOwner {

280:   function setMintLimit(uint256 mintLimit) external onlyOwner {

289:   function setMintLimitDuration(uint256 mintDuration) external onlyOwner {

298:   function pause() external onlyOwner {

307:   function unpause() external onlyOwner {

316:   function rescueTokens(address _token) external onlyOwner {

```

```solidity
File: example/RWADynamicOracle.sol

240:   function pauseOracle() external onlyRole(PAUSER_ROLE) {

247:   function unpauseOracle() external onlyRole(DEFAULT_ADMIN_ROLE) {

```

```solidity
File: example/rUSDY.sol

656:   function setOracle(address _oracle) external onlyRole(USDY_MANAGER_ROLE) {

679:   function pause() external onlyRole(PAUSER_ROLE) {

683:   function unpause() external onlyRole(USDY_MANAGER_ROLE) {

```

</details> 
 


 ### <a name="GAS-21"></a>[GAS-21] Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*Instances (11)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

42:   bytes32 public constant VERSION = "1.0";

```

```solidity
File: example/RWADynamicOracle.sol

22:   uint256 public constant DAY = 1 days;

26:   bytes32 public constant SETTER_ROLE = keccak256("SETTER_ROLE");

27:   bytes32 public constant PAUSER_ROLE = keccak256("PAUSER_ROLE");

```

```solidity
File: example/rUSDY.sol

85:   uint256 public constant BPS_DENOMINATOR = 10_000;

91:   bytes32 public constant USDY_MANAGER_ROLE = keccak256("ADMIN_ROLE");

92:   bytes32 public constant MINTER_ROLE = keccak256("MINTER_ROLE");

93:   bytes32 public constant PAUSER_ROLE = keccak256("PAUSER_ROLE");

94:   bytes32 public constant BURNER_ROLE = keccak256("BURN_ROLE");

95:   bytes32 public constant LIST_CONFIGURER_ROLE =

```

```solidity
File: example/rUSDYFactory.sol

40:   bytes32 public constant DEFAULT_ADMIN_ROLE = bytes32(0);

```

</details> 
 


 ### <a name="GAS-22"></a>[GAS-22] require()/revert() strings longer than 32 bytes cost extra gas
Each extra memory word of bytes past the original 32 [incurs an MSTORE](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#consider-having-short-revert-strings) which costs 3 gas.

*Instances (45)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

88:       revert InvalidVersion();

91:       revert ChainNotSupported();

94:       revert SourceNotSupported();

97:       revert NonceSpent();

139:       revert NoThresholdMatch();

156:           revert AlreadyApproved();

193:       revert NotApprover();

255:       revert ArrayLengthMismatch();

265:           revert ThresholdsNotInAscendingOrder();

```

```solidity
File: example/RWADynamicOracle.sol

42:     if (firstRangeStart >= firstRangeEnd) revert InvalidRange();

157:     if (lastRange.end >= endTimestamp) revert InvalidRange();

193:     if (newStart >= newEnd) revert InvalidRange();

201:         revert InvalidRange();

206:       if (newStart < ranges[indexToModify - 1].end) revert InvalidRange();

211:       if (newStart < ranges[indexToModify - 1].end) revert InvalidRange();

213:       if (newEnd > ranges[indexToModify + 1].start) revert InvalidRange();

376:             revert(0, 0)

380:             revert(0, 0)

386:               revert(0, 0)

390:               revert(0, 0)

404:     require(y == 0 || (z = x * y) / y == x);

```

```solidity
File: example/rUSDY.sol

301:     require(currentAllowance >= _amount, "TRANSFER_AMOUNT_EXCEEDS_ALLOWANCE");

352:     require(

429:     require(_USDYAmount > 0, "rUSDY: can't wrap zero USDY tokens");

444:     require(_rUSDYAmount > 0, "rUSDY: can't unwrap zero rUSDY tokens");

446:     if (usdyAmount < BPS_DENOMINATOR) revert UnwrapTooSmall();

484:     require(_owner != address(0), "APPROVE_FROM_ZERO_ADDRESS");

485:     require(_spender != address(0), "APPROVE_TO_ZERO_ADDRESS");

513:     require(_sender != address(0), "TRANSFER_FROM_THE_ZERO_ADDRESS");

514:     require(_recipient != address(0), "TRANSFER_TO_THE_ZERO_ADDRESS");

519:     require(

541:     require(_recipient != address(0), "MINT_TO_THE_ZERO_ADDRESS");

573:     require(_account != address(0), "BURN_FROM_THE_ZERO_ADDRESS");

578:     require(_sharesAmount <= accountShares, "BURN_AMOUNT_EXCEEDS_BALANCE");

628:       require(!_isBlocked(msg.sender), "rUSDY: 'sender' address blocked");

629:       require(!_isSanctioned(msg.sender), "rUSDY: 'sender' address sanctioned");

630:       require(

638:       require(!_isBlocked(from), "rUSDY: 'from' address blocked");

639:       require(!_isSanctioned(from), "rUSDY: 'from' address sanctioned");

640:       require(_isAllowed(from), "rUSDY: 'from' address not on allowlist");

645:       require(!_isBlocked(to), "rUSDY: 'to' address blocked");

646:       require(!_isSanctioned(to), "rUSDY: 'to' address sanctioned");

647:       require(_isAllowed(to), "rUSDY: 'to' address not on allowlist");

```

```solidity
File: example/rUSDYFactory.sol

130:       require(success, "Call Failed");

151:     require(msg.sender == guardian, "rUSDYFactory: You are not the Guardian");

```

</details> 
 


 ### <a name="GAS-23"></a>[GAS-23] Structs can be packed into fewer storage slots
Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

363:   struct Threshold {

368:   struct TxnThreshold {

373:   struct Transaction {

```

```solidity
File: example/RWADynamicOracle.sol

294:   struct Range {

```

</details> 
 


 ### <a name="GAS-24"></a>[GAS-24] Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency
Using uint256(1) and uint256(2) instead of true and false can save gas for certain changes. Consider using uint256(1)/uint256(2) when appropriate.

*Instances (11)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

64:     approvers[_ondoApprover] = true;

100:     isSpentNonce[chainToApprovedSender[srcChain]][nonce] = true;

174:       return true;

176:       return false;

205:     approvers[approver] = true;

340:           true

```

```solidity
File: example/rUSDY.sol

241:     return true;

272:     return true;

305:     return true;

330:     return true;

357:     return true;

```

</details> 
 


 ### <a name="GAS-25"></a>[GAS-25] Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead
Using uints or ints smaller than 32 bytes (256 bits) can incur overhead. Consider using uint256 or int256 to avoid potential issues.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/rUSDY.sol

203:   function decimals() public pure returns (uint8) {

```

</details> 
 


 ### <a name="GAS-26"></a>[GAS-26] Use != 0 instead of > 0 for unsigned integer comparison

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

153:     if (t.approvers.length > 0) {

264:         if (chainToThresholds[srcChain][i - 1].amount > amounts[i]) {

```

```solidity
File: example/RWADynamicOracle.sol

200:       if (rangeLength > 1 && newEnd > ranges[indexToModify + 1].start)

200:       if (rangeLength > 1 && newEnd > ranges[indexToModify + 1].start)

213:       if (newEnd > ranges[indexToModify + 1].start) revert InvalidRange();

```

```solidity
File: example/rUSDY.sol

429:     require(_USDYAmount > 0, "rUSDY: can't wrap zero USDY tokens");

444:     require(_rUSDYAmount > 0, "rUSDY: can't unwrap zero rUSDY tokens");

```

</details> 
 


 ### <a name="GAS-27"></a>[GAS-27] Optimize names to save gas
public/external function names and public member variable names can be optimized to save gas. See [this](https://gist.github.com/IllIllI000/a5d8b486a8259f9f77891a919febd1a9) link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92)

*Instances (58)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/DestinationBridge.sol

28:   IRWALike public immutable TOKEN;

31:   IAxelarGateway public immutable AXELAR_GATEWAY;

34:   IAllowlist public immutable ALLOWLIST;

37:   mapping(address => bool) public approvers;

38:   mapping(string => bytes32) public chainToApprovedSender;

39:   mapping(bytes32 => mapping(uint256 => bool)) public isSpentNonce;

42:   bytes32 public constant VERSION = "1.0";

45:   mapping(bytes32 => TxnThreshold) public txnToThresholdSet;

46:   mapping(string => Threshold[]) public chainToThresholds;

47:   mapping(bytes32 => Transaction) public txnHashToTransaction;

204:   function addApprover(address approver) external onlyOwner {

214:   function removeApprover(address approver) external onlyOwner {

231:   ) external onlyOwner {

253:   ) external onlyOwner {

280:   function setMintLimit(uint256 mintLimit) external onlyOwner {

289:   function setMintLimitDuration(uint256 mintDuration) external onlyOwner {

298:   function pause() external onlyOwner {

307:   function unpause() external onlyOwner {

316:   function rescueTokens(address _token) external onlyOwner {

355:   function getNumApproved(bytes32 txnHash) external view returns (uint256) {

```

```solidity
File: example/IRWADynamicOracle.sol

20:   function getPrice() external view returns (uint256);

```

```solidity
File: example/RWADynamicOracle.sol

22:   uint256 public constant DAY = 1 days;

24:   Range[] public ranges;

26:   bytes32 public constant SETTER_ROLE = keccak256("SETTER_ROLE");

27:   bytes32 public constant PAUSER_ROLE = keccak256("PAUSER_ROLE");

58:     external

74:   function getPrice() public view whenNotPaused returns (uint256 price) {

109:   ) external view returns (uint256 price) {

```

```solidity
File: example/rUSDY.sol

79:   IRWADynamicOracle public oracle;

82:   IUSDY public usdy;

85:   uint256 public constant BPS_DENOMINATOR = 10_000;

91:   bytes32 public constant USDY_MANAGER_ROLE = keccak256("ADMIN_ROLE");

92:   bytes32 public constant MINTER_ROLE = keccak256("MINTER_ROLE");

93:   bytes32 public constant PAUSER_ROLE = keccak256("PAUSER_ROLE");

94:   bytes32 public constant BURNER_ROLE = keccak256("BURN_ROLE");

95:   bytes32 public constant LIST_CONFIGURER_ROLE =

110:   ) public virtual initializer {

188:   function name() public pure returns (string memory) {

196:   function symbol() public pure returns (string memory) {

203:   function decimals() public pure returns (uint8) {

210:   function totalSupply() public view returns (uint256) {

220:   function balanceOf(address _account) public view returns (uint256) {

253:   ) public view returns (uint256) {

366:   function getTotalShares() public view returns (uint256) {

375:   function sharesOf(address _account) public view returns (uint256) {

384:   ) public view returns (uint256) {

391:   function getRUSDYByShares(uint256 _shares) public view returns (uint256) {

428:   function wrap(uint256 _USDYAmount) external whenNotPaused {

443:   function unwrap(uint256 _rUSDYAmount) external whenNotPaused {

694:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

705:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

716:   ) external override onlyRole(LIST_CONFIGURER_ROLE) {

```

```solidity
File: example/rUSDYFactory.sol

40:   bytes32 public constant DEFAULT_ADMIN_ROLE = bytes32(0);

43:   rUSDY public rUSDYImplementation;

44:   ProxyAdmin public rUSDYProxyAdmin;

45:   TokenProxy public rUSDYProxy;

77:   ) external onlyGuardian returns (address, address, address) {

124:   ) external payable override onlyGuardian returns (bytes[] memory results) {

```

</details> 
 

