# 🎫 Ticket Claiming System - How It Works

## For End Users (Simple Explanation)

### 📌 What's New?

We've implemented a **Fair Ticket Claiming System** to prevent spam and ensure everyone gets a fair chance at claiming tickets.

---

## 🚦 Rate Limits (Anti-Spam Protection)

To keep the system fair, there are limits on how often you can attempt to claim tickets:

- **3 attempts per minute** - Maximum 3 claim attempts every 60 seconds
- **10 attempts per hour** - Maximum 10 claim attempts every hour

**What this means:**
- If you try to claim too quickly, you'll need to wait a bit
- You'll see a message like: *"Rate limit exceeded. Please wait X seconds."*

---

## ⚖️ Priority Queue System

When multiple people try to claim the same ticket, we use a **priority queue** to decide who gets it first.

### How Priority Works:

Your priority is based on:

1. **Success Rate** (Most Important)
   - If you successfully complete exchanges, you get higher priority
   - Users who claim tickets and follow through are rewarded

2. **Spam Behavior**
   - Clicking claim repeatedly without success lowers your priority
   - The system learns who is a reliable exchanger

3. **Recent Activity**
   - If you just attempted a claim (within 30 seconds), your priority temporarily drops
   - This prevents the same person from grabbing every ticket

**Example:**
- User A: 80% success rate, 20 completed exchanges → High Priority
- User B: 30% success rate, lots of failed attempts → Low Priority
- If both try to claim the same ticket, User A gets it first

---

## ⏱️ Progressive Penalties

If you spam the claim button or make too many failed attempts, the system applies temporary cooldowns:

| Failed Attempts (Last Hour) | Cooldown Time |
|-----------------------------|---------------|
| 5 failed attempts           | 2 minutes     |
| 10 failed attempts          | 5 minutes     |
| 20 failed attempts          | 15 minutes    |
| 50 failed attempts          | 1 hour        |

**What happens:**
- You'll see: *"You are temporarily restricted from claiming tickets. Please wait X minutes."*
- Cooldown resets once the time expires
- **Tip:** Only claim tickets you can actually complete!

---

## 🔒 Ticket Locking

When someone clicks "Claim Ticket," the ticket is **locked for 45 seconds** to prevent conflicts.

**What you'll see:**
- If someone is processing: *"This ticket is currently being processed by another agent. Please wait X seconds."*
- The lock automatically releases after 45 seconds if processing fails
- This prevents two people from claiming the same ticket at once

---

## 📋 Queue System

If a ticket is locked or being processed, you can be added to a **queue**:

**How it works:**
1. You click "Claim Ticket" but someone else is processing it
2. You're added to the queue: *"You have been added to the queue (Position: 2)"*
3. When the ticket becomes available, users are processed in priority order
4. Higher priority users move ahead in the queue

**Queue Position:**
- Position 1: You're next in line
- Position 2+: Other users are ahead of you
- Your position can change based on priority calculations

---

## ✅ Benefits of Good Behavior

The system **rewards reliable exchangers**:

### You Get Higher Priority If:
- ✅ You successfully complete exchanges (high success rate)
- ✅ You only claim tickets you can handle
- ✅ You wait reasonable time between attempts
- ✅ You accept TOS and follow through

### You Get Lower Priority If:
- ❌ You spam the claim button repeatedly
- ❌ You claim tickets but don't complete them
- ❌ You have many failed attempts
- ❌ You try to claim too quickly after another attempt

---

## 🎯 Tips for Users

### How to Maximize Your Success:

1. **Only claim tickets you can complete**
   - Check your balance first
   - Make sure you have TOS setup for that payment method
   - Verify you can fulfill the exchange

2. **Don't spam the claim button**
   - If you get rate limited, wait the cooldown period
   - Spamming will only increase your penalties

3. **Build your reputation**
   - Complete exchanges successfully to build a good success rate
   - Higher success rate = higher priority for future tickets

4. **Wait between attempts**
   - If you just tried to claim a ticket, wait 30+ seconds before trying another
   - This prevents temporary priority drops

5. **Read error messages**
   - The system tells you exactly why you can't claim
   - Follow the instructions (wait time, setup TOS, etc.)

---

## 📊 What You'll See (User Messages)

### ✅ Success Messages:
- `"✅ You have successfully claimed this ticket!"`

### ⏱️ Rate Limit Messages:
- `"⏱️ Rate limit exceeded. You can make up to 3 attempts per minute. Please wait X seconds."`
- `"⏱️ Hourly rate limit exceeded. You can make up to 10 attempts per hour. Please wait X minutes."`

### ⚠️ Penalty Messages:
- `"⚠️ You are temporarily restricted from claiming tickets. Please wait X minutes."`

### 🔒 Lock Messages:
- `"🔒 This ticket is currently being processed by another agent. Please wait X seconds."`

### 📋 Queue Messages:
- `"📋 You have been added to the queue (Position: 2). You will be notified when it's your turn."`
- `"📋 You are in the queue for this ticket (Position: 3). Please wait for your turn."`

### ❌ Error Messages:
- Balance issues: Shows your balance vs required amount
- TOS missing: Instructions on how to setup TOS
- Wallet suspended: Contact support

---

## 🤔 Frequently Asked Questions

**Q: Why can't I claim tickets as fast as before?**
A: The rate limits prevent spam and ensure fair distribution. 3 attempts per minute is reasonable for genuine claims.

**Q: How do I improve my priority?**
A: Complete exchanges successfully! Your success rate is the biggest factor in priority.

**Q: I'm getting penalties but I'm not spamming!**
A: Penalties are based on failed attempts in the last hour. Make sure you can complete tickets before claiming.

**Q: How long do penalties last?**
A: Penalties range from 2 minutes to 1 hour depending on how many failed attempts you've made.

**Q: What counts as a "failed attempt"?**
A: Any claim attempt that doesn't result in a successful claim:
- Insufficient balance
- Missing TOS
- Ticket already claimed
- Rate limit hit

**Q: Can I see my stats?**
A: Currently no, but this feature may be added in the future.

**Q: The system seems unfair, I never get tickets!**
A: The system prioritizes users with higher success rates. Focus on completing the tickets you do claim, and your priority will improve over time.

---

## 🛠️ For Administrators

If you need to check system stats or user behavior, exported functions are available:
- `getCacheStats()` - Overall system statistics
- `getUserStats(userId)` - Individual user statistics

These can be integrated into admin commands if needed.

---

## 📝 Summary

The new system ensures:
- ✅ **Fair distribution** - Everyone gets a chance based on reliability
- ✅ **No spam** - Rate limits keep the system responsive
- ✅ **Quality exchangers rewarded** - Good behavior = better access
- ✅ **Transparent** - Clear messages explain why you can/cannot claim

**Bottom Line:** Be a reliable exchanger, don't spam, and you'll have great access to tickets! 🎉

