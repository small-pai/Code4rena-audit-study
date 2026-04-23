# Brix Money - C4 Audit Study

日期：2026-04-29

## 核心漏洞（Medium）
1. **跨链权限绕过**
   Composer 未校验受限角色，黑名单用户可跨链质押。

2. **LayerZero 除尘导致交易失败**
   minAmountLD 未处理精度截断，导致 69% 交易回退。

## 学习要点
- 跨链系统必须全链路校验角色权限
- LayerZero OFT 必须处理 dust removal
