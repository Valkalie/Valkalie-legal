# Valkalie Bot — Privacy Policy & Terms of Service

**Effective date:** 30 October 2026
**Contact:** Discord user `hoyorai` · Support server: https://discord.gg/GXPgH3AZCe

Valkalie is a multi-purpose Discord community management bot. This page explains what data Valkalie collects, why it collects it, who else processes it, how long it is kept, and how you can opt out or have it deleted.

---

## 1. Data we collect

### Server data
- The roles and members a server's owner or admins allow to manage each Valkalie feature.
- **Feature activity counts:** how many times each server's embeds, notifications, and scheduled actions ran or failed in each hour. These are totals only. They do not record who triggered them.
- Server, channel, and role IDs used to store each server's settings: welcome/leave messages, forms, embeds, sticky messages, scheduled actions, VarTable values and automation rules, mini-game setups, YouTube/Twitch notifications, server stat counters, XP settings, the XP shop, security settings, and server activity log settings.
- **Server activity logs (only in servers that turn them on):** Valkalie posts voice-channel joins, leaves, and moves (with how long the member stayed); channel changes (including which permissions changed); and member changes (nickname, username, display name, avatar, roles, and timeouts) to a channel the server's admins choose. A separate shop log can also post XP shop activity: purchases, deliveries, refunds, transfers between members (with the note the sender wrote), balance changes made by admins, and changes to the shop's items (added, removed, restocked, sold out, opened or closed for sale, and price changes). Each entry says where the change came from: a Valkalie feature, Discord itself (for example a server boost), another bot, an admin, or the member. When the audit log shows who made a change and why, that is included. For an avatar change, Valkalie posts the old and new avatar as one image in that channel. Discord deletes an old avatar as soon as it is changed, so in servers with the avatar log turned on, Valkalie keeps a copy of the avatars of members who recently chatted, joined a voice channel, or joined the server (in memory only, at most 1,500 images, never written to disk). Valkalie does not keep a copy. The log exists only as messages in that server's channel.
- **Message log (only in servers that turn it on):** when a message is deleted or edited, Valkalie posts its earlier text and attachment names, who sent it, and who deleted it, to the staff log channel. When many messages are deleted at once, it posts them as a text file. It also logs who pinned or unpinned a message. To do this, Valkalie holds recent messages from that server in memory (see section 2). They are never written to disk.
- **Invite use (only in servers that turn on the Invite Tracker or invite reward roles):** Valkalie reads the server's invite list (invite code, who created it, and how many times it was used) to tell which invite a new member used. The invite list is held in memory only. Valkalie also records who invited each new member (the inviter's user ID, the invite code, and the time). It uses this record to count how many invited members are still in the server and to give or remove the server's invite reward roles. The record is deleted when the invited member leaves the server.
- A backup of the server's channel and role structure (names, permissions, positions). Valkalie uses it to restore the server after a raid or nuke. It never includes message content.
- **Images used in embeds.** When an admin adds an image to an embed, Valkalie downloads it and re-uploads a copy to a private channel the bot owns, so the image keeps working after Discord's links expire. The original image URL is stored with the copy.
- **Embed share codes (only when an admin creates one).** When an admin presses 🔗 แชร์โค้ด on an embed, Valkalie stores a copy of that embed under a short code so admins of other servers can import it with `/embed import`. The copy contains the embed's content and settings (including the IDs of roles and channels its buttons use) and is updated each time the admin shares again. The admin can revoke the code at any time, and deleting the embed deletes its code.
- The user who added Valkalie to a server, read from the audit log. This is used for abuse prevention.

