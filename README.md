# RHEL Systemd Timer Lab

This repository contains a **practice lab for configuring a systemd timer in RHEL / RHCSA environments**.

The lab demonstrates how to:

* Create a custom script
* Configure a systemd service
* Configure a systemd timer
* Run tasks automatically every 1 minute

---

## Lab Objective

Create a script that collects logs from:

```
/var/tmp/ex200
```

and writes the output to:

```
/root/lookup_directory/ex200
```

The script should run automatically every **1 minute** using **systemd timers**.

---

## Repository Structure

```
lab/        → Step-by-step lab instructions
scripts/    → Script used by the service
systemd/    → systemd service and timer files
images/     → Architecture diagram
```

---

## Workflow

```
logger.timer
        ↓
logger.service
        ↓
/usr/local/bin/logger
        ↓
/root/lookup_directory/ex200
```

---

## Requirements

* RHEL 8 / RHEL 9
* Root or sudo access
* systemd

