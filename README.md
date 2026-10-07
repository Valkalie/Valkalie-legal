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

**มีผลบังคับใช้ตั้งแต่:** 7 ตุลาคม 2569

### 1. ข้อมูลที่เราเก็บรวบรวม

Valkalie Bot เก็บเฉพาะข้อมูลที่ฟีเจอร์ต่าง ๆ จำเป็นต้องใช้ ดังนี้

#### ข้อมูลของเซิร์ฟเวอร์ (Guild Data)
| ข้อมูล | วัตถุประสงค์ |
|--------|-------------|
| Guild ID / Channel ID / Role ID | ใช้บันทึกการตั้งค่าของแต่ละเซิร์ฟเวอร์ |
| การตั้งค่าฟีเจอร์ | Welcome/Leave, Forms, Embed, Sticky, Scheduler, Notify (YouTube/Twitch), ServerStats, XP, ร้านค้า XP และระบบความปลอดภัย |
| ServerStats | ตัวนับจำนวนสมาชิกทั้งหมด สมาชิก และบอท ที่แสดงเป็นชื่อห้องเสียง |
| สำเนาโครงสร้างเซิร์ฟเวอร์ | ชื่อ สิทธิ์ และตำแหน่งของห้องและยศ ใช้กู้คืนเซิร์ฟเวอร์เมื่อถูกโจมตี (raid/nuke) โดย**ไม่มีเนื้อหาข้อความ** |
| ผู้เชิญบอท | User ID ของผู้ที่เชิญบอทเข้าเซิร์ฟเวอร์ (ดึงจาก Audit Log) ใช้ป้องกันการใช้บอทในทางที่ผิด |

#### ข้อมูลของผู้ใช้ (User Data)
| ข้อมูล | วัตถุประสงค์ |
|--------|-------------|
| User ID / ชื่อที่แสดง | ระบุผู้ใช้ในสถิติ, XP, leaderboard, ฟอร์ม และรายชื่อผู้บริจาค |
| สถิติการใช้งาน | จำนวนข้อความ ห้อง และเวลาที่ส่ง (**ไม่เก็บเนื้อหา**), เวลาในห้องเสียง, อีโมจิที่ใช้, วันที่เข้าเซิร์ฟเวอร์ |
| กิจกรรมเกม (ผ่าน Presence) | ชื่อเกมที่เล่น และเวลาเริ่ม/จบ แสดงใน Stats Card และ leaderboard (ปิดได้ ดูข้อ 5) |
| XP / Level | XP, เลเวล, แต้ม, สกุลเงินที่เซิร์ฟเวอร์สร้างเอง, คำสั่งซื้อในร้านค้า XP, การตั้งค่าปิด DM แจ้งเลเวล |
| ฟอร์ม (Forms) | คำตอบที่ผู้ใช้ส่งผ่านฟอร์มที่แอดมินสร้าง เช่น Report หรือใบสมัคร (เห็นได้เฉพาะทีมงานของเซิร์ฟเวอร์นั้น) |
| ระบบความปลอดภัย | จำนวนครั้งที่ทำผิด (strike) และเวลาครั้งล่าสุด เมื่อถูกระบบกันสแปมหรือกันลิงก์อันตรายลงโทษ |
| มินิเกม | ผลแพ้/ชนะในเกมของบอท |
| Support Ticket | ข้อความที่ผู้ใช้เขียนเมื่อเปิด ticket ผ่าน `/valkalie_support` |
| การบริจาค (Donate) | User ID, ชื่อที่แสดง, ยอดเงิน, เลขอ้างอิงสลิป และวันที่ (ดูข้อ 4) |

### 🔑 สิทธิ์การเข้าถึงระดับสูงที่เราขอจาก Discord (Privileged Intents)