### User data
- **User IDs and display names.** These are used wherever a feature needs to show who did something, such as leaderboards, form submissions, and the donor list.
- **Activity statistics:** message counts with channel and timestamp, voice-channel session durations, emojis used, and server join dates. **We store the fact that a message was sent, not what it said.**
- **Voice time for voice-time roles (only in servers that set them up):** Valkalie records how many minutes you spend in each voice channel each day, so it can give the roles a server sets for voice time (and, for roles based on recent activity, take them back when your time drops below the target). Time in the AFK channel is not counted, and by default neither is time while you are deafened or alone in a channel. Daily records older than 90 days are combined into one running total per channel.
- **Stats-card settings:** your card's theme, colours, privacy setting, and any custom background image URL you set. They apply in every server unless you set different ones for a particular server.
- **Game activity from Discord Presence:** the name of the game you are playing and when you started and stopped. Valkalie uses this for per-server stats cards and leaderboards. See *Opting out* below.
- **Command usage:** each time you use a Valkalie slash command, we record your user ID, the server, the channel, the command name, and the time. This helps us see which features are used and fix problems. Command options and their values are not stored.
- **Embed interactions:** when you press a button on a Valkalie embed, we record your user ID, which button it was, and the time. Valkalie also records which dropdown rewards you have already claimed (so each one can only be claimed once) and which rooms you own if a button created one for you.
- **XP and levels:** XP totals, levels, point balances, custom currency balances, XP shop orders, and whether you have turned off level-up DMs.
- **Role transfer requests:** when you press a role-transfer button on an embed, Valkalie records your user ID, the account you want the roles moved to, which roles, your optional note, the time, and which staff member approved or rejected it. The request is posted to a staff channel the server's admins chose, and you get the decision by DM.
- **Transfers:** when you send points or a custom currency to another member, Valkalie records the sender's and recipient's user IDs, the amount, the currency, the optional note, and the time.
- **Form submissions:** your answers to forms a server admin creates (for example reports or applications), together with your user ID and username. For a report, the reported member's ID and username are stored too.
- **Security records:**
  - If the anti-spam, anti-link, or word filter system acts on your account, Valkalie stores how many times that system has acted on you, and when it last did, for that server. Each system keeps its own count.
  - Each server's security log keeps its 15 most recent events. Each event lists the member's ID, the channel, and the reason. The reason can include the domain of a blocked link or the blocked word that was found.
- **Mini-game results:** for each finished game, your side and role, whether you won, whether you survived, the number of players, and the date. If the server gives game rewards, the daily total you received is also stored.
- **Support tickets:** what you write when you open a ticket with `/valkalie_support`. It is sent to a staff channel in the Valkalie support server.
- **Donations:** your user ID, display name, amount, the bank slip reference number, and the date. See section 4.
- **Vlk wallet and monthly plan:** your Vlk balance, every change to it (top-ups, bonuses, codes, purchases, and adjustments, each with the amount, the time, and the slip or Ko-fi reference), your wallet's Ko-fi code, the servers you bought monthly plan time for, and whether you pay for a server's automatic renewal. See section 5.
- **Web panel sign-in (beta):** when you sign in to the Valkalie web panel with Discord, Valkalie asks Discord only for your basic profile (the `identify` permission): your user ID, display name, and avatar. It does not receive your email, your server list, or your messages. Discord's access token is used once to read your profile and is then revoked, so it is never stored. Valkalie keeps a login session with your user ID, display name, and avatar link. Your browser holds the session as a cookie, and the database stores only a scrambled (hashed) copy of it. The panel uses this one sign-in cookie and no tracking or advertising cookies. It also keeps a few display preferences in your browser's own storage (local storage), such as the last page and sections you had open; these stay in your browser and are never sent to Valkalie. Each server also has a server page in the panel. Signed-in members of that server can see their own level, points, activity, orders and form submissions there, and can buy from the server's shop or send its forms, exactly as they could in Discord. If a server admin makes the page public, anyone with the link can see the server's name, icon, banner, description, member count, emojis, the admin's introduction text and an invite link that Valkalie creates; no member's personal data is shown on the public part. Settings you change in the panel are recorded in the bot's log files with your user ID and display name.
- **Error reports and logs:** if a command fails, the developer receives a private report with your username, the server name, the command, and technical error details. The bot's own log files also contain user and server IDs and names.

### What we do NOT store
- **The text of your messages.** Message content is read in memory only (section 2) and is never written to disk. The only exceptions are the domain of a link that the security system blocks and the blocked word that the word filter finds. Both are kept in that server's security log. In servers that turn on the message log, recent messages are held in memory for a limited time, and the text of a deleted or edited message is posted to that server's staff log channel.
- Passwords or Discord login credentials.
- Your IP address.
- Images of bank-transfer slips. They are sent to SlipOK for verification and are not kept.
- Your bank account details, card numbers, or Ko-fi/PayPal login. Card and PayPal payments are handled entirely by Ko-fi.

### Where data is stored
All data is stored in databases on the developer's own server. No outside database or cloud-storage provider is used. The only exception is embed images, which are kept as files in a Discord channel the bot owns.

