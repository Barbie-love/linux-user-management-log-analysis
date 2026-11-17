# Screenshot checklist

Save your own screenshots in this folder. Use PNG format where possible and descriptive filenames. The filenames below are suggestions; adjust them to match the evidence you actually capture.

Suggested screenshots:

1. `01-forensic01-created.png` – evidence that forensic01 was created with the required home directory and shell.
2. `02-forensic01-sudo-group.png` – evidence that forensic01 belongs to the sudo group.
3. `03-forensic01-login.png` – terminal showing the session as forensic01.
4. `04-log-file-created.png` – directory listing and/or log file showing at least 20 mock log lines.
5. `05-grep-error.png` – lines matching ERROR.
6. `06-grep-root-user01.png` – lines matching root or user01.
7. `07-head-tail-cat.png` – first five, last five, and full log viewing evidence.
8. `08-error-report-saved.png` – evidence that error_report.txt was saved and contains output.
9. `09-confidential-permissions.png` – `ls -l` output showing the file permissions.
10. `10-confidential-root-owner.png` – evidence showing root ownership.
11. `11-confidential-access-test.png` – actual result of the read/edit attempt as forensic01.
12. `12-temporary-users.png` – evidence of guest1/guest2 creation and guest1 sudo membership.
13. `13-guest2-deleted.png` – evidence that guest2 was removed, including its home directory.

Only include screenshots for steps you actually performed. Make sure terminal text is readable and avoid showing passwords or other secrets.
