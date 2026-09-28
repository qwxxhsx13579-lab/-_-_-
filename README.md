# -_-_-
#personal notes
高保障密码学：极其严苛的数学/工程证明安全性                                                      #ML-DSA/ML-KEM:格密码的数字签名算法(身份验证，NIST标准)
verification theatre                                                                          &格密码密钥封装机制。
Verification Boundary:分离machine-checked proofs code和 trusted without proof code 的接口
• Every formally verified system embeds1接口,tightly|loosely,always exists
• Outside the boundary: compilers, operating system, hardware, platform
intrinsics(平台内建), “glue code”
• Experts understand that the boundary is there. Users often do not
The question is whether a project tells you where its boundary runs                                     
 “formally verified” with no 限制条件:
• Users read it as a guarantee over the whole library
• The gap between the claim and the reality produces false assurance
• Call that gap verification theatre
Cryspen（高保障软件服务）'s libcrux:已形式化证明的密码库，ML-KEM google使用，hpke-rs被Signal和OpenMLS使用，顶尖被发现13漏洞。
cross-platform testing and fuzzing catch what formal verification does not
