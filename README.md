# Valkalie Bot — Privacy Policy & Terms of Service

**Effective date:** 7 October 2026
**Contact:** Discord user `hoyorai` · Support server: https://discord.gg/GXPgH3AZCe

Valkalie is a multi-purpose Discord community management bot. This page explains what data Valkalie collects, why it collects it, who else processes it, how long it is kept, and how you can opt out or have it deleted.

---

## 1. Data we collect

### Server data
- Server, channel, and role IDs used to store each server's settings: welcome/leave messages, forms, embeds, sticky messages, scheduled actions, VarTable values and automation rules, mini-game setups, YouTube/Twitch notifications, server stat counters, XP settings, the XP shop, and security settings.
- A backup of the server's channel and role structure (names, permissions, positions). Valkalie uses it to restore the server after a raid or nuke. It never includes message content.
- **Images used in embeds.** When an admin adds an image to an embed, Valkalie downloads it and re-uploads a copy to a private channel the bot owns, so the image keeps working after Discord's links expire. The original image URL is stored with the copy.
- The user who added Valkalie to a server, read from the audit log. This is used for abuse prevention.

### User data
- **User IDs and display names.** These are used wherever a feature needs to show who did something, such as leaderboards, form submissions, and the donor list.
- **Activity statistics:** message counts with channel and timestamp, voice-channel session durations, emojis used, and server join dates. **We store the fact that a message was sent, not what it said.**
- **Stats-card settings:** your card's theme, colours, privacy setting, and any custom background image URL you set.
- **Game activity from Discord Presence:** the name of the game you are playing and when you started and stopped. Valkalie uses this for per-server stats cards and leaderboards. See *Opting out* below.
- **Command usage:** each time you use a Valkalie slash command, we record your user ID, the server, the channel, the command name, and the time. This helps us see which features are used and fix problems. Command options and their values are not stored.
- **Embed interactions:** when you press a button on a Valkalie embed, we record your user ID, which button it was, and the time. Valkalie also records which dropdown rewards you have already claimed (so each one can only be claimed once) and which rooms you own if a button created one for you.
- **XP and levels:** XP totals, levels, point balances, custom currency balances, XP shop orders, and whether you have turned off level-up DMs.
- **Form submissions:** your answers to forms a server admin creates (for example reports or applications), together with your user ID and username. For a report, the reported member's ID and username are stored too.
- **Security records:**
  - If the anti-spam or anti-link system acts on your account, Valkalie stores a strike count and the time of your last strike for that server.
  - Each server's security log keeps its 15 most recent events. Each event lists the member's ID, the channel, and the reason, which can include the domain of a blocked link.
- **Mini-game results:** for each finished game, your side and role, whether you won, whether you survived, the number of players, and the date. If the server gives game rewards, the daily total you received is also stored.
- **Support tickets:** what you write when you open a ticket with `/valkalie_support`. It is sent to a staff channel in the Valkalie support server.
- **Donations:** your user ID, display name, amount, the bank slip reference number, and the date. See section 4.
- **Error reports and logs:** if a command fails, the developer receives a private report with your username, the server name, the command, and technical error details. The bot's own log files also contain user and server IDs and names.

### What we do NOT store
- **The text of your messages.** Message content is read in memory only (section 2) and is never written to disk. The only exception is the domain of a link that the security system blocks, which is kept in that server's security log.
- Passwords or Discord login credentials.
- Your IP address.
- Images of bank-transfer slips. They are sent to SlipOK for verification and are not kept.

### Where data is stored
All data is stored in databases on the developer's own server. No outside database or cloud-storage provider is used. The only exception is embed images, which are kept as files in a Discord channel the bot owns.

---

## 2. How Valkalie uses message content

Valkalie uses Discord's Message Content intent for the features below. In each case the text is processed in memory and then discarded.

