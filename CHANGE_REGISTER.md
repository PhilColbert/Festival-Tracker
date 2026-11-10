# Change Register

This is the authoritative log of approved and proposed project changes.

| Change ID | Date | Request | Baseline | Scope | Status | Result |
|---|---|---|---|---|---|---|
| CT-001 | 2026-11-10 | Establish the Festival Tracker master specification and records in the supplied GitHub repository. | Empty repository | Documentation | FIXED | Initial project records committed. |
| CT-002 | 2026-11-10 | Remove the OLED display because the system will mainly be used through phones. | Initial recovered spec 0.1 | Hardware / UX / power assumptions | FIXED | OLED excluded; phone is primary UI. No hardware files existed or were edited. |

## CT-001 — Initial repository records
- **Request:** Create durable source-of-truth documentation in the user-provided repository.
- **Baseline:** Empty GitHub repository `PhilColbert/Festival-Tracker`.
- **Scope:** Documentation only.
- **Files:** README.md, SPECIFICATION.md, CHANGE_REGISTER.md, MANIFEST.md, VERSION_HISTORY.md.
- **Preserved functions:** Not applicable; repository was empty.
- **Checks:** Repository identity and admin/push permission verified; empty repository confirmed before writing.
- **Results:** See GitHub commit history.
- **Not performed:** No code, firmware, app, PCB, build, screenshot or device test.

## CT-002 — OLED removal
- **Request:** Remove OLED display; primary use will be through phones.
- **Baseline:** Initial recovered specification 0.1.
- **Scope:** Hardware design requirements and user interface assumptions.
- **Approved:** Yes, by user confirmation.
- **Files affected:** SPECIFICATION.md, README.md, CHANGE_REGISTER.md, MANIFEST.md, VERSION_HISTORY.md.
- **Result:** OLED excluded from the design baseline; phone-led UI recorded.
- **Preserved functions:** No existing code or hardware files were present to preserve.
- **Checks:** Documentation consistency and repository file verification.
- **Not performed:** No schematic, PCB, firmware or app modification; no compile, automated test or device test.
