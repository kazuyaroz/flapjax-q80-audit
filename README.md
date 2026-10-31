# FlapJax Treasury Audit — Q80 (10-29 COT)

**Auditor:** kazuyaroz  
**BSC Wallet:** 0x9b2a56b912659a24db94473526d2c67814a117Ac  
**Date:** 2026-10-31

## Method

- Block range: eth_getBlockByNumber binary search for 2026-10-29 00:00:00 COT (UTC-5) to 2026-10-30 00:00:00 COT
- First block: 130,413,458 (2026-10-29 05:00:00 UTC)
- Last block: 130,605,332 (2026-10-30 04:59:59 UTC)
- Transfers: eth_getLogs on FLAPJAX (0x90c8889f428F9Ebb77BB8f15CAD3a50a9aC680df), topic0=Transfer, topic1=treasury
- Treasury: 0x7C34E9e21eE28A49Ff0b84B61774119E6633359f
- RPC: rpc-bsc.48.club (public BSC node)
- Funder analysis: eth_getTransactionCount (nonce), eth_getCode (contract check), eth_getBalance at first FLAPJAX receipt block

## All 18 Treasury Outflows

| # | Block | Time (COT) | Recipient | Amount (FLAPJAX) | Tx Hash |
|---|-------|-----------|-----------|-------------------|---------|
| 1 | 130482214 | 2026-10-29 08:36:23 COT | 0x97cd18b8bbb629b17675d868259ea84c0a2a5a9c | 300,000 | 0x44a580d841831667955ea9e7bfcb75521ccc51c5b2ffc7299ef70bbb50fa78d5 |
| 2 | 130482223 | 2026-10-29 08:36:27 COT | 0xabc2c3daffa4c1963299da225c25f2aa7d4ddf62 | 25,000 | 0x6895a4d32f4367704230435d86202b048a06c2f9d3c452fc21419ca1e5a2dac5 |
| 3 | 130482233 | 2026-10-29 08:36:31 COT | 0xfb200657f7266157a45dfcc6c09690726daa24e6 | 25,000 | 0xce38980fb1f4add7ab7dc6cf739001ded5bfac0d80756e915a4ba48d0d40b292 |
| 4 | 130482242 | 2026-10-29 08:36:35 COT | 0xd16446a568f46bca1504422062f23767d8fa58d9 | 25,000 | 0x30a82d0d9c77d6dac96e6595cd4557845cd8695fb099d93fb54b5982e221ca02 |
| 5 | 130482252 | 2026-10-29 08:36:40 COT | 0x2ae18c3b2fc18545edd35beeaef97cc2ed908a02 | 25,000 | 0x58e92d0c8afedb71ca5b98e0810dc1856f1406e81b7fbe0f8bbab6c6ed8174b6 |
| 6 | 130482263 | 2026-10-29 08:36:45 COT | 0x97cd18b8bbb629b17675d868259ea84c0a2a5a9c | 25,000 | 0x81083d6b118a34358abdf3d1289ed469ca3af4871677043837d5d055c0e90e03 |
| 7 | 130482272 | 2026-10-29 08:36:49 COT | 0x2ae18c3b2fc18545edd35beeaef97cc2ed908a02 | 300,000 | 0x9e9358acf04da74162ba29333e988fe6f323256d9287c37d2ea06e8bbcfa2dd3 |
| 8 | 130482291 | 2026-10-29 08:36:57 COT | 0x32cf8fffd9ada47abd09a7b2269dd4835ee994f7 | 250,000 | 0x18324f74d9afbe0a7517cfc7c1c342f386817c71202bad7fa294ef05f83743e1 |
| 9 | 130488437 | 2026-10-29 09:23:03 COT | 0xa32fd912a81683804ec6bbd7ba4b6cad8e0ca3ac | 250,000 | 0x875c2ef38cdd206ebd49735f5cfd5755bcd5fc85cb60c78e073153953cd60550 |
| 10 | 130489446 | 2026-10-29 09:30:37 COT | 0xcf06c2f35e7671cbb1fcae42b50a447db189f1da | 100,000 | 0xc1eac754961dc07ecc103c831197f039b23588924ff0d56efccdb1ece523b11e |
| 11 | 130496859 | 2026-10-29 10:26:15 COT | 0xfdf05af8ddce3621f01713e01721d6e9ad702ea8 | 25,000 | 0x15e20669d88b516a43a8fafffbf2f6579ea43f15af1139e48550bef16569be46 |
| 12 | 130496868 | 2026-10-29 10:26:20 COT | 0xfdf05af8ddce3621f01713e01721d6e9ad702ea8 | 300,000 | 0x3ee7dff7623561a6ee06f3a599ef6025a44c28fd85855398e6acfc25565968b2 |
| 13 | 130496877 | 2026-10-29 10:26:24 COT | 0xd16446a568f46bca1504422062f23767d8fa58d9 | 300,000 | 0xf066f28c0de3964e4dc06e2481a468c53fd221f962905b922078d9efae154cbd |
| 14 | 130513085 | 2026-10-29 12:27:59 COT | 0xab39aa1e2db4036e01cf7e919b3f239b3ff90160 | 3,000,000 | 0x664cfae4cd1553557c05a31c5e3fbc662afb2472f3d93df461f9b4f6f0bc7bc4 |
| 15 | 130513134 | 2026-10-29 12:28:21 COT | 0xdf4ff9d2f45f99f11a90b16f277d4b7edddb72a5 | 120,000 | 0x814720410be30518ea1947c13b283b4dbe408a35c82f05f89fe00b07a4d14d1a |
| 16 | 130530103 | 2026-10-29 14:35:38 COT | 0x0a66a9def221efc698b6bbeca82cae6729a8aba8 | 600,000 | 0xfb6c7f0f5edf392be0b71da8561c01b2ef111b82e40d628b2d2b7173417efb85 |
| 17 | 130553103 | 2026-10-29 17:28:10 COT | 0x0a66a9def221efc698b6bbeca82cae6729a8aba8 | 25,000 | 0x1ff5c6086cc2f3960c0e1460f0482e5af5f9c059d091bfcd1f2ac888c88401b1 |
| 18 | 130600976 | 2026-10-29 23:27:19 COT | 0xe8797a6bb4693674d78e933e85cb159a0219d03b | 25,000 | 0x4c9170b0bab813ff1d43e8d200a3df72eb661a6446959a8485746ba2688d62bf |

