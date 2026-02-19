# 🚀 Multi‑Tab Google Images Opener

A lightweight, client-side tool that opens multiple Google Images searches at once from a list of words. It saves time and reduces the risk of triggering Google's CAPTCHA by spacing out tab openings.

---

## How It Works

1. Enter your words in the text area, one word per line.  
2. The tool reads each non-empty line and generates a Google Images search URL for each word:
3. If **delay is off**, all tabs open instantly.  
4. If **delay is on**, the first tab opens immediately, and the rest open with a short interval using `setTimeout`, mimicking human behavior and reducing automated request flags.  

> ⚠️ Make sure to allow pop-ups for the page. Delayed tabs may be blocked by pop-up blockers.  

Fully client-side, no server or tracking required—just enter your words and open multiple Google Images tabs instantly.
