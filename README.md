# -_-_-
#personal notes
高保障密码学：极其严苛的数学/工程证明安全性                                                      #ML-DSA/ML-KEM:格密码的数字签名算法(身份验证，NIST标准)
verification theatre                                                                          &格密码密钥封装机制。
Verification Boundary:分离machine-checked proofs code和 trusted without proof code 的接口       CRYSTALS-Kyber: Key encapsulation (KEM)
• CRYSTALS-Dilithium: Digital signatures
• FALCON: Digital signatures
• SPHINCS+: Hash-based signatures
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
 McEliece cryptosystem:Public key: (𝐺, 𝑡). 𝐺=S*G'*P looks like the
generator matrixG' of a random code.
Private key: (𝑆, 𝐺′, 𝑃)可逆
Why it can work: Anyone can encode
with 𝐺 and sprinkle in 𝑡 errors; only
someone who knows the hidden
structure can remove them again
伪造签名：哈希链（K->H(K)->...H^w(K))私钥K,公钥H^w(k),sign m==发送H^m(K),收到H^m(K),(w-m)次后验证=H^w(K)? Generalattack: From signature of 𝑀, can forge any 𝑀′ > 𝑀
• Fix: Sign both 𝑀 and 𝑤 − 𝑀 using two keys
• Signature: (Hash𝑀 (𝐾1), Hash𝑤−𝑀 (𝐾2))
• Now increasing 𝑀 requires decreasing 𝑤 − 𝑀
