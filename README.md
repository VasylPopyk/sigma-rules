# Sigma Detection Lab: Local Account Creation (T1136.001)

A practical detection engineering lab demonstrating how to write, validate, convert, and test a **Sigma** detection rule for local Windows user creation via `net.exe` / `net1.exe` (`net user <username> /add`).

## Repository Contents
- `net_user_add.yml` — Custom Sigma rule targeting Windows process creation events (`MITRE ATT&CK T1136.001`).
- `converted_query.txt` — Rule compiled via `sigma-cli` into a **Lucene** query using the **Sysmon** processing pipeline.
- `RESULTS.md` — Positive and negative test validation results recorded against live Windows Server Sysmon Event ID 1 telemetry.

# Лабораторна робота Sigma: Виявлення створення локального облікового запису (T1136.001)

Практичний кейс із Detection Engineering: написання, валідація, конвертація та тестування правила **Sigma** для виявлення створення локальних користувачів Windows через утиліти `net.exe` / `net1.exe` (`net user <username> /add`).

## Вміст репозиторію
- `net_user_add.yml` — Власне Sigma-правило для подій створення процесів у Windows (`MITRE ATT&CK T1136.001`).
- `converted_query.txt` — Правило, скомпільоване за допомогою `sigma-cli` у пошуковий запит **Lucene** з використанням пайплайну **Sysmon**.
- `RESULTS.md` — Звіт із результатами позитивного та негативного тестування на реальних логах Sysmon (Event ID 1) у Windows Server.