---

## 2. How Valkalie uses message content

Valkalie uses Discord's Message Content intent for the features below. In each case the text is processed in memory and is never written to disk. The message log is the only feature that holds message text for longer than it takes to process it. It holds it in memory, for a limited time (see the table).

| Feature | What it reads | What it keeps |
|---|---|---|
| **Anti-Link / anti-scam** | Links in messages. They are checked against a blocklist, for look-alike and punycode domains, and with online URL reputation services (section 3). | If a link is malicious, the message is deleted, moderators are alerted with the reason, and the offense is counted. The security log keeps the member ID, the channel, and the blocked domain. Nothing else from the message is kept. |
| **Word filter** | Whether your message contains a word or phrase on the server's blocked list, in servers where an admin has turned it on | If a blocked word is found, the message is deleted and the offense is counted. The security log keeps the member ID, the channel, and the blocked word that was found. Nothing else from the message is kept. |
| **Anti-Spam / cross-post detection** | A one-way hash of the message (text plus attachment names and sizes), compared against your recent messages to spot the same content posted in many channels. Also how many members and roles the message mentions, and whether it combines `@everyone`/`@here` with a link. | The hash is held in memory for about two minutes. Nothing is written to disk except the offense count and the security-log entry. |
| **Text-to-Speech (TTS)** | Messages in the **one** text channel a TTS session is started for, only while the session is running. If the "read names" option is on, the sender's display name is read too. | Nothing. The generated audio is held in memory only while it plays. |
| **Message log** | Messages in servers where an admin has turned on the message log | The latest 5,000 messages per server, held **in memory only** for up to 3 days, so that a deleted or edited message's earlier text and attachment names can be posted to the server's staff log channel. They are cleared when the message log is turned off or the bot restarts. Messages from Valkalie itself are not kept. |
| **Emoji statistics** | Emojis in your message | The emoji and a timestamp. |
| **Stats-card trigger word** | Whether your message exactly matches a trigger word an admin has set | Nothing. |

Message content is **never** sold, used to train AI or machine-learning models, or used for advertising.

---

## 3. Third-party services

Valkalie sends data to the following services only to provide the feature listed:

| Service | What is sent | Why |
|---|---|---|
| **Google Safe Browsing** | URLs found in messages, in servers with Anti-Link enabled | Detect phishing and malware links |
| **VirusTotal** | URLs found in messages, in servers with Anti-Link enabled | Detect phishing and malware links |
| **Google Text-to-Speech** | Text being read aloud: messages in a TTS channel or live-stream chat, plus the sender's name if "read names" is on | Turn text into speech |
| **YouTube / Twitch** | Channel names or IDs that a server follows, and the stream link when TTS reads a live chat | Live-stream and upload notifications, and reading live-stream chat aloud |
| **ngrok** | Incoming YouTube upload notifications, traffic to the developer's private dashboard, and traffic to the Valkalie web panel | Receive notifications from YouTube and make the web panel reachable |
| **Tailscale Funnel** | Incoming Ko-fi payment notifications and traffic to the Valkalie web panel | Make them reachable from the internet |
| **SlipOK** | Bank-transfer slip images sent with `/donate_slip` or `/billing` | Check that a slip is genuine |
| **Ko-fi** | Nothing is sent by Valkalie. When you pay on Ko-fi, Ko-fi sends Valkalie your Ko-fi display name, the amount and currency, your message, and your email address. Valkalie keeps the display name and amount, the message only if the payment could not be matched to a wallet, and a one-way hash of the email (never the email itself) to match later monthly Ko-fi payments to your wallet. | Top up Vlk with a card or PayPal |
| **Top.gg** | Total number of servers Valkalie is in | Bot listing |

We do not sell user data. We do not share it with anyone else unless you explicitly agree or the law requires it.

---

## 4. Donations

Donations are voluntary support for the developer and are separate from the monthly plan (section 5). A donation does not buy Vlk or plan time. When you donate with `/donate_slip`:
- your slip is checked with SlipOK, and the image is not kept;
- your user ID, display name, amount, slip reference number, and date are recorded so the donation is not counted twice and so you can receive the Donor role in the Valkalie server;
- your display name and total donated may appear on the `/donate_top` leaderboard.

If you do not want to appear on the leaderboard, contact us (section 9).

