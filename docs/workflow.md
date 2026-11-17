# Practical workflow

Follow the task in the supplied Linux Task 03 document. Commands below are guidance; adapt paths only when required by your environment and record the exact commands you execute in `commands_used.txt`.

## Part 1 – New user setup

1. Create a user named `forensic01` with a home directory and `/bin/bash` as its login shell.
2. Add `forensic01` to the `sudo` group.
3. Set a password interactively. **Do not write the password in this repository.**
4. Log in as `forensic01`.
5. Create `/home/forensic01/logs/`.
6. Create `sys_events.log` using `cat` and `echo`, containing at least 20 lines of mock log entries. Include timestamps and examples containing `ERROR`, `WARNING`, `INFO`, `user01`, and `root`.

Suggested command patterns (run only in your authorized lab environment):

```bash
sudo useradd -m -s /bin/bash forensic01
sudo usermod -aG sudo forensic01
sudo passwd forensic01
su - forensic01
mkdir -p /home/forensic01/logs
cd /home/forensic01/logs
```

Use `cat` and `echo` to create/populate the log file. Make your own mock entries; these are test data, not real system logs.

## Part 2 – Log filtering and analysis

From the directory containing `sys_events.log`:

```bash
grep "ERROR" sys_events.log
grep -E "root|user01" sys_events.log
grep "ERROR" sys_events.log | less
grep "ERROR" sys_events.log > error_report.txt
head -n 5 sys_events.log
tail -n 5 sys_events.log
cat sys_events.log
```

The task asks you to pipe the grep results to `less` for viewing and save the ERROR results in `error_report.txt`. If you also save the `root`/`user01` results, use a separate clearly named output file.

Copy the actual saved `error_report.txt` into this repository's `evidence/` folder after confirming it contains your output.

## Part 3 – Permissions and ownership

1. Create `confidential.txt` inside the `logs/` directory.
2. Use `chmod` so the owner has read/write access and group/others have no access. The intended permission mode is `600`.
3. Use `sudo chown` to change the file owner to `root`.
4. As `forensic01`, try reading or editing the file and record what happened.

Suggested command patterns:

```bash
touch confidential.txt
chmod 600 confidential.txt
sudo chown root confidential.txt
ls -l confidential.txt
cat confidential.txt
```

The file's contents and the observed access result depend on what you actually did. Record the real result; do not invent an error message.

## Part 4 – User management commands

1. Create the temporary users `guest1` and `guest2`.
2. Add `guest1` to the `sudo` group.
3. Remove `guest2` from the system, including its home directory.

Suggested command patterns:

```bash
sudo useradd -m guest1
sudo useradd -m guest2
sudo usermod -aG sudo guest1
sudo userdel -r guest2
```

Before deleting, verify that the username is exactly `guest2`.

## Evidence and screenshots

Use `screenshots/README.md` for the screenshot checklist. Capture your own terminal outputs, including user/group checks, grep results, first/last lines, permissions/ownership (`ls -l`), the access test, and the temporary-user operations.

## Before submission

- Check that every screenshot is readable and named clearly.
- Check that `commands_used.txt` contains the commands you really ran.
- Check that `evidence/error_report.txt` is your actual output, not an empty placeholder.
- Complete `docs/results-and-reflection.md`.