| Intent | ใช้ทำอะไร |
|--------|-----------|
| **Server Members Intent** | รับรู้เมื่อสมาชิกเข้า/ออก เพื่อส่งข้อความต้อนรับ/อำลา, อัปเดตตัวนับสมาชิก, มอบยศรางวัล XP, เก็บวันที่เข้าเซิร์ฟเวอร์ และตรวจจับเซิร์ฟเวอร์ bot-farm (สัดส่วนบอทต่อสมาชิกจริง) |
| **Presence Intent** | ดูเกมที่สมาชิกกำลังเล่น เพื่อทำสถิติกิจกรรมเกมใน Stats Card และ leaderboard, และแสดงจุดสถานะ (ออนไลน์/ไม่อยู่/สตรีม) บน Stats Card · **ผู้ใช้ปิดได้ด้วย `/status optout`** |
| **Message Content Intent** | ใช้กับระบบกันลิงก์อันตรายและกันสแปม, Text-to-Speech ในห้องที่แอดมินเปิด, สถิติอีโมจิ และคำ trigger ของ Stats Card · **ประมวลผลในหน่วยความจำเท่านั้น ไม่บันทึกเนื้อหาข้อความ** (รายละเอียดในข้อ 2) |

#### ข้อมูลที่ **ไม่ได้** เก็บ
- ❌ เนื้อหาข้อความ (Message Content) — อ่านเพื่อประมวลผลชั่วคราวแล้วทิ้ง ไม่บันทึกลงดิสก์
- ❌ รหัสผ่าน
- ❌ ที่อยู่ IP ของผู้ใช้
- ❌ รูปสลิปโอนเงิน — ส่งให้ SlipOK ตรวจสอบเท่านั้น ไม่เก็บไว้

---

### 2. วิธีที่เราใช้ข้อมูล
- ให้บริการฟีเจอร์ต่าง ๆ (Welcome/Leave, Forms, Stats, XP, Embed, Notify, TTS, ระบบความปลอดภัย, Donate)
- แสดงสถิติเซิร์ฟเวอร์และผู้ใช้ผ่าน Stats Card และ leaderboard
- ตรวจสอบสลิปบริจาคและมอบยศ Donor
- เก็บ Log การทำงานชั่วคราวเพื่อแก้ปัญหา (เก็บในหน่วยความจำสูงสุด 200 รายการ ไม่บันทึกถาวร)

#### การใช้เนื้อหาข้อความ (Message Content)
| ฟีเจอร์ | อ่านอะไร | เก็บอะไร |
|---------|---------|---------|
| **กันลิงก์อันตราย (Anti-Link)** | ลิงก์ในข้อความ ตรวจกับ blocklist, โดเมนเลียนแบบ/punycode และบริการตรวจ URL (ข้อ 3) | ไม่เก็บข้อความ ถ้าเป็นลิงก์อันตรายจะลบข้อความ แจ้งเตือนทีมงาน และบันทึก strike |
| **กันสแปม / โพสต์ซ้ำหลายห้อง** | ค่า hash ทางเดียวของข้อความ (ข้อความ + ชื่อและขนาดไฟล์แนบ) | เก็บ hash ในหน่วยความจำประมาณ 2 นาที ไม่บันทึกลงดิสก์ |
| **Text-to-Speech** | ข้อความในห้องที่แอดมินเปิด TTS ไว้ **ห้องเดียว** และเฉพาะตอนที่ session ทำงานอยู่ | ไม่เก็บ ไฟล์เสียงถูกลบหลังเล่นจบ |
| **สถิติอีโมจิ** | อีโมจิในข้อความ | อีโมจิและเวลา |
| **คำ trigger ของ Stats Card** | เทียบว่าข้อความตรงกับคำที่แอดมินตั้งไว้หรือไม่ | ไม่เก็บ |

เนื้อหาข้อความ**ไม่ถูก**ขาย ไม่ใช้ฝึก AI หรือ Machine Learning และไม่ใช้เพื่อโฆษณา

---

