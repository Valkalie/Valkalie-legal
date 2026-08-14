# 🛡️ Valkalie Bot — Legal Documents

> นโยบายความเป็นส่วนตัว และ ข้อกำหนดการให้บริการ สำหรับ **Valkalie Discord Bot**
> Privacy Policy & Terms of Service for the **Valkalie Discord Bot**

---

## 📋 สารบัญ / Table of Contents

- [🇹🇭 ภาษาไทย](#-ภาษาไทย)
  - [นโยบายความเป็นส่วนตัว](#-นโยบายความเป็นส่วนตัว-privacy-policy)
  - [ข้อกำหนดการให้บริการ](#-ข้อกำหนดการให้บริการ-terms-of-service)
- [🇬🇧 English](#-english)
  - [Privacy Policy](#privacy-policy)
  - [Terms of Service](#terms-of-service)
- [📬 ติดต่อเรา / Contact](#-ติดต่อเรา--contact)

---

# 🇹🇭 ภาษาไทย

## 🔒 นโยบายความเป็นส่วนตัว (Privacy Policy)

**มีผลบังคับใช้ตั้งแต่:** 21 มิถุนายน 2569

### 1. ข้อมูลที่เราเก็บรวบรวม

Valkalie Bot เก็บข้อมูลเฉพาะที่จำเป็นต่อการทำงานของฟีเจอร์ต่างๆ ดังนี้

#### ข้อมูลของเซิร์ฟเวอร์ (Guild Data)
| ข้อมูล | วัตถุประสงค์ |
|--------|-------------|
| Guild ID / Channel ID / Role ID | ระบุเซิร์ฟเวอร์/ช่อง/ยศ สำหรับบันทึกการตั้งค่าและระบบ XP role |
| การตั้งค่า Welcome/Leave | แสดงข้อความต้อนรับ/อำลาสมาชิก |
| การตั้งค่า Report | กำหนดช่องรับ Report และ Admin Panel |
| การตั้งค่า Notify (YouTube/Twitch) | แจ้งเตือนเมื่อช่องที่ติดตามไลฟ์ |
| การตั้งค่า ServerStats | ตัวนับสมาชิก/บอท/ออนไลน์ในห้องเสียง |
| Embed ที่สร้างไว้ | บันทึก Embed ที่ Admin สร้างผ่าน Embed Builder |

#### ข้อมูลของผู้ใช้ (User Data)
| ข้อมูล | วัตถุประสงค์ |
|--------|-------------|
| User ID | ระบุผู้ใช้สำหรับสถิติ, XP และ Report |
| สถิติการใช้งาน | จำนวนข้อความและเวลา (ไม่เก็บเนื้อหา), เวลาในห้องเสียง, อีโมจิที่ใช้, เกมที่เล่น (ผ่าน Presence) |
| ข้อมูล XP/Level | ระบบเลเวลและยศรางวัล |
| ข้อมูล Report | เหตุผล/หลักฐานที่ผู้ใช้ส่งผ่านระบบ Report |
| Premium / Coin | สถานะสมาชิก Premium, ยอด Coin, ประวัติธุรกรรม (จำนวนเงิน, เวลา, เลขอ้างอิง) |

### 🔑 สิทธิ์การเข้าถึงระดับสูงที่เราขอจาก Discord (Privileged Intents)

Valkalie Bot ขอสิทธิ์การเข้าถึงระดับสูง (Privileged Gateway Intents) จาก Discord ดังนี้ เพื่อให้ฟีเจอร์บางส่วนทำงานได้:

| Intent | ใช้ทำอะไร |
|--------|-----------|
| **Server Members Intent** | รับรู้เมื่อมีสมาชิกเข้า/ออกเซิร์ฟเวอร์ เพื่อส่งข้อความต้อนรับอัตโนมัติ (Welcome), ตรวจจับการโจมตีแบบ bot-farm (สัดส่วนบอทต่อสมาชิกจริง) และเก็บสถิติสมาชิกเข้า-ออก |
| **Presence Intent** | ดูสถานะเกม/กิจกรรมที่สมาชิกกำลังเล่น เพื่อแสดงในสถิติกิจกรรม (Game Activity) ของระบบ /stats |
| **Message Content Intent** | ใช้เฉพาะเพื่ออ่านคำสั่ง prefix (`!`) ที่จำกัดสิทธิ์เฉพาะเจ้าของบอทเท่านั้น (owner-only) สำหรับดูแลระบบ เช่น `!reload`, `!status` — **ไม่อ่าน ไม่บันทึก และไม่ประมวลผล** ข้อความของผู้ใช้ทั่วไปแต่อย่างใด |

#### ข้อมูลที่ **ไม่ได้** เก็บ
- ❌ เนื้อหาข้อความ (Message Content) — ไม่บันทึกถาวร
- ❌ รหัสผ่าน
- ❌ ที่อยู่ IP ของผู้ใช้
- ❌ รูปสลิปโอนเงิน — ส่งให้ผู้ตรวจสอบ (SlipOK) เพื่อยืนยันเท่านั้น ไม่เก็บไว้

---

### 2. วิธีที่เราใช้ข้อมูล
- ให้บริการฟีเจอร์ต่างๆ (Welcome/Leave, Report, Stats, XP, Embed, Notify, TTS, Premium)
- แสดงสถิติเซิร์ฟเวอร์และผู้ใช้ผ่าน Stats Card
- ประมวลผลการเติมเงิน/สมัคร Premium
- เก็บ Log การทำงานชั่วคราวเพื่อแก้ปัญหา (สูงสุด 200 รายการ ไม่ถาวร)

---

### 3. บริการของบุคคลที่สาม (Third-Party Services)
- **SlipOK** — บริการยืนยันสลิปโอนเงินของไทย ([slipok.com](https://slipok.com)) เมื่อผู้ใช้เติมเงิน รูปสลิปจะถูกส่งไปยัง SlipOK เพื่อตรวจสอบการโอนเท่านั้น (เราไม่เก็บรูปสลิป) ทาง SlipOK ระบุว่าไม่มีนโยบายส่งต่อข้อมูลผู้ใช้ให้บุคคลที่ไม่เกี่ยวข้อง หรือนำไปใช้โดยไม่ได้รับความยินยอม
- **YouTube & Twitch API** — สำหรับระบบแจ้งเตือนไลฟ์ (ใช้เฉพาะข้อมูลช่อง)
- **Google Text-to-Speech (gTTS)** — ข้อความที่ใช้ฟีเจอร์ TTS จะถูกส่งไปยัง Google
- เราไม่ขายหรือแบ่งปันข้อมูลให้บุคคลภายนอกอื่น ยกเว้นได้รับความยินยอมโดยชัดแจ้ง หรือกฎหมายกำหนด

---

### 4. การจัดเก็บและความปลอดภัย
- ข้อมูลจัดเก็บใน PostgreSQL, SQLite และไฟล์ JSON บนเซิร์ฟเวอร์ที่ควบคุมโดย Developer
- ข้อมูลทั้งหมดถูกเข้ารหัสขณะพัก (encryption at rest) ด้วยการเข้ารหัสทั้งดิสก์ (AES)
- ข้อมูลลับ (credentials) เก็บใน environment variables ไม่อยู่ในโค้ด และจำกัดสิทธิ์เข้าถึงเฉพาะผู้ดูแลบอท
- อย่างไรก็ตาม ไม่มีระบบใดปลอดภัย 100% เราไม่สามารถรับประกันความปลอดภัยสมบูรณ์แบบได้

---

### 5. ระยะเวลาเก็บข้อมูล
- สถิติการใช้งานถูกลบอัตโนมัติหลังครบ 90 วัน
- ข้อมูลอื่นเก็บไว้จนกว่าบอทจะถูกนำออกจากเซิร์ฟเวอร์ หรือผู้ใช้ขอลบ

---

### 6. สิทธิ์ของผู้ใช้
คุณมีสิทธิ์:
- **ขอดู** ข้อมูลที่เราเก็บเกี่ยวกับคุณ/เซิร์ฟเวอร์
- **ขอลบ** ข้อมูลของคุณออกจากระบบ
- **ลบบอทออกจากเซิร์ฟเวอร์** ได้ทุกเมื่อ — หยุดการเก็บข้อมูลของเซิร์ฟเวอร์นั้น

ติดต่อผ่านช่องทางด้านล่างเพื่อใช้สิทธิ์ดังกล่าว

---

### 7. การเปลี่ยนแปลงนโยบาย
เราอาจอัปเดตนโยบายนี้เป็นครั้งคราว การใช้งานบอทอย่างต่อเนื่องหลังการเปลี่ยนแปลง ถือว่าคุณยอมรับนโยบายที่อัปเดตแล้ว

---

## 📜 ข้อกำหนดการให้บริการ (Terms of Service)

**มีผลบังคับใช้ตั้งแต่:** 21 มิถุนายน 2569

### 1. การยอมรับข้อกำหนด
การเชิญหรือใช้งาน Valkalie Bot ในเซิร์ฟเวอร์ Discord ของคุณ ถือว่าคุณและผู้ดูแลเซิร์ฟเวอร์ยอมรับข้อกำหนดเหล่านี้

### 2. คุณสมบัติของผู้ใช้
- ต้องมีอายุไม่ต่ำกว่า 13 ปี ตาม [Discord Terms of Service](https://discord.com/terms)
- ต้องมีสิทธิ์ตามกฎหมายในการใช้ Discord และบริการที่เกี่ยวข้อง

### 3. การใช้งานที่อนุญาต
Valkalie Bot มีไว้สำหรับเซิร์ฟเวอร์ Discord ที่ถูกกฎหมาย เพื่อ:
- ระบบ XP/Level, Welcome/Leave, Report, ServerStats/Stats
- Embed Builder, Notify (YouTube/Twitch), Text-to-Speech, Support, Premium

### 4. สิ่งที่ห้ามกระทำ
คุณตกลงว่าจะ **ไม่**:
- ใช้บอทเพื่อสแปม, คุกคาม, หรือล่วงละเมิดผู้อื่น
- พยายาม Exploit, Hack, หรือทำให้บอททำงานผิดปกติ
- กระทำสิ่งที่ขัดต่อ [Discord Community Guidelines](https://discord.com/guidelines) หรือกฎหมาย
- ใช้ระบบ Report เพื่อแจ้งเท็จหรือกลั่นแกล้งผู้อื่น
- ชำระเงินหรือโอนสลิปโดยทุจริต

### 5. การชำระเงิน
การซื้อ Premium/Coin ชำระผ่านการโอนเงินที่ยืนยันด้วย SlipOK สินค้าดิจิทัลโดยทั่วไปไม่สามารถขอคืนเงินได้ ยกเว้นที่กฎหมายกำหนด

### 6. ความพร้อมใช้งานของบริการ
- ไม่รับประกันว่าบอทจะพร้อมใช้งานตลอด 24/7
- อาจหยุดให้บริการชั่วคราว/ถาวร หรือเปลี่ยนแปลงฟีเจอร์โดยไม่ต้องแจ้งล่วงหน้า

### 7. การระงับการใช้งาน
เราสงวนสิทธิ์ในการ **Blacklist เซิร์ฟเวอร์หรือผู้ใช้** หากพบการละเมิดข้อกำหนด หรือพฤติกรรมที่เป็นอันตรายต่อผู้อื่น

### 8. ข้อจำกัดความรับผิด
Valkalie Bot ให้บริการ **"ตามสภาพที่เป็น" (As-Is)** Developer ไม่รับผิดชอบต่อความเสียหายหรือข้อมูลสูญหายอันเกิดจากการใช้งานบอท

### 9. ทรัพย์สินทางปัญญา
โค้ด, ชื่อ และโลโก้ของ Valkalie Bot เป็นทรัพย์สินของ Developer ห้ามคัดลอก แก้ไข หรือนำไปใช้โดยไม่ได้รับอนุญาตเป็นลายลักษณ์อักษร

### 10. การเปลี่ยนแปลงข้อกำหนด
เราอาจแก้ไขข้อกำหนดได้ตลอดเวลา การใช้งานต่อเนื่องถือว่ายอมรับข้อกำหนดที่อัปเดตแล้ว

---

# 🇬🇧 English

## Privacy Policy

**Effective:** June 21, 2026

### 1. Data We Collect
- **Discord identifiers:** user IDs, server (guild) IDs, channel IDs, role IDs
- **Configuration:** welcome/leave, report, notification (YouTube/Twitch), embed, and server-stats settings
- **Activity statistics:** message counts and timestamps (NOT message content), voice-session durations, emojis used, games played (via Presence), XP/level data
- **Reports:** report submissions created by users
- **Premium & payments:** premium subscription status, coin balances, and transaction records (amount, timestamp, reference ID)
### 🔑 Privileged Discord Intents We Request

Valkalie Bot requests the following privileged Gateway Intents from Discord to power specific features:

| Intent | Purpose |
|--------|---------|
| **Server Members Intent** | Detect member joins/leaves to send automated welcome messages, detect bot-farm attacks (bot-to-human member ratio), and track join/leave statistics |
| **Presence Intent** | View members' current game/activity status to power the Game Activity stat shown in `/stats` |
| **Message Content Intent** | Used only to read owner-restricted prefix commands (e.g. `!reload`, `!status`) for bot administration. We do **not** read, log, or process the content of regular users' messages |

### 2. Data We Do NOT Store
- Message content
- Passwords
- Discord users' IP addresses
- Bank-transfer slip images (sent to our payment verifier for validation and not retained)

### 3. How We Use Data
- To operate bot features (welcome/leave, report, stats, XP, embed, notify, TTS, premium)
- To display server and user statistics via Stats Cards
- To process top-ups and premium subscriptions
- To keep temporary logs for troubleshooting (up to 200 entries, not persisted)

### 4. Third-Party Services
- **SlipOK** — a Thai bank-transfer slip verification service ([slipok.com](https://slipok.com)). When a user tops up, the uploaded slip is sent to SlipOK solely to verify the transfer; we do not retain the slip image. SlipOK states that it does not forward user data to unrelated parties or use it without consent.
- **YouTube & Twitch APIs** — used for live-stream notifications (channel data only)
- **Google Text-to-Speech (gTTS)** — text for the TTS feature is sent to Google
- We do not sell user data or share it otherwise, except with explicit consent or where legally required.

### 5. Storage & Security
- Data is stored in PostgreSQL, SQLite, and JSON files on developer-controlled infrastructure.
- All stored data is encrypted at rest using full-disk encryption (AES).
- Credentials are kept in environment variables, never in source code, and database access is restricted to the bot operator.
- No system is 100% secure; we cannot guarantee absolute security.

### 6. Data Retention
- Activity statistics are automatically deleted after 90 days.
- Other data is kept until the bot is removed from the server or deletion is requested.

### 7. Your Rights
- Request access to or deletion of your data via our support server.
- Removing the bot from a server stops data collection for that server.

### 8. Changes
We may update this policy from time to time. Continued use after changes constitutes acceptance of the updated policy.

---

## Terms of Service

**Effective:** June 21, 2026

**1. Acceptance** — Inviting or using Valkalie in your Discord server means you and the server's administrators accept these terms.

**2. Eligibility** — Minimum age 13, and you must comply with Discord's Terms of Service.

**3. Permitted Uses** — Leveling/XP, welcome/leave, report, server statistics, embed builder, live-stream notifications, text-to-speech, support tickets, and premium features.

**4. Prohibited Actions**
- Spam, harassment, or abuse
- Attempting to exploit, hack, or disrupt the bot
- Violating Discord's Community Guidelines or applicable law
- Submitting false reports or fraudulent payments

**5. Payments** — Premium and coin purchases are processed via bank transfer verified by SlipOK. Digital goods are generally non-refundable except as required by law.

**6. Service Availability** — Provided "as-is" with no uptime guarantee; features may change or be discontinued without notice.

**7. Suspension** — We reserve the right to blacklist any server or user that violates these terms or harms others.

**8. Liability** — The developer is not liable for damages or data loss arising from use of the bot.

**9. Intellectual Property** — The code, name, and logo are protected and may not be reproduced or used without written permission.

**10. Changes** — We may revise these terms at any time. Continued use constitutes acceptance.

---

## 📬 ติดต่อเรา / Contact

หากมีคำถาม ข้อสงสัย หรือต้องการใช้สิทธิ์ด้านข้อมูล กรุณาติดต่อ /
For questions or to exercise your data rights, contact:

- **Discord:** hoyorai
- **Support Server:** https://discord.gg/GXPgH3AZCe
- **GitHub Issues:** [github.com/Valkalie/Valkalie-legal/issues](https://github.com/Valkalie/Valkalie-legal/issues)

---

<div align="center">

**Valkalie Bot** · อัปเดตล่าสุด / Last updated: 21 มิถุนายน 2569 (June 21, 2026)

</div>
