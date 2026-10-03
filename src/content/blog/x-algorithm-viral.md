---
title: "I Read X's Algorithm. Here's What Goes Viral"
description: "X open-sourced its ranking code. The weights say replies are worth 9x a like — and almost everyone is chasing the wrong number."
pubDate: 'Oct 03 2026'
heroImage: '../../assets/blog-placeholder-1.jpg'
tags: ["x algorithm", "twitter algorithm", "how to go viral on x", "twitter recommendation algorithm", "grow on x", "social media growth", "free twitter growth"]
---

In March 2023, X open-sourced its recommendation algorithm — the actual code that decides what appears in your For You feed. Roughly 25 directories of Scala, Python, and Java. Candidate sourcing, light ranking, heavy ranking, filtering, mixing.

Most people read the headlines. I read the weights.

There's a file in the repo — `src/python/twitter/deepbird/projects/timelines/scripts/models/earlybird/example_weights.py` — that hands you the scoring function for engagement. Not a description of it. The actual numbers.

Here they are:

```
is_clicked          0.3
is_favorited        1.0
is_open_linked      0.1
is_photo_expanded   0.03
is_profile_clicked  1.0
is_replied          9.0
is_retweeted        1.0
is_video_playback_50 0.01
```

A reply is worth nine likes.

Read that again. The entire creator economy on X is organized around the 1.0 column, and the algorithm is paying 9.0 for the thing almost nobody asks for.

This post is what I found in the rest of the repo, and what to do about it if you're posting without a paid plan.

---

## First, the Honest Caveat

Before I build an entire strategy on that number — the file's own README says this model is old:

> *"the light ranker is an old part of the stack which we are currently in the process of replacing. The current model was last trained several years ago."*

So take 9.0 as a directional signal, not gospel. What I actually believe is more durable than the number: **the algorithm rewards depth per impression.** Replies and dwell time are depth. Likes and retweets are shallow, and they're already saturated — every account is chasing them, so they've lost most of their discriminating power as a ranking signal.

But the ratio itself is still the most concrete thing X has ever published about what it rewards. So let's use it.

---

## Replies Are Worth 9x. Here's How to Farm Them

The weight is the easy part. The hard part is that most people ask questions that nobody wants to answer.

**Bad question:** "What do you think?" — vague, zero cost to skip.

**Good question:** "What's the worst [specific thing] you've seen?" — narrow, personal, everyone has an answer.

The pattern: a question people can answer in one line without thinking, about something they've personally experienced. Fill-in-the-blank prompts. "Name one [thing] that [surprising condition]." Specificity is what makes it cheap to answer.

But the bigger lever is **give before you ask.** A reply to your tweet that just says "great post 🔥" gets nothing. A reply that adds a real data point, a counterexample, or a story — and *then* asks — gets replies back. You're demonstrating the behavior you want.

This is the single highest-leverage change most people could make, and it's free.

---

## Likes and Retweets Aren't Scoring You. They're Keeping You Visible.

This is the distinction nobody understands, and it's buried in how the system is architected.

The pipeline runs: **candidate sourcing → light ranking → heavy ranking → filtering → mixing**. Likes and retweets operate almost entirely in the *first* stage.

Your engagement history feeds SimClusters (community detection), TwHIN (graph embeddings), and UTEG (the user-to-post interaction graph). Those decide what gets *pulled* for you and, more importantly, what gets pulled *for people like you*.

So:

- **Likes/RTs** = "what should the algorithm show this account next?" (sourcing)
- **Replies/dwell** = "should this specific post rank higher?" (scoring)

They're not the same job. A post can score beautifully and go nowhere if sourcing never surfaced it. A post can surface and stall if scoring won't promote it. You need both — but they come from different behaviors, and almost everyone is only doing one.

Likes and retweets keep you in the pool. Replies win the pool.

---

## Video Is the Cheapest Path Off Your Followers

Watched-50%-of-a-video is weighted `0.01` — nearly nothing. And yet video is still the strongest lever for out-of-network distribution, because of *where* it acts.

Native video is routed through tweet-mixer and UTEG as an out-of-network candidate source. In-network posts compete against people you chose to follow. Out-of-network posts compete against the entire platform, and video is what makes you competitive there.

Meanwhile: external links suppress distribution. The `is_open_linked` weight is `0.1` — a tenth of a like. X has never publicly said "links are penalized," but the code shows what it's optimizing for, and it isn't the click-out.

**Practical version:** if you must include a link, put it in a reply. Let the main post stand alone.

---

## The Silent Killers

Nobody talks about the negative signals, but they're in the repo too, and they're more punishing than any positive weight.

**"Not interested"** and **Report** are explicit downrank signals. Not neutral — active penalties.

**Mutes and blocks** are worse than they look. They sever edges in the author graph, which means the paths that would have distributed your content to that user's network get cut. Getting blocked by a large account doesn't just remove you from their feed — it removes you from everyone downstream of them.

So rage-baiting has an asymmetric payoff. Provoking a few extra likes from people who hate you is a bad trade when the same post might get you muted by someone with a large, high-quality network.

There's also `tweepcred` — a PageRank over your account's reputation, factoring in follower quality, engagement authenticity, and spam signals. It functions as a multiplier on everything else. A new account starts near zero. It compounds daily. This is the least glamorous number in the repo and probably the most important one.

---

## The Formula

Here's the whole thing, assembled:

**Do:**
- Write posts that hold attention — text that rewards reading, video that hooks in the first two seconds
- End every post with a question designed to be answered in one line
- Reply to other people's posts aggressively, with substance
- Stay in one niche so SimClusters learns who you are and keeps sourcing you to receptive audiences
- Post when your niche is actually online

**Don't:**
- Put links in the main post
- Chase likes as the goal
- Bait, rage, or farm "not interested"
- Pivot topics every week — you reset your embedding every time

The compounding version of this: **consistency beats intensity.** One good post a day in a single niche for six months compounds into an audience that arrives for free. Fifty posts in one weekend into five different topics does not.

---

## What I'd Want Someone to Tell Me Two Years Ago

You don't need a paid plan. You never did — you need a reply.

The paid product sells you ad slots and better placement. It doesn't sell you the 9x, and it can't. The weight is in the ranking model, and the ranking model runs for everyone.

What a paid plan does is buy reach for tweets that already work. What it can't do is fix a post nobody responds to. So the free path is the same path — you just have to do the part the algorithm is actually paying for.

Reply to people. Ask questions that are cheap to answer. Post video. Stay in your niche. Let tweepcred do its work slowly.

That's it. It's not complicated. It was just never written down until now.