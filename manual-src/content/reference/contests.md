---
title: "Contest Support"
description: "WA7BNM contest calendar, contest templates, and Cabrillo export"
weight: 9
showToc: true
---

Carrier Wave provides contest support through integration with the WA7BNM contest calendar, pre-configured session templates, and Cabrillo log export for submission to contest sponsors.

## Overview

Contest support in Carrier Wave covers:

- **Contest discovery** via the WA7BNM calendar
- **Session templates** that pre-configure mode, band, and exchange fields
- **Cabrillo export** for log submission
- **Contest-specific exchange logging** with validation

## WA7BNM Contest Calendar

### Calendar Integration

Carrier Wave polls the WA7BNM contest calendar every **6 hours** to maintain an up-to-date list of upcoming and active contests. The calendar provides:

- **Contest name** and sponsor
- **Start and end times** (UTC)
- **Bands and modes** allowed
- **Exchange requirements** (serial number, state, grid, etc.)
- **Submission URL** for log uploads

### Browsing Contests

From the session start wizard, tap **Contest** to browse:

- **Active now** - Contests currently in progress
- **Upcoming** - Contests starting within the next 7 days
- **Recent** - Contests that ended within the last 48 hours (for late log submission)

Each contest listing shows:

- Contest name
- Time window (start/end in UTC)
- Modes (CW, SSB, Digital, Mixed)
- Primary bands

### Contest Detail

Tap a contest to view full details:

- **Rules summary** extracted from the calendar
- **Exchange format** showing what information to send and receive
- **Categories** (single-op, multi-op, QRP, etc.)
- **Submission deadline**
- **Link to full rules** on the sponsor's website

## Contest Templates

### Starting a Contest Session

When you select a contest from the calendar:

1. Carrier Wave creates a session pre-configured with:
   - **Mode** matching the contest (CW, SSB, or the contest's primary mode)
   - **Exchange fields** appropriate for the contest type
   - **Contest identifier** stored in session metadata
2. The session title is set to the contest name
3. Contest-specific exchange fields appear in the QSO entry form

### Exchange Fields

Contest sessions add exchange-specific fields to the Logger:

| Exchange Type | Field | Example |
|---------------|-------|---------|
| **Serial number** | Auto-incrementing counter | 001, 002, 003... |
| **State/Province** | US state or Canadian province | CA, ON |
| **Grid square** | 4-character Maidenhead | CM87 |
| **CQ Zone** | CQ zone number | 3 |
| **ITU Zone** | ITU zone number | 6 |
| **Name** | Operator name | JOHN |
| **Custom** | Contest-specific exchange | ARRL section, power category, etc. |

### Serial Number Management

For contests requiring serial numbers:

- Serial numbers auto-increment starting from 001
- The next serial number is displayed before you log the QSO
- If you delete a QSO, the serial number is **not** reused (gaps are acceptable per contest rules)
- Serial numbers are per-session

### Duplicate Checking

Contest duplicate checking uses contest-specific rules:

- **Per-band** duplicates (most contests allow working the same station on different bands)
- **Per-mode** duplicates (some contests count CW and SSB as separate)
- **Duplicate warning** shows which band/mode combination already has a QSO with this station
- Duplicates are **not blocked** (some contests allow duplicate QSOs for band-change logging)

## Cabrillo Export

### Generating a Cabrillo File

From a contest session's detail view:

1. Tap the **Export** button
2. Select **Cabrillo (.cbr)**
3. Review the header fields
4. Share or save the file

### Header Fields

Carrier Wave auto-populates the Cabrillo header:

```
START-OF-LOG: 3.0
CONTEST: CQ-WW-CW
CALLSIGN: W6JSV
CATEGORY-OPERATOR: SINGLE-OP
CATEGORY-BAND: ALL
CATEGORY-POWER: LOW
CATEGORY-MODE: CW
CLAIMED-SCORE: 12345
CLUB:
LOCATION: CA
NAME: Your Name
ADDRESS: ...
SOAPBOX: Logged with Carrier Wave
END-OF-HEADER:
```

### Editing Header Fields

Before exporting, you can edit any header field:

- **Category fields** - Tap to select from contest-valid options
- **Claimed score** - Auto-calculated from QSO data and contest scoring
- **Soapbox** - Free-text notes about your operation
- **Club affiliation** - For club competition scoring

### QSO Records

Each QSO is formatted according to the Cabrillo specification:

```
QSO: 14000 CW 2025-11-29 1423 W6JSV 599 CA K1ABC 599 CT
```

Fields include: frequency (kHz), mode, date, time, your call, sent exchange, their call, received exchange.

### Validation

Before export, Carrier Wave validates:

- All required exchange fields are populated
- Frequency data is present for each QSO
- Time stamps are within the contest window
- **Warnings** appear for QSOs outside the contest period (they're included but flagged)

## Tips for Contest Logging

### Speed

- Use **Quick Entry** mode for fastest logging
- **Command row** buttons for frequent operations (CQ, QSY, band change)
- **Auto-incrementing serial numbers** eliminate manual tracking

### Accuracy

- Review exchange fields before logging
- Use QRZ lookup to verify callsigns
- Check the duplicate indicator before calling a station

### Submission

- Export Cabrillo **promptly** after the contest ends
- Most contests have a 5-7 day submission deadline
- Verify the Cabrillo file before uploading to the sponsor's submission page

## See Also

- [Logger](/reference/logger/) - Session management and QSO entry
- [Export & Sharing](/reference/export/) - Cabrillo and ADIF export
- [Logs & Search](/reference/logs-search/) - Browse contest QSOs with `contest:*` query
