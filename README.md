# 📡 Stream Recorder Bot

A powerful Telegram bot for recording live streams from IPTV panels and OTT platforms.

---

## 📋 Table of Contents

- [Features](#-features)
- [Commands & Usage](#-commands--usage)
  - [XTREAM IPTV Recorder](#1-xtream-iptv-recorder)
  - [SonyLIV via WATCHO](#2-sonyliv-via-watcho-ott)
  - [JioTV+ Recorder](#3-jiotv-recorder)
  - [DishHome Go Nepal](#4-dishhome-go-nepal-recorder)
  - [OTT Direct Links](#5-ott-direct-link-recorder)
- [Supported Platforms](#-supported-platforms)
- [Notes](#-notes)

---

## ✨ Features

- 🔴 **Live IPTV Recording** via Xtream Codes API with channel scanning
- 📺 **SonyLIV** channel recording via WATCHO OTT
- 📡 **JioTV+** live stream recording
- 🇳🇵 **DishHome Go Nepal** live recording
- 🌐 **Multi-OTT Support** — CrunchyRoll, Zee5, DangalPlay, SunNXT, SonyLIV, Airtel Xstream, JioHotstar & more

---

## 🛠 Commands & Usage

---

### 1. XTREAM IPTV Recorder

Scan and record live channels from an Xtream Codes server panel.

**Syntax:**
```
/xstream <channel_name> <duration> <user>:<pass> <host>:<port>
```

> **Pagination is supported** for browsing available channels.

**When you know the channel name:**
```
/xstream CNN 02:00:00 user:pass vipneeene.top:8080
```

**When you don't know the channel name** (bot will scan and let you browse):
```
/xstream 02:00:00 user:pass vipneeene.top:8080
```

| Parameter | Description | Example |
|-----------|-------------|---------|
| `channel_name` | *(Optional)* Name of the channel to search | `CNN` |
| `duration` | Recording length in `HH:MM:SS` format | `02:00:00` |
| `user:pass` | Xtream panel credentials | `myuser:mypass` |
| `host:port` | Xtream server address and port | `vipneeene.top:8080` |

---

### 2. SonyLIV via WATCHO OTT

Record SonyLIV channels using the WATCHO OTT app integration.

**Syntax:**
```
/sony "<channel_name>" <duration_seconds> -p <proxy>
```

**Example:**
```
/sony "SET MAX" 600 -p http://user:pass@proxy:port
```

| Parameter | Description | Example |
|-----------|-------------|---------|
| `channel_name` | Channel name in quotes | `"SET MAX"` |
| `duration_seconds` | Recording duration in seconds | `600` |
| `-p <proxy>` | *(Optional)* Proxy in `http://user:pass@host:port` format | `-p http://user:pass@proxy:port` |

---

### 3. JioTV+ Recorder

Record live channels from JioTV+.

**Syntax:**
```
/jnew <channelName>-<duration>
```

**Example:**
```
/jnew sonymax-00:30:00
```

| Parameter | Description | Example |
|-----------|-------------|---------|
| `channelName` | JioTV+ channel slug/name | `sonymax` |
| `duration` | Recording length in `HH:MM:SS` format | `00:30:00` |

> ⚠️ The channel name and duration are separated by a **hyphen** (`-`).

---

### 4. DishHome Go Nepal Recorder

Record live channels from the DishHome Go Nepal streaming service.

**Syntax:**
```
/dhgo <channel_slug> <duration> <ChannelName>
```

**Example:**
```
/dhgo starplus 00:00:30 "Star Plus"
```

| Parameter | Description | Example |
|-----------|-------------|---------|
| `channel_slug` | Channel identifier slug | `starplus` |
| `duration` | Recording length in `HH:MM:SS` format | `00:30:00` |
| `ChannelName` | Display name of the channel | `Star Plus` |

---

### 5. OTT Direct Link Recorder

Record directly from supported OTT platform stream URLs or slugs.

**Supported Platforms:**

| Platform | Input Type |
|----------|-----------|
| 🎌 CrunchyRoll | Direct stream URL |
| 📺 Zee5 | Direct stream URL |
| 🎬 DangalPlay | Direct stream URL |
| ☀️ SunNXT | Direct stream URL |
| 🎭 SonyLIV | Direct stream URL |
| 📡 Airtel Xstream | **Slug only** |
| 🔥 JioHotstar | Direct stream URL |

> ℹ️ Usage varies by platform. Provide the stream URL or slug as applicable for your platform.

---

## 📦 Supported Platforms

```
✅ Xtream Codes IPTV
✅ SonyLIV (via WATCHO)
✅ JioTV+
✅ DishHome Go Nepal
✅ CrunchyRoll
✅ Zee5
✅ DangalPlay
✅ SunNXT
✅ Airtel Xstream (slug)
✅ JioHotstar
```

---

## 📝 Notes

- All durations follow `HH:MM:SS` format unless specified in seconds.
- Proxies are supported where indicated using the `-p` flag.
- Channel names with spaces must be wrapped in **double quotes** `" "`.
- Xtream recorder supports **pagination** to browse channels when no name is provided.
- Airtel Xstream requires a **slug** instead of a full URL.

---

> Made with ❤️ | For support, open an issue or reach out via Telegram.
