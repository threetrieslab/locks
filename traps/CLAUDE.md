# Real data in this folder (rules)

- Every data file here (databases, spreadsheets, exports) is my real data and the only copy. Treat it that way.
- Before you run anything that can write data (tests, scripts, migrations, imports, "setup" or "reset" commands), check which database or file it will touch. Read the setup code first.
- Tests and experiments never touch real data. If you can't tell what a command will touch, ask me before you run it.
- Before any command that might change data, make a dated backup copy next to it (for example backups/shop-2026-11-13.db) and tell me where it is.
- If data changed or went missing, stop and tell me right away. Don't try to rebuild it from memory.
