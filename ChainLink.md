# Report


## Medium Issues


| |Issue|Instances|
|-|:-|:-:|
| [M-1](#M-1) | Strings should use double quotes rather than single quotes | 86 |
| [M-2](#M-2) | Centralization Risk for trusted owners | 53 |
| [M-3](#M-3) | Unsafe use of ERC20 transferFrom() | 4 |
| [M-4](#M-4) | Unsafe use of ERC20 transfer() | 12 |
| [M-5](#M-5) | Timestamp may be manipulation | 37 |

## Low Issues


| |Issue|Instances|
|-|:-|:-:|
| [L-1](#L-1) | Division by zero not prevented | 6 |
| [L-2](#L-2) | Empty function body | 5 |
| [L-3](#L-3) | Loss of precision | 6 |
| [L-4](#L-4) | State variables not capped at reasonable values | 181 |
| [L-5](#L-5) | Some tokens may revert when zero value transfers are made | 12 |
| [L-6](#L-6) |  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard   | 12 |
| [L-7](#L-7) | Some tokens may revert when large transfers are made | 12 |
| [L-8](#L-8) | Unsafe downcast | 18 |
| [L-9](#L-9) | Unsafe ERC20 operation(s) | 16 |

## Non Critical Issues


| |Issue|Instances|
|-|:-|:-:|
| [NC-1](#NC-1) | Custom error has no error details | 61 |
| [NC-2](#NC-2) | Variables without visibility specifier | 93 |
| [NC-3](#NC-3) | Constants in comparisons should appear on the left side | 160 |
| [NC-4](#NC-4) | Consider using delete rather than assigning zero to clear value | 2 |
| [NC-5](#NC-5) | Consider using delete rather than assigning false to clear value | 4 |
| [NC-6](#NC-6) | Consider adding a block/deny-list" | 9 |
| [NC-7](#NC-7) | Events are missing sender information | 64 |
| [NC-8](#NC-8) | Events should use parameters to convey information | 5 |
| [NC-9](#NC-9) | If-statement can be converted to a ternary | 126 |
| [NC-10](#NC-10) | Variable names for immutables should use CONSTANT_CASE | 24 |
| [NC-11](#NC-11) | Imports should use double quotes rather than single quotes | 77 |
| [NC-12](#NC-12) | Consider using named mappings | 10 |
| [NC-13](#NC-13) | Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct | 10 |
| [NC-14](#NC-14) | Use of override is unnecessary | 107 |
| [NC-15](#NC-15) | Consider using descriptive constants when passing zero as a function argument | 15 |
| [NC-16](#NC-16) | Non-external/public variable names should begin with an underscore | 32 |
| [NC-17](#NC-17) |  `require()` / `revert()` statements should have descriptive reason strings | 13 |
| [NC-18](#NC-18) | Use the latest solidity version for deployment   | 22 |
| [NC-19](#NC-19) | Event is missing `indexed` fields | 18 |
| [NC-20](#NC-20) | Functions not used internally could be marked external | 3 |
| [NC-21](#NC-21) | Consider moving msg.sender checks to modifiers | 68 |
| [NC-22](#NC-22) | Array indices should be referenced via enums rather than numeric literals | 3 |

## Gas Optimizations


| |Issue|Instances|
|-|:-|:-:|
| [GAS-1](#GAS-1) | Nesting if-statements is cheaper than using && | 30 |
| [GAS-2](#GAS-2) | Consider using = instead of += and -= for gas efficiency | 50 |
| [GAS-3](#GAS-3) | Use >= instead of > for gas efficiency | 32 |
| [GAS-4](#GAS-4) | Use assembly to emit events, in order to save gas | 68 |
| [GAS-5](#GAS-5) | Using bools for storage incurs overhead | 1 |
| [GAS-6](#GAS-6) | Cache array length outside of loop | 12 |
| [GAS-7](#GAS-7) | Use calldata instead of memory for function arguments that do not get mutated | 3 |
| [GAS-8](#GAS-8) | Consider using assembly for simple zero checks to save gas | 20 |
| [GAS-9](#GAS-9) | Consider using constant rather than immutable to save gas | 24 |
| [GAS-10](#GAS-10) | Constructors can be marked payable | 8 |
| [GAS-11](#GAS-11) | Use assembly for small keccak256 hashes, in order to save gas | 3 |
| [GAS-12](#GAS-12) | Reduce gas usage by moving to Solidity 0.8.19 or later | 22 |
| [GAS-13](#GAS-13) | Functions guaranteed to revert when called by normal users can be marked `payable` | 23 |
| [GAS-14](#GAS-14) | `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too) | 3 |
| [GAS-15](#GAS-15) | Using `private` rather than `public` for constants, saves gas | 3 |
| [GAS-16](#GAS-16) | require()/revert() strings longer than 32 bytes cost extra gas | 157 |
| [GAS-17](#GAS-17) | Structs can be packed into fewer storage slots | 34 |
| [GAS-18](#GAS-18) | Use storage instead of memory for structs/arrays | 6 |
| [GAS-19](#GAS-19) | Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency | 34 |
| [GAS-20](#GAS-20) | Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead | 4 |
| [GAS-21](#GAS-21) | Use != 0 instead of > 0 for unsigned integer comparison | 32 |
| [GAS-22](#GAS-22) | `internal` functions not called by the contract should be removed | 12 |
| [GAS-23](#GAS-23) | Optimize names to save gas | 159 |

##################################################################### 
 
 DETAILED REPORT:: 


##################################################################### 


## Medium Issues


 ### <a name="M-1"></a>[M-1] Strings should use double quotes rather than single quotes

#### Impact:
Using consistent double quotes for strings improves code readability and maintainability. Also see it here https://docs.soliditylang.org/en/v0.8.20/style-guide.html#other-recommendations

*Instances (86)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

5:   '@chainlink/contracts/src/v0.8/interfaces/ERC677ReceiverInterface.sol';

7:   '@chainlink/contracts/src/v0.8/interfaces/TypeAndVersionInterface.sol';

9: import {MerkleProof} from '@openzeppelin/contracts/utils/cryptography/MerkleProof.sol';

11: import {IMerkleAccessController} from '../interfaces/IMerkleAccessController.sol';

12: import {OperatorStakingPool} from './OperatorStakingPool.sol';

13: import {StakingPoolBase} from './StakingPoolBase.sol';

150:     return 'CommunityStakingPool 1.0.0';

```

```solidity
File: example/IStakingPool.sol

4: import {IRewardVault} from './IRewardVault.sol';

5: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

```

```solidity
File: example/Migratable.sol

4: import {IMigratable} from './interfaces/IMigratable.sol';

```

```solidity
File: example/MigrationProxy.sol

5:   '@chainlink/contracts/src/v0.8/interfaces/ERC677ReceiverInterface.sol';

6: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

8:   '@chainlink/contracts/src/v0.8/interfaces/TypeAndVersionInterface.sol';

10: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

12: import {PausableWithAccessControl} from './PausableWithAccessControl.sol';

13: import {CommunityStakingPool} from './pools/CommunityStakingPool.sol';

14: import {OperatorStakingPool} from './pools/OperatorStakingPool.sol';

```

```solidity
File: example/OperatorStakingPool.sol

5:   '@chainlink/contracts/src/v0.8/interfaces/TypeAndVersionInterface.sol';

8:   '@openzeppelin/contracts/access/AccessControlDefaultAdminRules.sol';

9: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

10: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

12: import {ISlashable} from '../interfaces/ISlashable.sol';

13: import {IRewardVault} from '../interfaces/IRewardVault.sol';

14: import {RewardVault} from '../rewards/RewardVault.sol';

15: import {StakingPoolBase} from './StakingPoolBase.sol';

142:   bytes32 public constant SLASHER_ROLE = keccak256('SLASHER_ROLE');

157:     whenBeforeClosing //@audit why can't anyone add money

604:     return 'OperatorStakingPool 1.0.0';

```

```solidity
File: example/PausableWithAccessControl.sol

5:   '@openzeppelin/contracts/access/AccessControlDefaultAdminRules.sol';

6: import {Pausable} from '@openzeppelin/contracts/security/Pausable.sol';

8: import {IPausable} from './interfaces/IPausable.sol';

14:   bytes32 public constant PAUSER_ROLE = keccak256('PAUSER_ROLE');

```

```solidity
File: example/PriceFeedAlertsController.sol

5:   '@chainlink/contracts/src/v0.8/interfaces/AggregatorV3Interface.sol';

7:   '@chainlink/contracts/src/v0.8/interfaces/TypeAndVersionInterface.sol';

9: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

10: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

12: import {IMigratable} from '../interfaces/IMigratable.sol';

13: import {IMigrationDataReceiver} from '../interfaces/IMigrationDataReceiver.sol';

14: import {Migratable} from '../Migratable.sol';

15: import {PausableWithAccessControl} from '../PausableWithAccessControl.sol';

16: import {CommunityStakingPool} from '../pools/CommunityStakingPool.sol';

17: import {OperatorStakingPool} from '../pools/OperatorStakingPool.sol';

546:     } //@audit-ok - what's the difference btw regular alert and prority alert cause return value is same

589:     return 'PriceFeedAlertsController 1.0.0';

```

```solidity
File: example/RewardLib.sol

4: import {StakingPoolLib} from './StakingPoolLib.sol';

5: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

```

```solidity
File: example/RewardVault.sol

5:   '@chainlink/contracts/src/v0.8/interfaces/ERC677ReceiverInterface.sol';

6: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

8:   '@chainlink/contracts/src/v0.8/interfaces/TypeAndVersionInterface.sol';

10: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

11: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

13: import {FixedPointMathLib} from '@solmate/utils/FixedPointMathLib.sol';

15: import {IMigratable} from '../interfaces/IMigratable.sol';

16: import {IRewardVault} from '../interfaces/IRewardVault.sol';

17: import {IStakingPool} from '../interfaces/IStakingPool.sol';

18: import {Migratable} from '../Migratable.sol';

19: import {PausableWithAccessControl} from '../PausableWithAccessControl.sol';

20: import {CommunityStakingPool} from '../pools/CommunityStakingPool.sol';

21: import {OperatorStakingPool} from '../pools/OperatorStakingPool.sol';

284:   bytes32 public constant REWARDER_ROLE = keccak256('REWARDER_ROLE');

```

```solidity
File: example/Staking.sol

4: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

6:   '@chainlink/contracts/src/v0.8/interfaces/TypeAndVersionInterface.sol';

8:   '@chainlink/contracts/src/v0.8/interfaces/AggregatorV3Interface.sol';

9: import {ConfirmedOwner} from '@chainlink/contracts/src/v0.8/ConfirmedOwner.sol';

10: import {Pausable} from '@openzeppelin/contracts/security/Pausable.sol';

11: import {MerkleProof} from '@openzeppelin/contracts/utils/cryptography/MerkleProof.sol';

12: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

13: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

14: import {IStaking} from './IStaking.sol';

15: import {IStakingOwner} from './IStakingOwner.sol';

16: import {IMerkleAccessController} from './IMerkleAccessController.sol';

17: import {IAlertsController} from './IAlertsController.sol';

18: import {IMigratable} from './IMigratable.sol';

19: import {StakingPoolLib} from './StakingPoolLib.sol';

20: import {RewardLib, SafeCast} from './RewardLib.sol';

169:     return 'Staking 0.1.0';

```

```solidity
File: example/StakingPoolBase.sol

5:   '@chainlink/contracts/src/v0.8/interfaces/ERC677ReceiverInterface.sol';

6: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

8: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

9: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

11: import {IMigratable} from '../interfaces/IMigratable.sol';

12: import {IRewardVault} from '../interfaces/IRewardVault.sol';

13: import {IStakingOwner} from '../interfaces/IStakingOwner.sol';

14: import {IStakingPool} from '../interfaces/IStakingPool.sol';

15: import {Migratable} from '../Migratable.sol';

16: import {PausableWithAccessControl} from '../PausableWithAccessControl.sol';

```

</details> 
 


 ### <a name="M-2"></a>[M-2] Centralization Risk for trusted owners

#### Impact:
Contracts have owners with privileged rights to perform admin tasks and need to be trusted to not perform malicious updates or drain funds.

*Instances (53)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

121:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyRole(DEFAULT_ADMIN_ROLE) {

136:     onlyRole(DEFAULT_ADMIN_ROLE)

```

```solidity
File: example/MigrationProxy.sol

24:   PausableWithAccessControl,

64:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

```

```solidity
File: example/OperatorStakingPool.sol

156:     onlyRole(DEFAULT_ADMIN_ROLE)

173:   function withdrawAlerterReward(uint256 amount) external onlyRole(DEFAULT_ADMIN_ROLE) { @audit uint ko kaam kar do

221:   ) external override onlyRole(DEFAULT_ADMIN_ROLE) {

231:   ) external override onlyRole(DEFAULT_ADMIN_ROLE) {

409:     onlyRole(DEFAULT_ADMIN_ROLE)

435:     onlyRole(DEFAULT_ADMIN_ROLE)

476:     onlyRole(DEFAULT_ADMIN_ROLE)

```

```solidity
File: example/PausableWithAccessControl.sol

10: abstract contract PausableWithAccessControl is IPausable, Pausable, AccessControlDefaultAdminRules {

22:   function emergencyPause() external override onlyRole(PAUSER_ROLE) {

27:   function emergencyUnpause() external override onlyRole(PAUSER_ROLE) {

```

```solidity
File: example/PriceFeedAlertsController.sol

28:   PausableWithAccessControl,

231:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

263:     onlyRole(DEFAULT_ADMIN_ROLE)

276:     onlyRole(DEFAULT_ADMIN_ROLE)

290:     onlyRole(DEFAULT_ADMIN_ROLE) //@audit - what if the length of configs is 0? or too big

299:   function removeFeedConfig(address feed) external onlyRole(DEFAULT_ADMIN_ROLE) {

376:   ) external onlyRole(DEFAULT_ADMIN_ROLE) {

404:     onlyRole(DEFAULT_ADMIN_ROLE)

421:     onlyRole(DEFAULT_ADMIN_ROLE)

440:     onlyRole(DEFAULT_ADMIN_ROLE)

```

```solidity
File: example/RewardVault.sol

41:   PausableWithAccessControl,

309:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

385:     onlyRole(DEFAULT_ADMIN_ROLE)

455:     onlyRole(DEFAULT_ADMIN_ROLE)

466:   function setMigrationSource(address newMigrationSource) external onlyRole(DEFAULT_ADMIN_ROLE) {

490:     onlyRole(DEFAULT_ADMIN_ROLE)

511:     onlyRole(DEFAULT_ADMIN_ROLE)

792:   function close() external override onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

```

```solidity
File: example/Staking.sol

183:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyOwner {

202:   ) external override(IStakingOwner) onlyOwner whenActive {

228:   ) external override(IStakingOwner) onlyOwner {

246:   function conclude() external override(IStakingOwner) onlyOwner whenActive {

253:   function addReward(uint256 amount) external override(IStakingOwner) onlyOwner whenActive {

271:   function withdrawUnusedReward() external override(IStakingOwner) onlyOwner whenInactive {

287:   function addOperators(address[] calldata operators) external override(IStakingOwner) onlyOwner {

359:   function changeRewardRate(uint256 newRate) external override onlyOwner whenActive {

379:   function emergencyPause() external override(IStakingOwner) onlyOwner {

384:   function emergencyUnpause() external override(IStakingOwner) onlyOwner {

403:   function proposeMigrationTarget(address migrationTarget) external override(IMigratable) onlyOwner {

417:   function acceptMigrationTarget() external override(IMigratable) onlyOwner {

```

```solidity
File: example/StakingPoolBase.sol

197:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

260:     onlyRole(DEFAULT_ADMIN_ROLE)

294:   function setUnbondingPeriod(uint256 newUnbondingPeriod) external onlyRole(DEFAULT_ADMIN_ROLE) {

307:   function setClaimPeriod(uint256 claimPeriod) external onlyRole(DEFAULT_ADMIN_ROLE) {

314:   function setRewardVault(IRewardVault newRewardVault) external onlyRole(DEFAULT_ADMIN_ROLE) {

402:   ) external virtual override onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

411:     onlyRole(DEFAULT_ADMIN_ROLE)

424:   function close() external override(IStakingOwner) onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

435:   function setMigrationProxy(address migrationProxy) external override onlyRole(DEFAULT_ADMIN_ROLE) {

```

</details> 
 


 ### <a name="M-3"></a>[M-3] Unsafe use of ERC20 transferFrom()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transferFrom() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransferFrom() from OpenZeppelin instead.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

163:     i_LINK.transferFrom({from: msg.sender, to: address(this), value: amount});

```

```solidity
File: example/RewardVault.sol

369:     i_LINK.transferFrom({from: msg.sender, to: address(this), value: amount});

```

```solidity
File: example/Staking.sol

235:     i_LINK.transferFrom(msg.sender, address(this), amount);

256:     i_LINK.transferFrom(msg.sender, address(this), amount);

```

</details> 
 


 ### <a name="M-4"></a>[M-4] Unsafe use of ERC20 transfer()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transfer() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransfer() from OpenZeppelin instead.

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

117:     i_LINK.transfer(staker, amountToWithdraw);

```

```solidity
File: example/OperatorStakingPool.sol

181:     i_LINK.transfer(msg.sender, amount);

369:     i_LINK.transfer(alerter, alerterRewardActual);

552:     i_LINK.transfer(msg.sender, withdrawableAmount);

```

```solidity
File: example/RewardVault.sol

678:     i_LINK.transfer(staker, claimableReward);

797:     i_LINK.transfer(msg.sender, totalUnvestedRewards);

```

```solidity
File: example/Staking.sol

277:     i_LINK.transfer(msg.sender, unusedRewards);

488:     i_LINK.transfer(msg.sender, rewardAmount);

532:     i_LINK.transfer(msg.sender, amount + baseReward + delegationReward);

543:     i_LINK.transfer(msg.sender, amount);

698:       i_LINK.transfer(sender, remainder);

```

```solidity
File: example/StakingPoolBase.sol

501:     i_LINK.transfer(msg.sender, amount);

```

</details> 
 


 ### <a name="M-5"></a>[M-5] Timestamp may be manipulation
The block.timestamp can be manipulated by miners to perform MEV profiting or other time-based attacks.

*Instances (37)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

251:     state.lastSlashTimestamp = block.timestamp;

298:     s_slasherState[msg.sender].lastSlashTimestamp = block.timestamp;

382:       (block.timestamp - slasherState.lastSlashTimestamp) * slasherConfig.refillRate;

```

```solidity
File: example/PriceFeedAlertsController.sol

536:     if (block.timestamp < updatedAt + feedConfig.priorityPeriodThreshold) 

543:     if (block.timestamp >= updatedAt + feedConfig.regularPeriodThreshold) {

```

```solidity
File: example/RewardLib.sol

123:     uint32 blockTimestamp = block.timestamp._toUint32();

135:     return reward.endTimestamp <= block.timestamp;

182:       : block.timestamp - uint256(reward.delegated.lastAccumulateTimestamp);

202:       : block.timestamp - uint256(reward.base.lastAccumulateTimestamp);

302:     reward.endTimestamp = block.timestamp;

328:     return _isDepleted(reward) ? 0 : reward.endTimestamp - block.timestamp;

384:     reward.endTimestamp = block.timestamp + availableRewardDuration;

541:     return Math.min(uint256(reward.endTimestamp), block.timestamp);

```

```solidity
File: example/RewardVault.sol

825:       return s_rewardBuckets.operatorBase.rewardDurationEndsAt <= block.timestamp

826:         && s_rewardBuckets.operatorDelegated.rewardDurationEndsAt <= block.timestamp;

829:       return s_rewardBuckets.communityBase.rewardDurationEndsAt <= block.timestamp;

1030:       FixedPointMathLib.divWadDown(block.timestamp - stakedAt, multiplierDuration), MAX_MULTIPLIER

1104:     bucket.rewardDurationEndsAt = block.timestamp.toUint80();

1180:     bucket.rewardDurationEndsAt = (block.timestamp + (rewardAmount / emissionRate)).toUint80();

1339:     if (s_rewardPerTokenUpdatedAt < block.timestamp) {

1351:       s_rewardPerTokenUpdatedAt = block.timestamp;

1387:     uint256 latestRewardEmittedAt = Math.min(rewardBucket.rewardDurationEndsAt, block.timestamp);

1672:     return bucket.rewardDurationEndsAt <= block.timestamp

1674:       : bucket.emissionRate * (bucket.rewardDurationEndsAt - block.timestamp);

```

```solidity
File: example/Staking.sol

412:     s_proposedMigrationTargetAt = block.timestamp;

422:     if (block.timestamp < (uint256(s_proposedMigrationTargetAt) + 7 days)) {

459:     if (block.timestamp < lastFeedUpdatedAt + i_priorityPeriodThreshold) {

463:     bool isInPriorityPeriod = block.timestamp < lastFeedUpdatedAt + i_regularPeriodThreshold;

516:     if (block.timestamp < updatedAt + i_priorityPeriodThreshold) return false;

519:     if (block.timestamp >= updatedAt + i_regularPeriodThreshold) return true;

```

```solidity
File: example/StakingPoolBase.sol

282:     if (staker.unbondingPeriodEndsAt != 0 && block.timestamp <= staker.claimPeriodEndsAt) {

285:     staker.unbondingPeriodEndsAt = (block.timestamp + s_pool.configs.unbondingPeriod).toUint128();

426:     s_pool.state.closedAt = block.timestamp;

497:       latestStakedAtTime: updatedPrincipal == 0 ? 0 : block.timestamp

693:       latestStakedAtTime: block.timestamp

725:     if (staker.unbondingPeriodEndsAt == 0 || block.timestamp < staker.unbondingPeriodEndsAt) {

729:     return block.timestamp <= staker.claimPeriodEndsAt;

```

</details> 
 


## Low Issues


 ### <a name="L-1"></a>[L-1] Division by zero not prevented
The divisions below take an input parameter that has no zero-value checks, which can cause the functions reverting if zero is passed.  

*Instances (6)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RewardLib.sol

169:     return (amount * uint256(reward.base.rate) * duration) / REWARD_PRECISION;

210:     ) / REWARD_PRECISION;

312:     return amount / delegationRateDenominator;

```

```solidity
File: example/RewardVault.sol

397:       : communityRateWithoutDelegation / newDelegationRateDenominator;

430:       uint256 delegatedRewards = unvestedRewards / newDelegationRateDenominator;

937:       forfeitedRewardAmount = forfeitedRewardAmountTimesUnstakedAmount / oldPrincipal;

```

</details> 
 


 ### <a name="L-2"></a>[L-2] Empty function body
Consider adding a comment about why the function body is empty

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/PausableWithAccessControl.sol

19:   ) AccessControlDefaultAdminRules(adminRoleTransferDelay, defaultAdmin) {}

```

```solidity
File: example/RewardLib.sol

545:   function test() public {}

```

```solidity
File: example/RewardVault.sol

1506:     if (stakerReward.stakerType != StakerType.NOT_STAKED) {

```

```solidity
File: example/Staking.sol

912:   function test() public {}

```

```solidity
File: example/StakingPoolLib.sol

276:   function test() public {}

```

</details> 
 


 ### <a name="L-3"></a>[L-3] Loss of precision
Division by large numbers or variables may result in the result being zero, due to Solidity not supporting fractions.

*Instances (6)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RewardLib.sol

169:     return (amount * uint256(reward.base.rate) * duration) / REWARD_PRECISION;

210:     ) / REWARD_PRECISION;

312:     return amount / delegationRateDenominator;

```

```solidity
File: example/RewardVault.sol

397:       : communityRateWithoutDelegation / newDelegationRateDenominator;

430:       uint256 delegatedRewards = unvestedRewards / newDelegationRateDenominator;

937:       forfeitedRewardAmount = forfeitedRewardAmountTimesUnstakedAmount / oldPrincipal;

```

</details> 
 


 ### <a name="L-4"></a>[L-4] State variables not capped at reasonable values
Consider adding minimum/maximum value checks to ensure that the state variables below can never be used to excessively harm users, including via griefing

*Instances (181)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

35:     ConstructorParamsBase baseParams;

37:     OperatorStakingPool operatorStakingPool;

128:     return s_merkleRoot;

```

```solidity
File: example/IRewardVault.sol

21:     uint112 finalizedBaseReward;

26:     uint112 finalizedDelegatedReward;

29:     uint112 baseRewardPerToken;

31:     uint112 operatorDelegatedRewardPerToken;

40:     uint112 claimedBaseRewardsInPeriod;

45:     StakerType stakerType;

64:     uint256 storedBaseReward;

76:     uint256 earnedBaseRewardInPeriod;

```

```solidity
File: example/ISlashable.sol

21:     uint256 refillRate;

23:     uint256 slashCapacity;

31:     uint256 lastSlashTimestamp;

33:     uint256 remainingSlashCapacityAmount;

```

```solidity
File: example/IStakingPool.sol

91:     uint128 unbondingPeriodEndsAt;

93:     uint128 claimPeriodEndsAt;

```

```solidity
File: example/Migratable.sol

33:     return s_migrationTarget;

```

```solidity
File: example/MigrationProxy.sol

43:     LinkTokenInterface LINKAddress;

45:     address v01StakingAddress;

47:     OperatorStakingPool operatorStakingPool;

49:     CommunityStakingPool communityStakingPool;

51:     uint48 adminRoleTransferDelay;

```

```solidity
File: example/OperatorStakingPool.sol

109:     ConstructorParamsBase baseParams;

112:     uint256 minInitialOperatorCount;

118:     uint256 removedPrincipal;

120:     bool isOperator;

122:     bool isRemoved;

188:     return s_alerterRewardFunds;

317:     uint256 totalSlashedAmount;

343: 

559:     return s_numOperators;

```

```solidity
File: example/PriceFeedAlertsController.sol

118:     CommunityStakingPool communityStakingPool;

120:     OperatorStakingPool operatorStakingPool;

124:     uint48 adminRoleTransferDelay;

130:     address feed;

135:     uint32 priorityPeriodThreshold;

140:     uint32 regularPeriodThreshold;

144:     uint96 slashableAmount;

148:     uint96 alerterRewardAmount;

156:     address feed;

161:     uint32 priorityPeriodThreshold;

166:     uint32 regularPeriodThreshold;

170:     uint96 slashableAmount;

174:     uint96 alerterRewardAmount;

183:     uint32 priorityPeriodThreshold;

188:     uint32 regularPeriodThreshold;

192:     uint96 slashableAmount;

196:     uint96 alerterRewardAmount;

203:     address feed;

205:     uint256 roundId;

212:     bool canAlert;

214:     uint256 roundId;

216:     FeedConfig feedConfig;

365:     return pools;

537:       return returnValues; //@audit - QA what if the feed is stale but the timestamp is not updated yet

545:       return returnValues;

551:       return returnValues;

```

```solidity
File: example/RewardLib.sol

49:     uint8 delegatesCount;

54:     uint96 cumulativePerDelegate;

57:     uint32 lastAccumulateTimestamp;

62:     uint80 rate;

66:     uint96 cumulativePerMicroLINK;

68:     uint32 lastAccumulateTimestamp;

73:     uint96 base;

75:     uint96 delegated;

83:     uint96 base;

88:     uint96 delegated;

93:     DelegatedRewards delegated;

94:     BaseRewards base;

95:     ReservedRewards reserved;

99:     uint256 endTimestamp;

102:     uint32 startTimestamp;

428: 

430:     uint256 totalSlashedDelegatedReward;

494:     return slashedRewards;

511:     return slashedRewards;

```

```solidity
File: example/RewardVault.sol

202:     LinkTokenInterface linkToken;

204:     CommunityStakingPool communityStakingPool;

206:     OperatorStakingPool operatorStakingPool;

208:     uint32 delegationRateDenominator;

210:     uint32 initialMultiplierDuration;

212:     uint48 adminRoleTransferDelay;

218:     uint80 emissionRate;

220:     uint80 rewardDurationEndsAt;

224:     uint80 vestedRewardPerToken;

230:     RewardBucket operatorBase;

232:     RewardBucket communityBase;

234:     RewardBucket operatorDelegated;

240:     uint32 delegationRateDenominator;

242:     uint32 multiplierDuration;

244:     bool isOpen;

252:     uint256 operatorPoolTotalPrincipal;

255:     uint256 communityPoolTotalPrincipal;

258:     uint256 operatorPoolCheckpointId;

261:     uint256 communityPoolCheckpointId;

268:     uint256 communityReward;

270:     uint256 operatorReward;

272:     uint256 operatorDelegatedReward;

274:     uint256 communityRate;

276:     uint256 operatorRate;

278:     uint256 delegatedRate;

478:     return s_migrationSource;

570:     delete s_migrationSource;

655: 

680: 

766: 

784: 

843:     return s_rewardBuckets;

849:     return s_rewardPerTokenUpdatedAt;

886:     return s_finalVestingCheckpointData;

926:     uint256 forfeitedRewardAmount;

1105:     return unvestedRewards;

1228: 

1230:     uint256 delegatedRate;

1413: 

1432: 

1473: 

1534: 

1583: 

1585:     uint256 vestedRewardPerToken;

1586:     uint256 reclaimableReward;

```

```solidity
File: example/Staking.sol

40:     LinkTokenInterface LINKAddress;

42:     AggregatorV3Interface monitoredFeed;

44:     uint256 initialMaxPoolSize;

46:     uint256 initialMaxCommunityStakeAmount;

48:     uint256 initialMaxOperatorStakeAmount;

50:     uint256 minCommunityStakeAmount;

52:     uint256 minOperatorStakeAmount;

55:     uint256 priorityPeriodThreshold;

58:     uint256 regularPeriodThreshold;

61:     uint256 maxAlertingRewardAmount;

64:     uint256 minInitialOperatorCount;

67:     uint256 minRewardDuration;

69:     uint256 slashableDuration;

72:     uint256 delegationRateDenominator;

190:     return s_merkleRoot;

399:     return s_migrationTarget;

588:     return i_delegationRateDenominator;

```

```solidity
File: example/StakingPoolBase.sol

113:     LinkTokenInterface LINKAddress;

116:     uint96 initialMaxPoolSize;

118:     uint96 initialMaxPrincipalPerStaker;

120:     uint96 minPrincipalPerStaker;

122:     uint32 initialUnbondingPeriod;

124:     uint32 maxUnbondingPeriod;

126:     uint32 initialClaimPeriod;

128:     uint32 minClaimPeriod;

130:     uint32 maxClaimPeriod;

132:     uint48 adminRoleTransferDelay;

140:     uint96 maxPoolSize;

144:     uint96 maxPrincipalPerStaker;

148:     uint32 unbondingPeriod;

152:     uint32 claimPeriod;

158:     uint256 totalPrincipal;

160:     uint256 closedAt;

166:     PoolConfigs configs;

168:     PoolState state;

515:     return stakerPrincipal;

527:     return stakerPrincipal;

534:     return stakerStakedAtTime;

546:     return stakerStakedAtTime;

551:     return s_rewardVault;

561:     return s_migrationProxy;

566:     return s_isOpen;

610:     return s_checkpointId;

707: 

726:       return false;

```

```solidity
File: example/StakingPoolLib.sol

91:     uint96 maxPoolSize;

93:     uint80 maxCommunityStakeAmount;

95:     uint80 maxOperatorStakeAmount;

100:     bool isOpen;

102:     uint8 operatorsCount;

104:     uint96 totalCommunityStakedAmount;

106:     uint96 totalOperatorStakedAmount;

111:     bool isOperator;

113:     bool isFeedOperator;

115:     uint96 stakedAmount;

119:     uint96 removedStakeAmount;

125:     PoolState state;

126:     PoolLimits limits;

130:     uint256 totalOperatorRemovedAmount;

```

</details> 
 


 ### <a name="L-5"></a>[L-5] Some tokens may revert when zero value transfers are made
Despite the fact that [EIP-20](https://github.com/ethereum/EIPs/blob/7500ac4fc1bbdfaf684e7ef851f798f6b667b2fe/EIPS/eip-20.md?plain=1#L116) states that zero-value transfers must be accepted, some tokens, such as LEND, will revert if this is attempted, which may cause transactions that involve other tokens (such as batch operations) to fully revert. Consider skipping the transfer if the amount is zero, which will also save gas.

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

117:     i_LINK.transfer(staker, amountToWithdraw);

```

```solidity
File: example/OperatorStakingPool.sol

181:     i_LINK.transfer(msg.sender, amount);

369:     i_LINK.transfer(alerter, alerterRewardActual);

552:     i_LINK.transfer(msg.sender, withdrawableAmount);

```

```solidity
File: example/RewardVault.sol

678:     i_LINK.transfer(staker, claimableReward);

797:     i_LINK.transfer(msg.sender, totalUnvestedRewards);

```

```solidity
File: example/Staking.sol

277:     i_LINK.transfer(msg.sender, unusedRewards);

488:     i_LINK.transfer(msg.sender, rewardAmount);

532:     i_LINK.transfer(msg.sender, amount + baseReward + delegationReward);

543:     i_LINK.transfer(msg.sender, amount);

698:       i_LINK.transfer(sender, remainder);

```

```solidity
File: example/StakingPoolBase.sol

501:     i_LINK.transfer(msg.sender, amount);

```

</details> 
 


 ### <a name="L-6"></a>[L-6]  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard  
Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks opens the users of this protocol up to [read-only reentrancy](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) vulnerability with no way to protect them except by block-listing the entire protocol.

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

117:     i_LINK.transfer(staker, amountToWithdraw);

```

```solidity
File: example/OperatorStakingPool.sol

181:     i_LINK.transfer(msg.sender, amount);

369:     i_LINK.transfer(alerter, alerterRewardActual);

552:     i_LINK.transfer(msg.sender, withdrawableAmount);

```

```solidity
File: example/RewardVault.sol

678:     i_LINK.transfer(staker, claimableReward);

797:     i_LINK.transfer(msg.sender, totalUnvestedRewards);

```

```solidity
File: example/Staking.sol

277:     i_LINK.transfer(msg.sender, unusedRewards);

488:     i_LINK.transfer(msg.sender, rewardAmount);

532:     i_LINK.transfer(msg.sender, amount + baseReward + delegationReward);

543:     i_LINK.transfer(msg.sender, amount);

698:       i_LINK.transfer(sender, remainder);

```

```solidity
File: example/StakingPoolBase.sol

501:     i_LINK.transfer(msg.sender, amount);

```

</details> 
 


 ### <a name="L-7"></a>[L-7] Some tokens may revert when large transfers are made
Tokens such as COMP or UNI will revert when an address balance reaches type(uint96).max. Ensure that the calls below can be broken up into smaller batches if necessary.  

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

117:     i_LINK.transfer(staker, amountToWithdraw);

```

```solidity
File: example/OperatorStakingPool.sol

181:     i_LINK.transfer(msg.sender, amount);

369:     i_LINK.transfer(alerter, alerterRewardActual);

552:     i_LINK.transfer(msg.sender, withdrawableAmount);

```

```solidity
File: example/RewardVault.sol

678:     i_LINK.transfer(staker, claimableReward);

797:     i_LINK.transfer(msg.sender, totalUnvestedRewards);

```

```solidity
File: example/Staking.sol

277:     i_LINK.transfer(msg.sender, unusedRewards);

488:     i_LINK.transfer(msg.sender, rewardAmount);

532:     i_LINK.transfer(msg.sender, amount + baseReward + delegationReward);

543:     i_LINK.transfer(msg.sender, amount);

698:       i_LINK.transfer(sender, remainder);

```

```solidity
File: example/StakingPoolBase.sol

501:     i_LINK.transfer(msg.sender, amount);

```

</details> 
 


 ### <a name="L-8"></a>[L-8] Unsafe downcast
When a type is downcast to a smaller type, the higher order bits are truncated, effectively applying a modulo to the original value. Without any other checks, this wrapping will lead to unexpected behavior and bugs

*Instances (18)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

322:       uint256 operatorPrincipal = uint112(history >> 112);

323:       uint256 stakerStakedAtTime = uint112(history); //@audit unsafe downcasting

490:       uint256 principal = uint256(history >> 112);

491:       uint256 stakedAtTime = uint112(history);

```

```solidity
File: example/Staking.sol

738:     uint256 maxCommunityStakeAmount = uint256(s_pool.limits.maxCommunityStakeAmount);

785:     uint256 maxOperatorStakeAmount = uint256(s_pool.limits.maxOperatorStakeAmount);

846:       uint256 delegationReward = uint256(s_reward.delegated.cumulativePerDelegate)

```

```solidity
File: example/StakingPoolBase.sol

240:     uint112 stakerPrincipal = uint112(history >> 112);

241:     uint112 stakerStakedAtTime = uint112(history);

279:     uint112 stakerPrincipal = uint112(history >> 112);

355:     uint256 stakerPrincipal = uint256(history >> 112);

356:     uint256 stakedAt = uint112(history);

471:     uint256 stakerPrincipal = uint256(history >> 112);

472:     uint256 stakedAt = uint112(history);

514:     uint112 stakerPrincipal = uint112(history >> 112);

526:     uint112 stakerPrincipal = uint112(history >> 112);

533:     uint112 stakerStakedAtTime = uint112(history);

545:     uint112 stakerStakedAtTime = uint112(history);

```

</details> 
 


 ### <a name="L-9"></a>[L-9] Unsafe ERC20 operation(s)

*Instances (16)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

117:     i_LINK.transfer(staker, amountToWithdraw);

```

```solidity
File: example/OperatorStakingPool.sol

163:     i_LINK.transferFrom({from: msg.sender, to: address(this), value: amount});

181:     i_LINK.transfer(msg.sender, amount);

369:     i_LINK.transfer(alerter, alerterRewardActual);

552:     i_LINK.transfer(msg.sender, withdrawableAmount);

```

```solidity
File: example/RewardVault.sol

369:     i_LINK.transferFrom({from: msg.sender, to: address(this), value: amount});

678:     i_LINK.transfer(staker, claimableReward);

797:     i_LINK.transfer(msg.sender, totalUnvestedRewards);

```

```solidity
File: example/Staking.sol

235:     i_LINK.transferFrom(msg.sender, address(this), amount);

256:     i_LINK.transferFrom(msg.sender, address(this), amount);

277:     i_LINK.transfer(msg.sender, unusedRewards);

488:     i_LINK.transfer(msg.sender, rewardAmount);

532:     i_LINK.transfer(msg.sender, amount + baseReward + delegationReward);

543:     i_LINK.transfer(msg.sender, amount);

698:       i_LINK.transfer(sender, remainder);

```

```solidity
File: example/StakingPoolBase.sol

501:     i_LINK.transfer(msg.sender, amount);

```

</details> 
 


## Non Critical Issues


 ### <a name="NC-1"></a>[NC-1] Custom error has no error details

#### Impact:
Defining custom errors without error details can make error messages less informative.

*Instances (61)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

22:   error MerkleRootNotSet();

```

```solidity
File: example/IAlertsController.sol

18:   error AlertInvalid();

```

```solidity
File: example/IMigratable.sol

23:   error InvalidMigrationTarget();

```

```solidity
File: example/ISlashable.sol

6:   error InvalidSlasherConfig();

11:   error InvalidRole();

16:   error InvalidSlasher();

```

```solidity
File: example/IStaking.sol

18:   error SenderNotLinkToken();

22:   error AccessForbidden();

26:   error InvalidZeroAddress();

```

```solidity
File: example/IStakingOwner.sol

8:   error InvalidDelegationRate();

11:   error InvalidRegularPeriodThreshold();

15:   error InvalidMinOperatorStakeAmount();

19:   error InvalidMinCommunityStakeAmount();

23:   error InvalidMaxAlertingRewardAmount();

27:   error MerkleRootNotSet();

```

```solidity
File: example/IStakingPool.sol

10:   error AccessForbidden();

40:   error InvalidZeroAddress();

43:   error SenderNotLinkToken();

46:   error MigrationProxyNotSet();

49:   error RewardVaultNotSet();

52:   error InvalidData();

55:   error InsufficientStakeAmount();

58:   error ExceedsMaxStakeAmount();

61:   error ExceedsMaxPoolSize();

68:   error UnstakeZeroAmount();

72:   error UnstakeExceedsPrincipal();

76:   error UnstakePrincipalBelowMinAmount();

```

```solidity
File: example/MigrationProxy.sol

29:   error InvalidZeroAddress();

32:   error InvalidSourceAddress();

37:   error SenderNotLinkToken();

```

```solidity
File: example/OperatorStakingPool.sol

27:   error InvalidOperatorList();

29:   error StakerNotOperator();

59:   error InvalidAlerterRewardFundAmount();

```

```solidity
File: example/PriceFeedAlertsController.sol

35:   error InvalidZeroAddress();

37:   error InvalidPriorityPeriodThreshold();

39:   error InvalidRegularPeriodThreshold();

42:   error DoesNotHaveSlasherRole();

49:   error FeedDoesNotExist();

51:   error InvalidOperatorList();

54:   error InvalidSlashableAmount();

56:   error InvalidAlerterRewardAmount();

59:   error AlertInvalid();

```

```solidity
File: example/RewardLib.sol

39:   error RewardDurationTooShort();

```

```solidity
File: example/RewardVault.sol

48:   error InvalidPool();

51:   error InvalidRewardAmount();

54:   error InvalidEmissionRate();

57:   error InvalidDelegationRateDenominator();

61:   error InvalidMigrationSource();

66:   error AccessForbidden();

70:   error InvalidZeroAddress();

73:   error RewardDurationTooShort();

77:   error InsufficentRewardsForDelegationRate();

81:   error VaultAlreadyClosed();

85:   error NoRewardToClaim();

94:   error SenderNotLinkToken();

97:   error CannotClaimRewardWhenPaused();

```

```solidity
File: example/StakingPoolBase.sol

43:   error PoolNotActive();

46:   error InvalidUnbondingPeriod();

49:   error InvalidClaimPeriod();

73:   error RewardVaultNotActive();

77:   error CannotClaimRewardWhenPaused();

```

</details> 
 


 ### <a name="NC-2"></a>[NC-2] Variables without visibility specifier

#### Impact:
Specifying visibility for variables can improve code readability and maintainability.

*Instances (93)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/IRewardVault.sol

64:     uint256 storedBaseReward;

76:     uint256 earnedBaseRewardInPeriod;

```

```solidity
File: example/ISlashable.sol

21:     uint256 refillRate;

23:     uint256 slashCapacity;

31:     uint256 lastSlashTimestamp;

33:     uint256 remainingSlashCapacityAmount;

```

```solidity
File: example/IStakingPool.sol

91:     uint128 unbondingPeriodEndsAt;

93:     uint128 claimPeriodEndsAt;

```

```solidity
File: example/MigrationProxy.sol

45:     address v01StakingAddress;

```

```solidity
File: example/OperatorStakingPool.sol

112:     uint256 minInitialOperatorCount;

118:     uint256 removedPrincipal;

120:     bool isOperator;

122:     bool isRemoved;

317:     uint256 totalSlashedAmount;

319:     for (uint256 i; i < operators.length; ++i) { 

437:     for (uint256 i; i < operators.length; ++i) {

481:     for (uint256 i; i < operators.length; ++i) {

```

```solidity
File: example/PriceFeedAlertsController.sol

130:     address feed;

135:     uint32 priorityPeriodThreshold;

140:     uint32 regularPeriodThreshold;

156:     address feed;

161:     uint32 priorityPeriodThreshold;

166:     uint32 regularPeriodThreshold;

183:     uint32 priorityPeriodThreshold;

188:     uint32 regularPeriodThreshold;

203:     address feed;

205:     uint256 roundId;

212:     bool canAlert;

214:     uint256 roundId;

244:     for (uint256 i; i < params.feedConfigs.length; ++i) { //@audit - QA cache before

444:     for (uint256 i; i < feeds.length; ++i) { //@audit .length

476:     for (uint256 i; i < configs.length; ++i) {

563:     for (uint256 i; i < operators.length; ++i) { //@audit - QA

```

```solidity
File: example/RewardLib.sol

49:     uint8 delegatesCount;

57:     uint32 lastAccumulateTimestamp;

68:     uint32 lastAccumulateTimestamp;

99:     uint256 endTimestamp;

102:     uint32 startTimestamp;

429:     uint256 totalSlashedBaseReward;

430:     uint256 totalSlashedDelegatedReward;

437:     for (uint256 i; i < feedOperators.length; ++i) {

```

```solidity
File: example/RewardVault.sol

208:     uint32 delegationRateDenominator;

210:     uint32 initialMultiplierDuration;

240:     uint32 delegationRateDenominator;

242:     uint32 multiplierDuration;

244:     bool isOpen;

252:     uint256 operatorPoolTotalPrincipal;

255:     uint256 communityPoolTotalPrincipal;

258:     uint256 operatorPoolCheckpointId;

261:     uint256 communityPoolCheckpointId;

268:     uint256 communityReward;

270:     uint256 operatorReward;

272:     uint256 operatorDelegatedReward;

274:     uint256 communityRate;

276:     uint256 operatorRate;

278:     uint256 delegatedRate;

767:     uint256 claimedAmount;

926:     uint256 forfeitedRewardAmount;

1229:     uint256 operatorDelegatedReward;

1230:     uint256 delegatedRate;

1584:     uint256 vestedReward;

1585:     uint256 vestedRewardPerToken;

1586:     uint256 reclaimableReward;

```

```solidity
File: example/Staking.sol

44:     uint256 initialMaxPoolSize;

46:     uint256 initialMaxCommunityStakeAmount;

48:     uint256 initialMaxOperatorStakeAmount;

50:     uint256 minCommunityStakeAmount;

52:     uint256 minOperatorStakeAmount;

55:     uint256 priorityPeriodThreshold;

58:     uint256 regularPeriodThreshold;

61:     uint256 maxAlertingRewardAmount;

64:     uint256 minInitialOperatorCount;

67:     uint256 minRewardDuration;

69:     uint256 slashableDuration;

72:     uint256 delegationRateDenominator;

308:     for (uint256 i; i < operators.length; ++i) {

```

```solidity
File: example/StakingPoolBase.sol

122:     uint32 initialUnbondingPeriod;

124:     uint32 maxUnbondingPeriod;

126:     uint32 initialClaimPeriod;

128:     uint32 minClaimPeriod;

130:     uint32 maxClaimPeriod;

148:     uint32 unbondingPeriod;

152:     uint32 claimPeriod;

158:     uint256 totalPrincipal;

160:     uint256 closedAt;

```

```solidity
File: example/StakingPoolLib.sol

100:     bool isOpen;

102:     uint8 operatorsCount;

111:     bool isOperator;

113:     bool isFeedOperator;

130:     uint256 totalOperatorRemovedAmount;

231:     for (uint256 i; i < operators.length; ++i) {

254:     for (uint256 i; i < pool.feedOperators.length; ++i) {

259:     for (uint256 i; i < operators.length; ++i) {

```

</details> 
 


 ### <a name="NC-3"></a>[NC-3] Constants in comparisons should appear on the left side

#### Impact:
Placing constants on the left side of comparisons can improve code readability and prevent accidental assignment. Doing so will prevent typo [bugs](https://www.moserware.com/2008/01/constants-on-left-are-better-but-this.html)

*Instances (160)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

71:     if (

86:     if (s_merkleRoot == bytes32(0)) {

110:     if (s_merkleRoot == bytes32(0)) return true;

```

```solidity
File: example/Migratable.sol

23:     if (

38:     if (s_migrationTarget == address(0)) {

```

```solidity
File: example/MigrationProxy.sol

96:     if (source != i_v01StakingAddress) revert InvalidSourceAddress();

101:     if (stakerData.length == 0) {

108:     if (amountToStake + amountToWithdraw != amount) {

171:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

```

```solidity
File: example/OperatorStakingPool.sol

159:     if (amount == 0) revert InvalidAlerterRewardFundAmount();

175:     if (amount > s_alerterRewardFunds) {

208:     if (role == SLASHER_ROLE) revert InvalidRole(); //@audit-not following netspec

242:     if (config.slashCapacity == 0 || config.refillRate == 0) {

288:     if (combinedSlashAmount > remainingSlashCapacity) {

416:     if (s_numOperators < i_minInitialOperatorCount) {

440:       if (stakerReward.stakerType == IRewardVault.StakerType.COMMUNITY) {

444:       if (i < operators.length - 1 && operatorAddress >= operators[i + 1]) {

545:     if (withdrawableAmount == 0) {

592:     if (maxPoolSize < maxPrincipalPerStaker * numOperators) {

```

```solidity
File: example/PriceFeedAlertsController.sol

300:     if (s_feedConfigs[feed].priorityPeriodThreshold == 0) {

377:     if (feed == address(0)) revert InvalidZeroAddress();

380:     if (config.priorityPeriodThreshold == 0) revert FeedDoesNotExist();

446:       if (s_feedConfigs[feed].priorityPeriodThreshold == 0) {

478:       if (configParams.feed == address(0)) revert InvalidZeroAddress();

479:       if (configParams.priorityPeriodThreshold == 0) {

482:       if (configParams.regularPeriodThreshold < configParams.priorityPeriodThreshold) {

485:       if (configParams.slashableAmount == 0 || configParams.slashableAmount > operatorMaxPrincipal)

489:       if (configParams.alerterRewardAmount == 0) {

532:     if (principalInOperatorPool == 0 && principalInCommunityStakingPool == 0) return returnValues;

536:     if (block.timestamp < updatedAt + feedConfig.priorityPeriodThreshold) 

543:     if (block.timestamp >= updatedAt + feedConfig.regularPeriodThreshold) {

566:       if (i < operators.length - 1 && operator >= operators[i + 1]) { //i<49 and specific_operator>=

569:       if (operator == address(0)) revert InvalidZeroAddress();

```

```solidity
File: example/RewardLib.sol

119:     if (reward.startTimestamp != 0) revert();

254:       if (baseRewardAmount % REWARD_PRECISION > 0) deltaBaseReward++;

255:       if (delegatedRewardAmount % REWARD_PRECISION > 0) deltaDelegatedReward++;

354:     if (newRate != uint256(reward.base.rate)) {

363:     if (availableRewardDuration < minRewardDuration) {

421:     if (reward.delegated.delegatesCount == 0) return; // Skip slashing if there are no staking

440:       if (operatorStakedAmount == 0) continue;

```

```solidity
File: example/RewardVault.sol

352:     if (

388:     if (oldDelegationRateDenominator == newDelegationRateDenominator) {

399:     if (

415:     if (newDelegationRateDenominator == 0) {

422:     } else if (newDelegationRateDenominator == 1) {

429:     } else if (unvestedRewards != 0) {

566:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

567:     if (sender != s_migrationSource) revert AccessForbidden();

588:     if (totalUnvestedRewards != amount) revert InvalidRewardAmount();

669:     if (claimableReward == 0) {

692:     if (staker == address(0)) return; //@audit no need of this, as condition alr checked before

754:     if (fullForfeitedRewardAmount != 0) {

824:     if (stakingPool == address(i_operatorStakingPool)) {

828:     if (stakingPool == address(i_communityStakingPool)) {

934:     if (forfeitedRewardAmountTimesUnstakedAmount < oldPrincipal) {

950:     if (redistributedReward != 0) {

953:     if (reclaimableReward != 0) {

1024:     if (stakedAt == 0) return 0;

1027:     if (multiplierDuration == 0) return MAX_MULTIPLIER;

1090:     if (operatorPoolCheckpointId != 0) {

1094:     if (communityPoolCheckpointId != 0) {

1124:     if (emissionSplitData.communityRate != 0) {

1131:     if (emissionSplitData.operatorRate != 0) {

1138:     if (emissionSplitData.delegatedRate != 0) {

1160:     if (amount + remainingRewards < emissionRate) revert RewardDurationTooShort();

1179:     if (emissionRate == 0) return;

1233:     if (isDelegated && communityPoolShare != 0) {

1274:     if (

1303:     if (

1327:     if (communityReward != 0 && communityReward < delegationDenominator) {

1331:     if (communityRate != 0 && communityRate < delegationDenominator) {

1339:     if (s_rewardPerTokenUpdatedAt < block.timestamp) {

1385:     if (totalPrincipal == 0) return rewardBucket.vestedRewardPerToken;

1388:     if (latestRewardEmittedAt <= s_rewardPerTokenUpdatedAt) {

1506:     if (stakerReward.stakerType != StakerType.NOT_STAKED) {

1553:     if (vestedRewardPerToken != 0) {

1582:     if (forfeitedReward == 0) return (0, 0, 0);

1588:     if (amountOfRecipientTokens != 0) {

1684:     if (addedRewardAmount != 0 && addedRewardAmount < s_vaultConfig.delegationRateDenominator) {

1691:     if (totalEmissionRate == 0 || totalEmissionRate < s_vaultConfig.delegationRateDenominator) {

1721:     if (

```

```solidity
File: example/Staking.sol

125:     if (params.delegationRateDenominator == 0) revert InvalidDelegationRate();

126:     if (RewardLib.REWARD_PRECISION % params.delegationRateDenominator > 0) {

129:     if (params.regularPeriodThreshold <= params.priorityPeriodThreshold) {

132:     if (params.minOperatorStakeAmount == 0) {

135:     if (params.minOperatorStakeAmount > params.initialMaxOperatorStakeAmount) {

138:     if (params.minCommunityStakeAmount > params.initialMaxCommunityStakeAmount) {

141:     if (params.maxAlertingRewardAmount > params.initialMaxOperatorStakeAmount) {

178:     if (s_merkleRoot == bytes32(0)) return true;

229:     if (s_merkleRoot == bytes32(0)) revert MerkleRootNotSet();

290:     if (s_reward.startTimestamp > 0 && !isActive()) {

323:       if (principal > 0) {

360:     if (newRate == 0) revert();

404:     if (

418:     if (s_proposedMigrationTarget == address(0)) {

422:     if (block.timestamp < (uint256(s_proposedMigrationTargetAt) + 7 days)) {

433:     if (s_migrationTarget == address(0)) revert InvalidMigrationTarget();

453:     if (stakedAmount == 0) revert AccessForbidden();

457:     if (roundId == s_lastAlertedRoundId) revert AlertAlreadyExists(roundId);

459:     if (block.timestamp < lastFeedUpdatedAt + i_priorityPeriodThreshold) {

513:     if (roundId == s_lastAlertedRoundId) return false;

516:     if (block.timestamp < updatedAt + i_priorityPeriodThreshold) return false;

519:     if (block.timestamp >= updatedAt + i_regularPeriodThreshold) return true;

538:     if (amount == 0) revert StakingPoolLib.StakeNotFound(msg.sender);

600:     if (stake == 0) return 0;

615:     if (stakerAccount.stakedAmount == 0) return 0;

682:     if (amount < RewardLib.REWARD_PRECISION) {

696:     if (remainder > 0) {

706:       if (s_merkleRoot != bytes32(0)) {

707:         if (data.length == 0) revert AccessForbidden();

733:     if (newStakedAmount < i_minCommunityStakeAmount) {

739:     if (newStakedAmount > maxCommunityStakeAmount) {

746:     if (amount > remainingPoolSpace) {

780:     if (newStakedAmount < i_minOperatorStakeAmount) {

786:     if (newStakedAmount > maxOperatorStakeAmount) {

791:     if (currentStakedAmount == 0) {

803:       if (delegatesCount == 0) {

824:     if (stakerAccount.stakedAmount == 0) {

906:     if (msg.sender != getChainlinkToken()) revert SenderNotLinkToken();

```

```solidity
File: example/StakingPoolBase.sol

200:     if (params.minPrincipalPerStaker == 0) revert InvalidMinStakeAmount();

201:     if (params.minPrincipalPerStaker >= params.initialMaxPrincipalPerStaker) {

204:     if (MIN_UNBONDING_PERIOD > params.maxUnbondingPeriod) {

207:     if (params.minClaimPeriod == 0 || params.minClaimPeriod >= params.maxClaimPeriod) {

242:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

280:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

282:     if (staker.unbondingPeriodEndsAt != 0 && block.timestamp <= staker.claimPeriodEndsAt) {

344:     if (amount == 0) return;

348:     if (staker == address(0)) revert InvalidZeroAddress();

358:     if (stakerState.unbondingPeriodEndsAt != 0) {

436:     if (migrationProxy == address(0)) revert InvalidZeroAddress();

468:     if (amount == 0) revert UnstakeZeroAmount();

474:     if (amount > stakerPrincipal) revert UnstakeExceedsPrincipal();

478:     if (amount < stakerPrincipal && updatedPrincipal < i_minPrincipalPerStaker) {

624:     if (maxPoolSize == 0 || maxPoolSize < configs.maxPoolSize) {

628:     if (

633:     if (configs.maxPoolSize != maxPoolSize) {

637:     if (configs.maxPrincipalPerStaker != maxPrincipalPerStaker) {

646:     if (unbondingPeriod < MIN_UNBONDING_PERIOD || unbondingPeriod > i_maxUnbondingPeriod) {

658:     if (claimPeriod < i_minClaimPeriod || claimPeriod > i_maxClaimPeriod) {

675:     if (newPrincipal < i_minPrincipalPerStaker) {

678:     if (newPrincipal > s_pool.configs.maxPrincipalPerStaker) {

682:     if (newTotalPrincipal > s_pool.configs.maxPoolSize) {

703:     if (data.length == 0) revert InvalidData();

725:     if (staker.unbondingPeriodEndsAt == 0 || block.timestamp < staker.unbondingPeriodEndsAt) {

753:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

759:     if (s_migrationProxy == address(0)) revert MigrationProxyNotSet();

772:     if (s_pool.state.closedAt != 0) revert PoolHasBeenClosed();

778:     if (s_pool.state.closedAt != 0) revert PoolHasBeenClosed();

796:     if (s_pool.state.closedAt == 0) revert PoolNotClosed();

```

```solidity
File: example/StakingPoolLib.sol

143:     if (maxOperatorStakeAmount > maxPoolSize) {

147:     if (pool.limits.maxPoolSize > maxPoolSize) {

150:     if (pool.limits.maxCommunityStakeAmount > maxCommunityStakeAmount) {

153:     if (pool.limits.maxOperatorStakeAmount > maxOperatorStakeAmount) {

158:     if (

162:     if (pool.limits.maxPoolSize != maxPoolSize) {

166:     if (pool.limits.maxCommunityStakeAmount != maxCommunityStakeAmount) {

170:     if (pool.limits.maxOperatorStakeAmount != maxOperatorStakeAmount) {

227:     if (requiredReservedPoolSpace > remainingPoolSpace) {

235:       if (pool.stakers[operators[i]].stakedAmount > 0) {

240:       if (pool.stakers[operators[i]].removedStakeAmount > 0) {

```

</details> 
 


 ### <a name="NC-4"></a>[NC-4] Consider using delete rather than assigning zero to clear value

#### Impact:
Consider using delete rather than assigning zero to clear values. The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

548:     s_operators[msg.sender].removedPrincipal = 0;

```

```solidity
File: example/RewardVault.sol

1471:       forfeitedReward = 0;

```

</details> 
 


 ### <a name="NC-5"></a>[NC-5] Consider using delete rather than assigning false to clear value

#### Impact:
Consider using delete rather than assigning alse to clear values. The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

501:       operator.isOperator = false;

```

```solidity
File: example/Staking.sol

351:       s_pool.stakers[operator].isOperator = false;

```

```solidity
File: example/StakingPoolBase.sol

425:     s_isOpen = false;

```

```solidity
File: example/StakingPoolLib.sol

187:     pool.state.isOpen = false;

```

</details> 
 


 ### <a name="NC-6"></a>[NC-6] Consider adding a block/deny-list"
Doing so will significantly increase centralization, but will help to prevent hackers from using stolen tokens  

*Instances (9)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

19: contract CommunityStakingPool is StakingPoolBase, IMerkleAccessController, TypeAndVersionInterface {

```

```solidity
File: example/Migratable.sol

6: abstract contract Migratable is IMigratable {

```

```solidity
File: example/MigrationProxy.sol

22: contract MigrationProxy is

```

```solidity
File: example/OperatorStakingPool.sol

23: contract OperatorStakingPool is ISlashable, StakingPoolBase, TypeAndVersionInterface {

```

```solidity
File: example/PausableWithAccessControl.sol

10: abstract contract PausableWithAccessControl is IPausable, Pausable, AccessControlDefaultAdminRules {

```

```solidity
File: example/PriceFeedAlertsController.sol

26: contract PriceFeedAlertsController is

```

```solidity
File: example/RewardVault.sol

37: contract RewardVault is

```

```solidity
File: example/Staking.sol

22: contract StakingV01 is

```

```solidity
File: example/StakingPoolBase.sol

32: abstract contract StakingPoolBase is

```

</details> 
 


 ### <a name="NC-7"></a>[NC-7] Events are missing sender information

#### Impact:
Including msg.sender in events triggered by user actions can make events more useful for end users.

*Instances (64)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

123:     emit MerkleRootChanged(newMerkleRoot);

```

```solidity
File: example/Migratable.sol

17:     emit MigrationTargetSet(oldMigrationTarget, newMigrationTarget);

```

```solidity
File: example/OperatorStakingPool.sol

164:     emit AlerterRewardDeposited(amount, s_alerterRewardFunds);

182:     emit AlerterRewardWithdrawn(amount, s_alerterRewardFunds);

253:     emit SlasherConfigSet(slasher, config.refillRate, config.slashCapacity);

339:       emit Slashed(operators[i], slashedAmount, updatedPrincipal);

365:     emit AlertingRewardPaid(alerter, alerterRewardActual, alerterRewardAmount);

455:       emit OperatorAdded(operatorAddress);

508:       emit OperatorRemoved(operatorAddress, principal);

553:     emit Unstaked(msg.sender, withdrawableAmount, 0);

```

```solidity
File: example/PriceFeedAlertsController.sol

309:     emit FeedConfigRemoved(feed);

346:     emit AlertRaised(msg.sender, returnValues.roundId, returnValues.feedConfig.alerterRewardAmount);

410:     emit AlertsControllerMigrated(s_migrationTarget);

455:       emit FeedConfigRemoved(feed);

462:     emit MigrationDataSent(s_migrationTarget, feeds, migrationData);

499:       emit FeedConfigSet(

573:     emit SlashableOperatorsSet(feed, operators);

```

```solidity
File: example/RewardLib.sol

130:     emit RewardInitialized(rate, availableReward, reward.startTimestamp, reward.endTimestamp);

452:     emit RewardSlashed(feedOperators, slashedBaseAmounts, slashedDelegatedAmounts);

```

```solidity
File: example/RewardVault.sol

320:     emit DelegationRateDenominatorSet(0, params.delegationRateDenominator);

323:     emit MultiplierDurationSet(0, params.initialMultiplierDuration);

326:     emit VaultOpened();

371:     emit RewardAdded(pool, amount, emissionRate);

446:     emit DelegationRateDenominatorSet(oldDelegationRateDenominator, newDelegationRateDenominator);

460:     emit MultiplierDurationSet(oldMultiplierDuration, newMultiplierDuration);

472:     emit MigrationSourceSet(oldMigrationSource, newMigrationSource);

538:     emit VaultMigrated(s_migrationTarget, totalUnvestedRewards, totalEmissionRate);

612:     emit VaultMigrationProcessed(sender, totalUnvestedRewards, totalEmissionRate);

647:     emit StakerRewardUpdated(

679:     emit RewardClaimed(staker, claimableReward);

703:     emit StakerRewardUpdated(

775:     emit RewardFinalized(staker, shouldForfeit);

776:     emit StakerRewardUpdated(

798:     emit VaultClosed(totalUnvestedRewards);

1353:       emit PoolRewardUpdated(

1561:     emit ForfeitedRewardDistributed(

```

```solidity
File: example/Staking.sol

185:     emit MerkleRootChanged(newMerkleRoot);

413:     emit MigrationTargetProposed(migrationTarget);

428:     emit MigrationTargetAccepted(s_migrationTarget);

437:     emit Migrated(msg.sender, amount, baseReward, delegationReward, data);

484:     emit AlertRaised(msg.sender, roundId, rewardAmount);

531:     emit Unstaked(msg.sender, amount, baseReward, delegationReward);

542:     emit Unstaked(msg.sender, amount, 0, 0);

760:     emit Staked(staker, amount, newStakedAmount);

817:     emit Staked(staker, amount, newStakedAmount);

```

```solidity
File: example/StakingPoolBase.sol

251:     emit StakerMigrated(s_migrationTarget, stakerPrincipal, migrationData);

287:     emit UnbondingPeriodStarted(msg.sender);

361:       emit UnbondingPeriodReset(staker);

417:     emit PoolOpened();

427:     emit PoolClosed();

440:     emit MigrationProxySet(migrationProxy);

503:     emit Unstaked(msg.sender, amount, claimedReward);

635:       emit PoolSizeIncreased(maxPoolSize);

639:       emit MaxPrincipalAmountIncreased(maxPrincipalPerStaker);

652:     emit UnbondingPeriodSet(oldUnbondingPeriod, unbondingPeriod);

664:     emit ClaimPeriodSet(oldClaimPeriod, claimPeriod);

696:     emit Staked(sender, newPrincipal, newTotalPrincipal);

```

```solidity
File: example/StakingPoolLib.sol

164:       emit PoolSizeIncreased(maxPoolSize);

168:       emit MaxCommunityStakeAmountIncreased(maxCommunityStakeAmount);

172:       emit MaxOperatorStakeAmountIncreased(maxOperatorStakeAmount);

182:     emit PoolOpened();

188:     emit PoolConcluded();

244:       emit OperatorAdded(operators[i]);

272:     emit FeedOperatorsSet(operators);

```

</details> 
 


 ### <a name="NC-8"></a>[NC-8] Events should use parameters to convey information

#### Impact:
Using parameters in events can provide additional information to subscribers about the event occurrence.

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RewardVault.sol

326:     emit VaultOpened();

```

```solidity
File: example/StakingPoolBase.sol

417:     emit PoolOpened();

427:     emit PoolClosed();

```

```solidity
File: example/StakingPoolLib.sol

182:     emit PoolOpened();

188:     emit PoolConcluded();

```

</details> 
 


 ### <a name="NC-9"></a>[NC-9] If-statement can be converted to a ternary

#### Impact:
The code can be made more compact while also increasing readability by converting the following `if`-statements to ternaries (e.g. `foo += (x > y) ? a : b`)

*Instances (126)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

47:     if (address(params.operatorStakingPool) == address(0)) {

79:     if (s_operatorStakingPool.isOperator(staker) || s_operatorStakingPool.isRemoved(staker)) {

86:     if (s_merkleRoot == bytes32(0)) {

```

```solidity
File: example/Migratable.sol

38:     if (s_migrationTarget == address(0)) {

```

```solidity
File: example/MigrationProxy.sol

67:     if (address(params.v01StakingAddress) == address(0)) {

101:     if (stakerData.length == 0) {

108:     if (amountToStake + amountToWithdraw != amount) {

```

```solidity
File: example/OperatorStakingPool.sol

175:     if (amount > s_alerterRewardFunds) {

232:     if (!hasRole(SLASHER_ROLE, slasher)) {

242:     if (config.slashCapacity == 0 || config.refillRate == 0) {

288:     if (combinedSlashAmount > remainingSlashCapacity) {

416:     if (s_numOperators < i_minInitialOperatorCount) {

440:       if (stakerReward.stakerType == IRewardVault.StakerType.COMMUNITY) {

444:       if (i < operators.length - 1 && operatorAddress >= operators[i + 1]) {

448:       if (operator.isOperator) {

451:       if (operator.isRemoved) {

484:       if (!operator.isOperator) {

540:     if (!_canUnstake(s_stakers[msg.sender])) {

545:     if (withdrawableAmount == 0) {

574:     if (!hasRole(SLASHER_ROLE, msg.sender)) {

592:     if (maxPoolSize < maxPrincipalPerStaker * numOperators) {

```

```solidity
File: example/PriceFeedAlertsController.sol

233:     if (address(params.communityStakingPool) == address(0)) {

236:     if (address(params.operatorStakingPool) == address(0)) {

300:     if (s_feedConfigs[feed].priorityPeriodThreshold == 0) {

446:       if (s_feedConfigs[feed].priorityPeriodThreshold == 0) {

479:       if (configParams.priorityPeriodThreshold == 0) {

482:       if (configParams.regularPeriodThreshold < configParams.priorityPeriodThreshold) {

485:       if (configParams.slashableAmount == 0 || configParams.slashableAmount > operatorMaxPrincipal)

489:       if (configParams.alerterRewardAmount == 0) {

543:     if (block.timestamp >= updatedAt + feedConfig.regularPeriodThreshold) {

566:       if (i < operators.length - 1 && operator >= operators[i + 1]) { //i<49 and specific_operator>=

```

```solidity
File: example/RewardLib.sol

247:     if (isReserving) {

354:     if (newRate != uint256(reward.base.rate)) {

363:     if (availableRewardDuration < minRewardDuration) {

```

```solidity
File: example/RewardVault.sol

388:     if (oldDelegationRateDenominator == newDelegationRateDenominator) {

415:     if (newDelegationRateDenominator == 0) {

422:     } else if (newDelegationRateDenominator == 1) {

429:     } else if (unvestedRewards != 0) {

467:     if (address(newMigrationSource) == address(0) || address(newMigrationSource) == address(this)) {

669:     if (claimableReward == 0) {

754:     if (fullForfeitedRewardAmount != 0) {

769:     if (shouldClaim) {

824:     if (stakingPool == address(i_operatorStakingPool)) {

828:     if (stakingPool == address(i_communityStakingPool)) {

934:     if (forfeitedRewardAmountTimesUnstakedAmount < oldPrincipal) {

950:     if (redistributedReward != 0) {

953:     if (reclaimableReward != 0) {

1090:     if (operatorPoolCheckpointId != 0) {

1094:     if (communityPoolCheckpointId != 0) {

1124:     if (emissionSplitData.communityRate != 0) {

1131:     if (emissionSplitData.operatorRate != 0) {

1138:     if (emissionSplitData.delegatedRate != 0) {

1233:     if (isDelegated && communityPoolShare != 0) {

1327:     if (communityReward != 0 && communityReward < delegationDenominator) {

1331:     if (communityRate != 0 && communityRate < delegationDenominator) {

1339:     if (s_rewardPerTokenUpdatedAt < block.timestamp) {

1388:     if (latestRewardEmittedAt <= s_rewardPerTokenUpdatedAt) {

1467:     if (shouldForfeit) {

1506:     if (stakerReward.stakerType != StakerType.NOT_STAKED) {

1522:     if (isOperator) {

1553:     if (vestedRewardPerToken != 0) {

1588:     if (amountOfRecipientTokens != 0) {

1607:     if (isOperator) {

1646:     if (isOperator) {

1684:     if (addedRewardAmount != 0 && addedRewardAmount < s_vaultConfig.delegationRateDenominator) {

1691:     if (totalEmissionRate == 0 || totalEmissionRate < s_vaultConfig.delegationRateDenominator) {

1713:     if (!hasRole(REWARDER_ROLE, msg.sender)) {

```

```solidity
File: example/Staking.sol

122:     if (address(params.monitoredFeed) == address(0)) {

126:     if (RewardLib.REWARD_PRECISION % params.delegationRateDenominator > 0) {

129:     if (params.regularPeriodThreshold <= params.priorityPeriodThreshold) {

132:     if (params.minOperatorStakeAmount == 0) {

135:     if (params.minOperatorStakeAmount > params.initialMaxOperatorStakeAmount) {

138:     if (params.minCommunityStakeAmount > params.initialMaxCommunityStakeAmount) {

141:     if (params.maxAlertingRewardAmount > params.initialMaxOperatorStakeAmount) {

290:     if (s_reward.startTimestamp > 0 && !isActive()) {

312:       if (!staker.isOperator) {

317:       if (staker.isFeedOperator) {

323:       if (principal > 0) {

418:     if (s_proposedMigrationTarget == address(0)) {

422:     if (block.timestamp < (uint256(s_proposedMigrationTargetAt) + 7 days)) {

459:     if (block.timestamp < lastFeedUpdatedAt + i_priorityPeriodThreshold) {

465:     if (isInPriorityPeriod && !s_pool._isOperator(msg.sender)) {

602:     if (s_pool._isOperator(staker)) {

682:     if (amount < RewardLib.REWARD_PRECISION) {

696:     if (remainder > 0) {

701:     if (s_pool._isOperator(sender)) {

733:     if (newStakedAmount < i_minCommunityStakeAmount) {

739:     if (newStakedAmount > maxCommunityStakeAmount) {

746:     if (amount > remainingPoolSpace) {

780:     if (newStakedAmount < i_minOperatorStakeAmount) {

786:     if (newStakedAmount > maxOperatorStakeAmount) {

791:     if (currentStakedAmount == 0) {

824:     if (stakerAccount.stakedAmount == 0) {

832:     if (s_pool.state.isOpen) {

841:     if (stakerAccount.isOperator) {

```

```solidity
File: example/StakingPoolBase.sol

201:     if (params.minPrincipalPerStaker >= params.initialMaxPrincipalPerStaker) {

204:     if (MIN_UNBONDING_PERIOD > params.maxUnbondingPeriod) {

207:     if (params.minClaimPeriod == 0 || params.minClaimPeriod >= params.maxClaimPeriod) {

282:     if (staker.unbondingPeriodEndsAt != 0 && block.timestamp <= staker.claimPeriodEndsAt) {

358:     if (stakerState.unbondingPeriodEndsAt != 0) {

460:     if (!_canUnstake(staker)) {

463:     if (paused() && shouldClaimReward) {

478:     if (amount < stakerPrincipal && updatedPrincipal < i_minPrincipalPerStaker) {

624:     if (maxPoolSize == 0 || maxPoolSize < configs.maxPoolSize) {

633:     if (configs.maxPoolSize != maxPoolSize) {

637:     if (configs.maxPrincipalPerStaker != maxPrincipalPerStaker) {

646:     if (unbondingPeriod < MIN_UNBONDING_PERIOD || unbondingPeriod > i_maxUnbondingPeriod) {

658:     if (claimPeriod < i_minClaimPeriod || claimPeriod > i_maxClaimPeriod) {

675:     if (newPrincipal < i_minPrincipalPerStaker) {

678:     if (newPrincipal > s_pool.configs.maxPrincipalPerStaker) {

682:     if (newTotalPrincipal > s_pool.configs.maxPoolSize) {

725:     if (staker.unbondingPeriodEndsAt == 0 || block.timestamp < staker.unbondingPeriodEndsAt) {

```

```solidity
File: example/StakingPoolLib.sol

143:     if (maxOperatorStakeAmount > maxPoolSize) {

147:     if (pool.limits.maxPoolSize > maxPoolSize) {

150:     if (pool.limits.maxCommunityStakeAmount > maxCommunityStakeAmount) {

153:     if (pool.limits.maxOperatorStakeAmount > maxOperatorStakeAmount) {

162:     if (pool.limits.maxPoolSize != maxPoolSize) {

166:     if (pool.limits.maxCommunityStakeAmount != maxCommunityStakeAmount) {

170:     if (pool.limits.maxOperatorStakeAmount != maxOperatorStakeAmount) {

178:     if (uint256(pool.state.operatorsCount) < minInitialOperatorCount) {

227:     if (requiredReservedPoolSpace > remainingPoolSpace) {

232:       if (pool.stakers[operators[i]].isOperator) {

235:       if (pool.stakers[operators[i]].stakedAmount > 0) {

240:       if (pool.stakers[operators[i]].removedStakeAmount > 0) {

261:       if (!_isOperator(pool, newFeedOperator)) {

264:       if (pool.stakers[newFeedOperator].isFeedOperator) {

```

</details> 
 


 ### <a name="NC-10"></a>[NC-10] Variable names for immutables should use CONSTANT_CASE

#### Impact:
Using CONSTANT_CASE for immutables improves code readability and maintainability.

*Instances (24)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

55:   LinkTokenInterface private immutable i_LINK;

57:   address private immutable i_v01StakingAddress;

59:   OperatorStakingPool private immutable i_operatorStakingPool;

61:   CommunityStakingPool private immutable i_communityStakingPool;

```

```solidity
File: example/OperatorStakingPool.sol

138:   uint256 private immutable i_minInitialOperatorCount;

```

```solidity
File: example/RewardVault.sol

289:   LinkTokenInterface private immutable i_LINK;

291:   CommunityStakingPool private immutable i_communityStakingPool;

293:   OperatorStakingPool private immutable i_operatorStakingPool;

```

```solidity
File: example/Staking.sol

79:   LinkTokenInterface private immutable i_LINK;

83:   AggregatorV3Interface private immutable i_monitoredFeed;

97:   uint256 private immutable i_priorityPeriodThreshold;

100:   uint256 private immutable i_regularPeriodThreshold;

103:   uint256 private immutable i_maxAlertingRewardAmount;

105:   uint256 private immutable i_minOperatorStakeAmount;

107:   uint256 private immutable i_minCommunityStakeAmount;

110:   uint256 private immutable i_minInitialOperatorCount;

113:   uint256 private immutable i_minRewardDuration;

115:   uint256 private immutable i_slashableDuration;

118:   uint256 private immutable i_delegationRateDenominator;

```

```solidity
File: example/StakingPoolBase.sol

172:   LinkTokenInterface internal immutable i_LINK;

184:   uint96 internal immutable i_minPrincipalPerStaker;

186:   uint32 private immutable i_minClaimPeriod;

188:   uint32 private immutable i_maxClaimPeriod;

190:   uint32 private immutable i_maxUnbondingPeriod;

```

</details> 
 


 ### <a name="NC-11"></a>[NC-11] Imports should use double quotes rather than single quotes

#### Impact:
Using consistent double quotes for imports improves code readability and maintainability.

*Instances (77)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

4: import {ERC677ReceiverInterface} from

6: import {TypeAndVersionInterface} from

9: import {MerkleProof} from '@openzeppelin/contracts/utils/cryptography/MerkleProof.sol';

11: import {IMerkleAccessController} from '../interfaces/IMerkleAccessController.sol';

12: import {OperatorStakingPool} from './OperatorStakingPool.sol';

13: import {StakingPoolBase} from './StakingPoolBase.sol';

```

```solidity
File: example/IStakingPool.sol

4: import {IRewardVault} from './IRewardVault.sol';

5: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

```

```solidity
File: example/Migratable.sol

4: import {IMigratable} from './interfaces/IMigratable.sol';

```

```solidity
File: example/MigrationProxy.sol

4: import {ERC677ReceiverInterface} from

6: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

7: import {TypeAndVersionInterface} from

10: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

12: import {PausableWithAccessControl} from './PausableWithAccessControl.sol';

13: import {CommunityStakingPool} from './pools/CommunityStakingPool.sol';

14: import {OperatorStakingPool} from './pools/OperatorStakingPool.sol';

```

```solidity
File: example/OperatorStakingPool.sol

4: import {TypeAndVersionInterface} from

7: import {AccessControlDefaultAdminRules} from

9: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

10: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

12: import {ISlashable} from '../interfaces/ISlashable.sol';

13: import {IRewardVault} from '../interfaces/IRewardVault.sol';

14: import {RewardVault} from '../rewards/RewardVault.sol';

15: import {StakingPoolBase} from './StakingPoolBase.sol';

```

```solidity
File: example/PausableWithAccessControl.sol

4: import {AccessControlDefaultAdminRules} from

6: import {Pausable} from '@openzeppelin/contracts/security/Pausable.sol';

8: import {IPausable} from './interfaces/IPausable.sol';

```

```solidity
File: example/PriceFeedAlertsController.sol

4: import {AggregatorV3Interface} from

6: import {TypeAndVersionInterface} from

9: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

10: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

12: import {IMigratable} from '../interfaces/IMigratable.sol';

13: import {IMigrationDataReceiver} from '../interfaces/IMigrationDataReceiver.sol';

14: import {Migratable} from '../Migratable.sol';

15: import {PausableWithAccessControl} from '../PausableWithAccessControl.sol';

16: import {CommunityStakingPool} from '../pools/CommunityStakingPool.sol';

17: import {OperatorStakingPool} from '../pools/OperatorStakingPool.sol';

```

```solidity
File: example/RewardLib.sol

4: import {StakingPoolLib} from './StakingPoolLib.sol';

5: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

```

```solidity
File: example/RewardVault.sol

4: import {ERC677ReceiverInterface} from

6: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

7: import {TypeAndVersionInterface} from

10: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

11: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

13: import {FixedPointMathLib} from '@solmate/utils/FixedPointMathLib.sol';

15: import {IMigratable} from '../interfaces/IMigratable.sol';

16: import {IRewardVault} from '../interfaces/IRewardVault.sol';

17: import {IStakingPool} from '../interfaces/IStakingPool.sol';

18: import {Migratable} from '../Migratable.sol';

19: import {PausableWithAccessControl} from '../PausableWithAccessControl.sol';

20: import {CommunityStakingPool} from '../pools/CommunityStakingPool.sol';

21: import {OperatorStakingPool} from '../pools/OperatorStakingPool.sol';

```

```solidity
File: example/Staking.sol

4: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

5: import {TypeAndVersionInterface} from

7: import {AggregatorV3Interface} from

9: import {ConfirmedOwner} from '@chainlink/contracts/src/v0.8/ConfirmedOwner.sol';

10: import {Pausable} from '@openzeppelin/contracts/security/Pausable.sol';

11: import {MerkleProof} from '@openzeppelin/contracts/utils/cryptography/MerkleProof.sol';

12: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

13: import {Math} from '@openzeppelin/contracts/utils/math/Math.sol';

14: import {IStaking} from './IStaking.sol';

15: import {IStakingOwner} from './IStakingOwner.sol';

16: import {IMerkleAccessController} from './IMerkleAccessController.sol';

17: import {IAlertsController} from './IAlertsController.sol';

18: import {IMigratable} from './IMigratable.sol';

19: import {StakingPoolLib} from './StakingPoolLib.sol';

20: import {RewardLib, SafeCast} from './RewardLib.sol';

```

```solidity
File: example/StakingPoolBase.sol

4: import {ERC677ReceiverInterface} from

6: import {LinkTokenInterface} from '@chainlink/contracts/src/v0.8/interfaces/LinkTokenInterface.sol';

8: import {IERC165} from '@openzeppelin/contracts/interfaces/IERC165.sol';

9: import {Checkpoints} from '@openzeppelin/contracts/utils/Checkpoints.sol';

11: import {IMigratable} from '../interfaces/IMigratable.sol';

12: import {IRewardVault} from '../interfaces/IRewardVault.sol';

13: import {IStakingOwner} from '../interfaces/IStakingOwner.sol';

14: import {IStakingPool} from '../interfaces/IStakingPool.sol';

15: import {Migratable} from '../Migratable.sol';

16: import {PausableWithAccessControl} from '../PausableWithAccessControl.sol';

```

</details> 
 


 ### <a name="NC-12"></a>[NC-12] Consider using named mappings

#### Impact:
Using named mappings can improve code readability and maintainability.

*Instances (10)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

126:   mapping(address => Operator) private s_operators;

128:   mapping(address => ISlashable.SlasherConfig) private s_slasherConfigs;

130:   mapping(address => ISlashable.SlasherState) private s_slasherState;

```

```solidity
File: example/PriceFeedAlertsController.sol

224:   mapping(address => FeedConfig) private s_feedConfigs;

226:   mapping(address => address[]) private s_feedSlashableOperators;

228:   mapping(address => uint256) private s_lastAlertedRoundIds;

```

```solidity
File: example/RewardLib.sol

92:     mapping(address => MissedRewards) missed;

```

```solidity
File: example/RewardVault.sol

306:   mapping(address => StakerReward) private s_rewards;

```

```solidity
File: example/StakingPoolBase.sol

178:   mapping(address => IStakingPool.Staker) internal s_stakers;

```

```solidity
File: example/StakingPoolLib.sol

123:     mapping(address => Staker) stakers;

```

</details> 
 


 ### <a name="NC-13"></a>[NC-13] Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct

#### Impact:
Combining multiple mappings into a single mapping with a struct can improve readability and maintainability of the code.

*Instances (10)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

126:   mapping(address => Operator) private s_operators;

128:   mapping(address => ISlashable.SlasherConfig) private s_slasherConfigs;

130:   mapping(address => ISlashable.SlasherState) private s_slasherState;

```

```solidity
File: example/PriceFeedAlertsController.sol

224:   mapping(address => FeedConfig) private s_feedConfigs;

226:   mapping(address => address[]) private s_feedSlashableOperators;

228:   mapping(address => uint256) private s_lastAlertedRoundIds;

```

```solidity
File: example/RewardLib.sol

92:     mapping(address => MissedRewards) missed;

```

```solidity
File: example/RewardVault.sol

306:   mapping(address => StakerReward) private s_rewards;

```

```solidity
File: example/StakingPoolBase.sol

178:   mapping(address => IStakingPool.Staker) internal s_stakers;

```

```solidity
File: example/StakingPoolLib.sol

123:     mapping(address => Staker) stakers;

```

</details> 
 


 ### <a name="NC-14"></a>[NC-14] Use of override is unnecessary

#### Impact:
Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the override keyword when the function solely overrides an interface function, and the function doesnt exist in multiple base contracts, is unnecessary.

*Instances (107)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

63:   ) internal view override {

85:   function _handleOpen() internal view override(StakingPoolBase) {

99:   ) external view override returns (bool) {

121:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyRole(DEFAULT_ADMIN_ROLE) {

127:   function getMerkleRoot() external view override returns (bytes32) {

149:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/Migratable.sol

11:   function setMigrationTarget(address newMigrationTarget) external virtual override {

32:   function getMigrationTarget() external view virtual override returns (address) {

```

```solidity
File: example/MigrationProxy.sol

95:   ) external override whenNotPaused validateFromLINK {

156:   function supportsInterface(bytes4 interfaceId) public view override returns (bool) {

165:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/OperatorStakingPool.sol

207:   ) public virtual override(AccessControlDefaultAdminRules) {

221:   ) external override onlyRole(DEFAULT_ADMIN_ROLE) {

231:   ) external override onlyRole(DEFAULT_ADMIN_ROLE) {

257:   function getSlasherConfig(address slasher) external view override returns (SlasherConfig memory) {

262:   function getSlashCapacity(address slasher) external view override returns (uint256) {

282:   ) external override onlySlasher whenActive {

394:   function _validateOnTokenTransfer(address, address staker, bytes calldata) internal view override {

406:     override

415:   function _handleOpen() internal view override(StakingPoolBase) {

568:   function supportsInterface(bytes4 interfaceID) public view override returns (bool) {

603:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/PausableWithAccessControl.sol

22:   function emergencyPause() external override onlyRole(PAUSER_ROLE) {

27:   function emergencyUnpause() external override onlyRole(PAUSER_ROLE) {

```

```solidity
File: example/PriceFeedAlertsController.sol

403:     override(IMigratable)

420:     override(Migratable)

588:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/RewardVault.sol

489:     override(Migratable)

510:     override(IMigratable)

551:   function supportsInterface(bytes4 interfaceID) public view override returns (bool) {

565:   function onTokenTransfer(address sender, uint256 amount, bytes calldata data) external override {

622:   function claimReward() external override whenNotPaused returns (uint256) {

686:   function updateReward(address staker, uint256 stakerPrincipal) external override onlyStakingPool {

726:   ) external override onlyStakingPool returns (uint256) {

792:   function close() external override onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

802:   function getReward(address staker) external view override returns (uint256) {

818:   function isOpen() external view override returns (bool) {

823:   function hasRewardDurationEnded(address stakingPool) external view override returns (bool) {

836:   function getStoredReward(address staker) external view override returns (StakerReward memory) {

903:   function isPaused() external view override(IRewardVault) returns (bool) {

1740:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/Staking.sol

168:   function typeAndVersion() external pure override returns (string memory) {

177:   function hasAccess(address staker, bytes32[] memory proof) external view override returns (bool) {

183:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyOwner {

189:   function getMerkleRoot() external view override returns (bytes32) {

202:   ) external override(IStakingOwner) onlyOwner whenActive {

218:     override(IStakingOwner)

228:   ) external override(IStakingOwner) onlyOwner {

246:   function conclude() external override(IStakingOwner) onlyOwner whenActive {

253:   function addReward(uint256 amount) external override(IStakingOwner) onlyOwner whenActive {

271:   function withdrawUnusedReward() external override(IStakingOwner) onlyOwner whenInactive {

287:   function addOperators(address[] calldata operators) external override(IStakingOwner) onlyOwner {

300:     override(IStakingOwner)

359:   function changeRewardRate(uint256 newRate) external override onlyOwner whenActive {

379:   function emergencyPause() external override(IStakingOwner) onlyOwner {

384:   function emergencyUnpause() external override(IStakingOwner) onlyOwner {

389:   function getFeedOperators() external view override(IStakingOwner) returns (address[] memory) {

398:   function getMigrationTarget() external view override(IMigratable) returns (address) {

403:   function proposeMigrationTarget(address migrationTarget) external override(IMigratable) onlyOwner {

417:   function acceptMigrationTarget() external override(IMigratable) onlyOwner {

432:   function migrate(bytes calldata data) external override(IMigratable) whenInactive {

451:   function raiseAlert() external override(IAlertsController) whenActive {

509:   function canAlert(address alerter) external view override(IAlertsController) returns (bool) {

528:   function unstake() external override(IStaking) whenInactive {

536:   function withdrawRemovedStake() external override(IStaking) whenInactive {

547:   function getStake(address staker) public view override(IStaking) returns (uint256) {

552:   function isOperator(address staker) external view override(IStaking) returns (bool) {

557:   function isActive() public view override(IStaking) returns (bool) {

562:   function getMaxPoolSize() external view override(IStaking) returns (uint256) {

567:   function getCommunityStakerLimits() external view override(IStaking) returns (uint256, uint256) {

572:   function getOperatorLimits() external view override(IStaking) returns (uint256, uint256) {

577:   function getRewardTimestamps() external view override(IStaking) returns (uint256, uint256) {

582:   function getRewardRate() external view override(IStaking) returns (uint256) {

587:   function getDelegationRateDenominator() external view override(IStaking) returns (uint256) {

592:   function getAvailableReward() public view override(IStaking) returns (uint256) {

598:   function getBaseReward(address staker) public view override(IStaking) returns (uint256) {

612:   function getDelegationReward(address staker) public view override(IStaking) returns (uint256) {

620:   function getTotalDelegatedAmount() public view override(IStaking) returns (uint256) {

627:   function getDelegatesCount() external view override(IStaking) returns (uint256) {

632:   function getTotalStakedAmount() external view override(IStaking) returns (uint256) {

637:   function getTotalCommunityStakedAmount() external view override(IStaking) returns (uint256) {

642:   function getTotalRemovedAmount() external view override(IStaking) returns (uint256) {

647:   function getEarnedBaseRewards() external view override(IStaking) returns (uint256) {

652:   function getEarnedDelegationRewards() external view override(IStaking) returns (uint256) {

657:   function isPaused() external view override(IStaking) returns (bool) {

662:   function getChainlinkToken() public view override(IStaking) returns (address) {

667:   function getMonitoredFeed() external view override returns (address) {

```

```solidity
File: example/StakingPoolBase.sol

231:     override(IMigratable)

259:     override(Migratable)

337:     override

402:   ) external virtual override onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

410:     override(IStakingOwner)

424:   function close() external override(IStakingOwner) onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

435:   function setMigrationProxy(address migrationProxy) external override onlyRole(DEFAULT_ADMIN_ROLE) {

458:   function unstake(uint256 amount, bool shouldClaimReward) external override {

507:   function getTotalPrincipal() external view override returns (uint256) {

512:   function getStakerPrincipal(address staker) external view override returns (uint256) {

524:   ) external view override returns (uint256) {

531:   function getStakerStakedAtTime(address staker) external view override returns (uint256) {

543:   ) external view override returns (uint256) {

550:   function getRewardVault() external view override returns (IRewardVault) {

555:   function getChainlinkToken() external view override returns (address) {

560:   function getMigrationProxy() external view override returns (address) {

565:   function isOpen() external view override returns (bool) {

570:   function isActive() public view override returns (bool) {

575:   function getStakerLimits() external view override returns (uint256, uint256) {

580:   function getMaxPoolSize() external view override returns (uint256) {

```

</details> 
 


 ### <a name="NC-15"></a>[NC-15] Consider using descriptive constants when passing zero as a function argument

#### Impact:
Passing zero as a function argument/Event emission can sometimes result in a security issue (e.g. passing zero as the slippage parameter). Consider using a constant variable with a descriptive name, so its clear that the 0 is intentionally being used, and for the right reasons.

*Instances (15)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

504:       _updateStakerHistory({staker: staker, latestPrincipal: 0, latestStakedAtTime: 0});

553:     emit Unstaked(msg.sender, withdrawableAmount, 0);

```

```solidity
File: example/RewardLib.sol

128:     _updateDuration(reward, maxPoolSize, 0, rate, minRewardDuration, availableReward, 0);

```

```solidity
File: example/RewardVault.sol

320:     emit DelegationRateDenominatorSet(0, params.delegationRateDenominator);

323:     emit MultiplierDurationSet(0, params.initialMultiplierDuration);

1114:     BucketRewardEmissionSplit memory emissionSplitData = _getBucketRewardAndEmissionRateSplit({

1582:     if (forfeitedReward == 0) return (0, 0, 0);

```

```solidity
File: example/Staking.sol

410:     s_migrationTarget = address(0);

427:     s_proposedMigrationTarget = address(0);

542:     emit Unstaked(msg.sender, amount, 0, 0);

815:     s_reward._reserve(amount, 0);

862:       return (stakerAccount.stakedAmount, baseReward, 0);

```

```solidity
File: example/StakingPoolBase.sol

247:     _updateStakerHistory({staker: staker, latestPrincipal: 0, latestStakedAtTime: 0});

364:     s_rewardVault.finalizeReward({

494:     _updateStakerHistory({

```

</details> 
 


 ### <a name="NC-16"></a>[NC-16] Non-external/public variable names should begin with an underscore

#### Impact:
Using an underscore at the beginning of non-external/public variable names can improve code clarity and maintainability. According to the Solidity Style Guide, non-external/public variable names should begin with an [underscore](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables)

*Instances (32)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

41:   OperatorStakingPool private s_operatorStakingPool;

44:   bytes32 private s_merkleRoot;

```

```solidity
File: example/Migratable.sol

8:   address internal s_migrationTarget;

```

```solidity
File: example/OperatorStakingPool.sol

126:   mapping(address => Operator) private s_operators;

128:   mapping(address => ISlashable.SlasherConfig) private s_slasherConfigs;

130:   mapping(address => ISlashable.SlasherState) private s_slasherState;

132:   uint256 private s_numOperators;

135:   uint256 private s_alerterRewardFunds;

```

```solidity
File: example/PriceFeedAlertsController.sol

220:   CommunityStakingPool private s_communityStakingPool;

222:   OperatorStakingPool private s_operatorStakingPool;

224:   mapping(address => FeedConfig) private s_feedConfigs;

226:   mapping(address => address[]) private s_feedSlashableOperators;

228:   mapping(address => uint256) private s_lastAlertedRoundIds;

```

```solidity
File: example/RewardVault.sol

295:   RewardBuckets private s_rewardBuckets;

297:   VaultConfig private s_vaultConfig;

300:   VestingCheckpointData private s_finalVestingCheckpointData;

302:   uint256 private s_rewardPerTokenUpdatedAt;

304:   address private s_migrationSource;

306:   mapping(address => StakerReward) private s_rewards;

```

```solidity
File: example/Staking.sol

80:   StakingPoolLib.Pool private s_pool;

81:   RewardLib.Reward private s_reward;

85:   address private s_proposedMigrationTarget;

87:   uint256 private s_proposedMigrationTargetAt;

89:   address private s_migrationTarget;

91:   uint256 private s_lastAlertedRoundId;

94:   bytes32 private s_merkleRoot;

```

```solidity
File: example/StakingPoolBase.sol

176:   Pool internal s_pool;

178:   mapping(address => IStakingPool.Staker) internal s_stakers;

180:   address internal s_migrationProxy;

182:   IRewardVault internal s_rewardVault;

192:   uint32 private s_checkpointId;

194:   bool internal s_isOpen;

```

</details> 
 


 ### <a name="NC-17"></a>[NC-17]  `require()` / `revert()` statements should have descriptive reason strings

*Instances (13)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Staking.sol

291:       revert StakingPoolLib.InvalidPoolStatus(false, true);

313:         revert StakingPoolLib.OperatorDoesNotExist(operator);

318:         revert StakingPoolLib.OperatorIsAssignedToFeed(operator);

538:     if (amount == 0) revert StakingPoolLib.StakeNotFound(msg.sender);

683:       revert StakingPoolLib.InsufficientStakeAmount(RewardLib.REWARD_PRECISION);

734:       revert StakingPoolLib.InsufficientStakeAmount(i_minCommunityStakeAmount);

740:       revert StakingPoolLib.ExcessiveStakeAmount(maxCommunityStakeAmount - currentStakedAmount);

747:       revert StakingPoolLib.ExcessiveStakeAmount(remainingPoolSpace);

781:       revert StakingPoolLib.InsufficientStakeAmount(i_minOperatorStakeAmount);

787:       revert StakingPoolLib.ExcessiveStakeAmount(maxOperatorStakeAmount - currentStakedAmount);

825:       revert StakingPoolLib.StakeNotFound(staker);

886:     if (!isActive()) revert StakingPoolLib.InvalidPoolStatus(false, true);

899:     if (isActive()) revert StakingPoolLib.InvalidPoolStatus(true, false);

```

</details> 
 


 ### <a name="NC-18"></a>[NC-18] Use the latest solidity version for deployment  
Upgrading to a newer Solidity release can optimize gas usage, take advantage of new features and improve overall contract efficiency. Where possible, based on compatibility requirements, it is recommended to use newer/latest solidity version to take advantage of the latest optimizations and features.

*Instances (22)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IAlertsController.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IAlertsControllerOwner.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IMerkleAccessController.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IMigratable.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IMigrationDataReceiver.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IPausable.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IRewardVault.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/ISlashable.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IStaking.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IStakingOwner.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IStakingPool.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/Migratable.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/MigrationProxy.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/OperatorStakingPool.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/PausableWithAccessControl.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/PriceFeedAlertsController.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/RewardLib.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/RewardVault.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/Staking.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/StakingPoolBase.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/StakingPoolLib.sol

2: pragma solidity ^0.8.16;

```

</details> 
 


 ### <a name="NC-19"></a>[NC-19] Event is missing `indexed` fields
Index event fields make the field more quickly accessible to off-chain tools that parse events. However, note that each index field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields). Each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three fields, all of the fields should be indexed.

*Instances (18)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/IAlertsController.sol

9:   event AlertRaised(address alerter, uint256 roundId, uint256 rewardAmount);

```

```solidity
File: example/IMerkleAccessController.sol

7:   event MerkleRootChanged(bytes32 newMerkleRoot);

```

```solidity
File: example/IMigratable.sol

7:   event MigrationTargetProposed(address migrationTarget);

11:   event MigrationTargetAccepted(address migrationTarget);

18:   event Migrated(

```

```solidity
File: example/IStaking.sol

9:   event Staked(address staker, uint256 newStake, uint256 totalStake);

15:   event Unstaked(address staker, uint256 principal, uint256 baseReward, uint256 delegationReward);

```

```solidity
File: example/RewardLib.sol

16:   event RewardInitialized(

21:   event RewardRateChanged(uint256 rate);

24:   event RewardAdded(uint256 amountAdded);

27:   event RewardWithdrawn(uint256 amount);

34:   event RewardSlashed(

```

```solidity
File: example/StakingPoolLib.sol

15:   event PoolSizeIncreased(uint256 maxPoolSize);

19:   event MaxCommunityStakeAmountIncreased(uint256 maxStakeAmount);

23:   event MaxOperatorStakeAmountIncreased(uint256 maxStakeAmount);

26:   event OperatorAdded(address operator);

30:   event OperatorRemoved(address operator, uint256 amount);

34:   event FeedOperatorsSet(address[] feedOperators);

```

</details> 
 


 ### <a name="NC-20"></a>[NC-20] Functions not used internally could be marked external

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RewardLib.sol

545:   function test() public {}

```

```solidity
File: example/Staking.sol

912:   function test() public {}

```

```solidity
File: example/StakingPoolLib.sol

276:   function test() public {}

```

</details> 
 


 ### <a name="NC-21"></a>[NC-21] Consider moving msg.sender checks to modifiers
If some functions are only allowed to be called by some specific users, consider using a modifier instead of checking with a require statement, especially if this check is done in multiple functions.  

*Instances (68)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

64:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

171:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

```

```solidity
File: example/OperatorStakingPool.sol

163:     i_LINK.transferFrom({from: msg.sender, to: address(this), value: amount});

181:     i_LINK.transfer(msg.sender, amount);

283:     SlasherConfig storage slasherConfig = s_slasherConfigs[msg.sender];

286:     uint256 remainingSlashCapacity = _getRemainingSlashCapacity(slasherConfig, msg.sender);

296:     s_slasherState[msg.sender].remainingSlashCapacityAmount =

298:     s_slasherState[msg.sender].lastSlashTimestamp = block.timestamp;

540:     if (!_canUnstake(s_stakers[msg.sender])) {

541:       revert StakerNotInClaimPeriod(msg.sender);

544:     uint256 withdrawableAmount = s_operators[msg.sender].removedPrincipal;

548:     s_operators[msg.sender].removedPrincipal = 0;

552:     i_LINK.transfer(msg.sender, withdrawableAmount);

553:     emit Unstaked(msg.sender, withdrawableAmount, 0);

574:     if (!hasRole(SLASHER_ROLE, msg.sender)) {

```

```solidity
File: example/PriceFeedAlertsController.sol

231:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

332:     CanAlertReturnValues memory returnValues = _canAlert(msg.sender, feed);

341:       alerter: msg.sender,

346:     emit AlertRaised(msg.sender, returnValues.roundId, returnValues.feedConfig.alerterRewardAmount);

```

```solidity
File: example/RewardVault.sol

309:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

369:     i_LINK.transferFrom({from: msg.sender, to: address(this), value: amount});

566:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

625:     bool isOperator = _isOperator(msg.sender);

628:     uint256 stakerPrincipal = _getStakerPrincipal(msg.sender, stakingPool);

630:       staker: msg.sender,

638:       stakerStakedAtTime: _getStakerStakedAtTime(msg.sender, stakingPool)

644:     uint256 claimableRewards = _transferRewards(msg.sender, stakerReward);

645:     s_rewards[msg.sender] = stakerReward;

648:       msg.sender,

698:       isOperator: msg.sender == address(i_operatorStakingPool),

741:     bool isOperator = msg.sender == address(i_operatorStakingPool);

797:     i_LINK.transfer(msg.sender, totalUnvestedRewards);

1713:     if (!hasRole(REWARDER_ROLE, msg.sender)) {

1722:       msg.sender != address(i_operatorStakingPool) && msg.sender != address(i_communityStakingPool)

1722:       msg.sender != address(i_operatorStakingPool) && msg.sender != address(i_communityStakingPool)

```

```solidity
File: example/Staking.sol

120:   constructor(PoolConstructorParams memory params) ConfirmedOwner(msg.sender) {

235:     i_LINK.transferFrom(msg.sender, address(this), amount);

256:     i_LINK.transferFrom(msg.sender, address(this), amount);

277:     i_LINK.transfer(msg.sender, unusedRewards);

435:     (uint256 amount, uint256 baseReward, uint256 delegationReward) = _exit(msg.sender);

437:     emit Migrated(msg.sender, amount, baseReward, delegationReward, data);

442:       abi.encode(msg.sender, data)

452:     uint256 stakedAmount = getStake(msg.sender);

465:     if (isInPriorityPeriod && !s_pool._isOperator(msg.sender)) {

484:     emit AlertRaised(msg.sender, roundId, rewardAmount);

488:     i_LINK.transfer(msg.sender, rewardAmount);

529:     (uint256 amount, uint256 baseReward, uint256 delegationReward) = _exit(msg.sender);

531:     emit Unstaked(msg.sender, amount, baseReward, delegationReward);

532:     i_LINK.transfer(msg.sender, amount + baseReward + delegationReward);

537:     uint256 amount = s_pool.stakers[msg.sender].removedStakeAmount;

538:     if (amount == 0) revert StakingPoolLib.StakeNotFound(msg.sender);

541:     delete s_pool.stakers[msg.sender].removedStakeAmount;

542:     emit Unstaked(msg.sender, amount, 0, 0);

543:     i_LINK.transfer(msg.sender, amount);

906:     if (msg.sender != getChainlinkToken()) revert SenderNotLinkToken();

```

```solidity
File: example/StakingPoolBase.sol

197:     PausableWithAccessControl(params.adminRoleTransferDelay, msg.sender)

237:     IStakingPool.Staker storage staker = s_stakers[msg.sender];

242:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

244:     bytes memory migrationData = abi.encode(msg.sender, stakerStakedAtTime, data);

277:     Staker storage staker = s_stakers[msg.sender];

280:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

287:     emit UnbondingPeriodStarted(msg.sender);

459:     Staker storage staker = s_stakers[msg.sender];

461:       revert StakerNotInClaimPeriod(msg.sender);

483:       staker: msg.sender,

501:     i_LINK.transfer(msg.sender, amount);

503:     emit Unstaked(msg.sender, amount, claimedReward);

753:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

```

</details> 
 


 ### <a name="NC-22"></a>[NC-22] Array indices should be referenced via enums rather than numeric literals

#### Impact:
Referencing array indices via enums can improve code readability and maintainability.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/PriceFeedAlertsController.sol

246:       setFeedConfigParams[0] = SetFeedConfigParams({

363:     pools[0] = address(s_operatorStakingPool);

364:     pools[1] = address(s_communityStakingPool);

```

</details> 
 


## Gas Optimizations


 ### <a name="GAS-1"></a>[GAS-1] Nesting if-statements is cheaper than using &&
Nesting if-statements avoids the stack operations of setting up and using an extra jumpdest, and saves 6 [gas](https://gist.github.com/IllIllI000/7f3b818abecfadbef93b894481ae7d19)

*Instances (30)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

72:       sender != address(s_migrationProxy) && s_merkleRoot != bytes32(0)

73:         && !_hasAccess(staker, abi.decode(data, (bytes32[])))

```

```solidity
File: example/OperatorStakingPool.sol

444:       if (i < operators.length - 1 && operatorAddress >= operators[i + 1]) {

```

```solidity
File: example/PriceFeedAlertsController.sol

356:     return !paused() && s_operatorStakingPool.isActive() && returnValues.canAlert;

356:     return !paused() && s_operatorStakingPool.isActive() && returnValues.canAlert;

532:     if (principalInOperatorPool == 0 && principalInCommunityStakingPool == 0) return returnValues;

566:       if (i < operators.length - 1 && operator >= operators[i + 1]) { //i<49 and specific_operator>=

```

```solidity
File: example/RewardVault.sol

353:       pool != address(0) && pool != address(i_communityStakingPool)

354:         && pool != address(i_operatorStakingPool)

400:       delegatedRate == 0 && newDelegationRateDenominator != 0 && communityRateWithoutDelegation != 0

400:       delegatedRate == 0 && newDelegationRateDenominator != 0 && communityRateWithoutDelegation != 0

727:     if (paused() && shouldClaim) revert CannotClaimRewardWhenPaused();

826:         && s_rewardBuckets.operatorDelegated.rewardDurationEndsAt <= block.timestamp;

1233:     if (isDelegated && communityPoolShare != 0) {

1276:         && (

1279:               && rewardAmount.mulWadDown(operatorPoolShare) * FixedPointMathLib.WAD < totalPoolShare

1283:                 && rewardAmount.mulWadDown(communityPoolShare) * FixedPointMathLib.WAD < totalPoolShare

1306:           && emissionRate.mulWadDown(operatorPoolShare) * FixedPointMathLib.WAD < totalPoolShare

1310:             && emissionRate.mulWadDown(communityPoolShare) * FixedPointMathLib.WAD < totalPoolShare

1327:     if (communityReward != 0 && communityReward < delegationDenominator) {

1331:     if (communityRate != 0 && communityRate < delegationDenominator) {

1684:     if (addedRewardAmount != 0 && addedRewardAmount < s_vaultConfig.delegationRateDenominator) {

1722:       msg.sender != address(i_operatorStakingPool) && msg.sender != address(i_communityStakingPool)

```

```solidity
File: example/Staking.sol

290:     if (s_reward.startTimestamp > 0 && !isActive()) {

465:     if (isInPriorityPeriod && !s_pool._isOperator(msg.sender)) {

558:     return s_pool.state.isOpen && !s_reward._isDepleted();

```

```solidity
File: example/StakingPoolBase.sol

282:     if (staker.unbondingPeriodEndsAt != 0 && block.timestamp <= staker.claimPeriodEndsAt) {

463:     if (paused() && shouldClaimReward) {

478:     if (amount < stakerPrincipal && updatedPrincipal < i_minPrincipalPerStaker) {

571:     return s_isOpen && !s_rewardVault.hasRewardDurationEnded(address(this));

```

</details> 
 


 ### <a name="GAS-2"></a>[GAS-2] Consider using = instead of += and -= for gas efficiency
Using = instead of += and -= can save gas in certain scenarios. Consider using = when appropriate.

*Instances (50)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

160:     s_alerterRewardFunds += amount;

178:     s_alerterRewardFunds -= amount;

337:       totalSlashedAmount += slashedAmount;

342:     s_pool.state.totalPrincipal -= totalSlashedAmount;

458:     s_numOperators += operators.length;

500:       s_pool.state.totalPrincipal -= principal;

511:     s_numOperators -= operators.length;

```

```solidity
File: example/RewardLib.sol

257:       reward.reserved.base += deltaBaseReward;

258:       reward.reserved.delegated += deltaDelegatedReward;

260:       reward.reserved.base -= deltaBaseReward;

261:       reward.reserved.delegated -= deltaDelegatedReward;

446:       totalSlashedBaseReward += slashedBaseAmounts[i];

447:       totalSlashedDelegatedReward += slashedDelegatedAmounts[i];

449:     reward.reserved.base -= totalSlashedBaseReward._toUint96();

450:     reward.reserved.delegated -= totalSlashedDelegatedReward._toUint96();

493:     reward.missed[operator].base += slashedRewards._toUint96();

510:     reward.missed[operator].delegated += slashedRewards._toUint96();

```

```solidity
File: example/RewardVault.sol

641:     stakerReward.claimedBaseRewardsInPeriod += stakerReward.earnedBaseRewardInPeriod.toUint112();

954:       stakerReward.finalizedBaseReward += reclaimableReward.toUint112();

957:     stakerReward.storedBaseReward += fullForfeitedRewardAmount - forfeitedRewardAmount;

1243:       communityReward -= operatorDelegatedReward;

1247:       communityRate -= delegatedRate;

1463:     stakerReward.finalizedBaseReward += newlyEarnedBaseRewards;

1464:     stakerReward.earnedBaseRewardInPeriod += newlyEarnedBaseRewards;

1513:     stakerReward.storedBaseReward += _calculateEarnedBaseReward({

1525:       stakerReward.finalizedDelegatedReward += _calculateEarnedDelegatedReward({

1555:         s_rewardBuckets.operatorBase.vestedRewardPerToken += vestedRewardPerToken.toUint80();

1557:         s_rewardBuckets.communityBase.vestedRewardPerToken += vestedRewardPerToken.toUint80();

1639:     stakerReward.storedBaseReward += _calculateEarnedBaseReward({

1649:       stakerReward.finalizedDelegatedReward += _calculateEarnedDelegatedReward({

```

```solidity
File: example/Staking.sol

326:         s_reward.reserved.base -= getBaseReward(operator)._toUint96();

328:         s_reward.reserved.base -=

334:         s_reward.reserved.delegated -= getDelegationReward(operator)._toUint96();

336:         s_reward.delegated.delegatesCount -= 1;

339:         s_pool.state.totalOperatorStakedAmount -= castPrincipal;

342:         s_pool.totalOperatorRemovedAmount += castPrincipal;

355:     s_pool.state.operatorsCount -= operators.length._toUint8();

540:     s_pool.totalOperatorRemovedAmount -= amount;

697:       amount -= remainder;

753:     s_reward.missed[staker].base +=

758:     s_pool.state.totalCommunityStakedAmount += amount._toUint96();

804:         s_reward.reserved.delegated -= s_reward.delegated.cumulativePerDelegate;

813:     s_reward.missed[staker].base += s_reward._calculateAccruedBaseRewards(amount)._toUint96();

814:     s_pool.state.totalOperatorStakedAmount += amount._toUint96();

842:       s_pool.state.totalOperatorStakedAmount -= stakerAccount.stakedAmount;

850:       s_reward.reserved.base -= baseReward._toUint96();

851:       s_reward.reserved.delegated -= delegationReward._toUint96();

854:       s_pool.state.totalCommunityStakedAmount -= stakerAccount.stakedAmount;

861:       s_reward.reserved.base -= baseReward._toUint96();

```

```solidity
File: example/StakingPoolBase.sol

490:     s_pool.state.totalPrincipal -= amount;

```

</details> 
 


 ### <a name="GAS-3"></a>[GAS-3] Use >= instead of > for gas efficiency
Using >= costs less gas than >. Consider using >= when appropriate.

*Instances (32)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

175:     if (amount > s_alerterRewardFunds) {

288:     if (combinedSlashAmount > remainingSlashCapacity) {

325:         principalAmount > operatorPrincipal ? operatorPrincipal : principalAmount;

```

```solidity
File: example/PriceFeedAlertsController.sol

485:       if (configParams.slashableAmount == 0 || configParams.slashableAmount > operatorMaxPrincipal)

```

```solidity
File: example/RewardLib.sol

254:       if (baseRewardAmount % REWARD_PRECISION > 0) deltaBaseReward++;

255:       if (delegatedRewardAmount % REWARD_PRECISION > 0) deltaDelegatedReward++;

```

```solidity
File: example/RewardVault.sol

1459:     uint112 newlyEarnedBaseRewards = claimableBaseRewards > stakerReward.claimedBaseRewardsInPeriod

```

```solidity
File: example/Staking.sol

126:     if (RewardLib.REWARD_PRECISION % params.delegationRateDenominator > 0) {

135:     if (params.minOperatorStakeAmount > params.initialMaxOperatorStakeAmount) {

138:     if (params.minCommunityStakeAmount > params.initialMaxCommunityStakeAmount) {

141:     if (params.maxAlertingRewardAmount > params.initialMaxOperatorStakeAmount) {

290:     if (s_reward.startTimestamp > 0 && !isActive()) {

323:       if (principal > 0) {

696:     if (remainder > 0) {

739:     if (newStakedAmount > maxCommunityStakeAmount) {

746:     if (amount > remainingPoolSpace) {

786:     if (newStakedAmount > maxOperatorStakeAmount) {

```

```solidity
File: example/StakingPoolBase.sol

204:     if (MIN_UNBONDING_PERIOD > params.maxUnbondingPeriod) {

474:     if (amount > stakerPrincipal) revert UnstakeExceedsPrincipal();

629:       maxPrincipalPerStaker == 0 || maxPrincipalPerStaker > maxPoolSize

630:         || configs.maxPrincipalPerStaker > maxPrincipalPerStaker

646:     if (unbondingPeriod < MIN_UNBONDING_PERIOD || unbondingPeriod > i_maxUnbondingPeriod) {

658:     if (claimPeriod < i_minClaimPeriod || claimPeriod > i_maxClaimPeriod) {

678:     if (newPrincipal > s_pool.configs.maxPrincipalPerStaker) {

682:     if (newTotalPrincipal > s_pool.configs.maxPoolSize) {

```

```solidity
File: example/StakingPoolLib.sol

143:     if (maxOperatorStakeAmount > maxPoolSize) {

147:     if (pool.limits.maxPoolSize > maxPoolSize) {

150:     if (pool.limits.maxCommunityStakeAmount > maxCommunityStakeAmount) {

153:     if (pool.limits.maxOperatorStakeAmount > maxOperatorStakeAmount) {

227:     if (requiredReservedPoolSpace > remainingPoolSpace) {

235:       if (pool.stakers[operators[i]].stakedAmount > 0) {

240:       if (pool.stakers[operators[i]].removedStakeAmount > 0) {

```

</details> 
 


 ### <a name="GAS-4"></a>[GAS-4] Use assembly to emit events, in order to save gas
Using the [scratch space](https://github.com/Vectorized/solady/blob/30558f5402f02351b96eeb6eaf32bcea29773841/src/tokens/ERC1155.sol#L501-L504) for event arguments (two words or fewer) will save gas over needing Soliditys full abi memory expansion used for emitting normally.

*Instances (68)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

123:     emit MerkleRootChanged(newMerkleRoot);

141:     emit OperatorStakingPoolChanged(oldOperatorStakingPool, address(newOperatorStakingPool));

```

```solidity
File: example/Migratable.sol

17:     emit MigrationTargetSet(oldMigrationTarget, newMigrationTarget);

```

```solidity
File: example/OperatorStakingPool.sol

164:     emit AlerterRewardDeposited(amount, s_alerterRewardFunds);

182:     emit AlerterRewardWithdrawn(amount, s_alerterRewardFunds);

253:     emit SlasherConfigSet(slasher, config.refillRate, config.slashCapacity);

339:       emit Slashed(operators[i], slashedAmount, updatedPrincipal);

365:     emit AlertingRewardPaid(alerter, alerterRewardActual, alerterRewardAmount);

455:       emit OperatorAdded(operatorAddress);

508:       emit OperatorRemoved(operatorAddress, principal);

553:     emit Unstaked(msg.sender, withdrawableAmount, 0);

```

```solidity
File: example/PriceFeedAlertsController.sol

269:     emit CommunityStakingPoolSet(address(oldCommunityStakingPool), address(newCommunityStakingPool));

282:     emit OperatorStakingPoolSet(address(oldOperatorStakingPool), address(newOperatorStakingPool));

309:     emit FeedConfigRemoved(feed);

346:     emit AlertRaised(msg.sender, returnValues.roundId, returnValues.feedConfig.alerterRewardAmount);

410:     emit AlertsControllerMigrated(s_migrationTarget);

455:       emit FeedConfigRemoved(feed);

462:     emit MigrationDataSent(s_migrationTarget, feeds, migrationData);

499:       emit FeedConfigSet(

573:     emit SlashableOperatorsSet(feed, operators);

```

```solidity
File: example/RewardLib.sol

130:     emit RewardInitialized(rate, availableReward, reward.startTimestamp, reward.endTimestamp);

452:     emit RewardSlashed(feedOperators, slashedBaseAmounts, slashedDelegatedAmounts);

```

```solidity
File: example/RewardVault.sol

320:     emit DelegationRateDenominatorSet(0, params.delegationRateDenominator);

323:     emit MultiplierDurationSet(0, params.initialMultiplierDuration);

326:     emit VaultOpened();

371:     emit RewardAdded(pool, amount, emissionRate);

446:     emit DelegationRateDenominatorSet(oldDelegationRateDenominator, newDelegationRateDenominator);

460:     emit MultiplierDurationSet(oldMultiplierDuration, newMultiplierDuration);

472:     emit MigrationSourceSet(oldMigrationSource, newMigrationSource);

538:     emit VaultMigrated(s_migrationTarget, totalUnvestedRewards, totalEmissionRate);

612:     emit VaultMigrationProcessed(sender, totalUnvestedRewards, totalEmissionRate);

647:     emit StakerRewardUpdated(

679:     emit RewardClaimed(staker, claimableReward);

703:     emit StakerRewardUpdated(

775:     emit RewardFinalized(staker, shouldForfeit);

776:     emit StakerRewardUpdated(

798:     emit VaultClosed(totalUnvestedRewards);

1353:       emit PoolRewardUpdated(

1561:     emit ForfeitedRewardDistributed(

```

```solidity
File: example/Staking.sol

185:     emit MerkleRootChanged(newMerkleRoot);

413:     emit MigrationTargetProposed(migrationTarget);

428:     emit MigrationTargetAccepted(s_migrationTarget);

437:     emit Migrated(msg.sender, amount, baseReward, delegationReward, data);

484:     emit AlertRaised(msg.sender, roundId, rewardAmount);

531:     emit Unstaked(msg.sender, amount, baseReward, delegationReward);

542:     emit Unstaked(msg.sender, amount, 0, 0);

760:     emit Staked(staker, amount, newStakedAmount);

817:     emit Staked(staker, amount, newStakedAmount);

```

```solidity
File: example/StakingPoolBase.sol

251:     emit StakerMigrated(s_migrationTarget, stakerPrincipal, migrationData);

287:     emit UnbondingPeriodStarted(msg.sender);

318:     emit RewardVaultSet(oldRewardVault, address(newRewardVault));

361:       emit UnbondingPeriodReset(staker);

417:     emit PoolOpened();

427:     emit PoolClosed();

440:     emit MigrationProxySet(migrationProxy);

503:     emit Unstaked(msg.sender, amount, claimedReward);

635:       emit PoolSizeIncreased(maxPoolSize);

639:       emit MaxPrincipalAmountIncreased(maxPrincipalPerStaker);

652:     emit UnbondingPeriodSet(oldUnbondingPeriod, unbondingPeriod);

664:     emit ClaimPeriodSet(oldClaimPeriod, claimPeriod);

696:     emit Staked(sender, newPrincipal, newTotalPrincipal);

```

```solidity
File: example/StakingPoolLib.sol

164:       emit PoolSizeIncreased(maxPoolSize);

168:       emit MaxCommunityStakeAmountIncreased(maxCommunityStakeAmount);

172:       emit MaxOperatorStakeAmountIncreased(maxOperatorStakeAmount);

182:     emit PoolOpened();

188:     emit PoolConcluded();

244:       emit OperatorAdded(operators[i]);

272:     emit FeedOperatorsSet(operators);

```

</details> 
 


 ### <a name="GAS-5"></a>[GAS-5] Using bools for storage incurs overhead
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/StakingPoolBase.sol

194:   bool internal s_isOpen;

```

</details> 
 


 ### <a name="GAS-6"></a>[GAS-6] Cache array length outside of loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

319:     for (uint256 i; i < operators.length; ++i) { 

437:     for (uint256 i; i < operators.length; ++i) {

481:     for (uint256 i; i < operators.length; ++i) {

```

```solidity
File: example/PriceFeedAlertsController.sol

244:     for (uint256 i; i < params.feedConfigs.length; ++i) { //@audit - QA cache before

444:     for (uint256 i; i < feeds.length; ++i) { //@audit .length

476:     for (uint256 i; i < configs.length; ++i) {

563:     for (uint256 i; i < operators.length; ++i) { //@audit - QA

```

```solidity
File: example/RewardLib.sol

437:     for (uint256 i; i < feedOperators.length; ++i) {

```

```solidity
File: example/Staking.sol

308:     for (uint256 i; i < operators.length; ++i) {

```

```solidity
File: example/StakingPoolLib.sol

231:     for (uint256 i; i < operators.length; ++i) {

254:     for (uint256 i; i < pool.feedOperators.length; ++i) {

259:     for (uint256 i; i < operators.length; ++i) {

```

</details> 
 


 ### <a name="GAS-7"></a>[GAS-7] Use calldata instead of memory for function arguments that do not get mutated
Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/Staking.sol

120:   constructor(PoolConstructorParams memory params) ConfirmedOwner(msg.sender) {

177:   function hasAccess(address staker, bytes32[] memory proof) external view override returns (bool) {

680:     bytes memory data

```

</details> 
 


 ### <a name="GAS-8"></a>[GAS-8] Consider using assembly for simple zero checks to save gas
Using assembly for simple zero checks can save gas. Consider using assembly when appropriate.

*Instances (20)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

159:     if (amount == 0) revert InvalidAlerterRewardFundAmount();

545:     if (withdrawableAmount == 0) {

```

```solidity
File: example/RewardLib.sol

440:       if (operatorStakedAmount == 0) continue;

```

```solidity
File: example/RewardVault.sol

415:     if (newDelegationRateDenominator == 0) {

669:     if (claimableReward == 0) {

1024:     if (stakedAt == 0) return 0;

1027:     if (multiplierDuration == 0) return MAX_MULTIPLIER;

1179:     if (emissionRate == 0) return;

1385:     if (totalPrincipal == 0) return rewardBucket.vestedRewardPerToken;

1582:     if (forfeitedReward == 0) return (0, 0, 0);

```

```solidity
File: example/Staking.sol

360:     if (newRate == 0) revert();

453:     if (stakedAmount == 0) revert AccessForbidden();

538:     if (amount == 0) revert StakingPoolLib.StakeNotFound(msg.sender);

600:     if (stake == 0) return 0;

791:     if (currentStakedAmount == 0) {

803:       if (delegatesCount == 0) {

```

```solidity
File: example/StakingPoolBase.sol

242:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

280:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

344:     if (amount == 0) return;

468:     if (amount == 0) revert UnstakeZeroAmount();

```

</details> 
 


 ### <a name="GAS-9"></a>[GAS-9] Consider using constant rather than immutable to save gas

#### Impact:
Using constant variables instead of immutable can potentially save gas costs in some cases. You can see it [here](https://docs.soliditylang.org/en/v0.8.21/contracts.html#constant-and-immutable-state-variables)

*Instances (24)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/MigrationProxy.sol

55:   LinkTokenInterface private immutable i_LINK;

57:   address private immutable i_v01StakingAddress;

59:   OperatorStakingPool private immutable i_operatorStakingPool;

61:   CommunityStakingPool private immutable i_communityStakingPool;

```

```solidity
File: example/OperatorStakingPool.sol

138:   uint256 private immutable i_minInitialOperatorCount;

```

```solidity
File: example/RewardVault.sol

289:   LinkTokenInterface private immutable i_LINK;

291:   CommunityStakingPool private immutable i_communityStakingPool;

293:   OperatorStakingPool private immutable i_operatorStakingPool;

```

```solidity
File: example/Staking.sol

79:   LinkTokenInterface private immutable i_LINK;

83:   AggregatorV3Interface private immutable i_monitoredFeed;

97:   uint256 private immutable i_priorityPeriodThreshold;

100:   uint256 private immutable i_regularPeriodThreshold;

103:   uint256 private immutable i_maxAlertingRewardAmount;

105:   uint256 private immutable i_minOperatorStakeAmount;

107:   uint256 private immutable i_minCommunityStakeAmount;

110:   uint256 private immutable i_minInitialOperatorCount;

113:   uint256 private immutable i_minRewardDuration;

115:   uint256 private immutable i_slashableDuration;

118:   uint256 private immutable i_delegationRateDenominator;

```

```solidity
File: example/StakingPoolBase.sol

172:   LinkTokenInterface internal immutable i_LINK;

184:   uint96 internal immutable i_minPrincipalPerStaker;

186:   uint32 private immutable i_minClaimPeriod;

188:   uint32 private immutable i_maxClaimPeriod;

190:   uint32 private immutable i_maxUnbondingPeriod;

```

</details> 
 


 ### <a name="GAS-10"></a>[GAS-10] Constructors can be marked payable
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn  t provided. A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

46:   constructor(ConstructorParams memory params) StakingPoolBase(params.baseParams) {

```

```solidity
File: example/MigrationProxy.sol

63:   constructor(ConstructorParams memory params)

```

```solidity
File: example/OperatorStakingPool.sol

144:   constructor(ConstructorParams memory params) StakingPoolBase(params.baseParams) {

```

```solidity
File: example/PausableWithAccessControl.sol

16:   constructor(

```

```solidity
File: example/PriceFeedAlertsController.sol

230:   constructor(ConstructorParams memory params)

```

```solidity
File: example/RewardVault.sol

308:   constructor(ConstructorParams memory params)

```

```solidity
File: example/Staking.sol

120:   constructor(PoolConstructorParams memory params) ConfirmedOwner(msg.sender) {

```

```solidity
File: example/StakingPoolBase.sol

196:   constructor(ConstructorParamsBase memory params)

```

</details> 
 


 ### <a name="GAS-11"></a>[GAS-11] Use assembly for small keccak256 hashes, in order to save gas
If the arguments to the encode call can fit into the scratch space (two words or fewer), then its more efficient to use assembly to generate the hash (80 gas): keccak256(abi.encodePacked(x, y)) -> assembly {mstore(0x00, a); mstore(0x20, b); let hash := keccak256(0x00, 0x40); }

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

114:       leaf: keccak256(bytes.concat(keccak256(abi.encode(staker))))

```

```solidity
File: example/Staking.sol

179:     return MerkleProof.verify(proof, s_merkleRoot, keccak256(abi.encode(staker)));

710:             abi.decode(data, (bytes32[])), s_merkleRoot, keccak256(abi.encode(sender))

```

</details> 
 


 ### <a name="GAS-12"></a>[GAS-12] Reduce gas usage by moving to Solidity 0.8.19 or later
Solidity version 0.8.19 introduced a number of gas optimizations, refer to the [Solidity 0.8.19 Release Announcement](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement) for details.

*Instances (22)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IAlertsController.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IAlertsControllerOwner.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IMerkleAccessController.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IMigratable.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IMigrationDataReceiver.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IPausable.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IRewardVault.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/ISlashable.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/IStaking.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IStakingOwner.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/IStakingPool.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/Migratable.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/MigrationProxy.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/OperatorStakingPool.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/PausableWithAccessControl.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/PriceFeedAlertsController.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/RewardLib.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/RewardVault.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/Staking.sol

2: pragma solidity ^0.8.16;

```

```solidity
File: example/StakingPoolBase.sol

2: pragma solidity 0.8.19;

```

```solidity
File: example/StakingPoolLib.sol

2: pragma solidity ^0.8.16;

```

</details> 
 


 ### <a name="GAS-13"></a>[GAS-13] Functions guaranteed to revert when called by normal users can be marked `payable`
If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.

*Instances (23)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

121:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyRole(DEFAULT_ADMIN_ROLE) {

```

```solidity
File: example/OperatorStakingPool.sol

173:   function withdrawAlerterReward(uint256 amount) external onlyRole(DEFAULT_ADMIN_ROLE) { @audit uint ko kaam kar do

```

```solidity
File: example/PausableWithAccessControl.sol

22:   function emergencyPause() external override onlyRole(PAUSER_ROLE) {

27:   function emergencyUnpause() external override onlyRole(PAUSER_ROLE) {

```

```solidity
File: example/PriceFeedAlertsController.sol

299:   function removeFeedConfig(address feed) external onlyRole(DEFAULT_ADMIN_ROLE) {

```

```solidity
File: example/RewardVault.sol

466:   function setMigrationSource(address newMigrationSource) external onlyRole(DEFAULT_ADMIN_ROLE) {

686:   function updateReward(address staker, uint256 stakerPrincipal) external override onlyStakingPool {

792:   function close() external override onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

```

```solidity
File: example/Staking.sol

183:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyOwner {

246:   function conclude() external override(IStakingOwner) onlyOwner whenActive {

253:   function addReward(uint256 amount) external override(IStakingOwner) onlyOwner whenActive {

271:   function withdrawUnusedReward() external override(IStakingOwner) onlyOwner whenInactive {

287:   function addOperators(address[] calldata operators) external override(IStakingOwner) onlyOwner {

359:   function changeRewardRate(uint256 newRate) external override onlyOwner whenActive {

379:   function emergencyPause() external override(IStakingOwner) onlyOwner {

384:   function emergencyUnpause() external override(IStakingOwner) onlyOwner {

403:   function proposeMigrationTarget(address migrationTarget) external override(IMigratable) onlyOwner {

417:   function acceptMigrationTarget() external override(IMigratable) onlyOwner {

```

```solidity
File: example/StakingPoolBase.sol

294:   function setUnbondingPeriod(uint256 newUnbondingPeriod) external onlyRole(DEFAULT_ADMIN_ROLE) {

307:   function setClaimPeriod(uint256 claimPeriod) external onlyRole(DEFAULT_ADMIN_ROLE) {

314:   function setRewardVault(IRewardVault newRewardVault) external onlyRole(DEFAULT_ADMIN_ROLE) {

424:   function close() external override(IStakingOwner) onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

435:   function setMigrationProxy(address migrationProxy) external override onlyRole(DEFAULT_ADMIN_ROLE) {

```

</details> 
 


 ### <a name="GAS-14"></a>[GAS-14] `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too)
*Saves 5 gas per loop*

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RewardLib.sol

254:       if (baseRewardAmount % REWARD_PRECISION > 0) deltaBaseReward++;

255:       if (delegatedRewardAmount % REWARD_PRECISION > 0) deltaDelegatedReward++;

```

```solidity
File: example/StakingPoolBase.sol

742:       s_checkpointId++,

```

</details> 
 


 ### <a name="GAS-15"></a>[GAS-15] Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

142:   bytes32 public constant SLASHER_ROLE = keccak256('SLASHER_ROLE');

```

```solidity
File: example/PausableWithAccessControl.sol

14:   bytes32 public constant PAUSER_ROLE = keccak256('PAUSER_ROLE');

```

```solidity
File: example/RewardVault.sol

284:   bytes32 public constant REWARDER_ROLE = keccak256('REWARDER_ROLE');

```

</details> 
 


 ### <a name="GAS-16"></a>[GAS-16] require()/revert() strings longer than 32 bytes cost extra gas
Each extra memory word of bytes past the original 32 [incurs an MSTORE](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#consider-having-short-revert-strings) which costs 3 gas.

*Instances (157)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

48:       revert InvalidZeroAddress();

75:       revert AccessForbidden();

80:       revert AccessForbidden();

87:       revert MerkleRootNotSet();

138:     if (address(newOperatorStakingPool) == address(0)) revert InvalidZeroAddress();

```

```solidity
File: example/Migratable.sol

27:       revert InvalidMigrationTarget();

39:       revert InvalidMigrationTarget();

```

```solidity
File: example/MigrationProxy.sol

66:     if (address(params.LINKAddress) == address(0)) revert InvalidZeroAddress();

68:       revert InvalidZeroAddress();

70:     if (address(params.operatorStakingPool) == address(0)) revert InvalidZeroAddress();

71:     if (address(params.communityStakingPool) == address(0)) revert InvalidZeroAddress();

96:     if (source != i_v01StakingAddress) revert InvalidSourceAddress();

109:       revert InvalidAmounts(amountToStake, amountToWithdraw, amount);

171:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

```

```solidity
File: example/OperatorStakingPool.sol

159:     if (amount == 0) revert InvalidAlerterRewardFundAmount();

174:     if (s_isOpen) revert PoolNotClosed();

176:       revert InsufficientAlerterRewardFunds(amount, s_alerterRewardFunds);

208:     if (role == SLASHER_ROLE) revert InvalidRole(); //@audit-not following netspec

233:       revert InvalidSlasher();

243:       revert ISlashable.InvalidSlasherConfig();

396:     if (!s_operators[staker].isOperator) revert StakerNotOperator();

417:       revert InadequateInitialOperatorCount(s_numOperators, i_minInitialOperatorCount);

441:         revert OperatorCannotBeCommunityStaker(operatorAddress);

445:         revert InvalidOperatorList();

449:         revert OperatorAlreadyExists(operatorAddress);

452:         revert OperatorHasBeenRemoved(operatorAddress);

485:         revert OperatorDoesNotExist(operatorAddress);

541:       revert StakerNotInClaimPeriod(msg.sender);

546:       revert UnstakeExceedsPrincipal();

575:       revert AccessForbidden();

593:       revert InsufficientPoolSpace(maxPoolSize, maxPrincipalPerStaker, numOperators);

```

```solidity
File: example/PriceFeedAlertsController.sol

234:       revert InvalidZeroAddress();

237:       revert InvalidZeroAddress();

265:     if (address(newCommunityStakingPool) == address(0)) revert InvalidZeroAddress();

278:     if (address(newOperatorStakingPool) == address(0)) revert InvalidZeroAddress();

301:       revert FeedDoesNotExist(); //@audit what if by mistake or any reason while settong config priorityPeriodThreshold =0

333:     if (!returnValues.canAlert) revert AlertInvalid();

377:     if (feed == address(0)) revert InvalidZeroAddress();

380:     if (config.priorityPeriodThreshold == 0) revert FeedDoesNotExist();

429:       revert InvalidMigrationTarget();

447:         revert FeedDoesNotExist();

478:       if (configParams.feed == address(0)) revert InvalidZeroAddress();

480:         revert InvalidPriorityPeriodThreshold();

483:         revert InvalidRegularPeriodThreshold();

487:         revert InvalidSlashableAmount();

490:         revert InvalidAlerterRewardAmount();

567:         revert InvalidOperatorList();

569:       if (operator == address(0)) revert InvalidZeroAddress();

583:     if (!_hasSlasherRole()) revert DoesNotHaveSlasherRole();

```

```solidity
File: example/RewardLib.sol

119:     if (reward.startTimestamp != 0) revert();

364:       revert RewardDurationTooShort();

```

```solidity
File: example/RewardVault.sol

311:     if (address(params.linkToken) == address(0)) revert InvalidZeroAddress();

312:     if (address(params.communityStakingPool) == address(0)) revert InvalidZeroAddress();

313:     if (address(params.operatorStakingPool) == address(0)) revert InvalidZeroAddress();

356:       revert InvalidPool();

389:       revert InvalidDelegationRateDenominator();

403:       revert InsufficentRewardsForDelegationRate();

468:       revert InvalidMigrationSource();

498:       revert InvalidMigrationTarget();

566:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

567:     if (sender != s_migrationSource) revert AccessForbidden();

588:     if (totalUnvestedRewards != amount) revert InvalidRewardAmount();

670:       revert NoRewardToClaim();

727:     if (paused() && shouldClaim) revert CannotClaimRewardWhenPaused();

832:     revert InvalidPool();

1160:     if (amount + remainingRewards < emissionRate) revert RewardDurationTooShort();

1287:       revert InvalidRewardAmount();

1313:       revert InvalidEmissionRate();

1328:       revert InvalidRewardAmount();

1332:       revert InvalidEmissionRate();

1685:       revert InvalidRewardAmount();

1692:       revert InvalidEmissionRate();

1714:       revert AccessForbidden();

1724:       revert AccessForbidden();

1731:     if (!s_vaultConfig.isOpen) revert VaultAlreadyClosed();

```

```solidity
File: example/Staking.sol

121:     if (address(params.LINKAddress) == address(0)) revert InvalidZeroAddress();

123:       revert InvalidZeroAddress();

125:     if (params.delegationRateDenominator == 0) revert InvalidDelegationRate();

127:       revert InvalidDelegationRate();

130:       revert InvalidRegularPeriodThreshold();

133:       revert InvalidMinOperatorStakeAmount();

136:       revert InvalidMinOperatorStakeAmount();

139:       revert InvalidMinCommunityStakeAmount();

142:       revert InvalidMaxAlertingRewardAmount();

229:     if (s_merkleRoot == bytes32(0)) revert MerkleRootNotSet();

291:       revert StakingPoolLib.InvalidPoolStatus(false, true);

313:         revert StakingPoolLib.OperatorDoesNotExist(operator);

318:         revert StakingPoolLib.OperatorIsAssignedToFeed(operator);

360:     if (newRate == 0) revert();

408:     ) revert InvalidMigrationTarget();

419:       revert InvalidMigrationTarget();

423:       revert AccessForbidden();

433:     if (s_migrationTarget == address(0)) revert InvalidMigrationTarget();

453:     if (stakedAmount == 0) revert AccessForbidden();

457:     if (roundId == s_lastAlertedRoundId) revert AlertAlreadyExists(roundId);

460:       revert AlertInvalid();

466:       revert AlertInvalid();

538:     if (amount == 0) revert StakingPoolLib.StakeNotFound(msg.sender);

683:       revert StakingPoolLib.InsufficientStakeAmount(RewardLib.REWARD_PRECISION);

707:         if (data.length == 0) revert AccessForbidden();

712:         ) revert AccessForbidden();

734:       revert StakingPoolLib.InsufficientStakeAmount(i_minCommunityStakeAmount);

740:       revert StakingPoolLib.ExcessiveStakeAmount(maxCommunityStakeAmount - currentStakedAmount);

747:       revert StakingPoolLib.ExcessiveStakeAmount(remainingPoolSpace);

781:       revert StakingPoolLib.InsufficientStakeAmount(i_minOperatorStakeAmount);

787:       revert StakingPoolLib.ExcessiveStakeAmount(maxOperatorStakeAmount - currentStakedAmount);

825:       revert StakingPoolLib.StakeNotFound(staker);

886:     if (!isActive()) revert StakingPoolLib.InvalidPoolStatus(false, true);

899:     if (isActive()) revert StakingPoolLib.InvalidPoolStatus(true, false);

906:     if (msg.sender != getChainlinkToken()) revert SenderNotLinkToken();

```

```solidity
File: example/StakingPoolBase.sol

199:     if (address(params.LINKAddress) == address(0)) revert InvalidZeroAddress();

200:     if (params.minPrincipalPerStaker == 0) revert InvalidMinStakeAmount();

202:       revert InvalidMinStakeAmount();

205:       revert InvalidUnbondingPeriodRange(MIN_UNBONDING_PERIOD, params.maxUnbondingPeriod);

208:       revert InvalidClaimPeriodRange(params.minClaimPeriod, params.maxClaimPeriod);

242:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

268:       revert InvalidMigrationTarget();

280:     if (stakerPrincipal == 0) revert StakeNotFound(msg.sender);

283:       revert UnbondingPeriodActive(staker.unbondingPeriodEndsAt);

315:     if (address(newRewardVault) == address(0)) revert InvalidZeroAddress();

348:     if (staker == address(0)) revert InvalidZeroAddress();

436:     if (migrationProxy == address(0)) revert InvalidZeroAddress();

461:       revert StakerNotInClaimPeriod(msg.sender);

464:       revert CannotClaimRewardWhenPaused();

468:     if (amount == 0) revert UnstakeZeroAmount();

474:     if (amount > stakerPrincipal) revert UnstakeExceedsPrincipal();

479:       revert UnstakePrincipalBelowMinAmount();

625:       revert InvalidPoolSize(maxPoolSize);

631:     ) revert InvalidMaxStakeAmount(maxPrincipalPerStaker);

647:       revert InvalidUnbondingPeriod();

659:       revert InvalidClaimPeriod();

676:       revert InsufficientStakeAmount();

679:       revert ExceedsMaxStakeAmount();

683:       revert ExceedsMaxPoolSize();

703:     if (data.length == 0) revert InvalidData();

753:     if (msg.sender != address(i_LINK)) revert SenderNotLinkToken();

759:     if (s_migrationProxy == address(0)) revert MigrationProxyNotSet();

765:     if (address(s_rewardVault) == address(0)) revert RewardVaultNotSet();

771:     if (s_isOpen) revert PoolHasBeenOpened();

772:     if (s_pool.state.closedAt != 0) revert PoolHasBeenClosed();

778:     if (s_pool.state.closedAt != 0) revert PoolHasBeenClosed();

784:     if (!s_isOpen) revert PoolNotOpen();

790:     if (!isActive()) revert PoolNotActive();

796:     if (s_pool.state.closedAt == 0) revert PoolNotClosed();

802:     if (!s_rewardVault.isOpen() || s_rewardVault.isPaused()) revert RewardVaultNotActive();

```

```solidity
File: example/StakingPoolLib.sol

144:       revert InvalidMaxStakeAmount(maxOperatorStakeAmount);

148:       revert InvalidPoolSize(maxPoolSize);

151:       revert InvalidMaxStakeAmount(maxCommunityStakeAmount);

154:       revert InvalidMaxStakeAmount(maxOperatorStakeAmount);

161:     ) revert InvalidMaxStakeAmount(maxOperatorStakeAmount);

179:       revert InadequateInitialOperatorsCount(pool.state.operatorsCount, minInitialOperatorCount);

228:       revert InsufficientRemainingPoolSpace(remainingPoolSpace, requiredReservedPoolSpace);

233:         revert OperatorAlreadyExists(operators[i]);

236:         revert ExistingStakeFound(operators[i]);

241:         revert OperatorIsLocked(operators[i]);

262:         revert OperatorDoesNotExist(newFeedOperator);

265:         revert OperatorAlreadyExists(newFeedOperator);

```

</details> 
 


 ### <a name="GAS-17"></a>[GAS-17] Structs can be packed into fewer storage slots
Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings

*Instances (34)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

33:   struct ConstructorParams {

```

```solidity
File: example/IRewardVault.sol

13:   struct StakerReward {

```

```solidity
File: example/ISlashable.sol

19:   struct SlasherConfig {

27:   struct SlasherState {

```

```solidity
File: example/IStakingPool.sol

79:   struct Staker {

```

```solidity
File: example/MigrationProxy.sol

41:   struct ConstructorParams {

```

```solidity
File: example/OperatorStakingPool.sol

107:   struct ConstructorParams {

116:   struct Operator {

```

```solidity
File: example/PriceFeedAlertsController.sol

116:   struct ConstructorParams {

128:   struct ConstructorFeedConfigParams {

154:   struct SetFeedConfigParams {

178:   struct FeedConfig {

201:   struct LastAlertedRoundId {

210:   struct CanAlertReturnValues {

```

```solidity
File: example/RewardLib.sol

46:   struct DelegatedRewards {

60:   struct BaseRewards {

71:   struct MissedRewards {

78:   struct ReservedRewards {

91:   struct Reward {

```

```solidity
File: example/RewardVault.sol

200:   struct ConstructorParams {

216:   struct RewardBucket {

228:   struct RewardBuckets {

238:   struct VaultConfig {

249:   struct VestingCheckpointData {

266:   struct BucketRewardEmissionSplit {

```

```solidity
File: example/Staking.sol

38:   struct PoolConstructorParams {

```

```solidity
File: example/StakingPoolBase.sol

111:   struct ConstructorParamsBase {

136:   struct PoolConfigs {

156:   struct PoolState {

164:   struct Pool {

```

```solidity
File: example/StakingPoolLib.sol

89:   struct PoolLimits {

98:   struct PoolState {

109:   struct Staker {

122:   struct Pool {

```

</details> 
 


 ### <a name="GAS-18"></a>[GAS-18] Use storage instead of memory for structs/arrays
When fetching data from a storage location, assigning the data to a memory variable causes all fields of the struct/array to be read from storage, which incurs a Gcoldsload (2100 gas) for each field of the struct/array. If the fields are read from the new memory variable, they incur an additional MLOAD rather than a cheap stack read. Instead of declaring the variable with the memory keyword, declaring the variable with the storage keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incurring the Gcoldsload for the fields actually read. The only time it makes sense to read the whole struct/array into a memory variable, is if the full struct/array is being returned by the function, is being passed to a function that requires memory, or if the array/struct is being read from another memory array/struct.

*Instances (6)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

263:     SlasherConfig memory slasherConfig = s_slasherConfigs[slasher];

380:     SlasherState memory slasherState = s_slasherState[slasher];

```

```solidity
File: example/PriceFeedAlertsController.sol

477:       SetFeedConfigParams memory configParams = configs[i];

520:     FeedConfig memory feedConfig = s_feedConfigs[feed];

```

```solidity
File: example/RewardVault.sol

1504:     StakerReward memory stakerReward = s_rewards[staker];

1621:     StakerReward memory stakerReward = s_rewards[staker];

```

</details> 
 


 ### <a name="GAS-19"></a>[GAS-19] Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency
Using uint256(1) and uint256(2) instead of true and false can save gas for certain changes. Consider using uint256(1)/uint256(2) when appropriate.

*Instances (34)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

110:     if (s_merkleRoot == bytes32(0)) return true;

```

```solidity
File: example/OperatorStakingPool.sol

454:       operator.isOperator = true;

496:         shouldClaim: false,

501:       operator.isOperator = false;

502:       operator.isRemoved = true;

```

```solidity
File: example/PriceFeedAlertsController.sol

522:       CanAlertReturnValues({canAlert: false, roundId: roundId, feedConfig: feedConfig}); //default false return

522:       CanAlertReturnValues({canAlert: false, roundId: roundId, feedConfig: feedConfig}); //default false return

544:       returnValues.canAlert = true;

```

```solidity
File: example/RewardLib.sol

275:     _updateReservedRewards(reward, baseRewardAmount, delegatedRewardAmount, true);

288:     _updateReservedRewards(reward, baseRewardAmount, delegatedRewardAmount, false);

```

```solidity
File: example/RewardVault.sol

325:     s_vaultConfig.isOpen = true;

637:       shouldForfeit: false,

1658:       shouldForfeit: true,

```

```solidity
File: example/Staking.sol

178:     if (s_merkleRoot == bytes32(0)) return true;

291:       revert StakingPoolLib.InvalidPoolStatus(false, true);

291:       revert StakingPoolLib.InvalidPoolStatus(false, true);

351:       s_pool.stakers[operator].isOperator = false;

510:     if (getStake(alerter) == 0) return false;

511:     if (!isActive()) return false;

513:     if (roundId == s_lastAlertedRoundId) return false;

516:     if (block.timestamp < updatedAt + i_priorityPeriodThreshold) return false;

519:     if (block.timestamp >= updatedAt + i_regularPeriodThreshold) return true;

886:     if (!isActive()) revert StakingPoolLib.InvalidPoolStatus(false, true);

886:     if (!isActive()) revert StakingPoolLib.InvalidPoolStatus(false, true);

899:     if (isActive()) revert StakingPoolLib.InvalidPoolStatus(true, false);

899:     if (isActive()) revert StakingPoolLib.InvalidPoolStatus(true, false);

```

```solidity
File: example/StakingPoolBase.sol

368:       shouldClaim: false,

416:     s_isOpen = true;

425:     s_isOpen = false;

726:       return false;

```

```solidity
File: example/StakingPoolLib.sol

181:     pool.state.isOpen = true;

187:     pool.state.isOpen = false;

243:       pool.stakers[operators[i]].isOperator = true;

268:       pool.stakers[newFeedOperator].isFeedOperator = true;

```

</details> 
 


 ### <a name="GAS-20"></a>[GAS-20] Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead
Using uints or ints smaller than 32 bytes (256 bits) can incur overhead. Consider using uint256 or int256 to avoid potential issues.

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

281:     uint256 alerterRewardAmount //@audit-issue better to use uint8 or 32

```

```solidity
File: example/RewardLib.sol

49:     uint8 delegatesCount;

```

```solidity
File: example/Staking.sol

793:       uint8 delegatesCount = s_reward.delegated.delegatesCount;

```

```solidity
File: example/StakingPoolLib.sol

102:     uint8 operatorsCount;

```

</details> 
 


 ### <a name="GAS-21"></a>[GAS-21] Use != 0 instead of > 0 for unsigned integer comparison

*Instances (32)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/OperatorStakingPool.sol

175:     if (amount > s_alerterRewardFunds) {

288:     if (combinedSlashAmount > remainingSlashCapacity) {

325:         principalAmount > operatorPrincipal ? operatorPrincipal : principalAmount;

```

```solidity
File: example/PriceFeedAlertsController.sol

485:       if (configParams.slashableAmount == 0 || configParams.slashableAmount > operatorMaxPrincipal)

```

```solidity
File: example/RewardLib.sol

254:       if (baseRewardAmount % REWARD_PRECISION > 0) deltaBaseReward++;

255:       if (delegatedRewardAmount % REWARD_PRECISION > 0) deltaDelegatedReward++;

```

```solidity
File: example/RewardVault.sol

1459:     uint112 newlyEarnedBaseRewards = claimableBaseRewards > stakerReward.claimedBaseRewardsInPeriod

```

```solidity
File: example/Staking.sol

126:     if (RewardLib.REWARD_PRECISION % params.delegationRateDenominator > 0) {

135:     if (params.minOperatorStakeAmount > params.initialMaxOperatorStakeAmount) {

138:     if (params.minCommunityStakeAmount > params.initialMaxCommunityStakeAmount) {

141:     if (params.maxAlertingRewardAmount > params.initialMaxOperatorStakeAmount) {

290:     if (s_reward.startTimestamp > 0 && !isActive()) {

323:       if (principal > 0) {

696:     if (remainder > 0) {

739:     if (newStakedAmount > maxCommunityStakeAmount) {

746:     if (amount > remainingPoolSpace) {

786:     if (newStakedAmount > maxOperatorStakeAmount) {

```

```solidity
File: example/StakingPoolBase.sol

204:     if (MIN_UNBONDING_PERIOD > params.maxUnbondingPeriod) {

474:     if (amount > stakerPrincipal) revert UnstakeExceedsPrincipal();

629:       maxPrincipalPerStaker == 0 || maxPrincipalPerStaker > maxPoolSize

630:         || configs.maxPrincipalPerStaker > maxPrincipalPerStaker

646:     if (unbondingPeriod < MIN_UNBONDING_PERIOD || unbondingPeriod > i_maxUnbondingPeriod) {

658:     if (claimPeriod < i_minClaimPeriod || claimPeriod > i_maxClaimPeriod) {

678:     if (newPrincipal > s_pool.configs.maxPrincipalPerStaker) {

682:     if (newTotalPrincipal > s_pool.configs.maxPoolSize) {

```

```solidity
File: example/StakingPoolLib.sol

143:     if (maxOperatorStakeAmount > maxPoolSize) {

147:     if (pool.limits.maxPoolSize > maxPoolSize) {

150:     if (pool.limits.maxCommunityStakeAmount > maxCommunityStakeAmount) {

153:     if (pool.limits.maxOperatorStakeAmount > maxOperatorStakeAmount) {

227:     if (requiredReservedPoolSpace > remainingPoolSpace) {

235:       if (pool.stakers[operators[i]].stakedAmount > 0) {

240:       if (pool.stakers[operators[i]].removedStakeAmount > 0) {

```

</details> 
 


 ### <a name="GAS-22"></a>[GAS-22] `internal` functions not called by the contract should be removed
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/RewardLib.sol

112:   function _initialize(

217:   function _calculateConcludedBaseRewards(

270:   function _reserve(

294:   function _release(Reward storage reward, uint256 amount, uint256 delegatedAmount) internal {

319:   function _getNonDelegatedAmount(

413:   function _slashOnFeedOperators(

```

```solidity
File: example/StakingPoolLib.sol

137:   function _setConfig(

177:   function _open(Pool storage pool, uint256 minInitialOperatorCount) internal {

186:   function _close(Pool storage pool) internal {

200:   function _getTotalStakedAmount(Pool storage pool) internal view returns (uint256) {

223:   function _addOperators(Pool storage pool, address[] calldata operators) internal {

253:   function _setFeedOperators(Pool storage pool, address[] calldata operators) internal {

```

</details> 
 


 ### <a name="GAS-23"></a>[GAS-23] Optimize names to save gas
public/external function names and public member variable names can be optimized to save gas. See [this](https://gist.github.com/IllIllI000/a5d8b486a8259f9f77891a919febd1a9) link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92)

*Instances (159)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: example/CommunityStakingPool.sol

99:   ) external view override returns (bool) {

121:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyRole(DEFAULT_ADMIN_ROLE) {

127:   function getMerkleRoot() external view override returns (bytes32) {

149:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/IAlertsController.sol

25:   function canAlert(address alerter) external view returns (bool);

```

```solidity
File: example/IAlertsControllerOwner.sol

14:   function getSlashableOperators(bytes calldata data) external view returns (address[] memory);

```

```solidity
File: example/IMerkleAccessController.sol

12:   function hasAccess(address staker, bytes32[] calldata proof) external view returns (bool);

22:   function getMerkleRoot() external view returns (bytes32);

```

```solidity
File: example/IMigratable.sol

26:   function getMigrationTarget() external view returns (address);

```

```solidity
File: example/IRewardVault.sol

133:   function isOpen() external view returns (bool);

139:   function getReward(address staker) external view returns (uint256);

144:   function getStoredReward(address staker) external view returns (StakerReward memory);

148:   function isPaused() external view returns (bool);

153:   function hasRewardDurationEnded(address stakingPool) external view returns (bool);

```

```solidity
File: example/ISlashable.sol

49:   function getSlasherConfig(address slasher) external view returns (SlasherConfig memory);

54:   function getSlashCapacity(address slasher) external view returns (uint256);

```

```solidity
File: example/IStaking.sol

39:   function getChainlinkToken() external view returns (address);

43:   function getStake(address staker) external view returns (uint256);

46:   function isOperator(address staker) external view returns (bool);

51:   function isActive() external view returns (bool);

54:   function getMaxPoolSize() external view returns (uint256);

58:   function getCommunityStakerLimits() external view returns (uint256, uint256);

62:   function getOperatorLimits() external view returns (uint256, uint256);

66:   function getRewardTimestamps() external view returns (uint256, uint256);

69:   function getRewardRate() external view returns (uint256);

72:   function getDelegationRateDenominator() external view returns (uint256);

81:   function getAvailableReward() external view returns (uint256);

84:   function getBaseReward(address) external view returns (uint256);

87:   function getDelegationReward(address) external view returns (uint256);

93:   function getTotalDelegatedAmount() external view returns (uint256);

98:   function getDelegatesCount() external view returns (uint256);

101:   function getEarnedBaseRewards() external view returns (uint256);

104:   function getEarnedDelegationRewards() external view returns (uint256);

107:   function getTotalStakedAmount() external view returns (uint256);

110:   function getTotalCommunityStakedAmount() external view returns (uint256);

116:   function getTotalRemovedAmount() external view returns (uint256);

120:   function isPaused() external view returns (bool);

123:   function getMonitoredFeed() external view returns (address);

```

```solidity
File: example/IStakingOwner.sol

53:   function getFeedOperators() external view returns (address[] memory);

```

```solidity
File: example/IStakingPool.sol

104:   function getTotalPrincipal() external view returns (uint256);

109:   function getStakerPrincipal(address staker) external view returns (uint256);

119:   ) external view returns (uint256);

124:   function getStakerStakedAtTime(address staker) external view returns (uint256);

133:   ) external view returns (uint256);

137:   function getRewardVault() external view returns (IRewardVault);

141:   function getChainlinkToken() external view returns (address);

145:   function getMigrationProxy() external view returns (address);

149:   function isOpen() external view returns (bool);

154:   function isActive() external view returns (bool);

160:   function getStakerLimits() external view returns (uint256, uint256);

164:   function getMaxPoolSize() external view returns (uint256);

```

```solidity
File: example/Migratable.sol

11:   function setMigrationTarget(address newMigrationTarget) external virtual override {

32:   function getMigrationTarget() external view virtual override returns (address) {

```

```solidity
File: example/MigrationProxy.sol

95:   ) external override whenNotPaused validateFromLINK {

137:   function getConfig() external view returns (address, address, address, address) {

156:   function supportsInterface(bytes4 interfaceId) public view override returns (bool) {

165:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/OperatorStakingPool.sol

142:   bytes32 public constant SLASHER_ROLE = keccak256('SLASHER_ROLE');

187:   function getAlerterRewardFunds() external view returns (uint256) {

207:   ) public virtual override(AccessControlDefaultAdminRules) {

221:   ) external override onlyRole(DEFAULT_ADMIN_ROLE) {

231:   ) external override onlyRole(DEFAULT_ADMIN_ROLE) {

257:   function getSlasherConfig(address slasher) external view override returns (SlasherConfig memory) {

262:   function getSlashCapacity(address slasher) external view override returns (uint256) {

282:   ) external override onlySlasher whenActive {

405:     external

428:     external

517:   function isOperator(address staker) external view returns (bool) {

524:   function isRemoved(address staker) external view returns (bool) {

531:   function getRemovedPrincipal(address staker) external view returns (uint256) {

558:   function getNumOperators() external view returns (uint256) {

568:   function supportsInterface(bytes4 interfaceID) public view override returns (bool) {

603:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/PausableWithAccessControl.sol

14:   bytes32 public constant PAUSER_ROLE = keccak256('PAUSER_ROLE');

22:   function emergencyPause() external override onlyRole(PAUSER_ROLE) {

27:   function emergencyUnpause() external override onlyRole(PAUSER_ROLE) {

```

```solidity
File: example/PriceFeedAlertsController.sol

315:   function getFeedConfig(address feed) external view returns (FeedConfig memory) {

331:   function raiseAlert(address feed) external whenNotPaused { //@audit yeh dkhna ha again

354:   function canAlert(address alerter, address feed) external view returns (bool) {

361:   function getStakingPools() external view returns (address[] memory) {

388:   function getSlashableOperators(address feed) external view returns (address[] memory) {

588:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/RewardVault.sol

284:   bytes32 public constant REWARDER_ROLE = keccak256('REWARDER_ROLE');

349:   ) external onlyRewarder whenOpen whenNotPaused {

376:   function getDelegationRateDenominator() external view returns (uint256) {

477:   function getMigrationSource() external view returns (address) {

551:   function supportsInterface(bytes4 interfaceID) public view override returns (bool) {

565:   function onTokenTransfer(address sender, uint256 amount, bytes calldata data) external override {

622:   function claimReward() external override whenNotPaused returns (uint256) {

686:   function updateReward(address staker, uint256 stakerPrincipal) external override onlyStakingPool {

726:   ) external override onlyStakingPool returns (uint256) {

792:   function close() external override onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

802:   function getReward(address staker) external view override returns (uint256) {

818:   function isOpen() external view override returns (bool) {

823:   function hasRewardDurationEnded(address stakingPool) external view override returns (bool) {

836:   function getStoredReward(address staker) external view override returns (StakerReward memory) {

842:   function getRewardBuckets() external view returns (RewardBuckets memory) {

848:   function getRewardPerTokenUpdatedAt() external view returns (uint256) {

854:   function getMultiplierDuration() external view returns (uint256) {

863:   function getMultiplier(address staker) external view returns (uint256) {

876:     external

885:   function getVestingCheckpointData() external view returns (VestingCheckpointData memory) {

893:   function getUnvestedRewards() external view returns (uint256, uint256, uint256) {

903:   function isPaused() external view override(IRewardVault) returns (bool) {

1516:       baseRewardPerToken: isOperator //@audit yeh function kahan kahan call ho raha because yeh check kar raha ke community or operator both

1740:   function typeAndVersion() external pure virtual override returns (string memory) {

```

```solidity
File: example/Staking.sol

168:   function typeAndVersion() external pure override returns (string memory) {

177:   function hasAccess(address staker, bytes32[] memory proof) external view override returns (bool) {

183:   function setMerkleRoot(bytes32 newMerkleRoot) external override onlyOwner {

189:   function getMerkleRoot() external view override returns (bytes32) {

359:   function changeRewardRate(uint256 newRate) external override onlyOwner whenActive {

389:   function getFeedOperators() external view override(IStakingOwner) returns (address[] memory) {

398:   function getMigrationTarget() external view override(IMigratable) returns (address) {

509:   function canAlert(address alerter) external view override(IAlertsController) returns (bool) {

547:   function getStake(address staker) public view override(IStaking) returns (uint256) {

552:   function isOperator(address staker) external view override(IStaking) returns (bool) {

557:   function isActive() public view override(IStaking) returns (bool) {

562:   function getMaxPoolSize() external view override(IStaking) returns (uint256) {

567:   function getCommunityStakerLimits() external view override(IStaking) returns (uint256, uint256) {

572:   function getOperatorLimits() external view override(IStaking) returns (uint256, uint256) {

577:   function getRewardTimestamps() external view override(IStaking) returns (uint256, uint256) {

582:   function getRewardRate() external view override(IStaking) returns (uint256) {

587:   function getDelegationRateDenominator() external view override(IStaking) returns (uint256) {

592:   function getAvailableReward() public view override(IStaking) returns (uint256) {

598:   function getBaseReward(address staker) public view override(IStaking) returns (uint256) {

612:   function getDelegationReward(address staker) public view override(IStaking) returns (uint256) {

620:   function getTotalDelegatedAmount() public view override(IStaking) returns (uint256) {

627:   function getDelegatesCount() external view override(IStaking) returns (uint256) {

632:   function getTotalStakedAmount() external view override(IStaking) returns (uint256) {

637:   function getTotalCommunityStakedAmount() external view override(IStaking) returns (uint256) {

642:   function getTotalRemovedAmount() external view override(IStaking) returns (uint256) {

647:   function getEarnedBaseRewards() external view override(IStaking) returns (uint256) {

652:   function getEarnedDelegationRewards() external view override(IStaking) returns (uint256) {

657:   function isPaused() external view override(IStaking) returns (bool) {

662:   function getChainlinkToken() public view override(IStaking) returns (address) {

667:   function getMonitoredFeed() external view override returns (address) {

681:   ) external validateFromLINK whenNotPaused whenActive {

```

```solidity
File: example/StakingPoolBase.sol

301:   function getUnbondingPeriodLimits() external view returns (uint256, uint256) {

336:     external

389:   function getClaimPeriodLimits() external view returns (uint256, uint256) {

402:   ) external virtual override onlyRole(DEFAULT_ADMIN_ROLE) whenOpen {

435:   function setMigrationProxy(address migrationProxy) external override onlyRole(DEFAULT_ADMIN_ROLE) {

458:   function unstake(uint256 amount, bool shouldClaimReward) external override {

507:   function getTotalPrincipal() external view override returns (uint256) {

512:   function getStakerPrincipal(address staker) external view override returns (uint256) {

524:   ) external view override returns (uint256) {

531:   function getStakerStakedAtTime(address staker) external view override returns (uint256) {

543:   ) external view override returns (uint256) {

550:   function getRewardVault() external view override returns (IRewardVault) {

555:   function getChainlinkToken() external view override returns (address) {

560:   function getMigrationProxy() external view override returns (address) {

565:   function isOpen() external view override returns (bool) {

570:   function isActive() public view override returns (bool) {

575:   function getStakerLimits() external view override returns (uint256, uint256) {

580:   function getMaxPoolSize() external view override returns (uint256) {

588:   function getUnbondingEndsAt(address staker) external view returns (uint256) {

595:   function getUnbondingParams() external view returns (uint256, uint256) {

603:   function getClaimPeriodEndsAt(address staker) external view returns (uint256) {

609:   function getCurrentCheckpointId() external view returns (uint32) {

```

</details> 
 

