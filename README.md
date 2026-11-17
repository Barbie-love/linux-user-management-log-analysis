# Linux Task 03 – User Management, Log Analysis and Permissions

## Project overview
This repository documents the Linux Task 03 practical activity. It covers:

1. Creating and configuring the `forensic01` user.
2. Creating a mock system-events log and filtering it with text-processing commands.
3. Managing file permissions and ownership.
4. Creating, modifying and deleting temporary users.

**Important:** Complete the practical work in your own Linux environment. Add your actual command history, terminal output and screenshots. Do not claim a step is complete until you have performed it.

## Repository structure

```text
linux-task-03/
├── README.md
├── .gitignore
├── commands_used.txt
├── docs/
│   ├── workflow.md
│   └── results-and-reflection.md
├── evidence/
│   ├── README.md
│   ├── error_report.txt
│   └── log_analysis/
├── screenshots/
│   └── README.md
└── notes/
    └── README.md
```

## Requirements
- A Linux system or Linux virtual machine.
- A user account with `sudo` privileges.
- Terminal access.

## How to use this repository
1. Read [`docs/workflow.md`](docs/workflow.md).
2. Perform each part of the task in order.
3. Record the exact commands you personally run in `commands_used.txt`.
4. Save terminal screenshots in `screenshots/` using the checklist in `screenshots/README.md`.
5. Save actual output files in `evidence/`.
6. Complete [`docs/results-and-reflection.md`](docs/results-and-reflection.md).
7. Review the repository before pushing it to GitHub.

## Safety notes
- Use this exercise only on a Linux machine you own or are authorized to administer.
- Be careful when using `sudo`, changing ownership, and deleting users.
- The task specifically asks to delete `guest2` including its home directory. Verify the username before running the deletion command.
- Do not put passwords, private keys, personal data, or unrelated system logs in this repository.

## Submission checklist
- [ ] `commands_used.txt` contains the exact commands used.
- [ ] Screenshots show the required terminal evidence.
- [ ] `evidence/error_report.txt` contains the actual saved grep output.
- [ ] `docs/results-and-reflection.md` is completed.
- [ ] No passwords or sensitive information are included.