*Older records from a previous paid-features system (wallet balances, transaction history, and agreement acceptances) may still exist in our database. They are kept as financial records and can be deleted on request. That system's `/agreement` command has been removed, so no new agreement acceptances are recorded.*

---

## 5. Monthly plan and Vlk

### When a server needs the monthly plan
- A server with **100 or fewer members** (bots are not counted) uses Valkalie for free.
- When a server first has more than 100 members, it can keep using Valkalie for free for **14 days**. After that, it needs the monthly plan.
- The monthly plan costs **200 Vlk for 30 days**, whatever the server's size. Anyone in the server can buy it for the server with `/billing`.
- When a plan ends, the server can keep using Valkalie for **7 more days**. If you renew during those 7 days, the new 30 days start from the day the old plan ended.
- If a server that needs the plan does not have one, **every Valkalie feature stops in that server except 🛡️ Security** and the `/billing` page. Nothing is deleted. Features start again as soon as the plan is renewed.
- The server owner gets a DM before the free period or the plan ends, and when the server stops.

### What Vlk is
Vlk is Valkalie's own credit. You use it to buy the monthly plan.
- **1 baht = 5 Vlk.** You can top up any amount. Larger top-ups get bonus Vlk: **10% extra from 100 baht** and **15% extra from 200 baht**. Bonus amounts may change, but Vlk you already have never changes.
- Ways to top up: a bank transfer or PromptPay with the slip sent through `/billing`, or Ko-fi using your wallet code. Vlk can also come from codes the developer gives out.
- Your wallet belongs to **you**, not to a server. You can use it for any server you are in.
- **Vlk does not expire.**
- **Vlk can only be used for Valkalie's own services.** It has no cash value. You cannot withdraw it, exchange it for money, or send it to another user.
- Amounts under 1 Vlk (less than 0.20 baht) are not credited.

### Buying and automatic renewal
- Buying the plan takes 200 Vlk from your wallet straight away and adds 30 days to the server. **A purchase cannot be turned back into Vlk.**
- You can turn on **automatic renewal** for a server. Valkalie then takes 200 Vlk from your wallet **1 day before the server's plan or free period ends**. If you do not have enough Vlk, you get a DM and nothing is taken. You can turn it off at any time in `/billing`. It also turns off by itself if you leave that server.
- Only you can turn off your own automatic renewal. A server admin can switch the server's renewal to their own wallet.

### Refunds
- **Mistakes and double charges:** if a slip or Ko-fi payment was credited wrongly, a payment was taken twice, or Vlk was taken because of a Valkalie error, contact us (section 9) and we will fix it.
- **Unused Vlk you paid for:** you can ask for a refund of unused Vlk **within 14 days of the top-up**. We refund the money you paid for the Vlk still in your wallet. Bonus Vlk and Vlk from codes are not refunded. Refunds go back the same way you paid: by bank transfer, or through Ko-fi for Ko-fi payments.
- **Plan time already bought** is not refunded, except when Valkalie could not provide the service to that server for a long period because of our fault.
- **Chargebacks and fake payments:** if a payment is reversed, or a slip turns out not to be genuine, we remove the Vlk it added. If that Vlk was already spent, we may stop the plan time it bought.

### Price changes and closing
- We will announce price changes in the support server at least **30 days** before they apply. Plan time you already bought is not affected.
- If Valkalie closes, we will announce it at least **30 days** before and stop accepting top-ups. We will then refund the unused Vlk you paid for that is still in your wallet, if you ask for it before Valkalie closes. Bonus Vlk and Vlk from codes are not refunded.

### Records we keep
Wallet balances, the history of every wallet change, and each server's plan purchases are financial records. They are kept for **5 years after your last wallet change**, even if you ask us to delete your other data. You can ask us to close your wallet once no payment issue is open. Any Vlk left in it is lost, apart from refunds you are entitled to above. The financial records are still kept for the 5 years.

---

## 6. Opting out

- **Game activity (Presence):** run `/status optout stop_tracking:True`. Valkalie stops recording your game activity in **every** server immediately and **deletes all game-activity data it has already stored about you**. Run it with `False` to turn tracking back on.
- **Stats card visibility:** set your card to *Private* with `/status set`. Only you will be able to see it.
- **Level-up DMs:** use the opt-out button on any level-up DM.
- **Text-to-Speech:** TTS only reads the channel a session is started for, and only while the session is running. If you do not want to be read aloud, do not post in that channel during a session.
- **Security scanning and command-usage records:** anti-spam, anti-link, and command-usage records cover the whole bot, so individual users cannot opt out. None of them store message content. You can still ask us to delete your records (section 8).
- **Server activity logs:** these are turned on by each server's admins for moderation, so individual members cannot opt out. Valkalie keeps no copy. To have log messages removed, ask that server's admins.

