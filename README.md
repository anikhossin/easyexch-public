## Easy Exchange

Easy Exchange is a Discord-based P2P escrow service that helps users convert between **fiat currencies** and **cryptocurrencies** safely, using a bot to coordinate trades and hold funds in escrow during each transaction.

This repository is the public hub for **user-facing information, issue tracking, and the wiki**. It does **not** contain the full private implementation of the service.

---

## What Easy Exchange Does

- **P2P fiat ⇄ crypto trades**: Connects users who want to buy or sell crypto using supported fiat payment methods.
- **Escrow-style bot**: A Discord bot coordinates the trade, holds funds (or proofs) in escrow, and releases them when both sides fulfill their obligations.
- **Dispute handling**: If something goes wrong, a dispute flow allows moderators to review trade data and make a final decision.
- **Auditability**: Key actions are logged to help resolve disputes and improve trust in the system.

Easy Exchange aims to provide a **simple, chat-native way** to perform small to medium-size trades, focusing on clarity and safety-first UX.

---

## How It Works (High Level)

1. **Join the Discord server**  
   You access Easy Exchange via our official Discord server (link provided by the team).

2. **Verify & read the rules**  
   You may need to pass basic verification (e.g. captcha / introductions) and must read the trading rules.

3. **Create or respond to an offer**  
   - One party creates an offer to buy or sell a given crypto asset for a given fiat currency.  
   - Another party accepts that offer.

4. **Escrow and payment**  
   - The bot guides both users through the required steps (sending crypto, sending fiat, confirming receipt, etc.).  
   - Funds are held in escrow (or the bot tracks on-chain / payment proofs) until conditions are met.

5. **Completion or dispute**  
   - If everything checks out, the bot releases the escrowed asset and the trade is marked as completed.  
   - If there is a problem, users can open a dispute; moderators then use the bot’s logs and provided evidence to resolve it.

Exact commands, flows, and supported assets/payment methods are documented in the **Wiki**.

---

## Safety, Risks & Disclaimers

- **No financial advice**  
  Easy Exchange and its maintainers do **not** provide investment, trading, or financial advice. You are solely responsible for your decisions.

- **Use at your own risk**  
  P2P trading always carries risk (counterparty risk, chargebacks, volatile prices, scams, etc.). The escrow bot reduces but does not eliminate these risks.

- **Jurisdiction & compliance**  
  You are responsible for complying with the laws and regulations of your jurisdiction, including any restrictions on using cryptocurrency or P2P exchanges.

- **KYC and limits**  
  Depending on region and regulation, we may require KYC/identity verification or impose limits. See the **Wiki** or server rules for current policies.

- **Security**  
  Never share private keys, seed phrases, or sensitive account credentials with anyone, including staff. The bot will **never** ask for this information.

By using Easy Exchange or interacting with the Discord bot, you acknowledge that you have read and understood these risks and disclaimers.

---

## Getting Started as a User

1. **Get an invite link** to the official Easy Exchange Discord server from a trusted source (our website, staff member, or official announcement).
2. **Complete onboarding**: follow any verification steps and read the rules and FAQ channels.
3. **Review the Wiki** (linked from the server and this repository) for:
   - Supported coins and networks  
   - Supported fiat methods and regional notes  
   - Trade limits, fees, and timelines  
   - Example trade flows and screenshots
4. **Try a small test trade** first to become familiar with the interface and process.

If anything is unclear, ask in the designated help/support channel on Discord before trading larger amounts.

---

## Issues & Bug Reports

Use this GitHub repository’s **Issues** tab to report:

- **Bugs** in the Discord bot or service behavior  
- **Incorrect or unclear documentation** (including Wiki pages)  
- **UX problems** (confusing flows, misleading messages, missing confirmations)  
- **Feature requests** that could improve safety, usability, or clarity

### Before You Open an Issue

- **Check existing issues** to see if your problem or request is already reported.  
- **Check the Wiki** and Discord announcements in case the behavior is already explained or intentionally changed.

### What to Include in a Bug Report

Please provide as much detail as possible, for example:

- **Short summary** of what went wrong  
- **Exact steps to reproduce** (commands used, order of actions, etc.)  
- **Expected vs. actual behavior**  
- **Screenshots or copied bot messages** (redact sensitive info!)  
- **Trade ID / reference** if the issue relates to a specific trade

For anything that might be **security-sensitive** (e.g. ways to bypass escrow, steal funds, or leak private data), please follow the **Security & Responsible Disclosure** section below instead of posting full details publicly.

---

## Security & Responsible Disclosure

We highly value reports of vulnerabilities or weaknesses that could impact user funds or privacy.

- **Do not post exploit details publicly** in GitHub Issues or Discord.  
- Instead, contact the maintainers via the **security contact method** listed in the repository’s Security Policy or project Wiki.  
- Provide a clear description, steps to reproduce, and any relevant logs or screenshots.

We will review reports as quickly as possible and may coordinate a fix and responsible disclosure with you.

---

## Wiki

The **Wiki** is the primary source of in-depth documentation. It typically includes:

- **User guides**: how to initiate trades, read bot messages, handle disputes, etc.  
- **Supported assets & networks**: currently supported cryptocurrencies and chains.  
- **Payment methods**: supported fiat rails, recommended practices, and region-specific notes.  
- **Policies & rules**: trade limits, dispute policies, banned behavior, and moderation guidelines.  
- **Changelog / release notes**: notable changes in bot behavior and features.

If something feels missing or outdated in the Wiki, please **open an Issue** or suggest edits according to any contribution guidelines provided there.

---

## Contributing

This project’s core codebase is private, but:

- We **welcome feedback and suggestions** via GitHub Issues.  
- We may occasionally open specific public tasks or documentation issues for community help.  
- If you are interested in contributing in a more involved way, reach out to the maintainers via the contact details provided in the Wiki or Discord server.

Please be respectful, concise, and constructive in all interactions; our goal is to keep Easy Exchange safe and welcoming for everyone.

---

## Contact & Support

For **general support**, use the designated support/help channels in the Discord server.  
For **documentation questions**, open an Issue or comment on relevant Wiki pages (if enabled).  
For **security issues**, follow the **Security & Responsible Disclosure** section above.

If you are reading this on a mirror or third-party site, please verify that you are using the **official Discord server and links** provided in this repository or by trusted announcements from the Easy Exchange team.