**Total sent:** 5,720,000 FLAPJAX  
**Distinct recipients:** 13

## First BNB Funder Analysis

### Recipient Profile

| Recipient | Type | Nonce | BNB at first FLAPJAX | BNB now |
|-----------|------|-------|---------------------|---------|
| 0x0a66a9def221efc698b6bbeca82cae6729a8aba8 | EOA | 0 | 0.000000 | 0.000000 |
| 0x2ae18c3b2fc18545edd35beeaef97cc2ed908a02 | EOA | 0 | 0.000000 | 0.000006 |
| 0x32cf8fffd9ada47abd09a7b2269dd4835ee994f7 | EOA | 0 | 0.000000 | 0.000000 |
| 0x97cd18b8bbb629b17675d868259ea84c0a2a5a9c | EOA | 0 | 0.000000 | 0.000000 |
| 0xa32fd912a81683804ec6bbd7ba4b6cad8e0ca3ac | EOA | 0 | 0.000000 | 0.000000 |
| 0xab39aa1e2db4036e01cf7e919b3f239b3ff90160 | Contract | N/A | 0.000000 | 0.000000 |
| 0xabc2c3daffa4c1963299da225c25f2aa7d4ddf62 | EOA | 0 | 0.000000 | 0.000000 |
| 0xcf06c2f35e7671cbb1fcae42b50a447db189f1da | EOA | 0 | 0.000000 | 0.000000 |
| 0xd16446a568f46bca1504422062f23767d8fa58d9 | EOA | 0 | 0.000000 | 0.000000 |
| 0xdf4ff9d2f45f99f11a90b16f277d4b7edddb72a5 | EOA | 0 | 0.000000 | 0.000000 |
| 0xe8797a6bb4693674d78e933e85cb159a0219d03b | EOA | 0 | 0.000000 | 0.000000 |
| 0xfb200657f7266157a45dfcc6c09690726daa24e6 | EOA | 0 | 0.000000 | 0.000500 |
| 0xfdf05af8ddce3621f01713e01721d6e9ad702ea8 | EOA | 0 | 0.000000 | 0.000000 |

### Findings

1. **12 of 13 recipients are EOAs with nonce = 0** — they have never sent a single transaction. They are pure receive-only wallets.

2. **1 of 13 recipients is a smart contract** (0xab39aa1e2db4036e01cf7e919b3f239b3ff90160) — received 3,000,000 FLAPJAX, the largest single transfer.

3. **0 of 13 recipients have ever sent a transaction** (nonce = 0 for all EOAs).

4. **All 13 recipients had 0 BNB at their first FLAPJAX receipt block.** No recipient held BNB before receiving FLAPJAX.

5. **2 recipients received BNB after the audit window** via internal transactions (no direct BNB transfer found in the block):
   - 0x2ae18c3b2fc18545edd35beeaef97cc2ed908a02: 0.00000626 BNB at block 130,832,944 (internal tx)
   - 0xfb200657f7266157a45dfcc6c09690726daa24e6: 0.0005 BNB at block 130,832,972 (internal tx)

### Operator Groups

Since all 13 recipients had 0 BNB at their first FLAPJAX receipt and none have ever sent a transaction, **no recipient can be linked to another via a shared first BNB funder.** Each recipient is an independent wallet by the funder method.

- **Distinct operators implied:** 13 (one per recipient address)
- **No sybil links found** by the first-BNB-funder method
- **Caveat:** The 12 never-funded EOAs could in principle belong to a single operator using fresh payout-only wallets. This method proves they have no BNB funding link, not that they have distinct owners.

### Transfers Not Explained

None. All 18 transfers are plain treasury-to-recipient FLAPJAX Transfer logs, verifiable via eth_getLogs on any public BSC node.

## Verification

Re-check any row:
```
eth_getLogs on FLAPJAX (0x90c8889f428F9Ebb77BB8f15CAD3a50a9aC680df)
  topic0 = 0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef
  topic1 = 0x0000000000000000000000007C34E9e21eE28A49Ff0b84B61774119E6633359f
  fromBlock = 0x7c7f402 (130413458)
  toBlock = 0x7ca6ce4 (130605332)
```
