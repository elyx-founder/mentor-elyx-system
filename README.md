ELYX
AI Accountability Mentor
Not a chatbot. An accountability system.

What is ELYX?
ELYX is an AI-powered personal accountability mentor that actually holds you accountable — not with notifications and streaks, but with real consequences. It rejects your fake proof. It guilt trips you when you miss a day. It remembers everything.

Built solo, zero budget, in 74 days as a 1st year AIML student. Started January 5, 2026. Launched March 2026.

The core insight: Most productivity apps make you feel productive. ELYX makes you actually be productive.

The Problem
Every student and young professional has the same loop:

•	Set a goal on Sunday night
•	Feel motivated for 2 days
•	Life happens. Excuses happen.
•	Repeat next Sunday.

Existing tools — Notion, Todoist, even ChatGPT — are passive. They wait for you to show up. They never call you out. They never say 'you said you would do this. Prove it.'

ELYX does exactly that.

The Solution
ELYX is a 3-step system:

Step 1 — Set Your Goal
Tell ELYX your one big goal. It does not forget. Every mission, every reply, every nudge is built around this specific goal.

Step 2 — Complete Daily Missions
ELYX generates 3 missions every day — not generic tasks, but specific actions tied to your goal. Complete them and submit proof.

Step 3 — Submit Proof
Photo proof = instant approval. Text proof = AI-validated. Vague answers get rejected. Fake progress gets caught. Real work gets rewarded with Elite Coins and level-ups.

Tech Stack

Frontend	Vanilla HTML + CSS + JavaScript (single file)
AI	Google Gemini 1.5 Flash (primary) + OpenRouter (fallback)
Backend	FastAPI (Python) — REST API
Database	Supabase (PostgreSQL) — user data, messages, tasks
Hosting	GitHub Pages (frontend) + Render.com (backend)
Analytics	Microsoft Clarity — session recordings, heatmaps
Budget	₹0 — entirely on free tiers

Architecture

Frontend — elyx_v6.html
A single self-contained HTML file deployed on GitHub Pages. No build tools, no frameworks. Chosen for speed of iteration and zero cost.

•	Boot screen with psychological hook sequence
•	Single-page onboarding — name, profession, goal, tone selector
•	Cinematic mentor intro with profession-specific personal message
•	4-tab dashboard — Mentor (chat), Missions, Status, Rank
•	Proof submission modal — camera photo or text
•	Elite Coins system + level rewards (6 mentor personalities unlock at each level)
•	Global leaderboard with real-time activity
•	Viral share card — auto-triggers after every 3 completed tasks
•	Language detection — replies in Hinglish or English based on user input
•	Daily browser notifications (8 PM reminder)

Backend — main.py (FastAPI)
Python FastAPI server deployed on Render.com. Handles auth, AI calls (keeping API keys secure), conversation history, and task management.

•	POST /auth/signup — creates user account
•	POST /auth/login — returns JWT token
•	POST /chat/message — calls Gemini with full context + history
•	GET /tasks/today — fetches today's tasks
•	POST /tasks/generate — generates goal-specific tasks via Gemini
•	POST /tasks/proof — validates proof with AI, awards coins
•	GET /leaderboard — returns ranked users

Database — Supabase
Three tables:

users     — id, email, name, profession, goal, tone, level, coins, streak
messages  — id, user_id, role, content, created_at
tasks     — id, user_id, date, emoji, title, description, coins, status, proof

Key Features

Hyper-Personalized AI
Every AI response includes: user's name, exact goal, profession, level, day of week, time of day, streak, completion rate, and skipped tasks. The AI knows it is Thursday evening and that the user skipped their English task. It references this.

Strict Proof System
Text proof requires minimum 10 words with specific details — time spent, what exactly was done, measurable output. Vague answers like 'I did it' or 'done' are rejected with a shake animation. Photo proof is accepted instantly (camera opens directly).

Streak Guilt Mechanic
Miss one day — streak continues. Miss two or more days — ELYX calls it out on return: 'You were gone for 3 days. That gap is a choice. Streak reset. Day 1 again.' No sugar-coating.

Level Rewards System
6 levels, each unlocking a new mentor personality:
•	Level 0 — INITIATOR — ZERO (dark, magnetic)
•	Level 1 — SEEKER — BLAZE (electric hype)
•	Level 2 — BUILDER — TITAN (military discipline)
•	Level 3 — DOMINATOR — VULCAN (brutal, fact-based)
•	Level 4 — ELITE — APEX (cold elite peer)
•	Level 5 — APEX — ORACLE (philosophical)

Hinglish Support in next version
AI detects language from user input using keyword matching + Unicode Devanagari detection. If the user writes in Hinglish, the mentor replies in Hinglish. Language is passed to backend and injected into system prompt.

Early Traction

Metric	Result
Beta users tested	37+
LinkedIn post impressions	4000+ in 6 days
Feedback rounds	5 rounds, 30+ reviews
5-star user quote	"Boards prep ke liye use kar rahi hoon. Love it."

What I Learned

•	Ship first, perfect later. The first version was terrible. That is fine.
•	Real user feedback beats assumptions every time. 5 rounds of feedback completely changed the product.
•	Cold start is a real problem. Free tier Render takes 50 seconds to wake up — users leave in 12 seconds.
•	Hinglish is not optional for Indian products. It is required.
•	Design can hide broken UX. Microsoft Clarity recordings showed users clicking dead buttons that looked fine visually.
•	Personal AI > generic AI. When the AI knows your exact goal, day of week, and skipped tasks — it feels completely different.

What's Next

•	React Native mobile app — browser notifications are not enough
•	Paid tier — ₹199/month for unlimited AI + cloud sync
•	B2B — sell to coaching institutes and colleges
•	Custom domain — getelyx.com
•	Proper onboarding flow with interactive tutorial

Links

Live Product: elyx-founder.github.io/mentor-elyx-system
Backend: mentor-elyx-system-backend.onrender.com
Analytics: Microsoft Clarity — Project vx3jzkr86n

ELYX — Your Era Begins
Built solo. Zero budget. 74 days. 1st year.
