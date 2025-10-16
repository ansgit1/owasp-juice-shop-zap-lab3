# OWASP Juice Shop — ZAP Lab (Lab 3)

**Environment**

* Kali Linux (VM)
* OWASP Juice Shop running via Docker (`docker run --rm -p 3000:3000 bkimminich/juice-shop`)
* OWASP ZAP (used as proxy + scanner)

**Purpose (brief)**
This was to lab  learn ZAP basics: how to map an app, run scans, and understand alerts. Not an expert report — mostly learning and practice.

**What I did**

* Set up Juice Shop on Kali via Docker.
* Used ZAP as a proxy to monitor traffic.
* Explored the app manually (site tree, clicking around).
* Ran Spider and AJAX Spider to discover endpoints.
* Performed Baseline / Active Scan and Fuzzing on inputs.
* Checked History and Alerts after each run.

**Files saved**

* `AJAX spider result.session`
* `juice shop localhost.png`
* `juice-zap-pre-spider.session`
* `juice-zap-spider.session`
* `random fuzzing.png`
* `sites-tree-post-spider.png`
* `zap active scan report.csv`
* `zap active scanning report.csv`
* `zap active scanning.png`
* `ZAP alerts.png`
* `zap fuzzer alert.raw`
* `ZAP spidering.png`
* `zap sql injection alert.raw`

**Key observation**

* Found a timing-based indication that may be **SQL injection** (detected during AJAX Spider timing). This needs manual reproduction to confirm.

**What I learned (short)**

* How to map an app (site tree, spidering).
* How to run ZAP scans (baseline, active, fuzzer).
* How ZAP prioritizes alerts by color: **Red = High**, **Orange = Medium**, **Yellow = Low**, **Grey/White = Info**.
* Importance of reproducing scanner alerts manually before reporting.

