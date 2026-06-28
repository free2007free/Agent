# Gmail 垃圾信黑名單（篩選器用）

供 Gmail「篩選器」自動刪除使用（Google 24 小時執行，不依賴 Claude）。
與 `.claude/commands/cleanup-junk.md` 的清理名單同步。

## 一、可直接貼上的「寄件者」字串

Gmail → 設定 ⚙️ → 篩選器和封鎖的地址 → 建立新的篩選器 →「寄件者(From)」欄貼上：

```
msg.esunbank.com OR msg.tw.sc.com OR calendar-notification@google.com OR photos@onedrive.com OR forms-receipts-noreply@google.com OR googleplay-noreply@google.com OR googleplaypromo-noreply@google.com OR n.nejm.org OR info.nejm.org OR nejmtoc@n.nejm.org OR mail.medscape.org OR mailer.ueg.eu OR news5.thieme.de OR tasid.org.tw OR email.openai.com OR mail.consensus.app OR venice.ai OR elicit.com OR zencreator.pro OR splashtop.com OR news.manus.im OR scite.ai OR connect.readdle.com OR uber@uber.com OR emails.hertz.com OR pchome24h.com.tw OR pchome.com.tw OR books.com.tw OR hamibook.com.tw OR ecomm.lenovo.com OR e.cathaypacific.com OR gladocean.com OR wolftea.com OR customeremail.microsoftrewards.com OR plt-inc.com OR kaneka.co.jp OR mailgun.patreon.com OR em-s.dropbox.com OR bostonscientificasiapacific.com OR apac-comms.jnj.com
```

下一步 → 勾選「**刪除它**」+「**同時將篩選器套用到 N 個相符的會話群組**」（連已讀舊信一起清）→ 建立篩選器。

> 若一條太長，可拆成兩三條篩選器分批貼，效果相同。

## 二、黑名單分類（給人看的版本）

| 類別 | 寄件者 |
|------|------|
| 銀行/券商行銷 EDM | `msg.esunbank.com`(玉山行銷)、`msg.tw.sc.com`(渣打行銷) |
| Google/系統通知 | `calendar-notification@google.com`、`forms-receipts-noreply@google.com`、`googleplay-noreply@google.com`、`googleplaypromo-noreply@google.com` |
| 雲端/檔案通知 | `photos@onedrive.com`、`em-s.dropbox.com` |
| 醫學電子報 | `n.nejm.org`、`info.nejm.org`、`nejmtoc@n.nejm.org`、`mail.medscape.org`、`mailer.ueg.eu`(UEG)、`news5.thieme.de`(Endoscopy)、`tasid.org.tw` |
| AI/軟體推銷 | `email.openai.com`、`mail.consensus.app`、`venice.ai`、`elicit.com`、`zencreator.pro`、`splashtop.com`、`news.manus.im`、`scite.ai`、`connect.readdle.com` |
| 購物/旅遊/3C 促銷 | `uber@uber.com`、`emails.hertz.com`、`pchome24h.com.tw`、`pchome.com.tw`、`books.com.tw`、`hamibook.com.tw`、`ecomm.lenovo.com`、`e.cathaypacific.com`、`gladocean.com`(TCL)、`wolftea.com`、`customeremail.microsoftrewards.com`、`plt-inc.com`、`kaneka.co.jp`、`mailgun.patreon.com` |
| 醫材/藥廠行銷 | `bostonscientificasiapacific.com`、`apac-comms.jnj.com` |

## 三、白名單（絕不刪，請勿放進篩選器）

- **帳號安全**：`accounts.google.com`、`google-noreply@google.com`
- **銀行/金融（交易/帳單）**：`estatement@esunbank.com`、`info.esunbank.com`、`email.esunbank.com.tw`、HSBC `hsbc.com.tw`、兆豐 `megabank.com.tw`、玉山證券 `esunsec.com.tw`、合庫 `tcb-bank.com.tw`、渣打帳單 `tw-standardchartered.com.tw`、`SCBTW.TW@sc.com`
- **電信帳單**：`cht.com.tw`
- **工作/研究/試驗**：`vghtpe.gov.tw`、`cims.tw`(IRB/PTMS)、`astrazeneca.com`、`daiichisankyo.com`、`msd.com`、`iqvia.com`、`its.jnj.com`、`nycu.edu.tw`
- **收據**：`noreply@uber.com`、`apple.com`
- **個人/本人帳號**：`taipeidu2017@gmail.com`、`beclass.com`(報名)

> ⚠️ 注意同一機構可能同時在黑/白名單：例如玉山的 `msg.esunbank.com`(行銷=刪) vs `estatement@esunbank.com`(帳單=留)；渣打的 `msg.tw.sc.com`(行銷=刪) vs `tw-standardchartered.com.tw`(帳單=留)。設篩選器時務必用上面**精確的子網域/地址**，不要只寫 `esunbank.com` 或 `sc.com`。
