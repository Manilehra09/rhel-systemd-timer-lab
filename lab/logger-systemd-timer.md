# Systemd Timer Practice Lab

## Step 1: Create directories

mkdir -p /var/tmp/ex200
mkdir -p /root/lookup_directory

---

## Step 2: Copy script

cp scripts/logger.sh /usr/local/bin/logger
chmod +x /usr/local/bin/logger

---

## Step 3: Copy systemd files

cp systemd/logger.service /etc/systemd/system/
cp systemd/logger.timer /etc/systemd/system/

---

## Step 4: Reload systemd

systemctl daemon-reload

---

## Step 5: Enable timer

systemctl enable --now logger.timer

---

## Step 6: Verify

systemctl list-timers

cat /root/lookup_directory/ex200
