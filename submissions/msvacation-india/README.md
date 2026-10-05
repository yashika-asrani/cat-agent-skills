# msvacation-india — MS Vacation assistant for India-based teams

A Copilot Cowork skill for Microsoft's internal leave site **MS Vacation** (https://msvacation.microsoft.com).
It works for **whoever is signed in**. It has no personal data in it. Your alias, approver, company/location and
usual CCs are all looked up when the skill runs.

## What it does
- **Leave summary**: balances per leave type, optional holidays left, upcoming fixed and optional holidays,
  pending approvals and upcoming approved leave. It reads the MS Vacation site, or your MS Vacation emails
  as a fallback.
- **Book leave**: fills the New Request form for you (dates, leave type, comment, CC Line), clicks Add and Next,
  then **stops once** before Submit. You see a summary and a screenshot, then choose Submit, Change something
  or Cancel.
- **Leave history with reasons**: pairs your "pending approval" and "approved" mails to rebuild what you took and why.
- **Festival / long-weekend planner (India)**: works with Diwali, Navratri/Dussehra, Ganesh Chaturthi, Holi,
  Pongal/Sankranti, Ugadi/Gudi Padwa, Ram Navami, Onam, Christmas and New Year. It plans bridge days, uses
  optional holidays (Floating Public Holiday) and suggests WFH days, then shows your balance after each option.

## Install
Use one of these:
1. **Copy the folder.** Unzip and copy the `msvacation-india` folder (with `SKILL.md` inside) into your OneDrive:
   `Documents/Cowork/skills/msvacation-india/`. The skill is picked up when your next Cowork session starts.
2. **Upload it.** In Copilot Cowork, ask "create a skill from this file" or use the skills feature to upload
   `SKILL.md`.

Keep the folder name `msvacation-india` because it must match the `name:` in SKILL.md.

## Example prompts
- "What's my leave balance?" / "How many optional holidays do I have left?"
- "Show upcoming holidays"
- "Is my leave approved?"
- "apply AL 22-23 Oct, comment family function, cc <alias>"
- "Take an optional holiday on <date>"
- "What leaves did I take this year and why?"
- "Plan a long Diwali break with the fewest leave days"

## First-run notes
- **Approve browser access** when Cowork asks. The skill drives your local browser to open MS Vacation.
- **Be signed in to MS Vacation** (corporate SSO/MFA). If a sign-in prompt appears, complete it yourself.
  The skill never types or stores credentials.
- Approve the people, mail and calendar lookups when asked. These are used to find your alias, approver,
  CC aliases and calendar conflicts.
- **Nothing is submitted without your explicit "yes".** The skill also never sends an email or sets an
  auto-reply without asking you.
- Your approver comes from MS Vacation and is notified automatically, so it is never added to the CC Line.