---

## 7. Data retention

| Data | How long we keep it |
|---|---|
| Message counts, voice sessions, emoji usage, game activity | **Deleted automatically after 90 days** |
| Command usage records | **Deleted automatically after 180 days** |
| Voice time for voice-time roles | Daily records for 90 days, then combined into one total per channel. The totals are kept until a server admin runs `/stats_reset`, you ask us to delete them, or the developer removes the server's data. |
| Feature activity counts | Hourly for 30 days, then combined into daily totals and **deleted after 365 days** |
| Cross-post detection hashes | About 2 minutes, in memory only |
| Server activity logs | Not stored by Valkalie. They exist only as messages in the channel the server chose. |
| Message text for the message log | In memory only: up to 3 days and at most 5,000 messages per server. Cleared when the message log is turned off or the bot restarts. |
| Invite use counts (Invite Tracker) | In memory only, while the bot is running |
| Who invited each member (Invite Tracker) | Until the invited member leaves the server, or the server's data is removed |
| Security log | The 15 most recent events per server. Older events are removed as new ones are added. |
| Security offense counts | Each system's count starts again from zero if you get no new offense in that system within a period the server sets (30 days by default). The record itself stays until it is deleted (see the row below). |
| Embed button-click records | Until the embed is deleted |
| Web panel login sessions | 7 days, or until you sign out |
| Server join dates, stats-card settings, server settings, XP, forms, game results, donations, and other records | Until a server admin removes them, you ask us to delete them, or the developer removes the server's data |
| Error reports and bot log files | Until the developer clears them |
| Vlk wallet history and plan purchases | 5 years after your last wallet change (see section 5) |
| Server data deleted by the developer | Kept in a recovery bin for 30 days, then deleted permanently |

Removing Valkalie from your server **stops all further collection** for that server. Data already collected is **not deleted automatically** when the bot is removed. Ask us (section 9) if you want it deleted.

---

## 8. Deleting your data

- **Your own game activity:** `/status optout stop_tracking:True` deletes it immediately.
- **A server's statistics:** a server admin can run `/stats_reset`. It deletes that server's message counts, voice sessions, voice time for voice-time roles, emoji usage, game activity, member join dates, and the stats-card settings members made for that server only. Card settings that apply in every server are kept; ask us to delete them (see below).
- **Everything else:** ask through the support server or message `hoyorai` on Discord. Include your user ID, and the server ID if your request is about one server. We will delete the data within 30 days. Vlk wallet and plan purchase records are the exception and are kept as described in section 5. Deleted data may stay in the recovery bin for up to 30 more days before it is erased permanently.

Server admins should note that form answers can also be copied into the server's VarTable and shown in embeds. Deleting a form does not remove those copies; the admin has to remove them from the VarTable separately.

You can also ask for a copy of the data we hold about you.

---

## 9. Contact

- Discord: `hoyorai`
- Support server: https://discord.gg/GXPgH3AZCe

---

## Terms of Service (summary)

1. By adding Valkalie to a server or using its commands, you agree to these terms and to Discord's [Terms of Service](https://discord.com/terms) and [Community Guidelines](https://discord.com/guidelines).
2. You must meet the minimum age to use Discord in your country (at least 13).
3. Do not use Valkalie to spam, harass, scam, or break any law, and do not try to exploit, overload, or reverse-engineer it.
4. Server admins are responsible for how they configure Valkalie in their server. This includes forms, automated actions, security settings, and which channels can see form submissions. A submission is visible to everyone who can see the channel the admin sends it to.
5. Valkalie is provided "as is", with no guarantee of uptime or that it will be free of errors. Features may change or be removed.
6. We may block a user or server from using Valkalie if it is abused.
7. Donations are voluntary and do not purchase any service or feature. The monthly plan and Vlk follow the rules in section 5, including its refund rules. Vlk has no cash value and cannot be withdrawn or sent to other users.
8. We may update these terms and this policy. The effective date at the top of this page will change when we do.
