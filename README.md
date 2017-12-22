# Blockchain
On learning blockchain

## 区块链技术

### 基础知识
#### 专有名词解释

[Blockchain](https://en.wikipedia.org/wiki/Blockchain):
>
A blockchain,originally block chain,is a continuously growing list of records, called blocks, which are linked and secured using cryptography. 
Each block typically contains a hash pointer as a link to a previous block, a timestamp and transaction data.--*from wikiPedia*

Decentralised(去中心化)：
>没有中介机构，所有节点的权利和义务都相等，任一节点停止工作都会不影响系统整体的运作。
>
--*出自花旗报告Digital Disruption: How FinTech is Forcing Banking to a Tipping Point*

[Distributed lendger(分布式账单)](https://en.wikipedia.org/wiki/Distributed_ledger)：
>A distributed ledger (also called a shared ledger, or referred to as distributed ledger technology) is a consensus of replicated, shared, and synchronized digital data geographically spread across multiple sites, countries, or institutions.There is no central administrator or centralised data storage.
>
>--*from wikiPedia*

Public chain：
>顾名思义，任何人都可以参与使用和维护，典型的如比特币区块链，信息是完全公开的。如果引入许可机制，包括私有链和联盟链两种。


Private chain：
>集中管理者进行限制，只能得到内部少数人可以使用，信息不公开。


Consortium blockchain联盟链：
>联盟链则介于两者之间，由若干组织一起合作维护一条区块链，该区块链的使用必须是有权限的管理，相关信息会得到保护，典型如银联组织。
--来自[区块链技术指南](https://yeasy.gitbooks.io/blockchain_guide/content/born/what.html)

拜占庭将军问题：
>在某些节点出现不可知故障的情况下（包括节点本身的恶意行为），节点需要对数据库的某个值取得共识。

女巫问题：
>是指在对某个值获取共识的过程中，一个或几个节点获得大于自己所应占比例的影响力。这是一种“复制攻击”，一些看似不相关的节点一起欺骗系统。


Zero-Knowledge Proof零知识证明：
[不是程序员也能看懂的ZCash零知识证明](http://www.sohu.com/a/121847942_475384)

Double Spending Attack（双花问题）:
[山中无老虎，怎么保证猴子不捣乱？区块链时刻](https://zhuanlan.zhihu.com/p/25692826)


吞吐量：
>比特币网络平均每秒处理一笔交易，理论上最多7笔交易。如果每个块更大的话，吞吐量也可以更大，但是扩大每个块会带来尺寸的问题（见下面的容量和网络带宽部分）。这种吞吐量很多系统相比的话低的不可以接受，比如Visa系统（通常2000个交易每秒，峰值可达10000个每秒）和Twitter（通常5000个交易每秒，峰值可达15000个每秒）和广告网络（通常500000个交易每秒）和传统网络，以及电子邮件网络（全球每天1830亿个邮件，每秒两百一十万个）。一个理想的全球区块链，或者区块链集合需要支持这种高吞吐量的应用场景。

延迟：
>处理每个比特币的区块链中的块需要10分钟。为了足够的安全性，最好等待1小时好让更多的节点确认这笔交易。相比较，Visa系统的交易最多需要几秒钟。很多金融应用都要求延迟在30-100毫秒之间。

数字签名：
>数字签名，就是只有信息的发送者才能产生的别人无法伪造的一段数字串，这段数字串同时也是对信息的发送者发送信息真实性的一个有效证明。一套数字签名通常定义两种互补的运算，一个用于签名，另一个用于验证。


#### 区块链数据结构

#### Merkle Tree

* [Merkle Tree学习](http://www.cnblogs.com/fengzhiwu/p/5524324.html)/
[merkle Tree](https://www.youtube.com/watch?v=Js535LqapFE#t=238) YouTube版

#### 密码学知识

Hash256

* [什么是安全散列算法SHA256？](http://8btc.com/article-136-1.html)

Elliptic curve：

* [什么是椭圆曲线加密（ECC）](http://8btc.com/article-138-1.html)
* [什么是椭圆曲线数字签名算法（ECDSA）](http://8btc.com/article-140-1.html)
* [Elliptic-curve digital signatures
in basic blockchain programming](http://davidederosa.com/basic-blockchain-programming/elliptic-curve-digital-signatures/)


#### 运作

* [让这篇技术贴告诉你区块链是怎么运行的](https://yq.aliyun.com/articles/60218?spm=5176.8067842.tagmain.89.vy6RKf)
* [比特币协议是怎样工作的（上）](http://www.8btc.com/bitcoin-contract)
* [比特币协议是怎样工作的（下）](http://www.8btc.com/bitcoin-contract2)




#### 共识机制

* [【区块链之技术进阶】掰一掰区块链共识机制与分布式一致性算法](https://yq.aliyun.com/articles/60400)
* PoW：一致性算法：POW。比特币的挖矿奖励机制刺激节点来增加计算资源的使用，但是对于吞吐量，延迟和容量没有任何帮助。一个节点发出的确认平均需要10分钟，所以6个确认要大约1小时。[工作量证明机制是怎样的？](http://8btc.com/article-160-1.html)
* PoS：[POS白皮书：基于权益证明的交易](http://www.8btc.com/pos-white-book)
* DPOS: [信息图：股份授权证明机制（DPOS）](http://www.8btc.com/dpossha)、[DPOS共识算法 -- 缺失的白皮书](https://steemit.com/dpos/@legendx/dpos)
* PBFT（Practical Byzantine Fault Tolerance）：[区块链核心技术：拜占庭共识算法之PBFT](http://www.jianshu.com/p/fb5edf031afd)
* [Raft动态演示](http://thesecretlivesofdata.com/raft/?spm=5176.100239.blogcont60400.8.7rQOfk)

### 区块链架构

* [Blockchain Infrastructure Landscape: A First Principles Framing](https://blog.bigchaindb.com/blockchain-infrastructure-landscape-a-first-principles-framing-92cc5549bafe)/[区块链底层架构概览：第一原则框架](http://ethfans.org/posts/blockchain-infrastructure-landscape-a-first-principles)
* [各区块链架构的横向比较](http://www.sohu.com/a/159487224_684500)
* [区块链架构及应用](http://www.360doc.com/content/17/0820/04/30836886_680524486.shtml)




## 区块链主流应用

### Bitcoin
**书籍**

* [Mastering Bitcoin](http://chimera.labs.oreilly.com/books/1234000001802/index.html)/[精通比特币](http://book.8btc.com/books/1/master_bitcoin/_book/)


### Ethereum
* [Ethereum White Paper](https://github.com/ethereum/wiki/wiki/White-Paper)/[以太坊白皮书](https://github.com/ethereum/wiki/wiki/%5B%E4%B8%AD%E6%96%87%5D-%E4%BB%A5%E5%A4%AA%E5%9D%8A%E7%99%BD%E7%9A%AE%E4%B9%A6)


### Smart Contract
* [Solidity Docs](https://solidity.readthedocs.io/en/latest/introduction-to-smart-contracts.html)
* [以太坊智能合约安全编程最佳实践Smart-Contract-Best-practices](https://github.com/ConsenSys/smart-contract-best-practices)
* [Thinking About Smart Contract Security](https://blog.ethereum.org/2016/06/19/thinking-smart-contract-security/)

## 区块链制度标准（暂无链接关联）
* [ROADMAP FOR BLOCKCHAIN STANDARDS]()
* [中国区块链技术和产业发展论坛标准 区块链 参考框架20170516]()
* [Evaluation Forms for Blockchain-Based System ver. 1.0]()



  
    