| Feature | What it reads | What it keeps |
|---|---|---|
| **Anti-Link / anti-scam** | Links in messages. They are checked against a blocklist, for look-alike and punycode domains, and with online URL reputation services (section 3). | If a link is malicious, the message is deleted, moderators are alerted with the reason, and a strike is recorded. The security log keeps the member ID, the channel, and the blocked domain. Nothing else from the message is kept. |
| **Anti-Spam / cross-post detection** | A one-way hash of the message (text plus attachment names and sizes), compared against your recent messages to spot the same content posted in many channels. Also how many members and roles the message mentions, and whether it combines `@everyone`/`@here` with a link. | The hash is held in memory for about two minutes. Nothing is written to disk except the strike and the security-log entry. |
| **Text-to-Speech (TTS)** | Messages in the **one** text channel a TTS session is started for, only while the session is running. If the "read names" option is on, the sender's display name is read too. | Nothing. The generated audio file is deleted after it plays. |
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
| **ngrok** | Incoming YouTube upload notifications, and traffic to the developer's private dashboard | Receive notifications from YouTube |
| **SlipOK** | Bank-transfer slip images sent with `/donate_slip` | Check that a donation slip is genuine |
| **Top.gg** | Total number of servers Valkalie is in | Bot listing |

We do not sell user data. We do not share it with anyone else unless you explicitly agree or the law requires it.

---

## 4. Donations

Valkalie has no paid features or subscriptions. Donations are voluntary support for the developer. When you donate with `/donate_slip`:
- your slip is checked with SlipOK, and the image is not kept;
- your user ID, display name, amount, slip reference number, and date are recorded so the donation is not counted twice and so you can receive the Donor role in the Valkalie server;
- your display name and total donated may appear on the `/donate_top` leaderboard.

If you do not want to appear on the leaderboard, contact us (section 8).

*Older records from a previous paid-features system (wallet balances, transaction history, and agreement acceptances) may still exist in our database. They are kept as financial records and can be deleted on request. That system's `/agreement` command is still available. If you accept an agreement with it, your user ID, the agreement version, and the time are recorded.*

---

## 5. Opting out

- **Game activity (Presence):** run `/status optout stop_tracking:True`. Valkalie stops recording your game activity in **every** server immediately and **deletes all game-activity data it has already stored about you**. Run it with `False` to turn tracking back on.
- **Stats card visibility:** set your card to *Private* with `/status set`. Only you will be able to see it.
- **Level-up DMs:** use the opt-out button on any level-up DM.
- **Text-to-Speech:** TTS only reads the channel a session is started for, and only while the session is running. If you do not want to be read aloud, do not post in that channel during a session.
- **Security scanning and command-usage records:** anti-spam, anti-link, and command-usage records cover the whole bot, so individual users cannot opt out. None of them store message content. You can still ask us to delete your records (section 7).

---

## 6. Data retention

| Data | How long we keep it |
|---|---|
| Message counts, voice sessions, emoji usage, game activity | **Deleted automatically after 90 days** |
| Command usage records | **Deleted automatically after 180 days** |
| Cross-post detection hashes | About 2 minutes, in memory only |
| Security log | The 15 most recent events per server. Older events are removed as new ones are added. |
| Security strikes | Your count starts again from zero if you get no new strike within a period the server sets (30 days by default). The record itself stays until it is deleted (see the row below). |
| Embed button-click records | Until the embed is deleted |
| Server join dates, stats-card settings, server settings, XP, forms, game results, donations, and other records | Until a server admin removes them, you ask us to delete them, or the developer removes the server's data |
| Error reports and bot log files | Until the developer clears them |
| Server data deleted by the developer | Kept in a recovery bin for 30 days, then deleted permanently |

Removing Valkalie from your server **stops all further collection** for that server. Data already collected is **not deleted automatically** when the bot is removed. Ask us (section 8) if you want it deleted.

---

## 7. Deleting your data

- **Your own game activity:** `/status optout stop_tracking:True` deletes it immediately.
- **A server's statistics:** a server admin can run `/stats_reset`. It deletes that server's message counts, voice sessions, emoji usage, game activity, member join dates, and stats-card settings.
- **Everything else:** ask through the support server or message `hoyorai` on Discord. Include your user ID, and the server ID if your request is about one server. We will delete the data within 30 days. Deleted data may stay in the recovery bin for up to 30 more days before it is erased permanently.

Server admins should note that form answers can also be copied into the server's VarTable and shown in embeds. Deleting a form does not remove those copies; the admin has to remove them from the VarTable separately.

You can also ask for a copy of the data we hold about you.

---

## 8. Contact

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
7. Donations are voluntary and do not purchase any service or feature.
8. We may update these terms and this policy. The effective date at the top of this page will change when we do.
