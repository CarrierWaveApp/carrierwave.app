---
title: "Equipment Catalog"
description: "Structured equipment inventory, catalog matching, and usage tracking"
weight: 8
showToc: true
---

Carrier Wave includes a structured equipment catalog that replaces the legacy string-based equipment lists. Equipment items have detailed specs (bands, modes, portability, power) that power activation recommendations and usage analytics.

## Equipment Inventory

Your equipment inventory is the list of gear you own. Each item is either a **catalog item** (matched to the server-maintained catalog) or a **custom item** (manually entered).

### Adding Equipment

Add equipment from the inventory picker, available when starting a session or in Settings. Search the catalog by name — fuzzy matching suggests alternatives if your exact model isn't found ("did you mean?").

### Custom Equipment

If your gear isn't in the catalog, add it as a custom item with editable specs. Custom items show an "Is this a...?" banner if a close catalog match exists, letting you link it to the catalog entry for richer data.

Custom equipment is anonymously submitted to the server for catalog review, helping expand the catalog over time.

### Migration from Legacy Lists

When upgrading, an interactive migration sheet helps convert your old string-based equipment lists to structured catalog items. Each item shows:

- **Confidence indicator** for the fuzzy match quality
- **Manual search** to find the correct catalog entry
- **"Keep as Custom"** to preserve the item as-is

## Catalog

The equipment catalog is maintained on the activities server and cached locally with ETag-based refresh (24-hour interval). View cache status in **Settings -> External Data**.

## iCloud Sync

Equipment inventory syncs across devices via iCloud Key-Value Storage using a structured EquipmentRef format. The sync format is backward-compatible with CW Sweep.

## Session Equipment

Select equipment when starting a session using the unified inventory picker. Equipment usage is tracked per-session for analytics and activation recommendations.

## See Also

- [Logger](/reference/logger/) - Session management and equipment selection
- [Settings & Services](/reference/settings/) - External data cache management
