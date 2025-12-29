# Hacker News Monitoring

How to use Hacker News for tech buyer intelligence.

---

## Why Hacker News

- Tech decision-makers hang out here
- Brutally honest opinions (no marketing BS)
- Early signals on trends and tools
- "Ask HN" posts reveal real problems
- Competitor launches get discussed honestly

---

## Who's On Hacker News

| Role | What They Post About |
|------|----------------------|
| CTOs/VPs Eng | Architecture, team scaling, tool choices |
| Developers | Day-to-day tools, frustrations, recommendations |
| Founders | Startup problems, launches, advice requests |
| Product Managers | Product strategy, user research |

**Best for:** Selling to technical buyers, dev tools, infrastructure, B2B SaaS with technical users.

---

## What to Monitor

### 1. Competitor Mentions

When competitors launch or get discussed:
- What do people praise?
- What do people criticize?
- What alternatives do people suggest?

### 2. "Ask HN" Posts

People asking for recommendations:
- "Ask HN: What do you use for [X]?"
- "Ask HN: Best [category] for startups?"
- "Ask HN: How do you handle [problem]?"

### 3. "Show HN" Posts

New product launches:
- New competitors entering market
- How the community reacts
- Feature ideas from comments

### 4. Industry Discussions

Trends and shifts:
- New technologies
- Changing preferences
- Problems people are facing

---

## Search Techniques

### HN Search (Algolia)

Use: `hn.algolia.com`

**Search for competitor:**
```
[competitor name]
```

**Search for category:**
```
"best [category]"
"recommend [category]"
"[category] for startups"
```

**Search Ask HN:**
```
Ask HN [problem]
Ask HN [category]
```

**Filter by date:**
- Use the date filters on the left sidebar
- Check "Last 7 days" or "Last 30 days"

### Google Site Search
```
site:news.ycombinator.com "[competitor]"
site:news.ycombinator.com "looking for" "[category]"
site:news.ycombinator.com "alternative to" "[competitor]"
```

---

## Prompt Templates

**Competitor mentions:**
```
Search Hacker News for mentions of [COMPETITOR] in the last 30 days.

Summarize:
1. Overall sentiment
2. Main criticisms
3. Main praise
4. Alternatives people suggested
```

**Find buying signals:**
```
Search Hacker News for "Ask HN" posts about [CATEGORY] or [PROBLEM] in the last 90 days.

List posts where someone is looking for recommendations.
Note what requirements they mention.
```

**Track a launch:**
```
[COMPETITOR] was discussed on Hacker News: [URL]

Summarize the community reaction:
- What did people like?
- What did people criticize?
- What alternatives were mentioned?
- Any insights I can use?
```

**Trend research:**
```
What's Hacker News saying about [TREND/TOPIC]?

Look at recent discussions and summarize:
- Main opinions
- Concerns or criticisms
- Popular tools or solutions mentioned
```

---

## Valuable Post Types

### "Ask HN: What do you use for X?"

These are gold. People share their actual stack.

**Example searches:**
```
Ask HN CRM
Ask HN project management
Ask HN monitoring
Ask HN analytics
Ask HN sales tools
```

### "Ask HN: How do you handle X?"

Reveals pain points and workarounds.

**Example searches:**
```
Ask HN how do you handle onboarding
Ask HN how do you handle customer support
Ask HN how do you handle billing
```

### "Show HN: [New Product]"

Competitor launches. Read the comments for honest feedback.

### Big Discussion Threads

When a competitor raises funding, launches, or has drama - the comments are invaluable.

---

## Monitoring Workflow

### Weekly HN Check (15 mins)

1. Go to hn.algolia.com
2. Search each competitor - last 7 days
3. Search your category - last 7 days
4. Search "Ask HN" + your problem space
5. Note anything useful

### What to Capture

For each relevant thread:
```
URL: [link]
Date: [date]
Type: [Ask HN / Show HN / Discussion]
Topic: [what it's about]

Key Takeaways:
- [insight 1]
- [insight 2]

Useful Quotes:
- "[quote 1]"
- "[quote 2]"

Action Items:
- [what to do with this info]
```

---

## HN API

Hacker News has a free, open API.

### Endpoints

**Get item (post or comment):**
```
https://hacker-news.firebaseio.com/v0/item/[ID].json
```

**Get top stories:**
```
https://hacker-news.firebaseio.com/v0/topstories.json
```

**Get new stories:**
```
https://hacker-news.firebaseio.com/v0/newstories.json
```

**Get Ask HN:**
```
https://hacker-news.firebaseio.com/v0/askstories.json
```

**Get Show HN:**
```
https://hacker-news.firebaseio.com/v0/showstories.json
```

### Rate Limits

- No authentication required
- No strict rate limits (be reasonable)
- Real-time updates available via Firebase

---

## Tools for HN Monitoring

### Free Options

| Tool | What It Does |
|------|--------------|
| hn.algolia.com | Search HN with filters |
| hckrnews.com | Clean HN reader interface |
| F5Bot | Email alerts for keywords (free) |
| HNRSS | RSS feeds for HN searches |

### Setting Up Alerts

**F5Bot (recommended):**
1. Go to f5bot.com
2. Sign up (free)
3. Add keywords: competitor names, category terms
4. Get email when they're mentioned

**HNRSS:**
Create RSS feeds from HN searches:
```
hnrss.org/newest?q=[keyword]
```

Example:
```
hnrss.org/newest?q=salesforce
hnrss.org/newest?q=CRM
```

Add these to your RSS reader.

---

## Engaging on HN

### Should You Post?

HN hates marketing. But authentic participation works:

**Do:**
- Answer questions helpfully (without pitching)
- Share genuine insights from your experience
- Engage in technical discussions

**Don't:**
- Post your own product as "Show HN" unless it's genuinely new
- Shill in comments
- Create fake discussions

### Building Karma

If you want to eventually share your product:
1. Participate authentically for months first
2. Build karma through helpful comments
3. Only then consider a genuine "Show HN"

---

## Pro Tips

1. **Comments are better than posts** - Real insights are buried in replies
2. **Check "new" not just "top"** - Find discussions early
3. **Read the whole thread** - Context matters on HN
4. **Note usernames** - Some commenters are industry experts
5. **Don't take it personally** - HN can be harsh
6. **Use for research, not leads** - HN users hate being sold to
