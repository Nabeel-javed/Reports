# Report


## Medium Issues


| |Issue|Instances|
|-|:-|:-:|
| [M-1](#M-1) | Code will not work properly on L2 due to block.number | 9 |
| [M-2](#M-2) | Centralization Risk for trusted owners | 16 |
| [M-3](#M-3) | Unsafe use of ERC20 transferFrom() | 2 |
| [M-4](#M-4) | Unsafe use of ERC20 transfer() | 2 |
| [M-5](#M-5) | Timestamp may be manipulation | 2 |

## Low Issues


| |Issue|Instances|
|-|:-|:-:|
| [L-1](#L-1) | Do not use deprecated library functions | 4 |
| [L-2](#L-2) | Division by zero not prevented | 15 |
| [L-3](#L-3) | Empty function body | 1 |
| [L-4](#L-4) | Initializers could be front-run | 14 |
| [L-5](#L-5) | Loss of precision | 15 |
| [L-6](#L-6) | State variables not capped at reasonable values | 190 |
| [L-7](#L-7) | Some tokens may revert when zero value transfers are made | 2 |
| [L-8](#L-8) |  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard   | 2 |
| [L-9](#L-9) | Some tokens may revert when large transfers are made | 2 |

## Non Critical Issues


| |Issue|Instances|
|-|:-|:-:|
| [NC-1](#NC-1) | assert() should be replaced with require() or revert() | 1 |
| [NC-2](#NC-2) | Custom error has no error details | 35 |
| [NC-3](#NC-3) | Variables without visibility specifier | 160 |
| [NC-4](#NC-4) | Array is push()ed but not pop()ed | 3 |
| [NC-5](#NC-5) | Constants in comparisons should appear on the left side | 97 |
| [NC-6](#NC-6) | Consider using delete rather than assigning zero to clear value | 10 |
| [NC-7](#NC-7) | Consider using delete rather than assigning false to clear value | 1 |
| [NC-8](#NC-8) | Consider adding a block/deny-list" | 26 |
| [NC-9](#NC-9) | Events are missing sender information | 66 |
| [NC-10](#NC-10) | If-statement can be converted to a ternary | 124 |
| [NC-11](#NC-11) | Variable names for immutables should use CONSTANT_CASE | 3 |
| [NC-12](#NC-12) | Contract should expose an interface | 10 |
| [NC-13](#NC-13) | Large multiples of ten should use scientific notation | 2 |
| [NC-14](#NC-14) | Consider using named mappings | 12 |
| [NC-15](#NC-15) | Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct | 27 |
| [NC-16](#NC-16) | Use of override is unnecessary | 57 |
| [NC-17](#NC-17) | Consider using descriptive constants when using 0 in the code | 26 |
| [NC-18](#NC-18) | Non-external/public variable names should begin with an underscore | 72 |
| [NC-19](#NC-19) | Use the latest solidity version for deployment   | 28 |
| [NC-20](#NC-20) | Event is missing `indexed` fields | 59 |
| [NC-21](#NC-21) | Strings should use double quotes rather than single quotes | 1 |
| [NC-22](#NC-22) | Functions not used internally could be marked external | 5 |
| [NC-23](#NC-23) | Consider moving msg.sender checks to modifiers | 49 |
| [NC-24](#NC-24) | Array indices should be referenced via enums rather than numeric literals | 8 |
| [NC-25](#NC-25) | Use assembly to emit events, in order to save gas | 80 |
| [NC-26](#NC-26) | Don't initialize variables with default value | 2 |
| [NC-27](#NC-27) | Long revert strings | 54 |

## Gas Optimizations


| |Issue|Instances|
|-|:-|:-:|
| [GAS-1](#GAS-1) | Use scientific notation (e.g. 1e18) rather than exponentiation (e.g. 10**18) | 3 |
| [GAS-2](#GAS-2) | Nesting if-statements is cheaper than using && | 27 |
| [GAS-3](#GAS-3) | Consider using = instead of += and -= for gas efficiency | 2 |
| [GAS-4](#GAS-4) | Use >= instead of > for gas efficiency | 49 |
| [GAS-5](#GAS-5) | `array[index] += amount` is cheaper than `array[index] = array[index] + amount` (or related variants) | 4 |
| [GAS-6](#GAS-6) | Using bools for storage incurs overhead | 7 |
| [GAS-7](#GAS-7) | Cache array length outside of loop | 3 |
| [GAS-8](#GAS-8) | State variables should be cached in stack variables rather than re-reading them from storage | 3 |
| [GAS-9](#GAS-9) | Use calldata instead of memory for function arguments that do not get mutated | 15 |
| [GAS-10](#GAS-10) | Consider using assembly for simple zero checks to save gas | 6 |
| [GAS-11](#GAS-11) | Expressions for constant values should use immutable rather than constant | 22 |
| [GAS-12](#GAS-12) | Constructors can be marked payable | 11 |
| [GAS-13](#GAS-13) | Use Custom Errors | 89 |
| [GAS-14](#GAS-14) | Initializers can be marked as payable to save deployment gas | 7 |
| [GAS-15](#GAS-15) | Reduce gas usage by moving to Solidity 0.8.19 or later | 28 |
| [GAS-16](#GAS-16) | Functions guaranteed to revert when called by normal users can be marked `payable` | 18 |
| [GAS-17](#GAS-17) | `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too) | 1 |
| [GAS-18](#GAS-18) | Using `private` rather than `public` for constants, saves gas | 6 |
| [GAS-19](#GAS-19) | require()/revert() strings longer than 32 bytes cost extra gas | 170 |
| [GAS-20](#GAS-20) | Use shift Right/Left instead of division/multiplication if possible | 1 |
| [GAS-21](#GAS-21) | Splitting require() statements that use && saves gas | 2 |
| [GAS-22](#GAS-22) | Structs can be packed into fewer storage slots | 23 |
| [GAS-23](#GAS-23) | Variables can be packed into fewer storage slots by truncating timestamp bytes | 2 |
| [GAS-24](#GAS-24) | Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency | 18 |
| [GAS-25](#GAS-25) | Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead | 5 |
| [GAS-26](#GAS-26) | Use != 0 instead of > 0 for unsigned integer comparison | 49 |
| [GAS-27](#GAS-27) | `internal` functions not called by the contract should be removed | 10 |
| [GAS-28](#GAS-28) | Optimize names to save gas | 229 |

##################################################################### 
 
 DETAILED REPORT:: 


##################################################################### 


## Medium Issues


 ### <a name="M-1"></a>[M-1]
 ### Code will not work properly on L2 due to block.number
On L2, the block.number is not a reliable source of timing information and the time between each block is also different from Ethereum. This is because each transaction on L2 is placed in a separate block and blocks are not produce at a constant rate.

*Instances (9)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Lens/PoolLens.sol

459:         uint256 blockNumber = block.number;

480:         uint256 blockNumber = block.number;

```

```solidity
File: Pool/PoolRegistry.sol

400:         VenusPool memory pool = VenusPool(name, msg.sender, comptroller, block.number, block.timestamp);

```

```solidity
File: Rewards/RewardsDistributor.sol

295:         return block.number;

```

```solidity
File: Shortfall/Shortfall.sol

198:         auction.highestBidBlock = block.number;

213:             block.number > auction.highestBidBlock + nextBidderBlockLimit && auction.highestBidder != address(0),

420:         auction.startBlock = block.number;

468:         return noBidder && (block.number > auction.startBlock + waitForFirstBidder);

```

```solidity
File: VToken.sol

1431:         return block.number;

```

</details> 
 


 ### <a name="M-2"></a>[M-2]
 ### Centralization Risk for trusted owners

#### Impact:
Contracts have owners with privileged rights to perform admin tasks and need to be trusted to not perform malicious updates or drain funds.

*Instances (16)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

926:     function addRewardsDistributor(RewardsDistributor _rewardsDistributor) external onlyOwner {

960:     function setPriceOracle(PriceOracle newOracle) external onlyOwner {

972:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

```

```solidity
File: Pool/PoolRegistry.sol

187:     function setProtocolShareReserve(address payable protocolShareReserve_) external onlyOwner {

197:     function setShortfallContract(Shortfall shortfall_) external onlyOwner {

```

```solidity
File: Rewards/RewardsDistributor.sol

181:     function grantRewardToken(address recipient, uint256 amount) external onlyOwner {

219:     function setContributorRewardTokenSpeed(address contributor, uint256 rewardTokenSpeed) external onlyOwner {

249:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

53:     function setPoolRegistry(address _poolRegistry) external onlyOwner {

```

```solidity
File: RiskFund/RiskFund.sol

99:     function setPoolRegistry(address _poolRegistry) external onlyOwner {

110:     function setShortfallContractAddress(address shortfallContractAddress_) external onlyOwner {

126:     function setPancakeSwapRouter(address pancakeSwapRouter_) external onlyOwner {

205:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

```

```solidity
File: Shortfall/Shortfall.sol

347:     function updatePoolRegistry(address _poolRegistry) external onlyOwner {

```

```solidity
File: VToken.sol

505:     function setProtocolShareReserve(address payable protocolShareReserve_) external onlyOwner {

515:     function setShortfallContract(address shortfall_) external onlyOwner {

```

</details> 
 


 ### <a name="M-3"></a>[M-3]
 ### Unsafe use of ERC20 transferFrom()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transferFrom() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransferFrom() from OpenZeppelin instead.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: VToken.sol

114:     function transferFrom(

```

```solidity
File: VTokenInterfaces.sol

312:     function transferFrom(

```

</details> 
 


 ### <a name="M-4"></a>[M-4]
 ### Unsafe use of ERC20 transfer()
Some tokens do not implement the ERC20 standard properly. For example Tether (USDT)'s transfer() function does not return a boolean as the ERC20 specification requires, and instead has no return value. When these sorts of tokens are cast to IERC20/ERC20, their function signatures do not match and therefore the calls made will revert. It is recommended to use the SafeERC20's safeTransfer() from OpenZeppelin instead.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: VToken.sol

99:     function transfer(address dst, uint256 amount) external override nonReentrant returns (bool) {

```

```solidity
File: VTokenInterfaces.sol

310:     function transfer(address dst, uint256 amount) external virtual returns (bool);

```

</details> 
 


 ### <a name="M-5"></a>[M-5]
 ### Timestamp may be manipulation
The block.timestamp can be manipulated by miners to perform MEV profiting or other time-based attacks.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Pool/PoolRegistry.sol

400:         VenusPool memory pool = VenusPool(name, msg.sender, comptroller, block.number, block.timestamp);

```

```solidity
File: RiskFund/RiskFund.sol

265:                         block.timestamp

```

</details> 
 


## Low Issues


 ### <a name="L-1"></a>[L-1]
 ### Do not use deprecated library functions

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Pool/PoolRegistry.sol

321:         token.safeApprove(address(vToken), 0);

322:         token.safeApprove(address(vToken), amountToSupply);

```

```solidity
File: RiskFund/RiskFund.sol

258:                     IERC20Upgradeable(underlyingAsset).safeApprove(pancakeSwapRouter, 0);

259:                     IERC20Upgradeable(underlyingAsset).safeApprove(pancakeSwapRouter, balanceOfUnderlyingAsset);

```

</details> 
 


 ### <a name="L-2"></a>[L-2]
 ### Division by zero not prevented
The divisions below take an input parameter that has no zero-value checks, which can cause the functions reverting if zero is passed.  

*Instances (15)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

119:         uint256 rateToPool = (borrowRate * oneMinusReserveFactor) / BASE;

120:         return (utilizationRate(cash, borrows, reserves) * rateToPool) / BASE;

156:         baseRatePerBlock = baseRatePerYear / blocksPerYear;

158:         jumpMultiplierPerBlock = jumpMultiplierPerYear / blocksPerYear;

```

```solidity
File: ExponentialNoError.sol

22:     uint256 internal constant halfExpScale = expScale / 2;

31:         return exp.mantissa / expScale;

106:         return mul_(a, b.mantissa) / expScale;

118:         return mul_(a, b.mantissa) / doubleScale;

150:         return a / b;

```

```solidity
File: Shortfall/Shortfall.sol

243:             riskFundBidAmount = (auction.seizedRiskFund * auction.highestBidBps) / MAX_BPS;

```

```solidity
File: VToken.sol

1478:             uint256 exchangeRate = (cashPlusBorrowsMinusReserves * expScale) / _totalSupply;

```

```solidity
File: WhitePaperInterestRateModel.sol

37:         baseRatePerBlock = baseRatePerYear / blocksPerYear;

38:         multiplierPerBlock = multiplierPerYear / blocksPerYear;

75:         uint256 rateToPool = (borrowRate * oneMinusReserveFactor) / BASE;

76:         return (utilizationRate(cash, borrows, reserves) * rateToPool) / BASE;

```

</details> 
 


 ### <a name="L-3"></a>[L-3]
 ### Empty function body
Consider adding a comment about why the function body is empty

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: JumpRateModelV2.sol

21:     {

```

</details> 
 


 ### <a name="L-4"></a>[L-4]
 ### Initializers could be front-run
Initializers could be front-run, allowing an attacker to either set their own values, take ownership of the contract, and in the best case forcing a re-deployment

*Instances (14)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

137:     function initialize(uint256 loopLimit, address accessControlManager) external initializer {

137:     function initialize(uint256 loopLimit, address accessControlManager) external initializer {

```

```solidity
File: Pool/PoolRegistry.sol

163:     function initialize(

170:     ) external initializer {

```

```solidity
File: Rewards/RewardsDistributor.sol

111:     function initialize(

116:     ) external initializer {

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

39:     function initialize(address _protocolIncome, address _riskFund) external initializer {

39:     function initialize(address _protocolIncome, address _riskFund) external initializer {

```

```solidity
File: RiskFund/RiskFund.sol

73:     function initialize(

79:     ) external initializer {

```

```solidity
File: Shortfall/Shortfall.sol

130:     function initialize(

135:     ) external initializer {

```

```solidity
File: VToken.sol

59:     function initialize(

71:     ) external initializer {

```

</details> 
 


 ### <a name="L-5"></a>[L-5]
 ### Loss of precision
Division by large numbers or variables may result in the result being zero, due to Solidity not supporting fractions.

*Instances (15)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

119:         uint256 rateToPool = (borrowRate * oneMinusReserveFactor) / BASE;

120:         return (utilizationRate(cash, borrows, reserves) * rateToPool) / BASE;

156:         baseRatePerBlock = baseRatePerYear / blocksPerYear;

158:         jumpMultiplierPerBlock = jumpMultiplierPerYear / blocksPerYear;

```

```solidity
File: ExponentialNoError.sol

22:     uint256 internal constant halfExpScale = expScale / 2;

31:         return exp.mantissa / expScale;

106:         return mul_(a, b.mantissa) / expScale;

118:         return mul_(a, b.mantissa) / doubleScale;

150:         return a / b;

```

```solidity
File: Shortfall/Shortfall.sol

243:             riskFundBidAmount = (auction.seizedRiskFund * auction.highestBidBps) / MAX_BPS;

```

```solidity
File: VToken.sol

1478:             uint256 exchangeRate = (cashPlusBorrowsMinusReserves * expScale) / _totalSupply;

```

```solidity
File: WhitePaperInterestRateModel.sol

37:         baseRatePerBlock = baseRatePerYear / blocksPerYear;

38:         multiplierPerBlock = multiplierPerYear / blocksPerYear;

75:         uint256 rateToPool = (borrowRate * oneMinusReserveFactor) / BASE;

76:         return (utilizationRate(cash, borrows, reserves) * rateToPool) / BASE;

```

</details> 
 


 ### <a name="L-6"></a>[L-6]
 ### State variables not capped at reasonable values
Consider adding minimum/maximum value checks to ensure that the state variables below can never be used to excessively harm users, including via griefing

*Instances (190)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

137:             return 0;

182:             uint256 excessUtil;

```

```solidity
File: Comptroller.sol

167: 

204:             return NO_ERROR;

232: 

1038:         return allMarkets;

1059: 

1099:         uint256 seizeTokens;

1129:         return rewardSpeeds;

1136:         return _isComptroller;

1144:         return rewardsDistributors;

1358: 

1372:         return oraclePriceMantissa;

1410:         uint256 err;

```

```solidity
File: ComptrollerStorage.sol

8:         VToken vTokenCollateral;

9:         VToken vTokenBorrowed;

10:         uint256 repayAmount;

14:         uint256 totalCollateral;

15:         uint256 weightedCollateral;

16:         uint256 borrows;

17:         uint256 effects;

18:         uint256 liquidity;

19:         uint256 shortfall;

23:         address rewardToken;

24:         uint256 supplySpeed;

25:         uint256 borrowSpeed;

30:         bool isListed;

34:         uint256 collateralFactorMantissa;

38:         uint256 liquidationThresholdMantissa;

```

```solidity
File: ExponentialNoError.sol

13:         uint256 mantissa;

17:         uint256 mantissa;

```

```solidity
File: Factories/JumpRateModelFactory.sol

21: 

```

```solidity
File: Factories/VTokenProxyFactory.sol

12:         address underlying_;

13:         ComptrollerInterface comptroller_;

14:         InterestRateModel interestRateModel_;

15:         uint256 initialExchangeRateMantissa_;

16:         string name_;

17:         string symbol_;

18:         uint8 decimals_;

19:         address admin_;

20:         AccessControlManager accessControlManager_;

22:         address beaconAddress;

23:         uint256 reserveFactor;

```

```solidity
File: Factories/WhitePaperInterestRateModelFactory.sol

9: 

```

```solidity
File: Lens/PoolLens.sol

16:         string name;

17:         address creator;

18:         address comptroller;

19:         uint256 blockPosted;

20:         uint256 timestampPosted;

21:         string category;

22:         string logoURL;

23:         string description;

24:         address priceOracle;

25:         uint256 closeFactor;

26:         uint256 liquidationIncentive;

27:         uint256 minLiquidatableCollateral;

35:         address vToken;

36:         uint256 exchangeRateCurrent;

37:         uint256 supplyRatePerBlock;

38:         uint256 borrowRatePerBlock;

39:         uint256 reserveFactorMantissa;

40:         uint256 supplyCaps;

41:         uint256 borrowCaps;

42:         uint256 totalBorrows;

43:         uint256 totalReserves;

44:         uint256 totalSupply;

45:         uint256 totalCash;

46:         bool isListed;

47:         uint256 collateralFactorMantissa;

48:         address underlyingAssetAddress;

49:         uint256 vTokenDecimals;

50:         uint256 underlyingDecimals;

57:         address vToken;

58:         uint256 balanceOf;

59:         uint256 borrowBalanceCurrent;

60:         uint256 balanceOfUnderlying;

61:         uint256 tokenBalance;

62:         uint256 tokenAllowance;

69:         address vToken;

70:         uint256 underlyingPrice;

77:         address vTokenAddress;

78:         uint256 amount;

85:         address distributorAddress;

86:         address rewardTokenAddress;

87:         uint256 totalRewards;

96:         uint224 index;

98:         uint32 block;

105:         address vTokenAddress;

106:         uint256 badDebtUsd;

113:         address comptroller;

114:         uint256 totalBadDebtUsd;

129:         return res;

149: 

210:         return res;

236:         return rewardSummary;

248:         uint256 totalBadDebtUsd;

273: 

286:         uint256 tokenBalance;

287:         uint256 tokenAllowance;

343: 

356:         address underlyingAssetAddress;

357:         uint256 underlyingDecimals;

393:         return res;

449:         return pendingRewards;

512:         return borrowerDelta;

532:         return supplierDelta;

```

```solidity
File: Pool/PoolRegistry.sol

33:         address comptroller;

34:         address asset;

35:         uint8 decimals;

36:         string name;

37:         string symbol;

38:         InterestRateModels rateModel;

39:         uint256 baseRatePerYear;

40:         uint256 multiplierPerYear;

41:         uint256 jumpMultiplierPerYear;

42:         uint256 kink_;

43:         uint256 collateralFactor;

44:         uint256 liquidationThreshold;

45:         uint256 reserveFactor;

46:         AccessControlManager accessControlManager;

47:         address beaconAddress;

48:         uint256 initialSupply;

49:         address vTokenReceiver;

50:         uint256 supplyCap;

51:         uint256 borrowCap;

266: 

359:         return _pools;

406:         return _numberOfPools;

```

```solidity
File: Pool/PoolRegistryInterface.sol

9:         string name;

10:         address creator;

11:         address comptroller;

12:         uint256 blockPosted;

13:         uint256 timestampPosted;

20:         string category;

21:         string logoURL;

22:         string description;

```

```solidity
File: Rewards/RewardsDistributor.sol

17:         uint224 index;

19:         uint32 block;

420:             return 0;

422:         return amount;

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

88: 

```

```solidity
File: RiskFund/ReserveHelpers.sol

62:             uint256 balanceDifference;

```

```solidity
File: RiskFund/RiskFund.sol

160: 

180: 

197: 

233:         uint256 totalAmount;

273: 

```

```solidity
File: Shortfall/Shortfall.sol

34:         uint256 startBlock;

35:         AuctionType auctionType;

36:         AuctionStatus status;

38:         uint256 seizedRiskFund;

39:         address highestBidder;

40:         uint256 highestBidBps;

41:         uint256 highestBidBlock;

42:         uint256 startBidBps;

237: 

383:         uint256 poolBadDebt;

```

```solidity
File: VToken.sol

101:         return true;

120:         return true;

139:         return true;

159:         return totalBorrows;

184:         return NO_ERROR;

201:         return NO_ERROR;

217:         return NO_ERROR;

230:         return NO_ERROR;

245:         return NO_ERROR;

259:         return NO_ERROR;

274:         return NO_ERROR;

298:         return NO_ERROR;

401: 

634:         return true;

658:         return true;

685:             return NO_ERROR;

732: 

814: 

816:         uint256 redeemAmount;

975: 

1179:         uint256 totalReservesNew;

1180:         uint256 actualAddAmount;

1191: 

1202:         uint256 totalReservesNew;

1245:         InterestRateModel oldInterestRateModel;

1312:         uint256 startingAllowance;

1447:             return 0;

1470:             return initialExchangeRateMantissa;

1479: 

```

```solidity
File: VTokenInterfaces.sol

17:         uint256 principal;

18:         uint256 interestIndex;

134:         address shortfall;

```

```solidity
File: WhitePaperInterestRateModel.sol

93:             return 0;

```

</details> 
 


 ### <a name="L-7"></a>[L-7]
 ### Some tokens may revert when zero value transfers are made
Despite the fact that [EIP-20](https://github.com/ethereum/EIPs/blob/7500ac4fc1bbdfaf684e7ef851f798f6b667b2fe/EIPS/eip-20.md?plain=1#L116) states that zero-value transfers must be accepted, some tokens, such as LEND, will revert if this is attempted, which may cause transactions that involve other tokens (such as batch operations) to fully revert. Consider skipping the transfer if the amount is zero, which will also save gas.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: VToken.sol

99:     function transfer(address dst, uint256 amount) external override nonReentrant returns (bool) {

```

```solidity
File: VTokenInterfaces.sol

310:     function transfer(address dst, uint256 amount) external virtual returns (bool);

```

</details> 
 


 ### <a name="L-8"></a>[L-8]
 ###  Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard  
Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks opens the users of this protocol up to [read-only reentrancy](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) vulnerability with no way to protect them except by block-listing the entire protocol.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: VToken.sol

99:     function transfer(address dst, uint256 amount) external override nonReentrant returns (bool) {

```

```solidity
File: VTokenInterfaces.sol

310:     function transfer(address dst, uint256 amount) external virtual returns (bool);

```

</details> 
 


 ### <a name="L-9"></a>[L-9]
 ### Some tokens may revert when large transfers are made
Tokens such as COMP or UNI will revert when an address balance reaches type(uint96).max. Ensure that the calls below can be broken up into smaller batches if necessary.  

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: VToken.sol

99:     function transfer(address dst, uint256 amount) external override nonReentrant returns (bool) {

```

```solidity
File: VTokenInterfaces.sol

310:     function transfer(address dst, uint256 amount) external virtual returns (bool);

```

</details> 
 


## Non Critical Issues


 ### <a name="NC-1"></a>[NC-1]
 ### assert() should be replaced with require() or revert()
In versions of Solidity prior to 0.8.0, when encountering an assert all the remaining gas will be consumed. Even after Solidity 0.8.0, the assert function is still not recommended, as described in the [documentation:](https://docs.soliditylang.org/en/v0.8.20/control-structures.html#panic-via-assert-and-error-via-require)

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

224:         assert(assetIndex < len);

```

</details> 
 


 ### <a name="NC-2"></a>[NC-2]
 ### Custom error has no error details

#### Impact:
Defining custom errors without error details can make error messages less informative.

*Instances (35)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

72:     error InvalidCollateralFactor();

75:     error InvalidLiquidationThreshold();

90:     error ComptrollerMismatch();

102:     error InsufficientLiquidity();

105:     error InsufficientShortfall();

108:     error TooMuchRepay();

111:     error NonzeroBorrowBalance();

```

```solidity
File: ErrorReporter.sol

8:     error TransferNotAllowed();

9:     error TransferNotEnough();

10:     error TransferTooMuch();

13:     error MintFreshnessCheck();

16:     error RedeemFreshnessCheck();

17:     error RedeemTransferOutNotPossible();

20:     error BorrowFreshnessCheck();

21:     error BorrowCashNotAvailable();

24:     error RepayBorrowFreshnessCheck();

26:     error HealBorrowUnauthorized();

27:     error ForceLiquidateBorrowUnauthorized();

30:     error LiquidateFreshnessCheck();

31:     error LiquidateCollateralFreshnessCheck();

34:     error LiquidateLiquidatorIsBorrower();

35:     error LiquidateCloseAmountIsZero();

36:     error LiquidateCloseAmountIsUintMax();

40:     error LiquidateSeizeLiquidatorIsBorrower();

42:     error SetComptrollerOwnerCheck();

44:     error ProtocolSeizeShareTooBig();

46:     error SetReserveFactorFreshCheck();

47:     error SetReserveFactorBoundsCheck();

51:     error ReduceReservesAdminCheck();

52:     error ReduceReservesFreshCheck();

53:     error ReduceReservesCashNotAvailable();

54:     error ReduceReservesCashValidation();

56:     error SetInterestRateModelFreshCheck();

58:     error ZeroAddressNotAllowed();

```

```solidity
File: Pool/PoolRegistry.sol

146:     error ZeroAddressNotAllowed();

```

</details> 
 


 ### <a name="NC-3"></a>[NC-3]
 ### Variables without visibility specifier

#### Impact:
Specifying visibility for variables can improve code readability and maintainability.

*Instances (160)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

182:             uint256 excessUtil;

```

```solidity
File: Comptroller.sol

161:         for (uint256 i; i < len; ++i) {

216:         for (uint256 i; i < len; ++i) {

273:         for (uint256 i; i < rewardDistributorsCount; ++i) {

303:         for (uint256 i; i < rewardDistributorsCount; ++i) {

375:         for (uint256 i; i < rewardDistributorsCount; ++i) {

401:         for (uint256 i; i < rewardDistributorsCount; ++i) {

520:         for (uint256 i; i < rewardDistributorsCount; ++i) {

557:         for (uint256 i; i < rewardDistributorsCount; ++i) {

583:         for (uint256 i; i < userAssetsCount; ++i) {

610:         for (uint256 i; i < userAssetsCount; ++i) {

668:         for (uint256 i; i < ordersCount; ++i) {

689:         for (uint256 i; i < marketsCount; ++i) {

818:         for (uint256 i; i < rewardDistributorsCount; ++i) {

845:         for (uint256 i; i < numMarkets; ++i) {

870:         for (uint256 i; i < vTokensCount; ++i) {

896:         for (uint256 marketIdx; marketIdx < marketsCount; ++marketIdx) {

897:             for (uint256 actionIdx; actionIdx < actionsCount; ++actionIdx) {

931:         for (uint256 i; i < rewardsDistributorsLength; ++i) {

947:         for (uint256 i; i < marketsCount; ++i) {

1099:         uint256 seizeTokens;

1121:         for (uint256 i; i < rewardsDistributorsLength; ++i) {

1207:         for (uint256 i; i < marketsCount; ++i) {

1306:         for (uint256 i; i < assetsCount; ++i) {

1410:         uint256 err;

```

```solidity
File: ComptrollerStorage.sol

10:         uint256 repayAmount;

14:         uint256 totalCollateral;

15:         uint256 weightedCollateral;

16:         uint256 borrows;

17:         uint256 effects;

18:         uint256 liquidity;

19:         uint256 shortfall;

23:         address rewardToken;

24:         uint256 supplySpeed;

25:         uint256 borrowSpeed;

30:         bool isListed;

34:         uint256 collateralFactorMantissa;

38:         uint256 liquidationThresholdMantissa;

```

```solidity
File: ExponentialNoError.sol

13:         uint256 mantissa;

17:         uint256 mantissa;

```

```solidity
File: Factories/VTokenProxyFactory.sol

12:         address underlying_;

15:         uint256 initialExchangeRateMantissa_;

16:         string name_;

17:         string symbol_;

18:         uint8 decimals_;

19:         address admin_;

22:         address beaconAddress;

23:         uint256 reserveFactor;

```

```solidity
File: Lens/PoolLens.sol

16:         string name;

17:         address creator;

18:         address comptroller;

19:         uint256 blockPosted;

20:         uint256 timestampPosted;

21:         string category;

22:         string logoURL;

23:         string description;

24:         address priceOracle;

25:         uint256 closeFactor;

26:         uint256 liquidationIncentive;

27:         uint256 minLiquidatableCollateral;

35:         address vToken;

36:         uint256 exchangeRateCurrent;

37:         uint256 supplyRatePerBlock;

38:         uint256 borrowRatePerBlock;

39:         uint256 reserveFactorMantissa;

40:         uint256 supplyCaps;

41:         uint256 borrowCaps;

42:         uint256 totalBorrows;

43:         uint256 totalReserves;

44:         uint256 totalSupply;

45:         uint256 totalCash;

46:         bool isListed;

47:         uint256 collateralFactorMantissa;

48:         address underlyingAssetAddress;

49:         uint256 vTokenDecimals;

50:         uint256 underlyingDecimals;

57:         address vToken;

58:         uint256 balanceOf;

59:         uint256 borrowBalanceCurrent;

60:         uint256 balanceOfUnderlying;

61:         uint256 tokenBalance;

62:         uint256 tokenAllowance;

69:         address vToken;

70:         uint256 underlyingPrice;

77:         address vTokenAddress;

78:         uint256 amount;

85:         address distributorAddress;

86:         address rewardTokenAddress;

87:         uint256 totalRewards;

98:         uint32 block;

105:         address vTokenAddress;

106:         uint256 badDebtUsd;

113:         address comptroller;

114:         uint256 totalBadDebtUsd;

126:         for (uint256 i; i < vTokenCount; ++i) {

144:         for (uint256 i; i < poolLength; ++i) {

207:         for (uint256 i; i < vTokenCount; ++i) {

228:         for (uint256 i; i < rewardsDistributors.length; ++i) {

248:         uint256 totalBadDebtUsd;

262:         for (uint256 i; i < markets.length; ++i) {

286:         uint256 tokenBalance;

287:         uint256 tokenAllowance;

356:         address underlyingAssetAddress;

357:         uint256 underlyingDecimals;

390:         for (uint256 i; i < vTokenCount; ++i) {

417:         for (uint256 i; i < markets.length; ++i) {

```

```solidity
File: Pool/PoolRegistry.sol

33:         address comptroller;

34:         address asset;

35:         uint8 decimals;

36:         string name;

37:         string symbol;

39:         uint256 baseRatePerYear;

40:         uint256 multiplierPerYear;

41:         uint256 jumpMultiplierPerYear;

42:         uint256 kink_;

43:         uint256 collateralFactor;

44:         uint256 liquidationThreshold;

45:         uint256 reserveFactor;

47:         address beaconAddress;

48:         uint256 initialSupply;

49:         address vTokenReceiver;

50:         uint256 supplyCap;

51:         uint256 borrowCap;

```

```solidity
File: Pool/PoolRegistryInterface.sol

9:         string name;

10:         address creator;

11:         address comptroller;

12:         uint256 blockPosted;

13:         uint256 timestampPosted;

20:         string category;

21:         string logoURL;

22:         string description;

```

```solidity
File: Rewards/RewardsDistributor.sol

19:         uint32 block;

209:         for (uint256 i; i < numTokens; ++i) {

282:         for (uint256 i; i < vTokensCount; ++i) {

```

```solidity
File: RiskFund/ReserveHelpers.sol

62:             uint256 balanceDifference;

```

```solidity
File: RiskFund/RiskFund.sol

161:         uint256 totalAmount;

166:         for (uint256 i; i < marketsCount; ++i) {

233:         uint256 totalAmount;

```

```solidity
File: Shortfall/Shortfall.sol

34:         uint256 startBlock;

38:         uint256 seizedRiskFund;

39:         address highestBidder;

40:         uint256 highestBidBps;

41:         uint256 highestBidBlock;

42:         uint256 startBidBps;

174:         for (uint256 i; i < marketsCount; ++i) {

222:         for (uint256 i; i < marketsCount; ++i) {

238:         uint256 riskFundBidAmount;

373:         for (uint256 i; i < marketsCount; ++i) {

383:         uint256 poolBadDebt;

388:         for (uint256 i; i < marketsCount; ++i) {

```

```solidity
File: VToken.sol

402:         uint256 actualRepayAmount;

815:         uint256 redeemTokens;

816:         uint256 redeemAmount;

1179:         uint256 totalReservesNew;

1180:         uint256 actualAddAmount;

1202:         uint256 totalReservesNew;

1312:         uint256 startingAllowance;

```

```solidity
File: VTokenInterfaces.sol

17:         uint256 principal;

18:         uint256 interestIndex;

134:         address shortfall;

```

</details> 
 


 ### <a name="NC-4"></a>[NC-4]
 ### Array is push()ed but not pop()ed

#### Impact:
Array entries are added but are never removed. Consider whether this should be the case, or whether there should be a maximum, or whether old entries should be removed.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

942:         rewardsDistributors.push(_rewardsDistributor);

1194:         accountAssets[borrower].push(vToken);

```

```solidity
File: Pool/PoolRegistry.sol

317:         _supportedPools[input.asset].push(input.comptroller);

```

</details> 
 


 ### <a name="NC-5"></a>[NC-5]
 ### Constants in comparisons should appear on the left side

#### Impact:
Placing constants on the left side of comparisons can improve code readability and prevent accidental assignment. Doing so will prevent typo [bugs](https://www.moserware.com/2008/01/constants-on-left-are-better-but-this.html)

*Instances (97)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

136:         if (borrows == 0) {

178:         if (util <= kink) {

```

```solidity
File: Comptroller.sol

193:         if (amountOwed != 0) {

217:             if (userAssetList[i] == vToken) {

261:         if (supplyCap != type(uint256).max) {

265:             if (nextTotalSupply > supplyCap) {

350:         if (borrowCap != type(uint256).max) {

353:             if (nextTotalBorrows > borrowCap) {

366:         if (snapshot.shortfall > 0) {

449:             if (repayAmount > borrowBalance) {

458:         if (snapshot.totalCollateral <= minLiquidatableCollateral) {

463:         if (snapshot.shortfall == 0) {

469:         if (repayAmount > maxClose) {

500:         if (seizerContract == address(this)) {

590:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

594:         if (snapshot.shortfall == 0) {

617:             if (tokens != 0) {

621:             if (borrowBalance != 0) {

645:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

654:         if (collateralToSeize >= snapshot.totalCollateral) {

660:         if (snapshot.shortfall == 0) {

739:         if (newCollateralFactorMantissa > collateralFactorMaxMantissa) {

744:         if (newLiquidationThresholdMantissa > mantissaOne) {

749:         if (newLiquidationThresholdMantissa < newCollateralFactorMantissa) {

754:         if (newCollateralFactorMantissa != 0 && oracle.getUnderlyingPrice(address(vToken)) == 0) {

759:         if (newCollateralFactorMantissa != oldCollateralFactorMantissa) {

765:         if (newLiquidationThresholdMantissa != oldLiquidationThresholdMantissa) {

1208:             if (allMarkets[i] == VToken(vToken)) {

1261:         if (snapshot.shortfall > 0) {

1336:             if (asset == vTokenModify) {

1350:             if (snapshot.weightedCollateral > borrowPlusEffects) {

1369:         if (oraclePriceMantissa == 0) {

1412:         if (err != 0) {

1421:         if (msg.sender != expectedSender) {

```

```solidity
File: Lens/PoolLens.sol

461:         if (deltaBlocks > 0 && borrowSpeed > 0) {

469:         } else if (deltaBlocks > 0) {

482:         if (deltaBlocks > 0 && supplySpeed > 0) {

489:         } else if (deltaBlocks > 0) {

505:         if (borrowerIndex.mantissa == 0 && borrowIndex.mantissa > 0) {

525:         if (supplierIndex.mantissa == 0 && supplyIndex.mantissa > 0) {

```

```solidity
File: MaxLoopsLimitHelper.sol

40:         if (len > maxLoopsLimit) {

```

```solidity
File: Pool/PoolRegistry.sol

268:         if (input.rateModel == InterestRateModels.JumpRate) {

430:         if (protocolShareReserve_ == address(0)) {

```

```solidity
File: Rewards/RewardsDistributor.sol

134:         if (supplyState.index == 0) {

139:         if (borrowState.index == 0) {

222:         if (rewardTokenSpeed == 0) {

261:         if (deltaBlocks > 0 && rewardTokenSpeed > 0) {

348:         if (supplierIndex == 0 && supplyIndex >= rewardTokenInitialIndex) {

386:         if (borrowerIndex == 0 && borrowIndex >= rewardTokenInitialIndex) {

399:         if (borrowerAmount != 0) {

418:         if (amount > 0 && amount <= rewardTokenRemaining) {

435:         if (deltaBlocks > 0 && supplySpeed > 0) {

446:         } else if (deltaBlocks > 0) {

463:         if (deltaBlocks > 0 && borrowSpeed > 0) {

474:         } else if (deltaBlocks > 0) {

```

```solidity
File: RiskFund/ReserveHelpers.sol

61:         if (currentBalance > assetReserve) {

```

```solidity
File: RiskFund/RiskFund.sol

244:         if (balanceOfUnderlyingAsset > 0) {

248:             if (amountInUsd >= minAmountToConvert) {

252:                 if (underlyingAsset != convertibleBaseAsset) {

```

```solidity
File: Shortfall/Shortfall.sol

178:             if (auction.auctionType == AuctionType.LARGE_POOL_DEBT) {

179:                 if (auction.highestBidder != address(0)) {

188:                 if (auction.highestBidder != address(0)) {

226:             if (auction.auctionType == AuctionType.LARGE_POOL_DEBT) {

240:         if (auction.auctionType == AuctionType.LARGE_POOL_DEBT) {

405:         if (incentivizedRiskFundBalance >= riskFundBalance) {

```

```solidity
File: VToken.sol

313:         if (newProtocolSeizeShareMantissa_ + 1e18 > liquidationIncentive) {

395:         if (msg.sender != address(comptroller)) {

403:         if (repayAmount != 0) {

413:         if (badDebtDelta != 0) {

456:         if (msg.sender != address(comptroller)) {

684:         if (accrualBlockNumberPrior == currentBlockNumber) {

752:         if (accrualBlockNumber != _getBlockNumber()) {

808:         if (accrualBlockNumber != _getBlockNumber()) {

818:         if (redeemTokensIn > 0) {

837:         if (redeemTokens == 0 && redeemAmount > 0) {

882:         if (accrualBlockNumber != _getBlockNumber()) {

939:         if (accrualBlockNumber != _getBlockNumber()) {

999:         if (error != NO_ERROR) {

1035:         if (accrualBlockNumber != _getBlockNumber()) {

1045:         if (borrower == liquidator) {

1050:         if (repayAmount == 0) {

1055:         if (repayAmount == type(uint256).max) {

1107:         if (borrower == liquidator) {

1156:         if (accrualBlockNumber != _getBlockNumber()) {

1161:         if (newReserveFactorMantissa > reserveFactorMaxMantissa) {

1183:         if (accrualBlockNumber != _getBlockNumber()) {

1205:         if (accrualBlockNumber != _getBlockNumber()) {

1215:         if (reduceAmount > totalReserves) {

1248:         if (accrualBlockNumber != _getBlockNumber()) {

1307:         if (src == dst) {

1313:         if (spender == src) {

1331:         if (startingAllowance != type(uint256).max) {

1399:         if (shortfall_ == address(0)) {

1408:         if (protocolShareReserve_ == address(0)) {

1446:         if (borrowSnapshot.principal == 0) {

1465:         if (_totalSupply == 0) {

```

```solidity
File: WhitePaperInterestRateModel.sol

92:         if (borrows == 0) {

```

</details> 
 


 ### <a name="NC-6"></a>[NC-6]
 ### Consider using delete rather than assigning zero to clear value

#### Impact:
Consider using delete rather than assigning zero to clear values. The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*Instances (10)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

811:         newMarket.collateralFactorMantissa = 0;

812:         newMarket.liquidationThresholdMantissa = 0;

1352:                 snapshot.shortfall = 0;

1354:                 snapshot.liquidity = 0;

```

```solidity
File: ComptrollerStorage.sol

102:     uint256 internal constant NO_ERROR = 0;

```

```solidity
File: ErrorReporter.sol

5:     uint256 public constant NO_ERROR = 0; // support legacy return codes

```

```solidity
File: Shortfall/Shortfall.sol

369:         auction.highestBidBps = 0;

370:         auction.highestBidBlock = 0;

409:             remainingRiskFundBalance = 0;

```

```solidity
File: VToken.sol

424:         accountBorrows[borrower].principal = 0;

```

</details> 
 


 ### <a name="NC-7"></a>[NC-7]
 ### Consider using delete rather than assigning false to clear value

#### Impact:
Consider using delete rather than assigning alse to clear values. The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: VToken.sol

35:         _notEntered = false;

```

</details> 
 


 ### <a name="NC-8"></a>[NC-8]
 ### Consider adding a block/deny-list"
Doing so will significantly increase centralization, but will help to prevent hackers from using stolen tokens  

*Instances (26)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

11: abstract contract BaseJumpRateModelV2 is InterestRateModel {

```

```solidity
File: Comptroller.sol

16: contract Comptroller is

```

```solidity
File: ComptrollerStorage.sol

6: contract ComptrollerStorage {

```

```solidity
File: ErrorReporter.sol

4: contract TokenErrorReporter {

```

```solidity
File: ExponentialNoError.sol

11: contract ExponentialNoError {

```

```solidity
File: Factories/JumpRateModelFactory.sol

6: contract JumpRateModelFactory {

```

```solidity
File: Factories/VTokenProxyFactory.sol

10: contract VTokenProxyFactory {

```

```solidity
File: Factories/WhitePaperInterestRateModelFactory.sol

6: contract WhitePaperInterestRateModelFactory {

```

```solidity
File: InterestRateModel.sol

8: abstract contract InterestRateModel {

```

```solidity
File: JumpRateModelV2.sol

11: contract JumpRateModelV2 is BaseJumpRateModelV2 {

```

```solidity
File: Lens/PoolLens.sol

11: contract PoolLens is ExponentialNoError {

```

```solidity
File: MaxLoopsLimitHelper.sol

4: abstract contract MaxLoopsLimitHelper {

```

```solidity
File: Pool/PoolRegistry.sol

24: contract PoolRegistry is Ownable2StepUpgradeable, AccessControlledV8, PoolRegistryInterface {

```

```solidity
File: Proxy/UpgradeableBeacon.sol

6: contract Beacon is UpgradeableBeacon {

```

```solidity
File: Rewards/RewardsDistributor.sol

12: contract RewardsDistributor is ExponentialNoError, Ownable2StepUpgradeable, AccessControlledV8, MaxLoopsLimitHelper {

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

12: contract ProtocolShareReserve is Ownable2StepUpgradeable, ExponentialNoError, ReserveHelpers, IProtocolShareReserve {

```

```solidity
File: RiskFund/ReserveHelpers.sol

9: contract ReserveHelpers {

```

```solidity
File: RiskFund/RiskFund.sol

19: contract RiskFund is

111:         require(shortfallContractAddress_ != address(0), "Risk Fund: Shortfall contract address invalid");

191:         require(msg.sender == shortfall, "Risk fund: Only callable by Shortfall contract");

```

```solidity
File: Shortfall/Shortfall.sol

16: contract Shortfall is Ownable2StepUpgradeable, AccessControlledV8, ReentrancyGuardUpgradeable, IShortfall {

```

```solidity
File: VToken.sol

19: contract VToken is

489:         require(msg.sender == shortfall, "only shortfall contract can update bad debt");

```

```solidity
File: VTokenInterfaces.sol

10: contract VTokenStorage {

132: abstract contract VTokenInterface is VTokenStorage {

```

```solidity
File: WhitePaperInterestRateModel.sol

11: contract WhitePaperInterestRateModel is InterestRateModel {

```

</details> 
 


 ### <a name="NC-9"></a>[NC-9]
 ### Events are missing sender information

#### Impact:
Including msg.sender in events triggered by user actions can make events more useful for end users.

*Instances (66)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

161:         emit NewInterestParams(baseRatePerBlock, multiplierPerBlock, jumpMultiplierPerBlock, kink);

```

```solidity
File: Comptroller.sol

231:         emit MarketExited(vToken, msg.sender);

708:         emit NewCloseFactor(oldCloseFactorMantissa, closeFactorMantissa);

761:             emit NewCollateralFactor(vToken, oldCollateralFactorMantissa, newCollateralFactorMantissa);

767:             emit NewLiquidationThreshold(vToken, oldLiquidationThresholdMantissa, newLiquidationThresholdMantissa);

790:         emit NewLiquidationIncentive(oldLiquidationIncentiveMantissa, newLiquidationIncentiveMantissa);

822:         emit MarketSupported(vToken);

847:             emit NewBorrowCap(vTokens[i], newBorrowCaps[i]);

872:             emit NewSupplyCap(vTokens[i], newSupplyCaps[i]);

916:         emit NewMinLiquidatableCollateral(oldMinLiquidatableCollateral, newMinLiquidatableCollateral);

965:         emit NewPriceOracle(oldOracle, newOracle);

1196:         emit MarketEntered(vToken, borrower);

```

```solidity
File: Factories/VTokenProxyFactory.sol

47:         emit VTokenProxyDeployed(input);

```

```solidity
File: MaxLoopsLimitHelper.sol

31:         emit MaxLoopsLimitUpdated(oldMaxLoopsLimit, maxLoopsLimit);

```

```solidity
File: Pool/PoolRegistry.sol

336:         emit PoolNameSet(comptroller, oldName, name);

346:         emit PoolMetadataUpdated(comptroller, oldMetadata, _metadata);

405:         emit PoolRegistered(comptroller, pool);

435:         emit NewProtocolShareReserve(oldProtocolShareReserve, protocolShareReserve_);

```

```solidity
File: Rewards/RewardsDistributor.sol

149:         emit MarketInitialized(vToken);

184:         emit RewardTokenGranted(recipient, amount);

230:         emit ContributorRewardTokenSpeedUpdated(contributor, rewardTokenSpeed);

268:             emit ContributorRewardsUpdated(contributor, rewardTokenAccrued[contributor]);

319:             emit RewardTokenSupplySpeedUpdated(vToken, supplySpeed);

331:             emit RewardTokenBorrowSpeedUpdated(vToken, borrowSpeed);

450:         emit RewardTokenSupplyIndexUpdated(vToken);

478:         emit RewardTokenBorrowIndexUpdated(vToken, marketBorrowIndex);

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

57:         emit PoolRegistryUpdated(oldPoolRegistry, _poolRegistry);

87:         emit FundsReleased(comptroller, asset, amount);

```

```solidity
File: RiskFund/ReserveHelpers.sol

68:             emit AssetsReservesUpdated(comptroller, asset, balanceDifference);

```

```solidity
File: RiskFund/RiskFund.sol

103:         emit PoolRegistryUpdated(oldPoolRegistry, _poolRegistry);

119:         emit ShortfallContractUpdated(oldShortfallContractAddress, shortfallContractAddress_);

130:         emit PancakeSwapRouterUpdated(oldPancakeSwapRouter, pancakeSwapRouter_);

142:         emit MinAmountToConvertUpdated(oldMinAmountToConvert, minAmountToConvert_);

179:         emit SwappedPoolsAssets(markets, amountsOutMin, totalAmount);

196:         emit TransferredReserveForAuction(comptroller, amount);

```

```solidity
File: Shortfall/Shortfall.sol

200:         emit BidPlaced(comptroller, auction.startBlock, bidBps, msg.sender);

249:         emit AuctionClosed(

282:         emit AuctionRestarted(comptroller, auction.startBlock);

297:         emit NextBidderBlockLimitUpdated(oldNextBidderBlockLimit, _nextBidderBlockLimit);

311:         emit IncentiveBpsUpdated(oldIncentiveBps, _incentiveBps);

324:         emit MinimumPoolBadDebtUpdated(oldMinimumPoolBadDebt, _minimumPoolBadDebt);

337:         emit WaitForFirstBidderUpdated(oldWaitForFirstBidder, _waitForFirstBidder);

351:         emit PoolRegistryUpdated(oldPoolRegistry, _poolRegistry);

424:         emit AuctionStarted(

```

```solidity
File: VToken.sol

138:         emit Approval(src, spender, amount);

319:         emit NewProtocolSeizeShare(oldProtocolSeizeShareMantissa, newProtocolSeizeShareMantissa_);

408:             emit RepayBorrow(payer, borrower, actualRepayAmount, 0, totalBorrowsNew);

421:             emit BadDebtIncreased(borrower, badDebtDelta, badDebtOld, badDebtNew);

428:         emit HealBorrow(payer, borrower, repayAmount);

496:         emit BadDebtRecovered(badDebtOld, badDebtNew);

633:         emit Approval(src, spender, newAllowance);

657:         emit Approval(src, spender, currentAllowance);

731:         emit AccrueInterest(cashPrior, interestAccumulated, borrowIndexNew, totalBorrowsNew);

789:         emit Mint(minter, actualMintAmount, mintTokens, balanceAfter);

870:         emit Redeem(redeemer, redeemAmount, redeemTokens, balanceAfter);

920:         emit Borrow(borrower, borrowAmount, accountBorrowsNew, totalBorrowsNew);

974:         emit RepayBorrow(payer, borrower, actualRepayAmount, accountBorrowsNew, totalBorrowsNew);

1133:         emit Transfer(borrower, liquidator, liquidatorSeizeTokens);

1147:         emit NewComptroller(oldComptroller, newComptroller);

1168:         emit NewReserveFactor(oldReserveFactorMantissa, newReserveFactorMantissa);

1190:         emit ReservesAdded(msg.sender, actualAddAmount, totalReservesNew);

1235:         emit ReservesReduced(protocolShareReserve, reduceAmount, totalReservesNew);

1262:         emit NewMarketInterestRateModel(oldInterestRateModel, newInterestRateModel);

1336:         emit Transfer(src, dst, tokens);

1404:         emit NewShortfallContract(oldShortfall, shortfall_);

```

```solidity
File: WhitePaperInterestRateModel.sol

40:         emit NewInterestParams(baseRatePerBlock, multiplierPerBlock);

```

</details> 
 


 ### <a name="NC-10"></a>[NC-10]
 ### If-statement can be converted to a ternary

#### Impact:
The code can be made more compact while also increasing readability by converting the following `if`-statements to ternaries (e.g. `foo += (x > y) ? a : b`)

*Instances (124)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

96:         if (!isAllowedToCall) {

136:         if (borrows == 0) {

178:         if (util <= kink) {

```

```solidity
File: Comptroller.sol

193:         if (amountOwed != 0) {

203:         if (!marketToExit.accountMembership[msg.sender]) {

217:             if (userAssetList[i] == vToken) {

255:         if (!markets[vToken].isListed) {

261:         if (supplyCap != type(uint256).max) {

265:             if (nextTotalSupply > supplyCap) {

332:         if (!markets[vToken].isListed) {

336:         if (!markets[vToken].accountMembership[borrower]) {

344:         if (oracle.getUnderlyingPrice(vToken) == 0) {

350:         if (borrowCap != type(uint256).max) {

366:         if (snapshot.shortfall > 0) {

394:         if (!markets[vToken].isListed) {

438:         if (!markets[vTokenBorrowed].isListed) {

441:         if (!markets[vTokenCollateral].isListed) {

448:         if (skipLiquidityCheck || isDeprecated(VToken(vTokenBorrowed))) {

458:         if (snapshot.totalCollateral <= minLiquidatableCollateral) {

463:         if (snapshot.shortfall == 0) {

469:         if (repayAmount > maxClose) {

496:         if (!markets[vTokenCollateral].isListed) {

500:         if (seizerContract == address(this)) {

506:         } else {

512:             if (VToken(vTokenCollateral).comptroller() != VToken(seizerContract).comptroller()) {

590:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

594:         if (snapshot.shortfall == 0) {

606:         if (lessThanExp(Exp({ mantissa: mantissaOne }), percentage)) {

617:             if (tokens != 0) {

621:             if (borrowBalance != 0) {

645:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

654:         if (collateralToSeize >= snapshot.totalCollateral) {

660:         if (snapshot.shortfall == 0) {

669:             if (!markets[address(orders[i].vTokenBorrowed)].isListed) {

672:             if (!markets[address(orders[i].vTokenCollateral)].isListed) {

734:         if (!market.isListed) {

739:         if (newCollateralFactorMantissa > collateralFactorMaxMantissa) {

744:         if (newLiquidationThresholdMantissa > mantissaOne) {

749:         if (newLiquidationThresholdMantissa < newCollateralFactorMantissa) {

754:         if (newCollateralFactorMantissa != 0 && oracle.getUnderlyingPrice(address(vToken)) == 0) {

759:         if (newCollateralFactorMantissa != oldCollateralFactorMantissa) {

765:         if (newLiquidationThresholdMantissa != oldLiquidationThresholdMantissa) {

803:         if (markets[address(vToken)].isListed) {

1179:         if (!marketToJoin.isListed) {

1183:         if (marketToJoin.accountMembership[borrower]) {

1208:             if (allMarkets[i] == VToken(vToken)) {

1244:         if (!markets[vToken].isListed) {

1249:         if (!markets[vToken].accountMembership[redeemer]) {

1261:         if (snapshot.shortfall > 0) {

1336:             if (asset == vTokenModify) {

1350:             if (snapshot.weightedCollateral > borrowPlusEffects) {

1369:         if (oraclePriceMantissa == 0) {

1412:         if (err != 0) {

1421:         if (msg.sender != expectedSender) {

1430:         if (actionPaused(market, action)) {

```

```solidity
File: Lens/PoolLens.sol

461:         if (deltaBlocks > 0 && borrowSpeed > 0) {

469:         } else if (deltaBlocks > 0) {

482:         if (deltaBlocks > 0 && supplySpeed > 0) {

489:         } else if (deltaBlocks > 0) {

505:         if (borrowerIndex.mantissa == 0 && borrowIndex.mantissa > 0) {

525:         if (supplierIndex.mantissa == 0 && supplyIndex.mantissa > 0) {

```

```solidity
File: MaxLoopsLimitHelper.sol

40:         if (len > maxLoopsLimit) {

```

```solidity
File: Pool/PoolRegistry.sol

268:         if (input.rateModel == InterestRateModels.JumpRate) {

421:         if (address(shortfall_) == address(0)) {

430:         if (protocolShareReserve_ == address(0)) {

```

```solidity
File: Rewards/RewardsDistributor.sol

134:         if (supplyState.index == 0) {

139:         if (borrowState.index == 0) {

222:         if (rewardTokenSpeed == 0) {

261:         if (deltaBlocks > 0 && rewardTokenSpeed > 0) {

311:         if (rewardTokenSupplySpeeds[address(vToken)] != supplySpeed) {

322:         if (rewardTokenBorrowSpeeds[address(vToken)] != borrowSpeed) {

348:         if (supplierIndex == 0 && supplyIndex >= rewardTokenInitialIndex) {

386:         if (borrowerIndex == 0 && borrowIndex >= rewardTokenInitialIndex) {

399:         if (borrowerAmount != 0) {

418:         if (amount > 0 && amount <= rewardTokenRemaining) {

435:         if (deltaBlocks > 0 && supplySpeed > 0) {

446:         } else if (deltaBlocks > 0) {

463:         if (deltaBlocks > 0 && borrowSpeed > 0) {

474:         } else if (deltaBlocks > 0) {

```

```solidity
File: RiskFund/ReserveHelpers.sol

61:         if (currentBalance > assetReserve) {

```

```solidity
File: RiskFund/RiskFund.sol

244:         if (balanceOfUnderlyingAsset > 0) {

248:             if (amountInUsd >= minAmountToConvert) {

```

```solidity
File: Shortfall/Shortfall.sol

178:             if (auction.auctionType == AuctionType.LARGE_POOL_DEBT) {

187:             } else {

226:             if (auction.auctionType == AuctionType.LARGE_POOL_DEBT) {

240:         if (auction.auctionType == AuctionType.LARGE_POOL_DEBT) {

405:         if (incentivizedRiskFundBalance >= riskFundBalance) {

```

```solidity
File: VToken.sol

313:         if (newProtocolSeizeShareMantissa_ + 1e18 > liquidationIncentive) {

395:         if (msg.sender != address(comptroller)) {

403:         if (repayAmount != 0) {

413:         if (badDebtDelta != 0) {

456:         if (msg.sender != address(comptroller)) {

684:         if (accrualBlockNumberPrior == currentBlockNumber) {

752:         if (accrualBlockNumber != _getBlockNumber()) {

808:         if (accrualBlockNumber != _getBlockNumber()) {

818:         if (redeemTokensIn > 0) {

837:         if (redeemTokens == 0 && redeemAmount > 0) {

845:         if (_getCashPrior() - totalReserves < redeemAmount) {

882:         if (accrualBlockNumber != _getBlockNumber()) {

887:         if (_getCashPrior() - totalReserves < borrowAmount) {

939:         if (accrualBlockNumber != _getBlockNumber()) {

999:         if (error != NO_ERROR) {

1035:         if (accrualBlockNumber != _getBlockNumber()) {

1040:         if (vTokenCollateral.accrualBlockNumber() != _getBlockNumber()) {

1045:         if (borrower == liquidator) {

1050:         if (repayAmount == 0) {

1055:         if (repayAmount == type(uint256).max) {

1078:         if (address(vTokenCollateral) == address(this)) {

1107:         if (borrower == liquidator) {

1156:         if (accrualBlockNumber != _getBlockNumber()) {

1161:         if (newReserveFactorMantissa > reserveFactorMaxMantissa) {

1183:         if (accrualBlockNumber != _getBlockNumber()) {

1205:         if (accrualBlockNumber != _getBlockNumber()) {

1210:         if (_getCashPrior() < reduceAmount) {

1215:         if (reduceAmount > totalReserves) {

1248:         if (accrualBlockNumber != _getBlockNumber()) {

1307:         if (src == dst) {

1313:         if (spender == src) {

1331:         if (startingAllowance != type(uint256).max) {

1399:         if (shortfall_ == address(0)) {

1408:         if (protocolShareReserve_ == address(0)) {

1446:         if (borrowSnapshot.principal == 0) {

1465:         if (_totalSupply == 0) {

```

```solidity
File: WhitePaperInterestRateModel.sol

92:         if (borrows == 0) {

```

</details> 
 


 ### <a name="NC-11"></a>[NC-11]
 ### Variable names for immutables should use CONSTANT_CASE

#### Impact:
Using CONSTANT_CASE for immutables improves code readability and maintainability.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

26:     address public immutable poolRegistry;

```

```solidity
File: WhitePaperInterestRateModel.sol

22:     uint256 public immutable multiplierPerBlock;

27:     uint256 public immutable baseRatePerBlock;

```

</details> 
 


 ### <a name="NC-12"></a>[NC-12]
 ### Contract should expose an interface

#### Impact:
The contracts should expose an interface so that other projects can more easily integrate with it, without having to develop their own non-standard variants.

*Instances (10)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ComptrollerStorage.sol

6: contract ComptrollerStorage {

```

```solidity
File: ErrorReporter.sol

4: contract TokenErrorReporter {

```

```solidity
File: ExponentialNoError.sol

11: contract ExponentialNoError {

```

```solidity
File: Factories/JumpRateModelFactory.sol

6: contract JumpRateModelFactory {

```

```solidity
File: Factories/VTokenProxyFactory.sol

10: contract VTokenProxyFactory {

```

```solidity
File: Factories/WhitePaperInterestRateModelFactory.sol

6: contract WhitePaperInterestRateModelFactory {

```

```solidity
File: InterestRateModel.sol

8: abstract contract InterestRateModel {

```

```solidity
File: MaxLoopsLimitHelper.sol

4: abstract contract MaxLoopsLimitHelper {

```

```solidity
File: RiskFund/ReserveHelpers.sol

9: contract ReserveHelpers {

```

```solidity
File: VTokenInterfaces.sol

10: contract VTokenStorage {

```

</details> 
 


 ### <a name="NC-13"></a>[NC-13]
 ### Large multiples of ten should use scientific notation
Use a scientific notation rather than decimal literals (e.g. 1e6 instead of 1000000), for better code readability.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

22:     uint256 public constant blocksPerYear = 10512000;

```

```solidity
File: WhitePaperInterestRateModel.sol

17:     uint256 public constant blocksPerYear = 2102400;

```

</details> 
 


 ### <a name="NC-14"></a>[NC-14]
 ### Consider using named mappings

#### Impact:
Using named mappings can improve code readability and maintainability.

*Instances (12)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ComptrollerStorage.sol

40:         mapping(address => bool) accountMembership;

94:     mapping(address => mapping(Action => bool)) internal _actionPaused;

100:     mapping(address => bool) internal rewardsDistributorExists;

```

```solidity
File: Pool/PoolRegistry.sol

87:     mapping(uint256 => address) private _poolsByID;

97:     mapping(address => VenusPool) private _poolByComptroller;

102:     mapping(address => mapping(address => address)) private _vTokens;

107:     mapping(address => address[]) private _supportedPools;

```

```solidity
File: RiskFund/ReserveHelpers.sol

13:     mapping(address => uint256) internal assetsReserves;

17:     mapping(address => mapping(address => uint256)) internal poolsAssetsReserves;

```

```solidity
File: VTokenInterfaces.sol

106:     mapping(address => uint256) internal accountTokens;

109:     mapping(address => mapping(address => uint256)) internal transferAllowances;

112:     mapping(address => BorrowSnapshot) internal accountBorrows;

```

</details> 
 


 ### <a name="NC-15"></a>[NC-15]
 ### Consider combining multiple address/ID mappings into a single mapping of an address/ID to a struct

#### Impact:
Combining multiple mappings into a single mapping with a struct can improve readability and maintainability of the code.

*Instances (27)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ComptrollerStorage.sol

40:         mapping(address => bool) accountMembership;

73:     mapping(address => VToken[]) public accountAssets;

79:     mapping(address => Market) public markets;

85:     mapping(address => uint256) public borrowCaps;

91:     mapping(address => uint256) public supplyCaps;

94:     mapping(address => mapping(Action => bool)) internal _actionPaused;

100:     mapping(address => bool) internal rewardsDistributorExists;

```

```solidity
File: Pool/PoolRegistry.sol

82:     mapping(address => VenusPoolMetaData) public metadata;

97:     mapping(address => VenusPool) private _poolByComptroller;

102:     mapping(address => mapping(address => address)) private _vTokens;

107:     mapping(address => address[]) private _supportedPools;

```

```solidity
File: Rewards/RewardsDistributor.sol

23:     mapping(address => RewardToken) public rewardTokenSupplyState;

26:     mapping(address => mapping(address => uint256)) public rewardTokenSupplierIndex;

32:     mapping(address => uint256) public rewardTokenAccrued;

35:     mapping(address => uint256) public rewardTokenBorrowSpeeds;

38:     mapping(address => uint256) public rewardTokenSupplySpeeds;

41:     mapping(address => RewardToken) public rewardTokenBorrowState;

44:     mapping(address => uint256) public rewardTokenContributorSpeeds;

47:     mapping(address => uint256) public lastContributorBlock;

50:     mapping(address => mapping(address => uint256)) public rewardTokenBorrowerIndex;

```

```solidity
File: RiskFund/ReserveHelpers.sol

13:     mapping(address => uint256) internal assetsReserves;

17:     mapping(address => mapping(address => uint256)) internal poolsAssetsReserves;

```

```solidity
File: RiskFund/RiskFund.sol

35:     mapping(address => uint256) public poolReserves;

```

```solidity
File: Shortfall/Shortfall.sol

71:     mapping(address => Auction) public auctions;

```

```solidity
File: VTokenInterfaces.sol

106:     mapping(address => uint256) internal accountTokens;

109:     mapping(address => mapping(address => uint256)) internal transferAllowances;

112:     mapping(address => BorrowSnapshot) internal accountBorrows;

```

</details> 
 


 ### <a name="NC-16"></a>[NC-16]
 ### Use of override is unnecessary

#### Impact:
Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the override keyword when the function solely overrides an interface function, and the function doesnt exist in multiple base contracts, is unnecessary.

*Instances (57)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

116:     ) public view virtual override returns (uint256) {

```

```solidity
File: Comptroller.sol

153:     function enterMarkets(address[] memory vTokens) external override returns (uint256[] memory) {

186:     function exitMarket(address vTokenAddress) external override returns (uint256) {

252:     ) external override {

295:     ) external override {

327:     ) external override {

389:     function preRepayHook(address vToken, address borrower) external override {

429:     ) external override {

490:     ) external override {

545:     ) external override {

1037:     function getAllMarkets() external view override returns (VToken[] memory) {

1087:     ) external view override returns (uint256 error, uint256 tokensToSeize) {

1135:     function isComptroller() external pure override returns (bool) {

```

```solidity
File: JumpRateModelV2.sol

36:     ) external view override returns (uint256) {

```

```solidity
File: Pool/PoolRegistry.sol

353:     function getAllPools() external view override returns (VenusPool[] memory) {

366:     function getPoolByComptroller(address comptroller) external view override returns (VenusPool memory) {

374:     function getVenusPoolMetadata(address comptroller) external view override returns (VenusPoolMetaData memory) {

378:     function getVTokenForAsset(address comptroller, address asset) external view override returns (address) {

382:     function getPoolsSupportedByAsset(address asset) external view override returns (address[] memory) {

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

99:         override(IProtocolShareReserve, ReserveHelpers)

```

```solidity
File: RiskFund/RiskFund.sol

155:     ) external override returns (uint256) {

190:     function transferReserveForAuction(address comptroller, uint256 amount) external override returns (uint256) {

214:     function updateAssetsState(address comptroller, address asset) public override(IRiskFund, ReserveHelpers) {

```

```solidity
File: VToken.sol

99:     function transfer(address dst, uint256 amount) external override nonReentrant returns (bool) {

118:     ) external override nonReentrant returns (bool) {

133:     function approve(address spender, uint256 amount) external override returns (bool) {

148:     function balanceOfUnderlying(address owner) external override returns (uint256) {

157:     function totalBorrowsCurrent() external override nonReentrant returns (uint256) {

167:     function borrowBalanceCurrent(address account) external override nonReentrant returns (uint256) {

180:     function mint(uint256 mintAmount) external override nonReentrant returns (uint256) {

195:     function mintBehalf(address minter, uint256 mintAmount) external override nonReentrant returns (uint256) {

213:     function redeem(uint256 redeemTokens) external override nonReentrant returns (uint256) {

226:     function redeemUnderlying(uint256 redeemAmount) external override nonReentrant returns (uint256) {

241:     function borrow(uint256 borrowAmount) external override nonReentrant returns (uint256) {

255:     function repayBorrow(uint256 repayAmount) external override nonReentrant returns (uint256) {

270:     function repayBorrowBehalf(address borrower, uint256 repayAmount) external override nonReentrant returns (uint256) {

296:     ) external override returns (uint256) {

330:     function setReserveFactor(uint256 newReserveFactorMantissa) external override nonReentrant {

345:     function reduceReserves(uint256 reduceAmount) external override nonReentrant {

356:     function addReserves(uint256 addAmount) external override nonReentrant {

369:     function setInterestRateModel(InterestRateModel newInterestRateModel) external override {

394:     ) external override nonReentrant {

455:     ) external override {

477:     ) external override nonReentrant {

524:     function sweepToken(IERC20Upgradeable token) external override {

539:     function allowance(address owner, address spender) external view override returns (uint256) {

548:     function balanceOf(address owner) external view override returns (uint256) {

564:         override

579:     function getCash() external view override returns (uint256) {

587:     function borrowRatePerBlock() external view override returns (uint256) {

595:     function supplyRatePerBlock() external view override returns (uint256) {

604:     function borrowBalanceStored(address account) external view override returns (uint256) {

613:     function exchangeRateStored() external view override returns (uint256) {

665:     function exchangeRateCurrent() public override nonReentrant returns (uint256) {

678:     function accrueInterest() public virtual override returns (uint256) {

```

```solidity
File: WhitePaperInterestRateModel.sol

54:     ) public view override returns (uint256) {

72:     ) public view override returns (uint256) {

```

</details> 
 


 ### <a name="NC-17"></a>[NC-17]
 ### Consider using descriptive constants when using 0 in the code

#### Impact:
Passing zero as a function argument/Event emission can sometimes result in a security issue (e.g. passing zero as the slippage parameter). Consider using a constant variable with a descriptive name, so its clear that the 0 is intentionally being used, and for the right reasons.

*Instances (26)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

691:             require(borrowBalance == 0, "Nonzero borrow balance after liquidation");

841:         require(numMarkets != 0 && numMarkets == numBorrowCaps, "invalid input");

865:         require(vTokensCount != 0, "invalid number of markets");

```

```solidity
File: Lens/PoolLens.sol

465:             Double memory ratio = borrowAmount > 0 ? fraction(tokensAccrued, borrowAmount) : Double({ mantissa: 0 });

485:             Double memory ratio = supplyTokens > 0 ? fraction(tokensAccrued, supplyTokens) : Double({ mantissa: 0 });

```

```solidity
File: Rewards/RewardsDistributor.sol

183:         require(amountLeft == 0, "insufficient rewardToken for grant");

440:                 : Double({ mantissa: 0 });

468:                 : Double({ mantissa: 0 });

```

```solidity
File: RiskFund/RiskFund.sol

82:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

83:         require(loopsLimit_ > 0, "Risk Fund: Loops limit can not be zero");

139:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

231:         require(amountOutMin != 0, "RiskFund: amountOutMin must be greater than 0 to swap vToken");

253:                     require(path[0] == underlyingAsset, "RiskFund: swap path must start with the underlying asset");

258:                     IERC20Upgradeable(underlyingAsset).safeApprove(pancakeSwapRouter, 0);

```

```solidity
File: Shortfall/Shortfall.sol

138:         require(minimumPoolBadDebt_ != 0, "invalid minimum pool bad debt");

162:         require(bidBps <= MAX_BPS, "basis points cannot be more than 10000");

294:         require(_nextBidderBlockLimit != 0, "_nextBidderBlockLimit must not be 0");

308:         require(_incentiveBps != 0, "incentiveBps must not be 0");

422:         auction.highestBidder = address(0);

467:         bool noBidder = auction.highestBidder == address(0);

```

```solidity
File: VToken.sol

216:         _redeemFresh(msg.sender, redeemTokens, 0);

229:         _redeemFresh(msg.sender, 0, redeemAmount);

408:             emit RepayBorrow(payer, borrower, actualRepayAmount, 0, totalBorrowsNew);

805:         require(redeemTokensIn == 0 || redeemAmountIn == 0, "one of redeemTokensIn or redeemAmountIn must be zero");

1365:         require(accrualBlockNumber == 0 && borrowIndex == 0, "market may only be initialized once");

1369:         require(initialExchangeRateMantissa > 0, "initial exchange rate must be greater than zero.");

```

</details> 
 


 ### <a name="NC-18"></a>[NC-18]
 ### Non-external/public variable names should begin with an underscore

#### Impact:
Using an underscore at the beginning of non-external/public variable names can improve code clarity and maintainability. According to the Solidity Style Guide, non-external/public variable names should begin with an [underscore](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables)

*Instances (72)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

17:     IAccessControlManagerV8 public accessControlManager;

27:     uint256 public multiplierPerBlock;

32:     uint256 public baseRatePerBlock;

37:     uint256 public jumpMultiplierPerBlock;

42:     uint256 public kink;

```

```solidity
File: ComptrollerStorage.sol

58:     PriceOracle public oracle;

63:     uint256 public closeFactorMantissa;

68:     uint256 public liquidationIncentiveMantissa;

73:     mapping(address => VToken[]) public accountAssets;

79:     mapping(address => Market) public markets;

82:     VToken[] public allMarkets;

85:     mapping(address => uint256) public borrowCaps;

88:     uint256 public minLiquidatableCollateral;

91:     mapping(address => uint256) public supplyCaps;

97:     RewardsDistributor[] internal rewardsDistributors;

100:     mapping(address => bool) internal rewardsDistributorExists;

```

```solidity
File: MaxLoopsLimitHelper.sol

6:     uint256 public maxLoopsLimit;

```

```solidity
File: Pool/PoolRegistry.sol

57:     VTokenProxyFactory public vTokenFactory;

62:     JumpRateModelFactory public jumpRateFactory;

67:     WhitePaperInterestRateModelFactory public whitePaperFactory;

72:     Shortfall public shortfall;

77:     address payable public protocolShareReserve;

82:     mapping(address => VenusPoolMetaData) public metadata;

```

```solidity
File: Rewards/RewardsDistributor.sol

23:     mapping(address => RewardToken) public rewardTokenSupplyState;

26:     mapping(address => mapping(address => uint256)) public rewardTokenSupplierIndex;

32:     mapping(address => uint256) public rewardTokenAccrued;

35:     mapping(address => uint256) public rewardTokenBorrowSpeeds;

38:     mapping(address => uint256) public rewardTokenSupplySpeeds;

41:     mapping(address => RewardToken) public rewardTokenBorrowState;

44:     mapping(address => uint256) public rewardTokenContributorSpeeds;

47:     mapping(address => uint256) public lastContributorBlock;

50:     mapping(address => mapping(address => uint256)) public rewardTokenBorrowerIndex;

52:     Comptroller private comptroller;

54:     IERC20Upgradeable public rewardToken;

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

15:     address private protocolIncome;

16:     address private riskFund;

```

```solidity
File: RiskFund/ReserveHelpers.sol

13:     mapping(address => uint256) internal assetsReserves;

17:     mapping(address => mapping(address => uint256)) internal poolsAssetsReserves;

20:     address internal poolRegistry;

```

```solidity
File: RiskFund/RiskFund.sol

29:     address private pancakeSwapRouter;

30:     uint256 private minAmountToConvert;

31:     address private convertibleBaseAsset;

32:     address private shortfall;

35:     mapping(address => uint256) public poolReserves;

```

```solidity
File: Shortfall/Shortfall.sol

47:     address public poolRegistry;

50:     IRiskFund private riskFund;

53:     uint256 public minimumPoolBadDebt;

56:     uint256 private incentiveBps;

62:     uint256 public nextBidderBlockLimit;

65:     uint256 public waitForFirstBidder;

68:     address public convertibleBaseAsset;

71:     mapping(address => Auction) public auctions;

```

```solidity
File: VTokenInterfaces.sol

29:     address public underlying;

34:     string public name;

39:     string public symbol;

44:     uint8 public decimals;

49:     address payable public protocolShareReserve;

60:     ComptrollerInterface public comptroller;

65:     InterestRateModel public interestRateModel;

68:     uint256 internal initialExchangeRateMantissa;

73:     uint256 public reserveFactorMantissa;

78:     uint256 public accrualBlockNumber;

83:     uint256 public borrowIndex;

88:     uint256 public totalBorrows;

93:     uint256 public totalReserves;

98:     uint256 public totalSupply;

103:     uint256 public badDebt;

106:     mapping(address => uint256) internal accountTokens;

109:     mapping(address => mapping(address => uint256)) internal transferAllowances;

112:     mapping(address => BorrowSnapshot) internal accountBorrows;

117:     uint256 public protocolSeizeShareMantissa;

122:     address public shortfall;

```

</details> 
 


 ### <a name="NC-19"></a>[NC-19]
 ### Use the latest solidity version for deployment  
Upgrading to a newer Solidity release can optimize gas usage, take advantage of new features and improve overall contract efficiency. Where possible, based on compatibility requirements, it is recommended to use newer/latest solidity version to take advantage of the latest optimizations and features.

*Instances (28)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Comptroller.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ComptrollerInterface.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ComptrollerStorage.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ErrorReporter.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ExponentialNoError.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Factories/JumpRateModelFactory.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Factories/VTokenProxyFactory.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Factories/WhitePaperInterestRateModelFactory.sol

2: pragma solidity 0.8.13;

```

```solidity
File: IPancakeswapV2Router.sol

2: pragma solidity 0.8.13;

```

```solidity
File: InterestRateModel.sol

2: pragma solidity 0.8.13;

```

```solidity
File: JumpRateModelV2.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Lens/PoolLens.sol

2: pragma solidity 0.8.13;

```

```solidity
File: MaxLoopsLimitHelper.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Pool/PoolRegistry.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Pool/PoolRegistryInterface.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Proxy/UpgradeableBeacon.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Rewards/RewardsDistributor.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/IProtocolShareReserve.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/IRiskFund.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/ReserveHelpers.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/RiskFund.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Shortfall/IShortfall.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Shortfall/Shortfall.sol

2: pragma solidity 0.8.13;

```

```solidity
File: VToken.sol

2: pragma solidity 0.8.13;

```

```solidity
File: VTokenInterfaces.sol

2: pragma solidity 0.8.13;

```

```solidity
File: WhitePaperInterestRateModel.sol

2: pragma solidity 0.8.13;

```

</details> 
 


 ### <a name="NC-20"></a>[NC-20]
 ### Event is missing `indexed` fields
Index event fields make the field more quickly accessible to off-chain tools that parse events. However, note that each index field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields). Each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three fields, all of the fields should be indexed.

*Instances (59)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

44:     event NewInterestParams(

```

```solidity
File: Comptroller.sol

29:     event MarketEntered(VToken vToken, address account);

32:     event MarketExited(VToken vToken, address account);

35:     event NewCloseFactor(uint256 oldCloseFactorMantissa, uint256 newCloseFactorMantissa);

38:     event NewCollateralFactor(VToken vToken, uint256 oldCollateralFactorMantissa, uint256 newCollateralFactorMantissa);

41:     event NewLiquidationThreshold(

48:     event NewLiquidationIncentive(uint256 oldLiquidationIncentiveMantissa, uint256 newLiquidationIncentiveMantissa);

51:     event NewPriceOracle(PriceOracle oldPriceOracle, PriceOracle newPriceOracle);

54:     event ActionPausedMarket(VToken vToken, Action action, bool pauseState);

57:     event NewBorrowCap(VToken indexed vToken, uint256 newBorrowCap);

60:     event NewMinLiquidatableCollateral(uint256 oldMinLiquidatableCollateral, uint256 newMinLiquidatableCollateral);

63:     event NewSupplyCap(VToken indexed vToken, uint256 newSupplyCap);

69:     event MarketSupported(VToken vToken);

```

```solidity
File: Factories/VTokenProxyFactory.sol

26:     event VTokenProxyDeployed(VTokenArgs args);

```

```solidity
File: MaxLoopsLimitHelper.sol

16:     event MaxLoopsLimitUpdated(uint256 oldMaxLoopsLimit, uint256 newmaxLoopsLimit);

```

```solidity
File: Pool/PoolRegistry.sol

112:     event PoolRegistered(address indexed comptroller, VenusPool pool);

117:     event PoolNameSet(address indexed comptroller, string oldName, string newName);

122:     event PoolMetadataUpdated(

131:     event MarketAdded(address indexed comptroller, address vTokenAddress);

```

```solidity
File: Rewards/RewardsDistributor.sol

57:     event DistributedSupplierRewardToken(

66:     event DistributedBorrowerRewardToken(

75:     event RewardTokenSupplySpeedUpdated(VToken indexed vToken, uint256 newSpeed);

78:     event RewardTokenBorrowSpeedUpdated(VToken indexed vToken, uint256 newSpeed);

81:     event RewardTokenGranted(address recipient, uint256 amount);

84:     event ContributorRewardTokenSpeedUpdated(address indexed contributor, uint256 newSpeed);

87:     event MarketInitialized(address vToken);

90:     event RewardTokenSupplyIndexUpdated(address vToken);

93:     event RewardTokenBorrowIndexUpdated(address vToken, Exp marketBorrowIndex);

96:     event ContributorRewardsUpdated(address contributor, uint256 rewardAccrued);

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

22:     event FundsReleased(address comptroller, address asset, uint256 amount);

```

```solidity
File: RiskFund/ReserveHelpers.sol

30:     event AssetsReservesUpdated(address indexed comptroller, address indexed asset, uint256 amount);

```

```solidity
File: RiskFund/RiskFund.sol

47:     event AmountOutMinUpdated(uint256 oldAmountOutMin, uint256 newAmountOutMin);

50:     event MinAmountToConvertUpdated(uint256 oldMinAmountToConvert, uint256 newMinAmountToConvert);

53:     event SwappedPoolsAssets(address[] markets, uint256[] amountsOutMin, uint256 totalAmount);

56:     event TransferredReserveForAuction(address comptroller, uint256 amount);

```

```solidity
File: Shortfall/Shortfall.sol

74:     event AuctionStarted(

85:     event BidPlaced(address indexed comptroller, uint256 auctionStartBlock, uint256 bidBps, address indexed bidder);

88:     event AuctionClosed(

99:     event AuctionRestarted(address indexed comptroller, uint256 auctionStartBlock);

105:     event MinimumPoolBadDebtUpdated(uint256 oldMinimumPoolBadDebt, uint256 newMinimumPoolBadDebt);

108:     event WaitForFirstBidderUpdated(uint256 oldWaitForFirstBidder, uint256 newWaitForFirstBidder);

111:     event NextBidderBlockLimitUpdated(uint256 oldNextBidderBlockLimit, uint256 newNextBidderBlockLimit);

114:     event IncentiveBpsUpdated(uint256 oldIncentiveBps, uint256 newIncentiveBps);

```

```solidity
File: VTokenInterfaces.sol

148:     event AccrueInterest(uint256 cashPrior, uint256 interestAccumulated, uint256 borrowIndex, uint256 totalBorrows);

153:     event Mint(address indexed minter, uint256 mintAmount, uint256 mintTokens, uint256 accountBalance);

158:     event Redeem(address indexed redeemer, uint256 redeemAmount, uint256 redeemTokens, uint256 accountBalance);

163:     event Borrow(address indexed borrower, uint256 borrowAmount, uint256 accountBorrows, uint256 totalBorrows);

168:     event RepayBorrow(

183:     event BadDebtIncreased(address indexed borrower, uint256 badDebtDelta, uint256 badDebtOld, uint256 badDebtNew);

190:     event BadDebtRecovered(uint256 badDebtOld, uint256 badDebtNew);

231:     event NewProtocolSeizeShare(uint256 oldProtocolSeizeShareMantissa, uint256 newProtocolSeizeShareMantissa);

236:     event NewReserveFactor(uint256 oldReserveFactorMantissa, uint256 newReserveFactorMantissa);

241:     event ReservesAdded(address indexed benefactor, uint256 addAmount, uint256 newTotalReserves);

246:     event ReservesReduced(address indexed admin, uint256 reduceAmount, uint256 newTotalReserves);

251:     event Transfer(address indexed from, address indexed to, uint256 amount);

256:     event Approval(address indexed owner, address indexed spender, uint256 amount);

261:     event HealBorrow(address payer, address borrower, uint256 repayAmount);

266:     event SweepToken(address token);

```

```solidity
File: WhitePaperInterestRateModel.sol

29:     event NewInterestParams(uint256 baseRatePerBlock, uint256 multiplierPerBlock);

```

</details> 
 


 ### <a name="NC-21"></a>[NC-21]
 ### Strings should use double quotes rather than single quotes

#### Impact:
Using consistent double quotes for strings improves code readability and maintainability. Also see it here https://docs.soliditylang.org/en/v0.8.20/style-guide.html#other-recommendations

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Shortfall/Shortfall.sol

360:         require(pool.comptroller == comptroller, "comptroller doesn't exist pool registry");

```

</details> 
 


 ### <a name="NC-22"></a>[NC-22]
 ### Functions not used internally could be marked external

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

1143:     function getRewardDistributors() public view returns (RewardsDistributor[] memory) {

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

97:     function updateAssetsState(address comptroller, address asset)

```

```solidity
File: RiskFund/RiskFund.sol

214:     function updateAssetsState(address comptroller, address asset) public override(IRiskFund, ReserveHelpers) {

```

```solidity
File: VToken.sol

625:     function increaseAllowance(address spender, uint256 addedValue) public returns (bool) {

```

```solidity
File: WhitePaperInterestRateModel.sol

67:     function getSupplyRate(

```

</details> 
 


 ### <a name="NC-23"></a>[NC-23]
 ### Consider moving msg.sender checks to modifiers
If some functions are only allowed to be called by some specific users, consider using a modifier instead of checking with a require statement, especially if this check is done in multiple functions.  

*Instances (49)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

94:         bool isAllowedToCall = accessControlManager.isAllowedToCall(msg.sender, signature);

97:             revert Unauthorized(msg.sender, address(this), signature);

```

```solidity
File: Comptroller.sol

156:         uint256 accountAssetsLen = accountAssets[msg.sender].length;

164:             _addToMarket(vToken, msg.sender);

190:         (uint256 tokensHeld, uint256 amountOwed, ) = _safeGetAccountSnapshot(vToken, msg.sender);

198:         _checkRedeemAllowed(vTokenAddress, msg.sender, tokensHeld);

203:         if (!marketToExit.accountMembership[msg.sender]) {

208:         delete marketToExit.accountMembership[msg.sender];

212:         VToken[] memory userAssetList = accountAssets[msg.sender];

227:         VToken[] storage storedList = accountAssets[msg.sender];

231:         emit MarketExited(vToken, msg.sender);

341:             _addToMarket(VToken(msg.sender), borrower);

581:         address liquidator = msg.sender;

678:                 msg.sender,

1421:         if (msg.sender != expectedSender) {

1422:             revert UnexpectedSender(expectedSender, msg.sender);

```

```solidity
File: Pool/PoolRegistry.sol

244:         comptrollerProxy.transferOwnership(msg.sender);

293:             msg.sender,

320:         uint256 amountToSupply = _transferIn(token, msg.sender, input.initialSupply);

400:         VenusPool memory pool = VenusPool(name, msg.sender, comptroller, block.number, block.timestamp);

```

```solidity
File: Rewards/RewardsDistributor.sol

99:         require(address(comptroller) == msg.sender, "Only comptroller can call this function");

```

```solidity
File: RiskFund/RiskFund.sol

191:         require(msg.sender == shortfall, "Risk fund: Only callable by Shortfall contract");

```

```solidity
File: Shortfall/Shortfall.sol

186:                 erc20.safeTransferFrom(msg.sender, address(this), currentBidAmount);

192:                 erc20.safeTransferFrom(msg.sender, address(this), auction.marketDebt[auction.markets[i]]);

196:         auction.highestBidder = msg.sender;

200:         emit BidPlaced(comptroller, auction.startBlock, bidBps, msg.sender);

```

```solidity
File: VToken.sol

100:         _transferTokens(msg.sender, msg.sender, dst, amount);

100:         _transferTokens(msg.sender, msg.sender, dst, amount);

119:         _transferTokens(msg.sender, src, dst, amount);

136:         address src = msg.sender;

183:         _mintFresh(msg.sender, msg.sender, mintAmount);

183:         _mintFresh(msg.sender, msg.sender, mintAmount);

200:         _mintFresh(msg.sender, minter, mintAmount);

216:         _redeemFresh(msg.sender, redeemTokens, 0);

229:         _redeemFresh(msg.sender, 0, redeemAmount);

244:         _borrowFresh(msg.sender, borrowAmount);

258:         _repayBorrowFresh(msg.sender, msg.sender, repayAmount);

258:         _repayBorrowFresh(msg.sender, msg.sender, repayAmount);

273:         _repayBorrowFresh(msg.sender, borrower, repayAmount);

297:         _liquidateBorrow(msg.sender, borrower, repayAmount, vTokenCollateral, false);

395:         if (msg.sender != address(comptroller)) {

456:         if (msg.sender != address(comptroller)) {

478:         _seize(msg.sender, liquidator, borrower, seizeTokens);

489:         require(msg.sender == shortfall, "only shortfall contract can update bad debt");

525:         require(msg.sender == owner(), "VToken::sweepToken: only admin can sweep tokens");

628:         address src = msg.sender;

648:         address src = msg.sender;

1187:         actualAddAmount = _doTransferIn(msg.sender, addAmount);

1190:         emit ReservesAdded(msg.sender, actualAddAmount, totalReservesNew);

```

</details> 
 


 ### <a name="NC-24"></a>[NC-24]
 ### Array indices should be referenced via enums rather than numeric literals

#### Impact:
Referencing array indices via enums can improve code readability and maintainability.

*Instances (8)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ComptrollerStorage.sol

121:     uint256[50] private __gap;

```

```solidity
File: MaxLoopsLimitHelper.sol

13:     uint256[49] private __gap;

```

```solidity
File: Pool/PoolRegistry.sol

309:         newSupplyCaps[0] = input.supplyCap;

310:         newBorrowCaps[0] = input.borrowCap;

311:         vTokens[0] = vToken;

```

```solidity
File: RiskFund/ReserveHelpers.sol

26:     uint256[48] private __gap;

```

```solidity
File: RiskFund/RiskFund.sol

253:                     require(path[0] == underlyingAsset, "RiskFund: swap path must start with the underlying asset");

```

```solidity
File: VTokenInterfaces.sol

129:     uint256[50] private __gap;

```

</details> 
 


 ### <a name="NC-25"></a>[NC-25]
 ### Use assembly to emit events, in order to save gas
Using the [scratch space](https://github.com/Vectorized/solady/blob/30558f5402f02351b96eeb6eaf32bcea29773841/src/tokens/ERC1155.sol#L501-L504) for event arguments (two words or fewer) will save gas over needing Soliditys full abi memory expansion used for emitting normally.

*Instances (80)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

161:         emit NewInterestParams(baseRatePerBlock, multiplierPerBlock, jumpMultiplierPerBlock, kink);

```

```solidity
File: Comptroller.sol

231:         emit MarketExited(vToken, msg.sender);

708:         emit NewCloseFactor(oldCloseFactorMantissa, closeFactorMantissa);

761:             emit NewCollateralFactor(vToken, oldCollateralFactorMantissa, newCollateralFactorMantissa);

767:             emit NewLiquidationThreshold(vToken, oldLiquidationThresholdMantissa, newLiquidationThresholdMantissa);

790:         emit NewLiquidationIncentive(oldLiquidationIncentiveMantissa, newLiquidationIncentiveMantissa);

822:         emit MarketSupported(vToken);

847:             emit NewBorrowCap(vTokens[i], newBorrowCaps[i]);

872:             emit NewSupplyCap(vTokens[i], newSupplyCaps[i]);

916:         emit NewMinLiquidatableCollateral(oldMinLiquidatableCollateral, newMinLiquidatableCollateral);

951:         emit NewRewardsDistributor(address(_rewardsDistributor));

965:         emit NewPriceOracle(oldOracle, newOracle);

1196:         emit MarketEntered(vToken, borrower);

1230:         emit ActionPausedMarket(VToken(market), action, paused);

```

```solidity
File: Factories/VTokenProxyFactory.sol

47:         emit VTokenProxyDeployed(input);

```

```solidity
File: MaxLoopsLimitHelper.sol

31:         emit MaxLoopsLimitUpdated(oldMaxLoopsLimit, maxLoopsLimit);

```

```solidity
File: Pool/PoolRegistry.sol

325:         emit MarketAdded(address(comptroller), address(vToken));

336:         emit PoolNameSet(comptroller, oldName, name);

346:         emit PoolMetadataUpdated(comptroller, oldMetadata, _metadata);

405:         emit PoolRegistered(comptroller, pool);

426:         emit NewShortfallContract(oldShortfall, address(shortfall_));

435:         emit NewProtocolShareReserve(oldProtocolShareReserve, protocolShareReserve_);

```

```solidity
File: Rewards/RewardsDistributor.sol

149:         emit MarketInitialized(vToken);

184:         emit RewardTokenGranted(recipient, amount);

230:         emit ContributorRewardTokenSpeedUpdated(contributor, rewardTokenSpeed);

268:             emit ContributorRewardsUpdated(contributor, rewardTokenAccrued[contributor]);

319:             emit RewardTokenSupplySpeedUpdated(vToken, supplySpeed);

331:             emit RewardTokenBorrowSpeedUpdated(vToken, borrowSpeed);

366:         emit DistributedSupplierRewardToken(VToken(vToken), supplier, supplierDelta, supplierAccrued, supplyIndex);

405:             emit DistributedBorrowerRewardToken(VToken(vToken), borrower, borrowerDelta, borrowerAccrued, borrowIndex);

450:         emit RewardTokenSupplyIndexUpdated(vToken);

478:         emit RewardTokenBorrowIndexUpdated(vToken, marketBorrowIndex);

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

57:         emit PoolRegistryUpdated(oldPoolRegistry, _poolRegistry);

87:         emit FundsReleased(comptroller, asset, amount);

```

```solidity
File: RiskFund/ReserveHelpers.sol

68:             emit AssetsReservesUpdated(comptroller, asset, balanceDifference);

```

```solidity
File: RiskFund/RiskFund.sol

103:         emit PoolRegistryUpdated(oldPoolRegistry, _poolRegistry);

119:         emit ShortfallContractUpdated(oldShortfallContractAddress, shortfallContractAddress_);

130:         emit PancakeSwapRouterUpdated(oldPancakeSwapRouter, pancakeSwapRouter_);

142:         emit MinAmountToConvertUpdated(oldMinAmountToConvert, minAmountToConvert_);

179:         emit SwappedPoolsAssets(markets, amountsOutMin, totalAmount);

196:         emit TransferredReserveForAuction(comptroller, amount);

```

```solidity
File: Shortfall/Shortfall.sol

200:         emit BidPlaced(comptroller, auction.startBlock, bidBps, msg.sender);

249:         emit AuctionClosed(

282:         emit AuctionRestarted(comptroller, auction.startBlock);

297:         emit NextBidderBlockLimitUpdated(oldNextBidderBlockLimit, _nextBidderBlockLimit);

311:         emit IncentiveBpsUpdated(oldIncentiveBps, _incentiveBps);

324:         emit MinimumPoolBadDebtUpdated(oldMinimumPoolBadDebt, _minimumPoolBadDebt);

337:         emit WaitForFirstBidderUpdated(oldWaitForFirstBidder, _waitForFirstBidder);

351:         emit PoolRegistryUpdated(oldPoolRegistry, _poolRegistry);

424:         emit AuctionStarted(

```

```solidity
File: VToken.sol

138:         emit Approval(src, spender, amount);

319:         emit NewProtocolSeizeShare(oldProtocolSeizeShareMantissa, newProtocolSeizeShareMantissa_);

408:             emit RepayBorrow(payer, borrower, actualRepayAmount, 0, totalBorrowsNew);

420:             emit RepayBorrow(address(this), borrower, badDebtDelta, accountBorrowsPrev - badDebtDelta, totalBorrowsNew);

421:             emit BadDebtIncreased(borrower, badDebtDelta, badDebtOld, badDebtNew);

428:         emit HealBorrow(payer, borrower, repayAmount);

496:         emit BadDebtRecovered(badDebtOld, badDebtNew);

530:         emit SweepToken(address(token));

633:         emit Approval(src, spender, newAllowance);

657:         emit Approval(src, spender, currentAllowance);

731:         emit AccrueInterest(cashPrior, interestAccumulated, borrowIndexNew, totalBorrowsNew);

789:         emit Mint(minter, actualMintAmount, mintTokens, balanceAfter);

790:         emit Transfer(address(0), minter, mintTokens);

869:         emit Transfer(redeemer, address(this), redeemTokens);

870:         emit Redeem(redeemer, redeemAmount, redeemTokens, balanceAfter);

920:         emit Borrow(borrower, borrowAmount, accountBorrowsNew, totalBorrowsNew);

974:         emit RepayBorrow(payer, borrower, actualRepayAmount, accountBorrowsNew, totalBorrowsNew);

1085:         emit LiquidateBorrow(liquidator, borrower, actualRepayAmount, address(vTokenCollateral), seizeTokens);

1133:         emit Transfer(borrower, liquidator, liquidatorSeizeTokens);

1134:         emit Transfer(borrower, address(this), protocolSeizeTokens);

1135:         emit ReservesAdded(address(this), protocolSeizeAmount, totalReservesNew);

1147:         emit NewComptroller(oldComptroller, newComptroller);

1168:         emit NewReserveFactor(oldReserveFactorMantissa, newReserveFactorMantissa);

1190:         emit ReservesAdded(msg.sender, actualAddAmount, totalReservesNew);

1235:         emit ReservesReduced(protocolShareReserve, reduceAmount, totalReservesNew);

1262:         emit NewMarketInterestRateModel(oldInterestRateModel, newInterestRateModel);

1336:         emit Transfer(src, dst, tokens);

1404:         emit NewShortfallContract(oldShortfall, shortfall_);

1413:         emit NewProtocolShareReserve(oldProtocolShareReserve, address(protocolShareReserve_));

```

```solidity
File: WhitePaperInterestRateModel.sol

40:         emit NewInterestParams(baseRatePerBlock, multiplierPerBlock);

```

</details> 
 


 ### <a name="NC-26"></a>[NC-26]
 ### Don't initialize variables with default value

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ComptrollerStorage.sol

102:     uint256 internal constant NO_ERROR = 0;

```

```solidity
File: ErrorReporter.sol

5:     uint256 public constant NO_ERROR = 0; // support legacy return codes

```

</details> 
 


 ### <a name="NC-27"></a>[NC-27]
 ### Long revert strings

*Instances (54)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

691:             require(borrowBalance == 0, "Nonzero borrow balance after liquidation");

703:         require(closeFactorMaxMantissa >= newCloseFactorMantissa, "Close factor greater than maximum close factor");

704:         require(closeFactorMinMantissa <= newCloseFactorMantissa, "Close factor smaller than minimum close factor");

779:         require(newLiquidationIncentiveMantissa >= 1e18, "liquidation incentive should be greater than 1e18");

1228:         require(markets[market].isListed, "cannot pause a market that is not listed");

```

```solidity
File: MaxLoopsLimitHelper.sol

26:         require(limit > maxLoopsLimit, "Comptroller: Invalid maxLoopsLimit");

```

```solidity
File: Pool/PoolRegistry.sol

224:         require(beaconAddress != address(0), "PoolRegistry: Invalid Comptroller beacon address.");

225:         require(priceOracle != address(0), "PoolRegistry: Invalid PriceOracle address.");

256:         require(input.comptroller != address(0), "PoolRegistry: Invalid comptroller address");

257:         require(input.asset != address(0), "PoolRegistry: Invalid asset address");

258:         require(input.beaconAddress != address(0), "PoolRegistry: Invalid beacon address");

259:         require(input.vTokenReceiver != address(0), "PoolRegistry: Invalid vTokenReceiver address");

395:         require(venusPool.creator == address(0), "PoolRegistry: Pool already exists in the directory.");

```

```solidity
File: Rewards/RewardsDistributor.sol

99:         require(address(comptroller) == msg.sender, "Only comptroller can call this function");

183:         require(amountLeft == 0, "insufficient rewardToken for grant");

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

40:         require(_protocolIncome != address(0), "ProtocolShareReserve: Protocol Income address invalid");

41:         require(_riskFund != address(0), "ProtocolShareReserve: Risk Fund address invalid");

54:         require(_poolRegistry != address(0), "ProtocolShareReserve: Pool registry address invalid");

71:         require(asset != address(0), "ProtocolShareReserve: Asset address invalid");

72:         require(amount <= poolsAssetsReserves[comptroller][asset], "ProtocolShareReserve: Insufficient pool balance");

```

```solidity
File: RiskFund/ReserveHelpers.sol

39:         require(ComptrollerInterface(comptroller).isComptroller(), "ReserveHelpers: Comptroller address invalid");

40:         require(asset != address(0), "ReserveHelpers: Asset address invalid");

51:         require(ComptrollerInterface(comptroller).isComptroller(), "ReserveHelpers: Comptroller address invalid");

52:         require(asset != address(0), "ReserveHelpers: Asset address invalid");

53:         require(poolRegistry != address(0), "ReserveHelpers: Pool Registry address is not set");

```

```solidity
File: RiskFund/RiskFund.sol

80:         require(pancakeSwapRouter_ != address(0), "Risk Fund: Pancake swap address invalid");

81:         require(convertibleBaseAsset_ != address(0), "Risk Fund: Base asset address invalid");

82:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

83:         require(loopsLimit_ > 0, "Risk Fund: Loops limit can not be zero");

100:         require(_poolRegistry != address(0), "Risk Fund: Pool registry address invalid");

111:         require(shortfallContractAddress_ != address(0), "Risk Fund: Shortfall contract address invalid");

127:         require(pancakeSwapRouter_ != address(0), "Risk Fund: PancakeSwap address invalid");

139:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

157:         require(poolRegistry != address(0), "Risk fund: Invalid pool registry.");

158:         require(markets.length == amountsOutMin.length, "Risk fund: markets and amountsOutMin are unequal lengths");

159:         require(markets.length == paths.length, "Risk fund: markets and paths are unequal lengths");

171:             require(pool.comptroller == comptroller, "comptroller doesn't exist pool registry");

191:         require(msg.sender == shortfall, "Risk fund: Only callable by Shortfall contract");

192:         require(amount <= poolReserves[comptroller], "Risk Fund: Insufficient pool reserve.");

231:         require(amountOutMin != 0, "RiskFund: amountOutMin must be greater than 0 to swap vToken");

232:         require(amountOutMin >= minAmountToConvert, "RiskFund: amountOutMin should be greater than minAmountToConvert");

253:                     require(path[0] == underlyingAsset, "RiskFund: swap path must start with the underlying asset");

```

```solidity
File: Shortfall/Shortfall.sol

162:         require(bidBps <= MAX_BPS, "basis points cannot be more than 10000");

278:         require(_isStale(auction), "you need to wait for more time for first bidder");

294:         require(_nextBidderBlockLimit != 0, "_nextBidderBlockLimit must not be 0");

360:         require(pool.comptroller == comptroller, "comptroller doesn't exist pool registry");

```

```solidity
File: VToken.sol

489:         require(msg.sender == shortfall, "only shortfall contract can update bad debt");

490:         require(recoveredAmount_ <= badDebt, "more than bad debt recovered from auction");

525:         require(msg.sender == owner(), "VToken::sweepToken: only admin can sweep tokens");

526:         require(address(token) != underlying, "VToken::sweepToken: can not sweep underlying token");

805:         require(redeemTokensIn == 0 || redeemAmountIn == 0, "one of redeemTokensIn or redeemAmountIn must be zero");

1072:         require(amountSeizeError == NO_ERROR, "LIQUIDATE_COMPTROLLER_CALCULATE_AMOUNT_SEIZE_FAILED");

1365:         require(accrualBlockNumber == 0 && borrowIndex == 0, "market may only be initialized once");

1369:         require(initialExchangeRateMantissa > 0, "initial exchange rate must be greater than zero.");

```

</details> 
 


## Gas Optimizations


 ### <a name="GAS-1"></a>[GAS-1]
 ### Use scientific notation (e.g. 1e18) rather than exponentiation (e.g. 10**18)
While the compiler knows to optimize away the exponentiation, its still better coding practice to use idioms that do not require compiler optimization, if they exist.

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ExponentialNoError.sol

64:         require(n < 2**224, errorMessage);

69:         require(n < 2**32, errorMessage);

```

```solidity
File: Pool/PoolRegistry.sol

289:             10**(underlyingDecimals + 18 - input.decimals),

```

</details> 
 


 ### <a name="GAS-2"></a>[GAS-2]
 ### Nesting if-statements is cheaper than using &&
Nesting if-statements avoids the stack operations of setting up and using an extra jumpdest, and saves 6 [gas](https://gist.github.com/IllIllI000/7f3b818abecfadbef93b894481ae7d19)

*Instances (27)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

754:         if (newCollateralFactorMantissa != 0 && oracle.getUnderlyingPrice(address(vToken)) == 0) {

841:         require(numMarkets != 0 && numMarkets == numBorrowCaps, "invalid input");

1165:             markets[address(vToken)].collateralFactorMantissa == 0 &&

1166:             actionPaused(address(vToken), Action.BORROW) &&

```

```solidity
File: Lens/PoolLens.sol

461:         if (deltaBlocks > 0 && borrowSpeed > 0) {

482:         if (deltaBlocks > 0 && supplySpeed > 0) {

505:         if (borrowerIndex.mantissa == 0 && borrowIndex.mantissa > 0) {

525:         if (supplierIndex.mantissa == 0 && supplyIndex.mantissa > 0) {

```

```solidity
File: Rewards/RewardsDistributor.sol

205:             numTokens == supplySpeeds.length && numTokens == borrowSpeeds.length,

261:         if (deltaBlocks > 0 && rewardTokenSpeed > 0) {

348:         if (supplierIndex == 0 && supplyIndex >= rewardTokenInitialIndex) {

386:         if (borrowerIndex == 0 && borrowIndex >= rewardTokenInitialIndex) {

418:         if (amount > 0 && amount <= rewardTokenRemaining) {

435:         if (deltaBlocks > 0 && supplySpeed > 0) {

463:         if (deltaBlocks > 0 && borrowSpeed > 0) {

```

```solidity
File: Shortfall/Shortfall.sol

164:             (auction.auctionType == AuctionType.LARGE_POOL_DEBT &&

165:                 ((auction.highestBidder != address(0) && bidBps > auction.highestBidBps) ||

166:                     (auction.highestBidder == address(0) && bidBps >= auction.startBidBps))) ||

167:                 (auction.auctionType == AuctionType.LARGE_RISK_FUND &&

168:                     ((auction.highestBidder != address(0) && bidBps < auction.highestBidBps) ||

169:                         (auction.highestBidder == address(0) && bidBps <= auction.startBidBps))),

213:             block.number > auction.highestBidBlock + nextBidderBlockLimit && auction.highestBidder != address(0),

364:             (auction.startBlock == 0 && auction.status == AuctionStatus.NOT_STARTED) ||

458:         return auction.startBlock != 0 && auction.status == AuctionStatus.STARTED;

468:         return noBidder && (block.number > auction.startBlock + waitForFirstBidder);

```

```solidity
File: VToken.sol

837:         if (redeemTokens == 0 && redeemAmount > 0) {

1365:         require(accrualBlockNumber == 0 && borrowIndex == 0, "market may only be initialized once");

```

</details> 
 


 ### <a name="GAS-3"></a>[GAS-3]
 ### Consider using = instead of += and -= for gas efficiency
Using = instead of += and -= can save gas in certain scenarios. Consider using = when appropriate.

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: VToken.sol

630:         newAllowance += addedValue;

652:             currentAllowance -= subtractedValue;

```

</details> 
 


 ### <a name="GAS-4"></a>[GAS-4]
 ### Use >= instead of > for gas efficiency
Using >= costs less gas than >. Consider using >= when appropriate.

*Instances (49)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

265:             if (nextTotalSupply > supplyCap) {

353:             if (nextTotalBorrows > borrowCap) {

366:         if (snapshot.shortfall > 0) {

449:             if (repayAmount > borrowBalance) {

469:         if (repayAmount > maxClose) {

590:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

645:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

739:         if (newCollateralFactorMantissa > collateralFactorMaxMantissa) {

744:         if (newLiquidationThresholdMantissa > mantissaOne) {

1261:         if (snapshot.shortfall > 0) {

1350:             if (snapshot.weightedCollateral > borrowPlusEffects) {

```

```solidity
File: Lens/PoolLens.sol

461:         if (deltaBlocks > 0 && borrowSpeed > 0) {

461:         if (deltaBlocks > 0 && borrowSpeed > 0) {

465:             Double memory ratio = borrowAmount > 0 ? fraction(tokensAccrued, borrowAmount) : Double({ mantissa: 0 });

469:         } else if (deltaBlocks > 0) {

482:         if (deltaBlocks > 0 && supplySpeed > 0) {

482:         if (deltaBlocks > 0 && supplySpeed > 0) {

485:             Double memory ratio = supplyTokens > 0 ? fraction(tokensAccrued, supplyTokens) : Double({ mantissa: 0 });

489:         } else if (deltaBlocks > 0) {

505:         if (borrowerIndex.mantissa == 0 && borrowIndex.mantissa > 0) {

525:         if (supplierIndex.mantissa == 0 && supplyIndex.mantissa > 0) {

```

```solidity
File: MaxLoopsLimitHelper.sol

26:         require(limit > maxLoopsLimit, "Comptroller: Invalid maxLoopsLimit");

40:         if (len > maxLoopsLimit) {

```

```solidity
File: Rewards/RewardsDistributor.sol

261:         if (deltaBlocks > 0 && rewardTokenSpeed > 0) {

261:         if (deltaBlocks > 0 && rewardTokenSpeed > 0) {

418:         if (amount > 0 && amount <= rewardTokenRemaining) {

435:         if (deltaBlocks > 0 && supplySpeed > 0) {

435:         if (deltaBlocks > 0 && supplySpeed > 0) {

438:             Double memory ratio = supplyTokens > 0

446:         } else if (deltaBlocks > 0) {

463:         if (deltaBlocks > 0 && borrowSpeed > 0) {

463:         if (deltaBlocks > 0 && borrowSpeed > 0) {

466:             Double memory ratio = borrowAmount > 0

474:         } else if (deltaBlocks > 0) {

```

```solidity
File: RiskFund/ReserveHelpers.sol

61:         if (currentBalance > assetReserve) {

```

```solidity
File: RiskFund/RiskFund.sol

82:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

83:         require(loopsLimit_ > 0, "Risk Fund: Loops limit can not be zero");

139:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

244:         if (balanceOfUnderlyingAsset > 0) {

```

```solidity
File: Shortfall/Shortfall.sol

165:                 ((auction.highestBidder != address(0) && bidBps > auction.highestBidBps) ||

213:             block.number > auction.highestBidBlock + nextBidderBlockLimit && auction.highestBidder != address(0),

468:         return noBidder && (block.number > auction.startBlock + waitForFirstBidder);

```

```solidity
File: VToken.sol

313:         if (newProtocolSeizeShareMantissa_ + 1e18 > liquidationIncentive) {

818:         if (redeemTokensIn > 0) {

837:         if (redeemTokens == 0 && redeemAmount > 0) {

946:         uint256 repayAmountFinal = repayAmount > accountBorrowsPrev ? accountBorrowsPrev : repayAmount;

1161:         if (newReserveFactorMantissa > reserveFactorMaxMantissa) {

1215:         if (reduceAmount > totalReserves) {

1369:         require(initialExchangeRateMantissa > 0, "initial exchange rate must be greater than zero.");

```

</details> 
 


 ### <a name="GAS-5"></a>[GAS-5]
 ### `array[index] += amount` is cheaper than `array[index] = array[index] + amount` (or related variants)
When updating a value in an array with arithmetic, using `array[index] += amount` is cheaper than `array[index] = array[index] + amount`.
This is because you avoid an additonal `mload` when the array is stored in memory, and an `sload` when the array is stored in storage.
This can be applied for any arithmetic operation including `+=`, `-=`,`/=`,`*=`,`^=`,`&=`, `%=`, `<<=`,`>>=`, and `>>>=`.
This optimization can be particularly significant if the pattern occurs during a loop.

*Saves 28 gas for a storage array, 38 for a memory array*

*Instances (4)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: RiskFund/RiskFund.sol

175:             poolReserves[comptroller] = poolReserves[comptroller] + swappedTokens;

193:         poolReserves[comptroller] = poolReserves[comptroller] - amount;

```

```solidity
File: VToken.sol

1129:         accountTokens[borrower] = accountTokens[borrower] - seizeTokens;

1130:         accountTokens[liquidator] = accountTokens[liquidator] + liquidatorSeizeTokens;

```

</details> 
 


 ### <a name="GAS-6"></a>[GAS-6]
 ### Using bools for storage incurs overhead
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ComptrollerStorage.sol

40:         mapping(address => bool) accountMembership;

94:     mapping(address => mapping(Action => bool)) internal _actionPaused;

100:     mapping(address => bool) internal rewardsDistributorExists;

114:     bool internal constant _isComptroller = true;

```

```solidity
File: InterestRateModel.sol

10:     bool public constant isInterestRateModel = true;

```

```solidity
File: VTokenInterfaces.sol

24:     bool internal _notEntered;

141:     bool public constant isVToken = true;

```

</details> 
 


 ### <a name="GAS-7"></a>[GAS-7]
 ### Cache array length outside of loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Lens/PoolLens.sol

228:         for (uint256 i; i < rewardsDistributors.length; ++i) {

262:         for (uint256 i; i < markets.length; ++i) {

417:         for (uint256 i; i < markets.length; ++i) {

```

</details> 
 


 ### <a name="GAS-8"></a>[GAS-8]
 ### State variables should be cached in stack variables rather than re-reading them from storage
The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

*Saves 100 gas per instance*

*Instances (3)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: MaxLoopsLimitHelper.sol

31:         emit MaxLoopsLimitUpdated(oldMaxLoopsLimit, maxLoopsLimit);

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

85:         IRiskFund(riskFund).updateAssetsState(comptroller, asset);

```

```solidity
File: RiskFund/RiskFund.sol

259:                     IERC20Upgradeable(underlyingAsset).safeApprove(pancakeSwapRouter, balanceOfUnderlyingAsset);

```

</details> 
 


 ### <a name="GAS-9"></a>[GAS-9]
 ### Use calldata instead of memory for function arguments that do not get mutated
Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.

*Instances (15)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

153:     function enterMarkets(address[] memory vTokens) external override returns (uint256[] memory) {

```

```solidity
File: Factories/VTokenProxyFactory.sol

28:     function deployVTokenProxy(VTokenArgs memory input) external returns (VToken) {

```

```solidity
File: Lens/PoolLens.sol

308:     function getPoolDataFromVenusPool(address poolRegistryAddress, PoolRegistry.VenusPool memory venusPool)

387:     function vTokenMetadataAll(VToken[] memory vTokens) public view returns (VTokenMetadata[] memory) {

```

```solidity
File: Pool/PoolRegistry.sol

254:     function addMarket(AddMarketInput memory input) external {

342:     function updatePoolMetadata(address comptroller, VenusPoolMetaData memory _metadata) external {

```

```solidity
File: Rewards/RewardsDistributor.sol

166:         Exp memory marketBorrowIndex

187:     function updateRewardTokenBorrowIndex(address vToken, Exp memory marketBorrowIndex) external onlyComptroller {

198:         VToken[] memory vTokens,

199:         uint256[] memory supplySpeeds,

200:         uint256[] memory borrowSpeeds

277:     function claimRewardToken(address holder, VToken[] memory vTokens) public {

```

```solidity
File: VToken.sol

64:         string memory name_,

65:         string memory symbol_,

69:         RiskManagementInit memory riskManagement,

```

</details> 
 


 ### <a name="GAS-10"></a>[GAS-10]
 ### Consider using assembly for simple zero checks to save gas
Using assembly for simple zero checks can save gas. Consider using assembly when appropriate.

*Instances (6)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

136:         if (borrows == 0) {

```

```solidity
File: Comptroller.sol

1369:         if (oraclePriceMantissa == 0) {

```

```solidity
File: Rewards/RewardsDistributor.sol

222:         if (rewardTokenSpeed == 0) {

```

```solidity
File: VToken.sol

1050:         if (repayAmount == 0) {

1465:         if (_totalSupply == 0) {

```

```solidity
File: WhitePaperInterestRateModel.sol

92:         if (borrows == 0) {

```

</details> 
 


 ### <a name="GAS-11"></a>[GAS-11]
 ### Expressions for constant values should use immutable rather than constant

#### Impact:
While it doesnt save any gas because the compiler knows that developers often make this mistake, its still best to use the right tool for the task at hand. There is a difference between constant variables and immutable variables, and they should each be used in their appropriate contexts. constants should be used for literal values written into the code, and immutable variables should be used for expressions, or values calculated in, or passed into the constructor.  

*Instances (22)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

12:     uint256 private constant BASE = 1e18;

22:     uint256 public constant blocksPerYear = 10512000;

```

```solidity
File: ComptrollerStorage.sol

102:     uint256 internal constant NO_ERROR = 0;

105:     uint256 internal constant closeFactorMinMantissa = 0.05e18; // 0.05

108:     uint256 internal constant closeFactorMaxMantissa = 0.9e18; // 0.9

111:     uint256 internal constant collateralFactorMaxMantissa = 0.9e18; // 0.9

114:     bool internal constant _isComptroller = true;

```

```solidity
File: ErrorReporter.sol

5:     uint256 public constant NO_ERROR = 0; // support legacy return codes

```

```solidity
File: ExponentialNoError.sol

20:     uint256 internal constant expScale = 1e18;

21:     uint256 internal constant doubleScale = 1e36;

22:     uint256 internal constant halfExpScale = expScale / 2;

23:     uint256 internal constant mantissaOne = expScale;

```

```solidity
File: InterestRateModel.sol

10:     bool public constant isInterestRateModel = true;

```

```solidity
File: Rewards/RewardsDistributor.sol

29:     uint224 public constant rewardTokenInitialIndex = 1e36;

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

18:     uint256 private constant protocolSharePercentage = 70;

19:     uint256 private constant baseUnit = 100;

```

```solidity
File: Shortfall/Shortfall.sol

59:     uint256 private constant MAX_BPS = 10000;

```

```solidity
File: VTokenInterfaces.sol

52:     uint256 internal constant borrowRateMaxMantissa = 0.0005e16;

55:     uint256 internal constant reserveFactorMaxMantissa = 1e18;

141:     bool public constant isVToken = true;

```

```solidity
File: WhitePaperInterestRateModel.sol

12:     uint256 private constant BASE = 1e18;

17:     uint256 public constant blocksPerYear = 2102400;

```

</details> 
 


 ### <a name="GAS-12"></a>[GAS-12]
 ### Constructors can be marked payable
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn  t provided. A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

*Instances (11)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

64:     constructor(

```

```solidity
File: Comptroller.sol

126:     constructor(address poolRegistry_) {

```

```solidity
File: JumpRateModelV2.sol

12:     constructor(

```

```solidity
File: Pool/PoolRegistry.sol

149:     constructor() {

```

```solidity
File: Proxy/UpgradeableBeacon.sol

7:     constructor(address implementation_) UpgradeableBeacon(implementation_) {

```

```solidity
File: Rewards/RewardsDistributor.sol

104:     constructor() {

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

28:     constructor() {

```

```solidity
File: RiskFund/RiskFund.sol

61:     constructor() {

```

```solidity
File: Shortfall/Shortfall.sol

117:     constructor() {

```

```solidity
File: VToken.sol

41:     constructor() {

```

```solidity
File: WhitePaperInterestRateModel.sol

36:     constructor(uint256 baseRatePerYear, uint256 multiplierPerYear) {

```

</details> 
 


 ### <a name="GAS-13"></a>[GAS-13]
 ### Use Custom Errors
[Source](https://blog.soliditylang.org/2021/04/21/custom-errors/)
Instead of using error strings, to reduce deployment and runtime cost, you should use Custom Errors. This would save both deployment and runtime cost.

*Instances (89)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

71:         require(address(accessControlManager_) != address(0), "invalid ACM address");

```

```solidity
File: Comptroller.sol

127:         require(poolRegistry_ != address(0), "invalid pool registry address");

691:             require(borrowBalance == 0, "Nonzero borrow balance after liquidation");

703:         require(closeFactorMaxMantissa >= newCloseFactorMantissa, "Close factor greater than maximum close factor");

704:         require(closeFactorMinMantissa <= newCloseFactorMantissa, "Close factor smaller than minimum close factor");

779:         require(newLiquidationIncentiveMantissa >= 1e18, "liquidation incentive should be greater than 1e18");

807:         require(vToken.isVToken(), "Comptroller: Invalid vToken"); // Sanity check to make sure its really a VToken

841:         require(numMarkets != 0 && numMarkets == numBorrowCaps, "invalid input");

865:         require(vTokensCount != 0, "invalid number of markets");

866:         require(vTokensCount == newSupplyCaps.length, "invalid number of markets");

927:         require(!rewardsDistributorExists[address(_rewardsDistributor)], "already exists");

961:         require(address(newOracle) != address(0), "invalid price oracle address");

1228:         require(markets[market].isListed, "cannot pause a market that is not listed");

```

```solidity
File: MaxLoopsLimitHelper.sol

26:         require(limit > maxLoopsLimit, "Comptroller: Invalid maxLoopsLimit");

```

```solidity
File: Pool/PoolRegistry.sol

224:         require(beaconAddress != address(0), "PoolRegistry: Invalid Comptroller beacon address.");

225:         require(priceOracle != address(0), "PoolRegistry: Invalid PriceOracle address.");

256:         require(input.comptroller != address(0), "PoolRegistry: Invalid comptroller address");

257:         require(input.asset != address(0), "PoolRegistry: Invalid asset address");

258:         require(input.beaconAddress != address(0), "PoolRegistry: Invalid beacon address");

259:         require(input.vTokenReceiver != address(0), "PoolRegistry: Invalid vTokenReceiver address");

395:         require(venusPool.creator == address(0), "PoolRegistry: Pool already exists in the directory.");

439:         require(bytes(name).length <= 100, "Pool's name is too large");

```

```solidity
File: Proxy/UpgradeableBeacon.sol

8:         require(implementation_ != address(0), "Invalid implementation address");

```

```solidity
File: Rewards/RewardsDistributor.sol

99:         require(address(comptroller) == msg.sender, "Only comptroller can call this function");

183:         require(amountLeft == 0, "insufficient rewardToken for grant");

284:             require(comptroller.isMarketListed(vToken), "market must be listed");

309:         require(comptroller.isMarketListed(vToken), "rewardToken market is not listed");

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

40:         require(_protocolIncome != address(0), "ProtocolShareReserve: Protocol Income address invalid");

41:         require(_riskFund != address(0), "ProtocolShareReserve: Risk Fund address invalid");

54:         require(_poolRegistry != address(0), "ProtocolShareReserve: Pool registry address invalid");

71:         require(asset != address(0), "ProtocolShareReserve: Asset address invalid");

72:         require(amount <= poolsAssetsReserves[comptroller][asset], "ProtocolShareReserve: Insufficient pool balance");

```

```solidity
File: RiskFund/ReserveHelpers.sol

39:         require(ComptrollerInterface(comptroller).isComptroller(), "ReserveHelpers: Comptroller address invalid");

40:         require(asset != address(0), "ReserveHelpers: Asset address invalid");

51:         require(ComptrollerInterface(comptroller).isComptroller(), "ReserveHelpers: Comptroller address invalid");

52:         require(asset != address(0), "ReserveHelpers: Asset address invalid");

53:         require(poolRegistry != address(0), "ReserveHelpers: Pool Registry address is not set");

```

```solidity
File: RiskFund/RiskFund.sol

80:         require(pancakeSwapRouter_ != address(0), "Risk Fund: Pancake swap address invalid");

81:         require(convertibleBaseAsset_ != address(0), "Risk Fund: Base asset address invalid");

82:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

83:         require(loopsLimit_ > 0, "Risk Fund: Loops limit can not be zero");

100:         require(_poolRegistry != address(0), "Risk Fund: Pool registry address invalid");

111:         require(shortfallContractAddress_ != address(0), "Risk Fund: Shortfall contract address invalid");

127:         require(pancakeSwapRouter_ != address(0), "Risk Fund: PancakeSwap address invalid");

139:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

157:         require(poolRegistry != address(0), "Risk fund: Invalid pool registry.");

158:         require(markets.length == amountsOutMin.length, "Risk fund: markets and amountsOutMin are unequal lengths");

159:         require(markets.length == paths.length, "Risk fund: markets and paths are unequal lengths");

171:             require(pool.comptroller == comptroller, "comptroller doesn't exist pool registry");

172:             require(Comptroller(comptroller).isMarketListed(vToken), "market is not listed");

191:         require(msg.sender == shortfall, "Risk fund: Only callable by Shortfall contract");

192:         require(amount <= poolReserves[comptroller], "Risk Fund: Insufficient pool reserve.");

231:         require(amountOutMin != 0, "RiskFund: amountOutMin must be greater than 0 to swap vToken");

232:         require(amountOutMin >= minAmountToConvert, "RiskFund: amountOutMin should be greater than minAmountToConvert");

253:                     require(path[0] == underlyingAsset, "RiskFund: swap path must start with the underlying asset");

```

```solidity
File: Shortfall/Shortfall.sol

136:         require(convertibleBaseAsset_ != address(0), "invalid base asset address");

137:         require(address(riskFund_) != address(0), "invalid risk fund address");

138:         require(minimumPoolBadDebt_ != 0, "invalid minimum pool bad debt");

160:         require(_isStarted(auction), "no on-going auction");

161:         require(!_isStale(auction), "auction is stale, restart it");

162:         require(bidBps <= MAX_BPS, "basis points cannot be more than 10000");

211:         require(_isStarted(auction), "no on-going auction");

277:         require(_isStarted(auction), "no on-going auction");

278:         require(_isStale(auction), "you need to wait for more time for first bidder");

294:         require(_nextBidderBlockLimit != 0, "_nextBidderBlockLimit must not be 0");

308:         require(_incentiveBps != 0, "incentiveBps must not be 0");

348:         require(_poolRegistry != address(0), "invalid address");

360:         require(pool.comptroller == comptroller, "comptroller doesn't exist pool registry");

400:         require(poolBadDebt >= minimumPoolBadDebt, "pool bad debt is too low");

```

```solidity
File: VToken.sol

34:         require(_notEntered, "re-entered");

72:         require(admin_ != address(0), "invalid admin address");

134:         require(spender != address(0), "invalid spender address");

196:         require(minter != address(0), "invalid minter address");

489:         require(msg.sender == shortfall, "only shortfall contract can update bad debt");

490:         require(recoveredAmount_ <= badDebt, "more than bad debt recovered from auction");

525:         require(msg.sender == owner(), "VToken::sweepToken: only admin can sweep tokens");

526:         require(address(token) != underlying, "VToken::sweepToken: can not sweep underlying token");

626:         require(spender != address(0), "invalid spender address");

646:         require(spender != address(0), "invalid spender address");

650:         require(currentAllowance >= subtractedValue, "decreased allowance below zero");

696:         require(borrowRateMantissa <= borrowRateMaxMantissa, "borrow rate is absurdly high");

805:         require(redeemTokensIn == 0 || redeemAmountIn == 0, "one of redeemTokensIn or redeemAmountIn must be zero");

838:             revert("redeemTokens zero");

1072:         require(amountSeizeError == NO_ERROR, "LIQUIDATE_COMPTROLLER_CALCULATE_AMOUNT_SEIZE_FAILED");

1075:         require(vTokenCollateral.balanceOf(borrower) >= seizeTokens, "LIQUIDATE_SEIZE_TOO_MUCH");

1141:         require(newComptroller.isComptroller(), "marker method returned false");

1256:         require(newInterestRateModel.isInterestRateModel(), "marker method returned false");

1365:         require(accrualBlockNumber == 0 && borrowIndex == 0, "market may only be initialized once");

1369:         require(initialExchangeRateMantissa > 0, "initial exchange rate must be greater than zero.");

```

</details> 
 


 ### <a name="GAS-14"></a>[GAS-14]
 ### Initializers can be marked as payable to save deployment gas
Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. Initializers can be safely marked as payable, because only the deployer or the factory contract would call the function without carrying any funds.

*Instances (7)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

137:     function initialize(uint256 loopLimit, address accessControlManager) external initializer {

```

```solidity
File: Pool/PoolRegistry.sol

163:     function initialize(

```

```solidity
File: Rewards/RewardsDistributor.sol

111:     function initialize(

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

39:     function initialize(address _protocolIncome, address _riskFund) external initializer {

```

```solidity
File: RiskFund/RiskFund.sol

73:     function initialize(

```

```solidity
File: Shortfall/Shortfall.sol

130:     function initialize(

```

```solidity
File: VToken.sol

59:     function initialize(

```

</details> 
 


 ### <a name="GAS-15"></a>[GAS-15]
 ### Reduce gas usage by moving to Solidity 0.8.19 or later
Solidity version 0.8.19 introduced a number of gas optimizations, refer to the [Solidity 0.8.19 Release Announcement](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement) for details.

*Instances (28)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Comptroller.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ComptrollerInterface.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ComptrollerStorage.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ErrorReporter.sol

2: pragma solidity 0.8.13;

```

```solidity
File: ExponentialNoError.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Factories/JumpRateModelFactory.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Factories/VTokenProxyFactory.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Factories/WhitePaperInterestRateModelFactory.sol

2: pragma solidity 0.8.13;

```

```solidity
File: IPancakeswapV2Router.sol

2: pragma solidity 0.8.13;

```

```solidity
File: InterestRateModel.sol

2: pragma solidity 0.8.13;

```

```solidity
File: JumpRateModelV2.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Lens/PoolLens.sol

2: pragma solidity 0.8.13;

```

```solidity
File: MaxLoopsLimitHelper.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Pool/PoolRegistry.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Pool/PoolRegistryInterface.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Proxy/UpgradeableBeacon.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Rewards/RewardsDistributor.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/IProtocolShareReserve.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/IRiskFund.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/ReserveHelpers.sol

2: pragma solidity 0.8.13;

```

```solidity
File: RiskFund/RiskFund.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Shortfall/IShortfall.sol

2: pragma solidity 0.8.13;

```

```solidity
File: Shortfall/Shortfall.sol

2: pragma solidity 0.8.13;

```

```solidity
File: VToken.sol

2: pragma solidity 0.8.13;

```

```solidity
File: VTokenInterfaces.sol

2: pragma solidity 0.8.13;

```

```solidity
File: WhitePaperInterestRateModel.sol

2: pragma solidity 0.8.13;

```

</details> 
 


 ### <a name="GAS-16"></a>[GAS-16]
 ### Functions guaranteed to revert when called by normal users can be marked `payable`
If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.

*Instances (18)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

926:     function addRewardsDistributor(RewardsDistributor _rewardsDistributor) external onlyOwner {

960:     function setPriceOracle(PriceOracle newOracle) external onlyOwner {

972:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

```

```solidity
File: Pool/PoolRegistry.sol

197:     function setShortfallContract(Shortfall shortfall_) external onlyOwner {

```

```solidity
File: Rewards/RewardsDistributor.sol

125:     function initializeMarket(address vToken) external onlyComptroller {

171:     function updateRewardTokenSupplyIndex(address vToken) external onlyComptroller {

181:     function grantRewardToken(address recipient, uint256 amount) external onlyOwner {

187:     function updateRewardTokenBorrowIndex(address vToken, Exp memory marketBorrowIndex) external onlyComptroller {

219:     function setContributorRewardTokenSpeed(address contributor, uint256 rewardTokenSpeed) external onlyOwner {

233:     function distributeSupplierRewardToken(address vToken, address supplier) external onlyComptroller {

249:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

53:     function setPoolRegistry(address _poolRegistry) external onlyOwner {

```

```solidity
File: RiskFund/RiskFund.sol

99:     function setPoolRegistry(address _poolRegistry) external onlyOwner {

110:     function setShortfallContractAddress(address shortfallContractAddress_) external onlyOwner {

126:     function setPancakeSwapRouter(address pancakeSwapRouter_) external onlyOwner {

205:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

```

```solidity
File: Shortfall/Shortfall.sol

347:     function updatePoolRegistry(address _poolRegistry) external onlyOwner {

```

```solidity
File: VToken.sol

515:     function setShortfallContract(address shortfall_) external onlyOwner {

```

</details> 
 


 ### <a name="GAS-17"></a>[GAS-17]
 ### `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too)
*Saves 5 gas per loop*

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Pool/PoolRegistry.sol

398:         _numberOfPools++;

```

</details> 
 


 ### <a name="GAS-18"></a>[GAS-18]
 ### Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*Instances (6)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

22:     uint256 public constant blocksPerYear = 10512000;

```

```solidity
File: ErrorReporter.sol

5:     uint256 public constant NO_ERROR = 0; // support legacy return codes

```

```solidity
File: InterestRateModel.sol

10:     bool public constant isInterestRateModel = true;

```

```solidity
File: Rewards/RewardsDistributor.sol

29:     uint224 public constant rewardTokenInitialIndex = 1e36;

```

```solidity
File: VTokenInterfaces.sol

141:     bool public constant isVToken = true;

```

```solidity
File: WhitePaperInterestRateModel.sol

17:     uint256 public constant blocksPerYear = 2102400;

```

</details> 
 


 ### <a name="GAS-19"></a>[GAS-19]
 ### require()/revert() strings longer than 32 bytes cost extra gas
Each extra memory word of bytes past the original 32 [incurs an MSTORE](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#consider-having-short-revert-strings) which costs 3 gas.

*Instances (170)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

71:         require(address(accessControlManager_) != address(0), "invalid ACM address");

97:             revert Unauthorized(msg.sender, address(this), signature);

```

```solidity
File: Comptroller.sol

127:         require(poolRegistry_ != address(0), "invalid pool registry address");

194:             revert NonzeroBorrowBalance();

256:             revert MarketNotListed(address(vToken));

266:                 revert SupplyCapExceeded(vToken, supplyCap);

333:             revert MarketNotListed(address(vToken));

345:             revert PriceError(address(vToken));

354:                 revert BorrowCapExceeded(vToken, borrowCap);

367:             revert InsufficientLiquidity();

395:             revert MarketNotListed(address(vToken));

439:             revert MarketNotListed(address(vTokenBorrowed));

442:             revert MarketNotListed(address(vTokenCollateral));

450:                 revert TooMuchRepay();

460:             revert MinimalCollateralViolated(minLiquidatableCollateral, snapshot.totalCollateral);

464:             revert InsufficientShortfall();

470:             revert TooMuchRepay();

497:             revert MarketNotListed(vTokenCollateral);

504:                 revert ComptrollerMismatch();

510:                 revert MarketNotListed(seizerContract);

513:                 revert ComptrollerMismatch();

591:             revert CollateralExceedsThreshold(minLiquidatableCollateral, snapshot.totalCollateral);

595:             revert InsufficientShortfall();

607:             revert CollateralExceedsThreshold(scaledBorrows.mantissa, collateral.mantissa);

647:             revert CollateralExceedsThreshold(minLiquidatableCollateral, snapshot.totalCollateral);

657:             revert InsufficientCollateral(collateralToSeize, snapshot.totalCollateral);

661:             revert InsufficientShortfall();

670:                 revert MarketNotListed(address(orders[i].vTokenBorrowed));

673:                 revert MarketNotListed(address(orders[i].vTokenCollateral));

691:             require(borrowBalance == 0, "Nonzero borrow balance after liquidation");

703:         require(closeFactorMaxMantissa >= newCloseFactorMantissa, "Close factor greater than maximum close factor");

704:         require(closeFactorMinMantissa <= newCloseFactorMantissa, "Close factor smaller than minimum close factor");

735:             revert MarketNotListed(address(vToken));

740:             revert InvalidCollateralFactor();

745:             revert InvalidLiquidationThreshold();

750:             revert InvalidLiquidationThreshold();

755:             revert PriceError(address(vToken));

779:         require(newLiquidationIncentiveMantissa >= 1e18, "liquidation incentive should be greater than 1e18");

804:             revert MarketAlreadyListed(address(vToken));

807:         require(vToken.isVToken(), "Comptroller: Invalid vToken"); // Sanity check to make sure its really a VToken

841:         require(numMarkets != 0 && numMarkets == numBorrowCaps, "invalid input");

865:         require(vTokensCount != 0, "invalid number of markets");

866:         require(vTokensCount == newSupplyCaps.length, "invalid number of markets");

927:         require(!rewardsDistributorExists[address(_rewardsDistributor)], "already exists");

933:             require(

961:         require(address(newOracle) != address(0), "invalid price oracle address");

1180:             revert MarketNotListed(address(vToken));

1209:                 revert MarketAlreadyListed(vToken);

1228:         require(markets[market].isListed, "cannot pause a market that is not listed");

1245:             revert MarketNotListed(address(vToken));

1262:             revert InsufficientLiquidity();

1370:             revert PriceError(address(asset));

1413:             revert SnapshotError(address(vToken), user);

1422:             revert UnexpectedSender(expectedSender, msg.sender);

1431:             revert ActionPaused(market, action);

```

```solidity
File: ExponentialNoError.sol

64:         require(n < 2**224, errorMessage);

69:         require(n < 2**32, errorMessage);

```

```solidity
File: MaxLoopsLimitHelper.sol

26:         require(limit > maxLoopsLimit, "Comptroller: Invalid maxLoopsLimit");

41:             revert MaxLoopsLimitExceeded(maxLoopsLimit, len);

```

```solidity
File: Pool/PoolRegistry.sol

224:         require(beaconAddress != address(0), "PoolRegistry: Invalid Comptroller beacon address.");

225:         require(priceOracle != address(0), "PoolRegistry: Invalid PriceOracle address.");

256:         require(input.comptroller != address(0), "PoolRegistry: Invalid comptroller address");

257:         require(input.asset != address(0), "PoolRegistry: Invalid asset address");

258:         require(input.beaconAddress != address(0), "PoolRegistry: Invalid beacon address");

259:         require(input.vTokenReceiver != address(0), "PoolRegistry: Invalid vTokenReceiver address");

262:         require(

395:         require(venusPool.creator == address(0), "PoolRegistry: Pool already exists in the directory.");

422:             revert ZeroAddressNotAllowed();

431:             revert ZeroAddressNotAllowed();

439:         require(bytes(name).length <= 100, "Pool's name is too large");

```

```solidity
File: Proxy/UpgradeableBeacon.sol

8:         require(implementation_ != address(0), "Invalid implementation address");

```

```solidity
File: Rewards/RewardsDistributor.sol

99:         require(address(comptroller) == msg.sender, "Only comptroller can call this function");

183:         require(amountLeft == 0, "insufficient rewardToken for grant");

204:         require(

284:             require(comptroller.isMarketListed(vToken), "market must be listed");

309:         require(comptroller.isMarketListed(vToken), "rewardToken market is not listed");

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

40:         require(_protocolIncome != address(0), "ProtocolShareReserve: Protocol Income address invalid");

41:         require(_riskFund != address(0), "ProtocolShareReserve: Risk Fund address invalid");

54:         require(_poolRegistry != address(0), "ProtocolShareReserve: Pool registry address invalid");

71:         require(asset != address(0), "ProtocolShareReserve: Asset address invalid");

72:         require(amount <= poolsAssetsReserves[comptroller][asset], "ProtocolShareReserve: Insufficient pool balance");

```

```solidity
File: RiskFund/ReserveHelpers.sol

39:         require(ComptrollerInterface(comptroller).isComptroller(), "ReserveHelpers: Comptroller address invalid");

40:         require(asset != address(0), "ReserveHelpers: Asset address invalid");

51:         require(ComptrollerInterface(comptroller).isComptroller(), "ReserveHelpers: Comptroller address invalid");

52:         require(asset != address(0), "ReserveHelpers: Asset address invalid");

53:         require(poolRegistry != address(0), "ReserveHelpers: Pool Registry address is not set");

54:         require(

```

```solidity
File: RiskFund/RiskFund.sol

80:         require(pancakeSwapRouter_ != address(0), "Risk Fund: Pancake swap address invalid");

81:         require(convertibleBaseAsset_ != address(0), "Risk Fund: Base asset address invalid");

82:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

83:         require(loopsLimit_ > 0, "Risk Fund: Loops limit can not be zero");

100:         require(_poolRegistry != address(0), "Risk Fund: Pool registry address invalid");

111:         require(shortfallContractAddress_ != address(0), "Risk Fund: Shortfall contract address invalid");

112:         require(

127:         require(pancakeSwapRouter_ != address(0), "Risk Fund: PancakeSwap address invalid");

139:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

157:         require(poolRegistry != address(0), "Risk fund: Invalid pool registry.");

158:         require(markets.length == amountsOutMin.length, "Risk fund: markets and amountsOutMin are unequal lengths");

159:         require(markets.length == paths.length, "Risk fund: markets and paths are unequal lengths");

171:             require(pool.comptroller == comptroller, "comptroller doesn't exist pool registry");

172:             require(Comptroller(comptroller).isMarketListed(vToken), "market is not listed");

191:         require(msg.sender == shortfall, "Risk fund: Only callable by Shortfall contract");

192:         require(amount <= poolReserves[comptroller], "Risk Fund: Insufficient pool reserve.");

231:         require(amountOutMin != 0, "RiskFund: amountOutMin must be greater than 0 to swap vToken");

232:         require(amountOutMin >= minAmountToConvert, "RiskFund: amountOutMin should be greater than minAmountToConvert");

253:                     require(path[0] == underlyingAsset, "RiskFund: swap path must start with the underlying asset");

254:                     require(

```

```solidity
File: Shortfall/Shortfall.sol

136:         require(convertibleBaseAsset_ != address(0), "invalid base asset address");

137:         require(address(riskFund_) != address(0), "invalid risk fund address");

138:         require(minimumPoolBadDebt_ != 0, "invalid minimum pool bad debt");

160:         require(_isStarted(auction), "no on-going auction");

161:         require(!_isStale(auction), "auction is stale, restart it");

162:         require(bidBps <= MAX_BPS, "basis points cannot be more than 10000");

163:         require(

211:         require(_isStarted(auction), "no on-going auction");

212:         require(

277:         require(_isStarted(auction), "no on-going auction");

278:         require(_isStale(auction), "you need to wait for more time for first bidder");

294:         require(_nextBidderBlockLimit != 0, "_nextBidderBlockLimit must not be 0");

308:         require(_incentiveBps != 0, "incentiveBps must not be 0");

348:         require(_poolRegistry != address(0), "invalid address");

360:         require(pool.comptroller == comptroller, "comptroller doesn't exist pool registry");

363:         require(

400:         require(poolBadDebt >= minimumPoolBadDebt, "pool bad debt is too low");

```

```solidity
File: VToken.sol

34:         require(_notEntered, "re-entered");

72:         require(admin_ != address(0), "invalid admin address");

134:         require(spender != address(0), "invalid spender address");

196:         require(minter != address(0), "invalid minter address");

314:             revert ProtocolSeizeShareTooBig();

396:             revert HealBorrowUnauthorized();

457:             revert ForceLiquidateBorrowUnauthorized();

489:         require(msg.sender == shortfall, "only shortfall contract can update bad debt");

490:         require(recoveredAmount_ <= badDebt, "more than bad debt recovered from auction");

525:         require(msg.sender == owner(), "VToken::sweepToken: only admin can sweep tokens");

526:         require(address(token) != underlying, "VToken::sweepToken: can not sweep underlying token");

626:         require(spender != address(0), "invalid spender address");

646:         require(spender != address(0), "invalid spender address");

650:         require(currentAllowance >= subtractedValue, "decreased allowance below zero");

696:         require(borrowRateMantissa <= borrowRateMaxMantissa, "borrow rate is absurdly high");

753:             revert MintFreshnessCheck();

805:         require(redeemTokensIn == 0 || redeemAmountIn == 0, "one of redeemTokensIn or redeemAmountIn must be zero");

809:             revert RedeemFreshnessCheck();

838:             revert("redeemTokens zero");

846:             revert RedeemTransferOutNotPossible();

883:             revert BorrowFreshnessCheck();

888:             revert BorrowCashNotAvailable();

940:             revert RepayBorrowFreshnessCheck();

1001:             revert LiquidateAccrueCollateralInterestFailed(error);

1036:             revert LiquidateFreshnessCheck();

1041:             revert LiquidateCollateralFreshnessCheck();

1046:             revert LiquidateLiquidatorIsBorrower();

1051:             revert LiquidateCloseAmountIsZero();

1056:             revert LiquidateCloseAmountIsUintMax();

1072:         require(amountSeizeError == NO_ERROR, "LIQUIDATE_COMPTROLLER_CALCULATE_AMOUNT_SEIZE_FAILED");

1075:         require(vTokenCollateral.balanceOf(borrower) >= seizeTokens, "LIQUIDATE_SEIZE_TOO_MUCH");

1108:             revert LiquidateSeizeLiquidatorIsBorrower();

1141:         require(newComptroller.isComptroller(), "marker method returned false");

1157:             revert SetReserveFactorFreshCheck();

1162:             revert SetReserveFactorBoundsCheck();

1184:             revert AddReservesFactorFreshCheck(actualAddAmount);

1206:             revert ReduceReservesFreshCheck();

1211:             revert ReduceReservesCashNotAvailable();

1216:             revert ReduceReservesCashValidation();

1249:             revert SetInterestRateModelFreshCheck();

1256:         require(newInterestRateModel.isInterestRateModel(), "marker method returned false");

1308:             revert TransferNotAllowed();

1365:         require(accrualBlockNumber == 0 && borrowIndex == 0, "market may only be initialized once");

1369:         require(initialExchangeRateMantissa > 0, "initial exchange rate must be greater than zero.");

1400:             revert ZeroAddressNotAllowed();

1409:             revert ZeroAddressNotAllowed();

```

</details> 
 


 ### <a name="GAS-20"></a>[GAS-20]
 ### Use shift Right/Left instead of division/multiplication if possible

*Instances (1)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ExponentialNoError.sol

22:     uint256 internal constant halfExpScale = expScale / 2;

```

</details> 
 


 ### <a name="GAS-21"></a>[GAS-21]
 ### Splitting require() statements that use && saves gas

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

841:         require(numMarkets != 0 && numMarkets == numBorrowCaps, "invalid input");

```

```solidity
File: VToken.sol

1365:         require(accrualBlockNumber == 0 && borrowIndex == 0, "market may only be initialized once");

```

</details> 
 


 ### <a name="GAS-22"></a>[GAS-22]
 ### Structs can be packed into fewer storage slots
Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings

*Instances (23)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: ComptrollerStorage.sol

7:     struct LiquidationOrder {

13:     struct AccountLiquiditySnapshot {

22:     struct RewardSpeeds {

28:     struct Market {

```

```solidity
File: ExponentialNoError.sol

12:     struct Exp {

16:     struct Double {

```

```solidity
File: Factories/VTokenProxyFactory.sol

11:     struct VTokenArgs {

```

```solidity
File: Lens/PoolLens.sol

15:     struct PoolData {

34:     struct VTokenMetadata {

56:     struct VTokenBalances {

68:     struct VTokenUnderlyingPrice {

76:     struct PendingReward {

84:     struct RewardSummary {

94:     struct RewardTokenState {

104:     struct BadDebt {

112:     struct BadDebtSummary {

```

```solidity
File: Pool/PoolRegistry.sol

32:     struct AddMarketInput {

```

```solidity
File: Pool/PoolRegistryInterface.sol

8:     struct VenusPool {

19:     struct VenusPoolMetaData {

```

```solidity
File: Rewards/RewardsDistributor.sol

15:     struct RewardToken {

```

```solidity
File: Shortfall/Shortfall.sol

33:     struct Auction {

```

```solidity
File: VTokenInterfaces.sol

16:     struct BorrowSnapshot {

133:     struct RiskManagementInit {

```

</details> 
 


 ### <a name="GAS-23"></a>[GAS-23]
 ### Variables can be packed into fewer storage slots by truncating timestamp bytes
By using a uint32 rather than a larger type for variables that track timestamps, one can save gas at the expense of the protocol breaking after the year 2106 (when uint32 wraps). Subsequent reads as well as writes have smaller gas savings

*Instances (2)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Lens/PoolLens.sol

459:         uint256 blockNumber = block.number;

480:         uint256 blockNumber = block.number;

```

</details> 
 


 ### <a name="GAS-24"></a>[GAS-24]
 ### Consider using uint256(1)/uint256(2) instead of true/false for gas efficiency
Using uint256(1) and uint256(2) instead of true and false can save gas for certain changes. Consider using uint256(1)/uint256(2) when appropriate.

*Instances (18)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

682:                 true

810:         newMarket.isListed = true;

943:         rewardsDistributorExists[address(_rewardsDistributor)] = true;

1193:         marketToJoin.accountMembership[borrower] = true;

```

```solidity
File: ComptrollerStorage.sol

114:     bool internal constant _isComptroller = true;

```

```solidity
File: InterestRateModel.sol

10:     bool public constant isInterestRateModel = true;

```

```solidity
File: VToken.sol

35:         _notEntered = false;

37:         _notEntered = true; // get a gas-refund post-Istanbul

101:         return true;

120:         return true;

139:         return true;

297:         _liquidateBorrow(msg.sender, borrower, repayAmount, vTokenCollateral, false);

634:         return true;

658:         return true;

1141:         require(newComptroller.isComptroller(), "marker method returned false");

1256:         require(newInterestRateModel.isInterestRateModel(), "marker method returned false");

1394:         _notEntered = true;

```

```solidity
File: VTokenInterfaces.sol

141:     bool public constant isVToken = true;

```

</details> 
 


 ### <a name="GAS-25"></a>[GAS-25]
 ### Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead
Using uints or ints smaller than 32 bytes (256 bits) can incur overhead. Consider using uint256 or int256 to avoid potential issues.

*Instances (5)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Factories/VTokenProxyFactory.sol

18:         uint8 decimals_;

```

```solidity
File: Pool/PoolRegistry.sol

35:         uint8 decimals;

```

```solidity
File: VToken.sol

66:         uint8 decimals_,

1357:         uint8 decimals_,

```

```solidity
File: VTokenInterfaces.sol

44:     uint8 public decimals;

```

</details> 
 


 ### <a name="GAS-26"></a>[GAS-26]
 ### Use != 0 instead of > 0 for unsigned integer comparison

*Instances (49)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

265:             if (nextTotalSupply > supplyCap) {

353:             if (nextTotalBorrows > borrowCap) {

366:         if (snapshot.shortfall > 0) {

449:             if (repayAmount > borrowBalance) {

469:         if (repayAmount > maxClose) {

590:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

645:         if (snapshot.totalCollateral > minLiquidatableCollateral) {

739:         if (newCollateralFactorMantissa > collateralFactorMaxMantissa) {

744:         if (newLiquidationThresholdMantissa > mantissaOne) {

1261:         if (snapshot.shortfall > 0) {

1350:             if (snapshot.weightedCollateral > borrowPlusEffects) {

```

```solidity
File: Lens/PoolLens.sol

461:         if (deltaBlocks > 0 && borrowSpeed > 0) {

461:         if (deltaBlocks > 0 && borrowSpeed > 0) {

465:             Double memory ratio = borrowAmount > 0 ? fraction(tokensAccrued, borrowAmount) : Double({ mantissa: 0 });

469:         } else if (deltaBlocks > 0) {

482:         if (deltaBlocks > 0 && supplySpeed > 0) {

482:         if (deltaBlocks > 0 && supplySpeed > 0) {

485:             Double memory ratio = supplyTokens > 0 ? fraction(tokensAccrued, supplyTokens) : Double({ mantissa: 0 });

489:         } else if (deltaBlocks > 0) {

505:         if (borrowerIndex.mantissa == 0 && borrowIndex.mantissa > 0) {

525:         if (supplierIndex.mantissa == 0 && supplyIndex.mantissa > 0) {

```

```solidity
File: MaxLoopsLimitHelper.sol

26:         require(limit > maxLoopsLimit, "Comptroller: Invalid maxLoopsLimit");

40:         if (len > maxLoopsLimit) {

```

```solidity
File: Rewards/RewardsDistributor.sol

261:         if (deltaBlocks > 0 && rewardTokenSpeed > 0) {

261:         if (deltaBlocks > 0 && rewardTokenSpeed > 0) {

418:         if (amount > 0 && amount <= rewardTokenRemaining) {

435:         if (deltaBlocks > 0 && supplySpeed > 0) {

435:         if (deltaBlocks > 0 && supplySpeed > 0) {

438:             Double memory ratio = supplyTokens > 0

446:         } else if (deltaBlocks > 0) {

463:         if (deltaBlocks > 0 && borrowSpeed > 0) {

463:         if (deltaBlocks > 0 && borrowSpeed > 0) {

466:             Double memory ratio = borrowAmount > 0

474:         } else if (deltaBlocks > 0) {

```

```solidity
File: RiskFund/ReserveHelpers.sol

61:         if (currentBalance > assetReserve) {

```

```solidity
File: RiskFund/RiskFund.sol

82:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

83:         require(loopsLimit_ > 0, "Risk Fund: Loops limit can not be zero");

139:         require(minAmountToConvert_ > 0, "Risk Fund: Invalid min amount to convert");

244:         if (balanceOfUnderlyingAsset > 0) {

```

```solidity
File: Shortfall/Shortfall.sol

165:                 ((auction.highestBidder != address(0) && bidBps > auction.highestBidBps) ||

213:             block.number > auction.highestBidBlock + nextBidderBlockLimit && auction.highestBidder != address(0),

468:         return noBidder && (block.number > auction.startBlock + waitForFirstBidder);

```

```solidity
File: VToken.sol

313:         if (newProtocolSeizeShareMantissa_ + 1e18 > liquidationIncentive) {

818:         if (redeemTokensIn > 0) {

837:         if (redeemTokens == 0 && redeemAmount > 0) {

946:         uint256 repayAmountFinal = repayAmount > accountBorrowsPrev ? accountBorrowsPrev : repayAmount;

1161:         if (newReserveFactorMantissa > reserveFactorMaxMantissa) {

1215:         if (reduceAmount > totalReserves) {

1369:         require(initialExchangeRateMantissa > 0, "initial exchange rate must be greater than zero.");

```

</details> 
 


 ### <a name="GAS-27"></a>[GAS-27]
 ### `internal` functions not called by the contract should be removed
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword

*Instances (10)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: Comptroller.sol

1380:     function _getCollateralFactor(VToken asset) internal view returns (Exp memory) {

1389:     function _getLiquidationThreshold(VToken asset) internal view returns (Exp memory) {

```

```solidity
File: ExponentialNoError.sol

38:     function mul_ScalarTruncate(Exp memory a, uint256 scalar) internal pure returns (uint256) {

47:     function mul_ScalarTruncateAddUInt(

59:     function lessThanExp(Exp memory left, Exp memory right) internal pure returns (bool) {

63:     function safe224(uint256 n, string memory errorMessage) internal pure returns (uint224) {

68:     function safe32(uint256 n, string memory errorMessage) internal pure returns (uint32) {

153:     function fraction(uint256 a, uint256 b) internal pure returns (Double memory) {

```

```solidity
File: MaxLoopsLimitHelper.sol

25:     function _setMaxLoopsLimit(uint256 limit) internal {

39:     function _ensureMaxLoops(uint256 len) internal view {

```

</details> 
 


 ### <a name="GAS-28"></a>[GAS-28]
 ### Optimize names to save gas
public/external function names and public member variable names can be optimized to save gas. See [this](https://gist.github.com/IllIllI000/a5d8b486a8259f9f77891a919febd1a9) link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92)

*Instances (229)*:
 
 <details>
 <summary>Click to expand!</summary>

```solidity
File: BaseJumpRateModelV2.sol

17:     IAccessControlManagerV8 public accessControlManager;

22:     uint256 public constant blocksPerYear = 10512000;

27:     uint256 public multiplierPerBlock;

32:     uint256 public baseRatePerBlock;

37:     uint256 public jumpMultiplierPerBlock;

42:     uint256 public kink;

92:     ) external virtual {

116:     ) public view virtual override returns (uint256) {

134:     ) public pure returns (uint256) {

```

```solidity
File: Comptroller.sol

26:     address public immutable poolRegistry;

137:     function initialize(uint256 loopLimit, address accessControlManager) external initializer {

153:     function enterMarkets(address[] memory vTokens) external override returns (uint256[] memory) {

186:     function exitMarket(address vTokenAddress) external override returns (uint256) {

252:     ) external override {

295:     ) external override {

327:     ) external override {

389:     function preRepayHook(address vToken, address borrower) external override {

429:     ) external override {

490:     ) external override {

545:     ) external override {

926:     function addRewardsDistributor(RewardsDistributor _rewardsDistributor) external onlyOwner {

960:     function setPriceOracle(PriceOracle newOracle) external onlyOwner {

972:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

985:         external

1014:         external

1037:     function getAllMarkets() external view override returns (VToken[] memory) {

1046:     function isMarketListed(VToken vToken) external view returns (bool) {

1057:     function getAssetsIn(address account) external view returns (VToken[] memory) {

1069:     function checkMembership(address account, VToken vToken) external view returns (bool) {

1087:     ) external view override returns (uint256 error, uint256 tokensToSeize) {

1118:     function getRewardsByMarket(address vToken) external view returns (RewardSpeeds[] memory rewardSpeeds) {

1135:     function isComptroller() external pure override returns (bool) {

1143:     function getRewardDistributors() public view returns (RewardsDistributor[] memory) {

1153:     function actionPaused(address market, Action action) public view returns (bool) {

1163:     function isDeprecated(VToken vToken) public view returns (bool) {

```

```solidity
File: ComptrollerInterface.sol

58:     function isComptroller() external view returns (bool);

66:     ) external view returns (uint256, uint256);

68:     function getAllMarkets() external view returns (VToken[] memory);

72:     function markets(address) external view returns (bool, uint256);

74:     function oracle() external view returns (PriceOracle);

76:     function getAssetsIn(address) external view returns (VToken[] memory);

78:     function closeFactorMantissa() external view returns (uint256);

80:     function liquidationIncentiveMantissa() external view returns (uint256);

82:     function minLiquidatableCollateral() external view returns (uint256);

84:     function getRewardDistributors() external view returns (RewardsDistributor[] memory);

86:     function getAllMarkets() external view returns (VToken[] memory);

88:     function borrowCaps(address) external view returns (uint256);

90:     function supplyCaps(address) external view returns (uint256);

```

```solidity
File: ComptrollerStorage.sol

58:     PriceOracle public oracle;

63:     uint256 public closeFactorMantissa;

68:     uint256 public liquidationIncentiveMantissa;

73:     mapping(address => VToken[]) public accountAssets;

79:     mapping(address => Market) public markets;

82:     VToken[] public allMarkets;

85:     mapping(address => uint256) public borrowCaps;

88:     uint256 public minLiquidatableCollateral;

91:     mapping(address => uint256) public supplyCaps;

```

```solidity
File: ErrorReporter.sol

5:     uint256 public constant NO_ERROR = 0; // support legacy return codes

```

```solidity
File: InterestRateModel.sol

10:     bool public constant isInterestRateModel = true;

23:     ) external view virtual returns (uint256);

38:     ) external view virtual returns (uint256);

```

```solidity
File: JumpRateModelV2.sol

36:     ) external view override returns (uint256) {

```

```solidity
File: Lens/PoolLens.sol

137:     function getAllPools(address poolRegistryAddress) external view returns (PoolData[] memory) {

159:         external

177:     ) external view returns (address) {

188:         external

201:         external

220:         external

247:     function getPoolBadDebt(address comptrollerAddress) external view returns (BadDebtSummary memory) {

309:         public

351:     function vTokenMetadata(VToken vToken) public view returns (VTokenMetadata memory) {

387:     function vTokenMetadataAll(VToken[] memory vTokens) public view returns (VTokenMetadata[] memory) {

400:     function vTokenUnderlyingPrice(VToken vToken) public view returns (VTokenUnderlyingPrice memory) {

```

```solidity
File: MaxLoopsLimitHelper.sol

6:     uint256 public maxLoopsLimit;

```

```solidity
File: Pool/PoolRegistry.sol

57:     VTokenProxyFactory public vTokenFactory;

62:     JumpRateModelFactory public jumpRateFactory;

67:     WhitePaperInterestRateModelFactory public whitePaperFactory;

72:     Shortfall public shortfall;

77:     address payable public protocolShareReserve;

82:     mapping(address => VenusPoolMetaData) public metadata;

170:     ) external initializer {

187:     function setProtocolShareReserve(address payable protocolShareReserve_) external onlyOwner {

197:     function setShortfallContract(Shortfall shortfall_) external onlyOwner {

221:     ) external virtual returns (uint256 index, address proxyAddress) {

353:     function getAllPools() external view override returns (VenusPool[] memory) {

366:     function getPoolByComptroller(address comptroller) external view override returns (VenusPool memory) {

374:     function getVenusPoolMetadata(address comptroller) external view override returns (VenusPoolMetaData memory) {

378:     function getVTokenForAsset(address comptroller, address asset) external view override returns (address) {

382:     function getPoolsSupportedByAsset(address asset) external view override returns (address[] memory) {

```

```solidity
File: Pool/PoolRegistryInterface.sol

26:     function getAllPools() external view returns (VenusPool[] memory);

29:     function getPoolByComptroller(address comptroller) external view returns (VenusPool memory);

32:     function getVTokenForAsset(address comptroller, address asset) external view returns (address);

35:     function getPoolsSupportedByAsset(address asset) external view returns (address[] memory);

38:     function getVenusPoolMetadata(address comptroller) external view returns (VenusPoolMetaData memory);

```

```solidity
File: Rewards/RewardsDistributor.sol

23:     mapping(address => RewardToken) public rewardTokenSupplyState;

26:     mapping(address => mapping(address => uint256)) public rewardTokenSupplierIndex;

29:     uint224 public constant rewardTokenInitialIndex = 1e36;

32:     mapping(address => uint256) public rewardTokenAccrued;

35:     mapping(address => uint256) public rewardTokenBorrowSpeeds;

38:     mapping(address => uint256) public rewardTokenSupplySpeeds;

41:     mapping(address => RewardToken) public rewardTokenBorrowState;

44:     mapping(address => uint256) public rewardTokenContributorSpeeds;

47:     mapping(address => uint256) public lastContributorBlock;

50:     mapping(address => mapping(address => uint256)) public rewardTokenBorrowerIndex;

54:     IERC20Upgradeable public rewardToken;

116:     ) external initializer {

125:     function initializeMarket(address vToken) external onlyComptroller {

167:     ) external onlyComptroller {

171:     function updateRewardTokenSupplyIndex(address vToken) external onlyComptroller {

181:     function grantRewardToken(address recipient, uint256 amount) external onlyOwner {

187:     function updateRewardTokenBorrowIndex(address vToken, Exp memory marketBorrowIndex) external onlyComptroller {

219:     function setContributorRewardTokenSpeed(address contributor, uint256 rewardTokenSpeed) external onlyOwner {

233:     function distributeSupplierRewardToken(address vToken, address supplier) external onlyComptroller {

249:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

294:     function getBlockNumber() public view virtual returns (uint256) {

```

```solidity
File: RiskFund/IRiskFund.sol

15:     function poolReserves(address comptroller) external view returns (uint256);

```

```solidity
File: RiskFund/ProtocolShareReserve.sol

39:     function initialize(address _protocolIncome, address _riskFund) external initializer {

53:     function setPoolRegistry(address _poolRegistry) external onlyOwner {

```

```solidity
File: RiskFund/ReserveHelpers.sol

38:     function getPoolAssetReserve(address comptroller, address asset) external view returns (uint256) {

50:     function updateAssetsState(address comptroller, address asset) public virtual {

```

```solidity
File: RiskFund/RiskFund.sol

35:     mapping(address => uint256) public poolReserves;

79:     ) external initializer {

99:     function setPoolRegistry(address _poolRegistry) external onlyOwner {

110:     function setShortfallContractAddress(address shortfallContractAddress_) external onlyOwner {

126:     function setPancakeSwapRouter(address pancakeSwapRouter_) external onlyOwner {

155:     ) external override returns (uint256) {

190:     function transferReserveForAuction(address comptroller, uint256 amount) external override returns (uint256) {

205:     function setMaxLoopsLimit(uint256 limit) external onlyOwner {

```

```solidity
File: Shortfall/Shortfall.sol

47:     address public poolRegistry;

53:     uint256 public minimumPoolBadDebt;

62:     uint256 public nextBidderBlockLimit;

65:     uint256 public waitForFirstBidder;

68:     address public convertibleBaseAsset;

71:     mapping(address => Auction) public auctions;

135:     ) external initializer {

157:     function placeBid(address comptroller, uint256 bidBps) external nonReentrant {

208:     function closeAuction(address comptroller) external nonReentrant {

347:     function updatePoolRegistry(address _poolRegistry) external onlyOwner {

```

```solidity
File: VToken.sol

71:     ) external initializer {

99:     function transfer(address dst, uint256 amount) external override nonReentrant returns (bool) {

118:     ) external override nonReentrant returns (bool) {

133:     function approve(address spender, uint256 amount) external override returns (bool) {

148:     function balanceOfUnderlying(address owner) external override returns (uint256) {

157:     function totalBorrowsCurrent() external override nonReentrant returns (uint256) {

167:     function borrowBalanceCurrent(address account) external override nonReentrant returns (uint256) {

180:     function mint(uint256 mintAmount) external override nonReentrant returns (uint256) {

195:     function mintBehalf(address minter, uint256 mintAmount) external override nonReentrant returns (uint256) {

213:     function redeem(uint256 redeemTokens) external override nonReentrant returns (uint256) {

226:     function redeemUnderlying(uint256 redeemAmount) external override nonReentrant returns (uint256) {

241:     function borrow(uint256 borrowAmount) external override nonReentrant returns (uint256) {

255:     function repayBorrow(uint256 repayAmount) external override nonReentrant returns (uint256) {

270:     function repayBorrowBehalf(address borrower, uint256 repayAmount) external override nonReentrant returns (uint256) {

296:     ) external override returns (uint256) {

330:     function setReserveFactor(uint256 newReserveFactorMantissa) external override nonReentrant {

345:     function reduceReserves(uint256 reduceAmount) external override nonReentrant {

356:     function addReserves(uint256 addAmount) external override nonReentrant {

369:     function setInterestRateModel(InterestRateModel newInterestRateModel) external override {

394:     ) external override nonReentrant {

455:     ) external override {

477:     ) external override nonReentrant {

505:     function setProtocolShareReserve(address payable protocolShareReserve_) external onlyOwner {

515:     function setShortfallContract(address shortfall_) external onlyOwner {

524:     function sweepToken(IERC20Upgradeable token) external override {

539:     function allowance(address owner, address spender) external view override returns (uint256) {

548:     function balanceOf(address owner) external view override returns (uint256) {

562:         external

579:     function getCash() external view override returns (uint256) {

587:     function borrowRatePerBlock() external view override returns (uint256) {

595:     function supplyRatePerBlock() external view override returns (uint256) {

604:     function borrowBalanceStored(address account) external view override returns (uint256) {

613:     function exchangeRateStored() external view override returns (uint256) {

645:     function decreaseAllowance(address spender, uint256 subtractedValue) public virtual returns (bool) {

665:     function exchangeRateCurrent() public override nonReentrant returns (uint256) {

678:     function accrueInterest() public virtual override returns (uint256) {

```

```solidity
File: VTokenInterfaces.sol

29:     address public underlying;

34:     string public name;

39:     string public symbol;

44:     uint8 public decimals;

49:     address payable public protocolShareReserve;

60:     ComptrollerInterface public comptroller;

65:     InterestRateModel public interestRateModel;

73:     uint256 public reserveFactorMantissa;

78:     uint256 public accrualBlockNumber;

83:     uint256 public borrowIndex;

88:     uint256 public totalBorrows;

93:     uint256 public totalReserves;

98:     uint256 public totalSupply;

103:     uint256 public badDebt;

117:     uint256 public protocolSeizeShareMantissa;

122:     address public shortfall;

141:     bool public constant isVToken = true;

270:     function mint(uint256 mintAmount) external virtual returns (uint256);

272:     function mintBehalf(address minter, uint256 mintAllowed) external virtual returns (uint256);

274:     function redeem(uint256 redeemTokens) external virtual returns (uint256);

276:     function redeemUnderlying(uint256 redeemAmount) external virtual returns (uint256);

278:     function borrow(uint256 borrowAmount) external virtual returns (uint256);

280:     function repayBorrow(uint256 repayAmount) external virtual returns (uint256);

282:     function repayBorrowBehalf(address borrower, uint256 repayAmount) external virtual returns (uint256);

288:     ) external virtual returns (uint256);

294:     ) external virtual;

302:     ) external virtual;

308:     ) external virtual;

310:     function transfer(address dst, uint256 amount) external virtual returns (bool);

316:     ) external virtual returns (bool);

318:     function accrueInterest() external virtual returns (uint256);

320:     function sweepToken(IERC20Upgradeable token) external virtual;

324:     function setReserveFactor(uint256 newReserveFactorMantissa) external virtual;

326:     function reduceReserves(uint256 reduceAmount) external virtual;

328:     function exchangeRateCurrent() external virtual returns (uint256);

330:     function borrowBalanceCurrent(address account) external virtual returns (uint256);

332:     function setInterestRateModel(InterestRateModel newInterestRateModel) external virtual;

334:     function addReserves(uint256 addAmount) external virtual;

336:     function totalBorrowsCurrent() external virtual returns (uint256);

338:     function balanceOfUnderlying(address owner) external virtual returns (uint256);

340:     function approve(address spender, uint256 amount) external virtual returns (bool);

342:     function allowance(address owner, address spender) external view virtual returns (uint256);

344:     function balanceOf(address owner) external view virtual returns (uint256);

347:         external

357:     function borrowRatePerBlock() external view virtual returns (uint256);

359:     function supplyRatePerBlock() external view virtual returns (uint256);

361:     function borrowBalanceStored(address account) external view virtual returns (uint256);

363:     function exchangeRateStored() external view virtual returns (uint256);

365:     function getCash() external view virtual returns (uint256);

```

```solidity
File: WhitePaperInterestRateModel.sol

17:     uint256 public constant blocksPerYear = 2102400;

22:     uint256 public immutable multiplierPerBlock;

27:     uint256 public immutable baseRatePerBlock;

54:     ) public view override returns (uint256) {

72:     ) public view override returns (uint256) {

90:     ) public pure returns (uint256) {

```

</details> 
 

