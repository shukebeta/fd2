# 公式

遊戲所使用的公式（小數點以下均去除）：

物理攻擊傷害計算順序：

```
AP = 攻方AP
DP = 守方DP
暴擊時，DP = 守方DP/2，取整數
AP = AP * (1 + 攻方地形 AP 修正率) ，取整數
DP = DP * (1 + 守方地形 DP 修正率) ，取整數
最大傷害 = AP - DP
實際傷害 = 最大傷害 * 0.9 ～ 最大傷害 - 1
物理攻擊命中率 = (攻方 HIT - 守方 EV)%
```

劍技攻擊傷害計算順序：

```
AP = 攻方 AP * 劍技加乘率，取整數
DP = 守方 DP
最大傷害 = AP - DP
實際傷害 = 最大傷害 * 0.9 ～ 最大傷害 - 1
```

法術攻擊傷害計算順序：

```
最大傷害 = 法術最大傷害 * (1 - 守方魔法抗性)
實際傷害 = 最大傷害 * 0.9 ～ 最大傷害 - 1
法術攻擊命中率 = 法術內定命中率
```

* `攻擊經驗值 = (傷害HP/總HP) * (守方等級*守方每級經驗) * (守方等級/攻方等級)` ，攻擊導致死亡視同 `傷害HP=總HP`
* `法術恢復力 = 最大恢復 * 0.9 ～ 最大恢復 - 1`
* `恢復法術經驗值 = (40 / 施法者等級) * Σ(恢復HP / 總HP) * 受法者等級`
* `傳送術經驗值 = 10 * (受法者等級/施法者等級)`
* `行動術經驗值 = 8 * (受法者等級/施法者等級)`
* `魔刃術／魔鎧術／風行術經驗值 = 2 * Σ(受法者等級/施法者等級)`
* `麻痹術／毒擊術經驗值 = Σ (40 * 9/受法者總HP) * (受法者等級/施法者等級)`
* `解毒術／祛麻術經驗值 = Σ (40 * 9/受法者總HP) * (受法者等級/施法者等級)`
