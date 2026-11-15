# GG Eazy: Conversational Photo Search for Google Photos

**Find a photo by describing the moment, not by guessing keywords or dates.**
NextLeap Product Manager Fellowship project · Oct 2026

🔗 **[Try the MVP chat](ADD-YOUR-N8N-CHAT-LINK)** · **[Design preview (Lovable)](ADD-YOUR-LOVABLE-LINK)** · **[Full deck (PDF)](NL_GGEAZY.pdf)**

---

## The problem

People remember a photo as a story: who was there and what they were doing. Google Photos search often needs the right keyword, date or place, so people guess, scroll by hand, or give up.

> *"Main photo ko keywords ke form mein remember nahi karta."* (I don't remember photos as keywords. 24 yrs)

**North Star: Session Success Rate**, the share of photo-search sessions where the user finds the photo within 3 tries.

## Research

| Source | What it showed |
|---|---|
| **Survey** (n=18) | 17 of 18 tried to find a half-remembered photo; **13 of 18** missed on the first try; only 3 remembered roughly when it was taken; 9 of 18 scrolled by hand |
| **5 user interviews** | **5 of 5** remember people or events more than dates; 5 of 5 retry words or scroll; 3 of 5 want search that understands normal sentences |
| **Discovery Engine** (n8n AI agent): 41 public reviews tagged across 9 fields | 23 reviews about finding photos, and **none** describes a quick find |

## Target user

Google Photos users in India aged 18–25, with 3+ years on the app and 5,000+ photos. **The Story-Rememberer** wants to describe the moment and see only a few right photos.

## Solution and prioritisation

| Option | Reach | Impact | Confidence | Effort | RICE |
|---|---|---|---|---|---|
| **A: GG Eazy chat** ✅ | 4 | 4 | 3 | 2 | **24** |
| C: "I only remember…" filters | 3 | 3 | 4 | 3 | 12 |
| B: Sentence search box | 4 | 3 | 3 | 4 | 9 |

The chat asks one short question at a time about what's missing, and you can say "not this one" to narrow the results.

## MVP

- A public chat page (n8n) with an AI agent that turns what you remember into a search.
- It remembers the conversation, so follow-up replies narrow the results.
- It handles stories, follow-up questions and Hinglish.
- Photos come from Unsplash, because Google closed full-library API access in March 2025. The next step is real photos through Google's Picker API.
- A UI prototype was designed in Lovable.

## Tests and next steps

| Test | Input | Result |
|---|---|---|
| Story | "my parents during Diwali at home" | ✅ Pass |
| Refine | "No, it was daytime and just my mother was in it" | ✅ Pass (loose match) |
| Hinglish | "farewell wali photo" | ⚠️ Pass, 1 bug (old chat context leaked) |

**Next:** a new chat for every visitor, "I think" captions, real photos through the Picker API, and testing with 5+ users from the target segment.

## Success metrics

| Metric | Proposed target |
|---|---|
| Session Success Rate (North Star) | Above 50% (baseline: 2 of 8 found the photo quickly) |
| Tries per search | 3 or fewer |
| Cue pick-up (cues understood ÷ cues given) | 80% or more |
| Reply time | Under 5 seconds |

## Tools

n8n (AI agent and chat) · Lovable (UI prototype) · Unsplash API · Google Forms · RICE prioritisation