### 3. บริการของบุคคลที่สาม (Third-Party Services)
| บริการ | ข้อมูลที่ส่ง | เพื่อ |
|--------|------------|------|
| **Google Safe Browsing** | URL ที่พบในข้อความ (เฉพาะเซิร์ฟเวอร์ที่เปิด Anti-Link) | ตรวจลิงก์ฟิชชิง/มัลแวร์ |
| **VirusTotal** | URL ที่พบในข้อความ (เฉพาะเซิร์ฟเวอร์ที่เปิด Anti-Link) | ตรวจลิงก์ฟิชชิง/มัลแวร์ |
| **Google Text-to-Speech (gTTS)** | ข้อความในห้องที่เปิด TTS และแชทไลฟ์สตรีมที่ให้อ่านออกเสียง | แปลงข้อความเป็นเสียง |
| **YouTube & Twitch API** | ชื่อ/ID ช่องที่เซิร์ฟเวอร์ติดตาม | แจ้งเตือนไลฟ์และคลิปใหม่ |
| **SlipOK** ([slipok.com](https://slipok.com)) | รูปสลิปที่ส่งผ่าน `/donate_slip` | ตรวจสอบว่าสลิปบริจาคเป็นของจริง (เราไม่เก็บรูปสลิป) |
| **Top.gg** | จำนวนเซิร์ฟเวอร์ทั้งหมดที่ใช้บอท | แสดงในหน้ารายชื่อบอท |

เราไม่ขายหรือแบ่งปันข้อมูลให้บุคคลภายนอกอื่น ยกเว้นได้รับความยินยอมโดยชัดแจ้ง หรือกฎหมายกำหนด

---

### 4. การบริจาค (Donate)
Valkalie ไม่มีฟีเจอร์แบบเสียเงินหรือการสมัครสมาชิก การบริจาคเป็นการสนับสนุนผู้พัฒนาโดยสมัครใจ เมื่อบริจาคผ่าน `/donate_slip`:
- สลิปจะถูกตรวจกับ SlipOK โดยเราไม่เก็บรูปสลิป
- เราบันทึก User ID, ชื่อที่แสดง, ยอดเงิน, เลขอ้างอิงสลิป และวันที่ เพื่อกันสลิปซ้ำและมอบยศ Donor ในเซิร์ฟเวอร์ Valkalie
- ชื่อที่แสดงและยอดบริจาครวมอาจปรากฏใน leaderboard `/donate_top`

*ข้อมูลจากระบบ Premium/Coin เดิม (ยอดคงเหลือ ประวัติธุรกรรม และการยอมรับข้อตกลง) อาจยังอยู่ในฐานข้อมูลในฐานะบันทึกทางการเงิน และขอลบได้ตามข้อ 7*

---

### 5. การเลือกไม่ให้เก็บข้อมูล (Opt-out)
- **กิจกรรมเกม (Presence):** ใช้ `/status optout stop_tracking:True` บอทจะหยุดเก็บกิจกรรมเกมของคุณใน**ทุกเซิร์ฟเวอร์**ทันที และ**ลบข้อมูลกิจกรรมเกมเดิมทั้งหมด** ถ้าต้องการเปิดกลับ ใช้ค่า `False`
- **การมองเห็น Stats Card:** ตั้งเป็น *Private* ผ่าน `/status set` แล้วจะดูได้เฉพาะตัวคุณ
- **DM แจ้งเลเวล:** กดปุ่มปิดใน DM แจ้งเลเวลอันไหนก็ได้
- **Text-to-Speech:** บอทอ่านเฉพาะห้องที่แอดมินเลือก และเฉพาะตอนที่ session ทำงาน
- **ระบบความปลอดภัย:** ระบบกันสแปมและกันลิงก์อันตรายป้องกันทั้งเซิร์ฟเวอร์ จึงเลือกปิดเป็นรายคนไม่ได้ และระบบนี้ไม่เก็บเนื้อหาข้อความ

---

### 6. การจัดเก็บและความปลอดภัย
- ข้อมูลจัดเก็บใน PostgreSQL, SQLite และไฟล์ JSON บนเซิร์ฟเวอร์ที่ Developer ควบคุม
- ข้อมูลทั้งหมดถูกเข้ารหัสขณะพัก (encryption at rest) ด้วยการเข้ารหัสทั้งดิสก์ (AES)
- ข้อมูลลับ (credentials) เก็บใน environment variables ไม่อยู่ในโค้ด และเฉพาะผู้ดูแลบอทเท่านั้นที่เข้าถึงฐานข้อมูลได้
- ไม่มีระบบใดปลอดภัย 100% เราจึงไม่สามารถรับประกันความปลอดภัยได้อย่างสมบูรณ์

---

### 7. ระยะเวลาเก็บข้อมูลและการลบข้อมูล
| ข้อมูล | เก็บนานแค่ไหน |
|--------|-------------|
| จำนวนข้อความ, เวลาในห้องเสียง, อีโมจิ, กิจกรรมเกม | **ลบอัตโนมัติหลัง 90 วัน** |
| hash สำหรับตรวจโพสต์ซ้ำ | ประมาณ 2 นาที (เก็บในหน่วยความจำเท่านั้น) |
| Strike ของระบบความปลอดภัย | รีเซ็ตตามระยะเวลาที่เซิร์ฟเวอร์ตั้ง (ค่าเริ่มต้น 30 วัน) |
| การตั้งค่า, XP, ฟอร์ม, การบริจาค และข้อมูลอื่น | จนกว่าแอดมินจะลบ ผู้ใช้ขอลบ หรือ Developer ลบข้อมูลของเซิร์ฟเวอร์ |
| ข้อมูลเซิร์ฟเวอร์ที่ Developer ลบ | อยู่ในถังขยะ 30 วันเพื่อให้กู้คืนได้ จากนั้นลบถาวร |

การนำบอทออกจากเซิร์ฟเวอร์จะ**หยุดการเก็บข้อมูลใหม่**ทั้งหมด แต่ข้อมูลที่เก็บไปแล้ว**ไม่ถูกลบอัตโนมัติ** ถ้าต้องการให้ลบ กรุณาติดต่อเรา

**วิธีลบข้อมูล**
- **กิจกรรมเกมของตัวเอง:** `/status optout stop_tracking:True` (ลบทันที)
- **สถิติทั้งเซิร์ฟเวอร์:** แอดมินใช้ `/stats_reset` ซึ่งจะลบจำนวนข้อความ, voice, อีโมจิ, กิจกรรมเกม, วันที่เข้าเซิร์ฟเวอร์ และการตั้งค่า Stats Card ของเซิร์ฟเวอร์นั้น
- **ข้อมูลอื่นทั้งหมด:** ติดต่อเราตามช่องทางด้านล่าง พร้อมแจ้ง User ID (และ Server ID ถ้าเกี่ยวกับเซิร์ฟเวอร์ใดเซิร์ฟเวอร์หนึ่ง)

---

### 8. สิทธิ์ของผู้ใช้
คุณมีสิทธิ์:
- **ขอดู** ข้อมูลที่เราเก็บเกี่ยวกับคุณหรือเซิร์ฟเวอร์ของคุณ
- **ขอลบ** ข้อมูลของคุณ รวมถึงขอนำชื่อออกจาก leaderboard ผู้บริจาค
- **หยุดการเก็บกิจกรรมเกม** ได้ทุกเมื่อด้วย `/status optout`
- **นำบอทออกจากเซิร์ฟเวอร์** ได้ทุกเมื่อ เพื่อหยุดการเก็บข้อมูลของเซิร์ฟเวอร์นั้น

---

### 9. การเปลี่ยนแปลงนโยบาย
เราอาจอัปเดตนโยบายนี้เป็นครั้งคราว และจะเปลี่ยนวันที่มีผลบังคับใช้ด้านบนทุกครั้ง การใช้บอทต่อหลังการเปลี่ยนแปลงถือว่าคุณยอมรับนโยบายที่อัปเดตแล้ว

---

## 📜 ข้อกำหนดการให้บริการ (Terms of Service)

**มีผลบังคับใช้ตั้งแต่:** 7 ตุลาคม 2569

### 1. การยอมรับข้อกำหนด
การเชิญหรือใช้ Valkalie Bot ในเซิร์ฟเวอร์ Discord ถือว่าคุณและผู้ดูแลเซิร์ฟเวอร์ยอมรับข้อกำหนดเหล่านี้

### 2. คุณสมบัติของผู้ใช้
- ต้องมีอายุไม่ต่ำกว่า 13 ปี ตาม [Discord Terms of Service](https://discord.com/terms)
- ต้องมีสิทธิ์ตามกฎหมายในการใช้ Discord และบริการที่เกี่ยวข้อง

### 3. การใช้งานที่อนุญาต
Valkalie Bot มีไว้สำหรับเซิร์ฟเวอร์ Discord ที่ถูกกฎหมาย เพื่อใช้ระบบต่าง ๆ ได้แก่:
- XP/Level และร้านค้า XP, Welcome/Leave, Forms, ServerStats/Stats
- Embed Builder, Sticky, Scheduler, Notify (YouTube/Twitch), Text-to-Speech
- ระบบความปลอดภัย (กันสแปม/กันลิงก์อันตราย/กัน raid), มินิเกม, Support, Donate

### 4. สิ่งที่ห้ามกระทำ
คุณตกลงว่าจะ **ไม่**:
- ใช้บอทเพื่อสแปม คุกคาม หรือล่วงละเมิดผู้อื่น
- พยายาม Exploit, Hack หรือทำให้บอททำงานผิดปกติ
- กระทำสิ่งที่ขัดต่อ [Discord Community Guidelines](https://discord.com/guidelines) หรือกฎหมาย
- ใช้ระบบฟอร์มหรือ Report เพื่อแจ้งเท็จหรือกลั่นแกล้งผู้อื่น
- ส่งสลิปปลอมหรือสลิปที่ไม่ใช่ของตนเอง

### 5. การบริจาค
การบริจาคเป็นไปโดยสมัครใจ ไม่ได้เป็นการซื้อสินค้า บริการ หรือฟีเจอร์ใด ๆ และตรวจสอบสลิปผ่าน SlipOK ผู้บริจาคจะได้รับยศ Donor ในเซิร์ฟเวอร์ Valkalie เป็นการขอบคุณ

### 6. ความพร้อมใช้งานของบริการ
- ไม่รับประกันว่าบอทจะใช้งานได้ตลอด 24/7
- อาจหยุดให้บริการชั่วคราวหรือถาวร หรือเปลี่ยนแปลงฟีเจอร์โดยไม่แจ้งล่วงหน้า

### 7. การระงับการใช้งาน
เราสงวนสิทธิ์ในการ **Blacklist เซิร์ฟเวอร์หรือผู้ใช้** ที่ละเมิดข้อกำหนด หรือมีพฤติกรรมที่เป็นอันตรายต่อผู้อื่น

### 8. ข้อจำกัดความรับผิด
Valkalie Bot ให้บริการ **"ตามสภาพที่เป็น" (As-Is)** แอดมินเป็นผู้รับผิดชอบการตั้งค่าบอทในเซิร์ฟเวอร์ของตนเอง (เช่น ระบบลงโทษอัตโนมัติ) Developer ไม่รับผิดชอบต่อความเสียหายหรือข้อมูลสูญหายที่เกิดจากการใช้บอท

### 9. ทรัพย์สินทางปัญญา
โค้ด ชื่อ และโลโก้ของ Valkalie Bot เป็นทรัพย์สินของ Developer ห้ามคัดลอก แก้ไข หรือนำไปใช้โดยไม่ได้รับอนุญาตเป็นลายลักษณ์อักษร

### 10. การเปลี่ยนแปลงข้อกำหนด
เราอาจแก้ไขข้อกำหนดได้ตลอดเวลา การใช้บอทต่อถือว่ายอมรับข้อกำหนดที่อัปเดตแล้ว

---

# 🇬🇧 English

## Privacy Policy

**Effective:** October 7, 2026

### 1. Data We Collect

**Server data**
- Server (guild), channel, and role IDs, used to store each server's settings: welcome/leave, forms, embeds, sticky messages, scheduled actions, YouTube/Twitch notifications, server-stat counters, XP, the XP shop, and security.
- Server-stat counters: total, member, and bot counts, shown as voice-channel names.
- A backup of the server's channel and role structure (names, permissions, positions), used to restore the server after a raid or nuke. It never contains message content.
- The user who added the bot to the server, read from the audit log, used to prevent abuse.

**User data**
- **User IDs and display names**, used for stats, XP, leaderboards, forms, and the donor list.
- **Activity statistics:** message counts with channel and timestamp (**not message content**), voice-session durations, emojis used, and server join dates.
- **Game activity (via Presence):** the game name and when you started and stopped playing. It powers stats cards and leaderboards and can be turned off (Section 5).
- **XP and levels:** XP, levels, points, server-created currency balances, XP shop orders, and whether you turned off level-up DMs.
- **Form submissions:** your answers to forms a server admin creates (for example reports or applications). Only that server's staff can see them.
- **Security records:** a strike count and the time of the last strike if the anti-spam or anti-link system acts on your account.
- **Mini-game results:** wins and losses in the bot's games.
- **Support tickets:** what you write when you open a ticket with `/valkalie_support`.
- **Donations:** user ID, display name, amount, slip reference number, and date (Section 4).

### 🔑 Privileged Discord Intents We Request

| Intent | Purpose |
|--------|---------|
| **Server Members Intent** | Detect member joins and leaves to send welcome/leave messages, update member counters, grant XP reward roles, record server join dates, and detect bot-farm servers (bot-to-human ratio) |
| **Presence Intent** | Read which game members are playing for game-activity stats on stats cards and leaderboards, and show an online/idle/streaming status dot on stats cards. **Users can turn this off with `/status optout`.** |
| **Message Content Intent** | Used for anti-phishing and anti-spam protection, Text-to-Speech in an admin-enabled channel, emoji statistics, and the stats-card trigger word. **Processed in memory only. Message content is never stored.** (See Section 2.) |

### 2. How We Use Data
- To run bot features: welcome/leave, forms, stats, XP, embeds, notifications, TTS, security, and donations
- To show server and user statistics on stats cards and leaderboards
- To verify donation slips and grant the Donor role
- To keep temporary troubleshooting logs (up to 200 entries, in memory only, never saved)

#### How message content is used
| Feature | What it reads | What it keeps |
|---------|---------------|---------------|
| **Anti-Link** | Links in messages, checked against a blocklist, look-alike/punycode domain detection, and URL reputation services (Section 3) | Nothing from the message. A malicious link is deleted, moderators are alerted, and a strike is recorded. |
| **Anti-Spam / cross-post detection** | A one-way hash of the message (text plus attachment names and sizes) | The hash, in memory for about 2 minutes. Never saved to disk. |
| **Text-to-Speech** | Messages in the **one** channel an admin enables, only while a TTS session is running | Nothing. The audio file is deleted after it plays. |
| **Emoji statistics** | Emojis in the message | The emoji and a timestamp |
| **Stats-card trigger word** | Whether the message exactly matches a trigger word an admin has set | Nothing |

Message content is **never** sold, used to train AI or machine-learning models, or used for advertising.

### 3. Data We Do NOT Store
- Message content (read only for in-memory processing, then discarded)
- Passwords
- Users' IP addresses
- Bank-transfer slip images (sent to SlipOK for verification only, never kept)

### 4. Donations
Valkalie has no paid features or subscriptions. Donations are voluntary support for the developer. When you donate with `/donate_slip`:
- your slip is checked with SlipOK, and the image is not kept;
- your user ID, display name, amount, slip reference number, and date are recorded to stop duplicate slips and to grant the Donor role in the Valkalie server;
- your display name and total donated may appear on the `/donate_top` leaderboard.

*Records from the former Premium/Coin system (balances, transaction history, and agreement acceptances) may still exist as financial records. You can ask us to delete them (Section 8).*

### 5. Third-Party Services
| Service | Data sent | Purpose |
|---------|-----------|---------|
| **Google Safe Browsing** | URLs found in messages (only in servers with Anti-Link enabled) | Detect phishing and malware links |
| **VirusTotal** | URLs found in messages (only in servers with Anti-Link enabled) | Detect phishing and malware links |
| **Google Text-to-Speech (gTTS)** | Messages in a TTS-enabled channel, and live-stream chat being read aloud | Convert text to speech |
| **YouTube & Twitch APIs** | Names or IDs of channels a server follows | Live-stream and upload notifications |
| **SlipOK** ([slipok.com](https://slipok.com)) | Slip images sent with `/donate_slip` | Check that a donation slip is genuine (we do not keep the image) |
| **Top.gg** | Total number of servers using the bot | Bot listing |

We do not sell user data. We do not share it with anyone else unless you explicitly agree or the law requires it.

### 6. Opting Out
- **Game activity (Presence):** run `/status optout stop_tracking:True`. Tracking stops in **every** server immediately and **all previously stored game-activity data is deleted**. Run it with `False` to turn tracking back on.
- **Stats card visibility:** set your card to *Private* with `/status set`.
- **Level-up DMs:** use the opt-out button on any level-up DM.
- **Text-to-Speech:** the bot reads only the channel an admin chooses, and only while a session is running.
- **Security scanning:** anti-spam and anti-link protect the whole server, so individual users cannot opt out. They do not store message content.

### 7. Storage & Security
- Data is stored in PostgreSQL, SQLite, and JSON files on developer-controlled infrastructure.
- All stored data is encrypted at rest using full-disk encryption (AES).
- Credentials are kept in environment variables, never in source code, and only the bot operator can access the databases.
- No system is 100% secure, so we cannot guarantee absolute security.

### 8. Data Retention & Deletion
| Data | How long we keep it |
|------|---------------------|
| Message counts, voice sessions, emoji usage, game activity | **Deleted automatically after 90 days** |
| Cross-post detection hashes | About 2 minutes, in memory only |
| Security strikes | Reset after a period the server sets (30 days by default) |
| Settings, XP, forms, donations, and other records | Until an admin removes them, you ask us to delete them, or the developer removes the server's data |
| Server data removed by the developer | Kept in a recovery bin for 30 days, then deleted permanently |

Removing the bot from a server **stops all further collection** for that server. Data already collected is **not deleted automatically**. Contact us if you want it deleted.

**How to delete data**
- **Your own game activity:** `/status optout stop_tracking:True` deletes it immediately.
- **A server's statistics:** an admin can run `/stats_reset`. It deletes that server's message counts, voice sessions, emoji usage, game activity, join dates, and stats-card settings.
- **Everything else:** contact us (below) with your user ID, plus the server ID if your request is about one server.

### 9. Your Rights
- Request a copy of the data we hold about you or your server.
- Request deletion of your data, including removing your name from the donor leaderboard.
- Stop game-activity tracking at any time with `/status optout`.
- Remove the bot from a server at any time to stop data collection there.

### 10. Changes
We may update this policy from time to time. We will change the effective date above whenever we do. Continued use after a change means you accept the updated policy.

---

## Terms of Service

**Effective:** October 7, 2026

**1. Acceptance** — Inviting or using Valkalie in your Discord server means you and the server's administrators accept these terms.

**2. Eligibility** — Minimum age 13, and you must comply with Discord's [Terms of Service](https://discord.com/terms).

**3. Permitted Uses** — Leveling/XP and the XP shop, welcome/leave, forms, server statistics, embed builder, sticky messages, scheduler, live-stream notifications, text-to-speech, server security (anti-spam, anti-link, anti-raid), mini-games, support tickets, and donations.

**4. Prohibited Actions**
- Spam, harassment, or abuse
- Attempting to exploit, hack, or disrupt the bot
- Violating Discord's [Community Guidelines](https://discord.com/guidelines) or applicable law
- Using forms or reports to submit false reports or harass others
- Submitting fake slips or slips that are not your own

**5. Donations** — Donations are voluntary and do not purchase any product, service, or feature. Slips are verified through SlipOK. Donors receive a Donor role in the Valkalie server as a thank-you.

**6. Service Availability** — Provided "as-is" with no uptime guarantee. Features may change or be discontinued without notice.

**7. Suspension** — We may blacklist any server or user that violates these terms or harms others.

**8. Liability** — Server admins are responsible for how they configure the bot in their server, including automated punishments. The developer is not liable for damages or data loss arising from use of the bot.

**9. Intellectual Property** — The code, name, and logo are protected and may not be reproduced or used without written permission.

**10. Changes** — We may revise these terms at any time. Continued use means you accept the revised terms.

---

## 📬 ติดต่อเรา / Contact

หากมีคำถาม ข้อสงสัย หรือต้องการใช้สิทธิ์ด้านข้อมูล กรุณาติดต่อ /
For questions or to exercise your data rights, contact:

- **Discord:** hoyorai
- **Support Server:** https://discord.gg/GXPgH3AZCe
- **GitHub Issues:** [github.com/Valkalie/Valkalie-legal/issues](https://github.com/Valkalie/Valkalie-legal/issues)

---

<div align="center">

**Valkalie Bot** · อัปเดตล่าสุด / Last updated: 7 ตุลาคม 2569 (October 7, 2026)

</div>
