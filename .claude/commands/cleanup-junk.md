---
description: 清理垃圾信（已讀＋未讀，依寄件者黑名單，移到垃圾桶）
---

請清理收件匣的垃圾信，**已讀與未讀都處理**。

## 做法
1. 用 `search_threads` 搜尋（不要限定 `is:unread`，這樣已讀垃圾信也會被清）：

   `in:inbox from:(n.nejm.org OR info.nejm.org OR nejmtoc OR mail.medscape.org OR mailer.ueg.eu OR news5.thieme.de OR tasid.org.tw OR email.openai.com OR mail.consensus.app OR venice.ai OR elicit.com OR zencreator.pro OR splashtop.com OR news.manus.im OR scite.ai OR connect.readdle.com OR uber@uber.com OR emails.hertz.com OR pchome24h.com.tw OR pchome.com.tw OR books.com.tw OR hamibook.com.tw OR ecomm.lenovo.com OR e.cathaypacific.com OR gladocean.com OR wolftea.com OR customeremail.microsoftrewards.com OR plt-inc.com OR kaneka.co.jp OR mailgun.patreon.com OR em-s.dropbox.com OR msg.esunbank.com OR msg.tw.sc.com OR Priority@msg.tw.sc.com OR bostonscientificasiapacific.com OR apac-comms.jnj.com OR calendar-notification@google.com OR photos@onedrive.com OR forms-receipts-noreply@google.com OR googleplay-noreply@google.com OR googleplaypromo-noreply@google.com)`

2. 對每個結果用 `label_thread` 加上 `TRASH`（移到垃圾桶，30 天內可救回）。
3. 分頁處理直到沒有結果為止。
4. 回報這次清了幾封。

## 安全規則（務必遵守）
- **只刪上面黑名單寄件者的信。** 不在名單上的一律保留，寧可漏刪、不可誤刪。
- **絕不碰**以下白名單（即使看起來像廣告）：
  - 帳號安全：`accounts.google.com`、`google-noreply`
  - 銀行/金融：玉山帳單與帳務（`estatement`、`info.esunbank`、`email.esunbank`）、HSBC、兆豐、玉山證券、合庫 `tcb-bank`、渣打帳單 `tw-standardchartered`、`SCBTW.TW@sc.com`
  - 電信：`cht.com.tw`
  - 工作/研究/試驗：`vghtpe.gov.tw`、`cims.tw`、AstraZeneca、第一三共、MSD、`its.jnj.com`、`nycu.edu.tw`
  - 收據：`noreply@uber.com`、`apple.com`
  - 個人/本人帳號：`taipeidu2017@gmail.com`、`beclass.com`
- 若發現黑名單沒涵蓋的新垃圾來源，**先列給我看**，我同意後再把該寄件者加進黑名單。
