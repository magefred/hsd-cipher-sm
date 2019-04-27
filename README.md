# HSD-CIPHER-SM 
Chinese Cipher Algorithm


## 国密算法介绍

国密即国家密码局认定的国产密码算法，即商用密码。主要有SM1，SM2，SM3，SM4。密钥长度和分组长度均为128位。

* SM1 为对称加密。其加密强度与AES相当。该算法不公开，调用该算法时，需要通过加密芯片的接口进行调用。
* SM2为非对称加密，基于ECC。该算法已公开。由于该算法基于ECC，故其签名速度与秘钥生成速度都快于RSA。ECC 256位（SM2采用的就是ECC 256位的一种）安全强度比RSA 2048位高，但运算速度快于RSA。
* SM3 消息摘要。可以用MD5作为对比理解。该算法已公开。校验结果为256位。
* SM4 无线局域网标准的分组数据算法。对称加密，密钥长度和分组长度均为128位。
 
由于SM1、SM4加解密的分组大小为128bit，故对消息进行加解密时，若消息长度过长，需要进行分组，要消息长度不足，则要进行填充。

作为密码学算法，一定要公开接受行业的检验。

* 1. 对称算法：                  （DES 3DES AES） --迁移-->   SM1 SM4

* 2. 非对称密码算法：             (RSA) --迁移-->   SM2(椭圆曲线密码)

* 3. 散列算法：                   (HASH MD4、MD5 SHA-1、SHA-256、SHA-384、SHA512) --迁移-->   SM3


## 国密算法的面临的机遇和挑战

### 1、推广情况说明

     国家在金融领域启动国产密码算法试点工作以来，国家发改委启动了金融领域安全IC卡及密码关键产品专项支持工作，积极推动产业链发展。目前支持国密算法的软硬件密码产品共699项，包括SSL网关、数字证书认证系统、密钥管理系统、金融数据加密机、签名验签服务器、智能密码钥匙、智能IC卡、PCI密码卡等多种类型，目前已初步形成形式多样、功能互补的产品链，并保持着持续增长的势头。

### 2、数字认证系统（CA）的升级改造情况

      2015年2月国家商业密码管理办公室发布公告称：根据要求全国第三方电子认证服务机构针对电子认证服务系统和密钥管理系统公钥算法进行了升级改造完毕已经全面支持国产算法，同时各认证服务机构正在积极推动国产算法的应用服务改造，淘汰有安全风险以及低强度的密码算法和产品。北京天威诚信作为最早成立的第三方电子认证服务机构也最早按照国密的要求完成了电子认证服务系统的升级改造，并且同步开始对服务类型的证书应用进行升级改造，目前已经累计完成150余个企业的应用升级工作，使得企业信息系统的安全性得到了极大的提升，也为我们带来了相应的经济效益。

### 3、挑战和机遇

      虽然在SSL VPN、数字证书认证系统、密钥管理系统、金融数据加密机、签名验签服务器、智能密码钥匙、智能IC卡、PCI密码卡等产品上改造完毕，但是目前的信息系统整体架构中还有操作系统、数据库、中间件、浏览器、网络设备、负载均衡设备、芯片等软硬件，由于复杂的原因无法完全把密码模块升级为国产密码模块，导致整个信息系统还存在安全薄弱环节。

      作为电子认证机构这个国产密码算法排头兵来说，由于密码服务是信息化安全建设的基础服务，密码的国产化改造和推广就成为我们重要的历史使命。为了普及和推广国产密码我们可以：一方面是产品升级改造，对于国外的产品，通过国产算法的标准出海战略，让国产算法成为国际标准从而国外的产品也就能够支持；对于国产的产品，加快国产算法模块的改造和应用，真正让国产算法为信息系统的安全自主可控；另一方面是应用的宣传和推广，国产算法虽然在安全圈里面是众所周知的事情，但是在其它领域根本就没有听说。所以对于从业者来说，就要不断对用户灌输使用国产密码算法以及尽快升级到国产算法的思想。只有从以上这两个方面入手并且持之以恒，相信国家提出的信息安全领域的自主可控战略最终就会实现。


