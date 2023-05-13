# 第3课 课后作业

## 第1题 二次非剩余

prover想说服验证者 ：针对公共已知的`m`, `x`，$QR(m, x) = 0$。即不存在`s`，满足$s^2 = x (\mod m)$。

那么就是verifer选择一个数字`s`，并且给出`b = 0 or 1`。如果是0，$y = s^2 x$，如果是1，$y = s^2$。

由prover来根据计算QR(m, y)并返回给verifier。

如果 b = 0，必须是此时不存在s。

如果 b=1，此时应该是存在s。

因此可以根据概率来验证

## 第二题 二次剩余

prover在不提供s的情况下，让verifier证明 QR(m, x) = 0

1. prover 随机选择 t。并且发送 y = t^2 * x (mod m)。此时y = (st)^2 (mod m)
2. verifier随机提供b = 0 或者1。如果b = 0，发送u = t; 如果b = 1, 发送 u = st。
3. 此时 如果 b=0，y = u^2 * x (mod m)。如果 b = 1，y = u^2 (mod m)。





