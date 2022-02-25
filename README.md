# lucky_dog_contract
luckyDog合约部署说明

马蹄测试服

ERC2O合约（用于模拟WETH,已下简称WETH）:0x1Cb420513f755e4E368F765b4CcB8F6D41C04ec8

ERC721合约(用户创建活动的门票,以下简称NFT):0xF1Db72B50735C3E7Dc6EA69A0390f0464D63872E

LuckyDog合约（用于创建活动，已下简称LD）：0xd5D6159365709Ec65F08a8Bc11540e656B0F9a12


马蹄mainnet主网

ERC2O合约（用于模拟WETH,已下简称WETH）:0x7ceB23fD6bC0adD59E62ac25578270cFf1b9f619

ERC721合约(用户创建活动的门票,以下简称NFT):0x45C5A27c1013eB0513D66519948e38361610703b

LuckyDog合约（用于创建活动，已下简称LD）：0x4Bc2283194becAAB4Fd5EB4A7dA1Cf03626c024e


关键函数使用步骤

1.isApprovedForAll，在LD创建活动时，用户检测当前选择的NFT是否已经授权给LD，伪代码:loadContarct(NFT合约地址).isApprovedForAll('用户地址',’LD合约地址‘)

2.setApprovalForAll，将当前用户的NFT转移权限委托给LD,伪代码:loadContarct(NFT合约地址).setApprovalForAll('LD合约地址',true)

3.balanceOf,查询WETH余额，loadContarct(WETH合约地址).balanceOf('用户地址')；

4.approve，授权LD合约地址可以转移参与活动的费用比如，500WETH,loadContarct(NFT合约地址).approve('LD合约地址','500')
