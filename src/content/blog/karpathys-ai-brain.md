---
title: "Karpathy's AI Brain: How to Build a Self-Growing Personal Wiki"
description: "Stop hoarding content. Build a second brain that compounds — with one command, zero maintenance, and an LLM that does the heavy lifting."
pubDate: 'Jul 05 2026'
heroImage: '../../assets/blog-placeholder-1.jpg'
---

I've got thousands of dollars worth of saved content across YouTube, podcasts, articles, newsletters, Reddit threads, and Twitter threads. Most of it sits there — untouched, unread, unloved. Total information graveyard.

You know the feeling. You save a YouTube video to watch later and just... never watch it. You bookmark an article thinking "this has the answer" and six months later you can't even find the bookmark. You highlight a passage in a book, close the cover, and the insight dissolves within a week.

The question isn't whether you're collecting good material. You are. The question is whether any of it compounds.

So when Andrej Karpathy tweeted about a system where an LLM builds and maintains a personal wiki from everything you save — I stopped scrolling. And when Lex Fridman replied saying he does the exact same thing, I built it that same night.

This post is everything I learned. By the end, you'll have a second brain that grows smarter with every source you add, run by an AI that handles every ounce of maintenance. And I built a free skill file that makes it a one-command setup.

---

## The Problem: Why Your Knowledge Doesn't Compound

Here's what most people get wrong. You're not bad at organizing. You're not lazy. The problem is deeper — the tools we use don't allow knowledge to compound.

Here's the typical loop. You find something interesting. You save it. It disappears into a folder, a bookmark manager, a read-later app. Months pass. You vaguely remember reading something about the topic. You spend twenty minutes digging. You give up and Google it instead.

The content you saved added zero value to your future self. Every new piece of information starts at zero. Nothing builds on anything else.

AI tools don't solve this either — they make it worse by removing friction from the input without solving the compounding problem. You upload a file to ChatGPT, ask a question, get an answer. Close the tab. Tomorrow comes, you ask the same question. It starts from scratch. Nothing carries over. Every session is a fresh start, every chat a new island.

The system I built flips this entirely. Instead of the AI rummaging through raw files every time you ask a question, it builds a permanent, interconnected wiki that gets smarter with every single source you add. Every article. Every transcript. Every podcast note. Every highlighted paragraph. They all feed into one brain that actually remembers.

---

## How It Works: Your Personal Librarian

Think of it as hiring a personal librarian.

You bring in the books — articles, transcripts, podcast notes, research papers, whatever you find interesting. You dump them on the desk and walk away. That's your only job: find good material.

The librarian takes everything you brought in. Reads each one. Organizes them into a proper library. Writes summaries. Creates topic sections. Connects related books with cross-references. Flags where two sources contradict each other. When you bring in something new, the librarian updates every shelf it touches — not just the one for the new book, but every related shelf in the library.

Every new book you bring gets woven into the existing collection. You never organize a single shelf. You never tag a single file. The librarian handles everything. You just keep finding and bringing in quality material.

The library gets smarter with every addition. Everything is connected. You can browse, search, ask questions, and find things you forgot you even had.

But this isn't a metaphor. It's literally how the system works. Let me break down the three layers.

### Layer One: Raw Sources

This is your dumping ground. A folder on your computer where everything lands — YouTube transcripts, saved articles, book notes, research PDFs, newsletter issues, podcast transcripts. The AI never touches or modifies these files. They live untouched as your source of truth. If the AI ever gets something wrong (and it will occasionally hallucinate), you can always trace back to the original.

### Layer Two: The Wiki

This is where the AI lives. It reads your raw sources and creates organized, linked pages — organized by concept, not by source.

This distinction matters. Most knowledge bases organize by source: here's the summary of Video A, here's the summary of Article B. That's filing, not thinking. The wiki organizes by concept: here's a page on "attention mechanisms" that synthesizes what every source says about attention mechanisms. Here's a page on "transformer architectures" that pulls from eight different sources — articles, videos, and a research paper you added last week.

Pages cross-reference each other. New sources update multiple pages at once. The wiki isn't a mirror of your sources — it's a synthesis of everything they contain, organized the way your brain actually thinks.

### Layer Three: The Instruction File

A single document that tells the AI exactly how to behave. What format to use for new pages. How to handle contradictions between sources. How to log every change so you can audit what happened. What tone to write in. How deep to go on summaries. When to flag something as low-confidence.

You and the AI tweak this file together over time. As you learn what works and what doesn't, you update the instructions. The AI gets better at being your librarian because you keep refining the job description. This is the meta-layer that makes the whole thing self-improving.

---

## Why This Survives Past Month One

Most knowledge systems fail for one reason: maintenance.

You start a wiki. It's exciting. You add pages. You link things. You write summaries. For two weeks, it's the most productive system you've ever used. Then life gets busy. A link breaks. A page goes stale. You add something new but forget to update the related pages. The backlog of maintenance grows faster than the value you get out. So you abandon it. The wiki becomes another item in your information graveyard — just a fancier one.

This is why 99% of personal wikis die. Not because the idea is bad. Not because the tools are flawed. Because the maintenance cost grows linearly with the content while the creator's attention remains fixed.

An AI doesn't have that problem.

It doesn't get bored. It doesn't forget to update a cross-reference. It doesn't mind touching fifteen files to integrate one new source. It doesn't procrastinate on writing summaries. It doesn't fall behind. The maintenance cost drops from hours per week to effectively zero.

So the system actually survives past the first month. It compounds instead of collecting dust. Day ninety looks better than day thirty. Year two looks better than year one. That's what makes it fundamentally different from every other knowledge system you've tried.

---

## The Loop: Add, Ask, Audit

Once the system is running, your entire interaction boils down to three actions.

### 1. Add

Find something good. Save it to the raw folder. Tell the AI to process it.

The AI reads the entire source. Writes a structured summary. Updates every related topic page. Flags any contradictions with existing content. Logs everything to a changelog. One source might ripple through ten to fifteen pages. Your entire knowledge base gets smarter from a single addition.

The key insight here: you don't need to read the source fully before adding it. The AI reads it for you. You add first, consume later. When you need to understand a topic, you go to the wiki page — which already synthesizes everything you've collected on that topic — instead of reading individual sources.

### 2. Ask

Not surface-level questions like "what did this one video say." Real questions that synthesize across your entire collection.

"What's the consensus across my sources on X?" "Where do my sources disagree about Y and why?" "What framework emerges from combining the approaches in sources A, B, and C?" "What's the strongest counter-argument to the position in source D?"

The AI searches the wiki — not the raw sources — so answers come from synthesized understanding, not word-matching. Each answer includes citations pointing back to specific wiki pages, which themselves trace back to original sources.

And here's the kicker: every good question-and-answer pair gets saved back into the wiki as a new page. Your questions compound too. Ask something insightful today, and tomorrow's questions can build on it.

### 3. Audit

Health checks. Ask the AI to review the wiki and tell you what's wrong.

It finds orphaned pages — pages nothing links to, so they're effectively invisible. It spots contradictions between pages that need resolving. It identifies topics where your coverage is thin and suggests specific sources to go find. It highlights pages that haven't been updated in months and might be stale.

The system tells you what it's missing. You don't have to guess. The librarian audits the library and hands you a prioritized list of what needs attention.

Add, ask, audit. That's the entire loop. Three verbs. Everything else is automated.

---

## The Free Skill File: One Command

I built a skill file that automates the entire setup process. One markdown file. Give it to your AI agent — Claude, ChatGPT, OpenCode, whichever you use.

Type `create-2nd-brain`. It asks you three questions:

1. **What topic are you building this for?** (Could be one domain or several — AI research, startup strategy, philosophy, anything.)
2. **What categories do you want?** (The high-level buckets your wiki will organize around.)
3. **What kind of sources are you collecting?** (YouTube transcripts, articles, research papers, book notes, podcasts, etc.)

Answer those three questions. Then let it run.

The skill creates the full directory structure — `raw/`, `wiki/`, `archive/`. It writes the instruction file with all the rules baked in — formatting, contradiction handling, changelog format, tone, depth requirements. It tells you exactly what to do next and how to start feeding in sources.

No manual setup. No guessing at prompts. No configuration files to tweak. One command, three answers, and your second brain is ready to grow.

The skill file is free. No email required. No sign-up. Download link at the end of this post.

---

## Tutorial: Setting Up Your Second Brain

Here's the full walkthrough — start to finish.

### Step 1: Install Obsidian

Obsidian is a free markdown editor. Think of it as a fancy folder browser — everything you see is just files on your computer. No cloud lock-in, no proprietary format, no loading spinners.

Download it at [obsidian.md](https://obsidian.md). Install it. Open it up.

Click "Create new vault." Call it whatever you want — I named mine "Second Brain." Pick a folder on your computer. Hit create.

You now have a vault. It's empty, but it's yours.

### Step 2: Install the Web Clipper

Go to the Chrome Web Store (or your browser's extension store) and search for "Obsidian Web Clipper." Install it.

Once installed, click the extension icon and point it at your Obsidian vault. Takes ten seconds.

Now, whenever you're on a YouTube video, an article, a Substack post — click the clipper icon. It saves the entire page as a markdown file straight into your vault's `raw/` folder. For YouTube videos, it automatically pulls the transcript. For articles, it grabs the full text. No copy-paste. No formatting to fix.

### Step 3: Collect Sources

This is the fun part. Go find five to ten good sources on whatever topic you're building your second brain around.

YouTube videos. Blog posts you've been meaning to read. That Twitter thread you bookmarked three months ago. The research paper someone recommended. Clipping each one takes one click. You'll have a collection faster than you'd expect.

Five to ten sources is plenty to start. You don't need fifty. The system compounds — start small and let it grow.

### Step 4: Run the Skill

Open your AI agent in the same folder as your vault. I use OpenCode, but this works with Claude Code, Cursor, Windsurf, or any agent that can read local files.

Type the command for the skill. It asks those three questions. Answer them honestly — you're defining the shape of your knowledge base, so be specific about your categories and source types.

Let it run. You'll see it creating directories, writing the instruction file, and setting up the structure. On a modern machine, this takes about thirty seconds.

### Step 5: Feed It Sources

Now point the AI at your raw folder. Tell it to process the sources.

It reads each one. Writes summaries. Creates concept pages. Links everything together. What used to take hours of manual organizing now takes minutes, hands-off.

When it finishes, open your vault in Obsidian. You'll see concept pages with proper titles and descriptions. Summaries under each source. Cross-references between pages. A graph view that shows every connection. Everything is linked. Everything is searchable.

### Step 6: Start Asking Questions

This is where the system earns its keep.

Ask a real question — not "what's in source three," but something that requires synthesis. "Based on my wiki, what's the strongest through-line across my sources on this topic?" "What's the biggest gap in my current coverage?" "Which of my sources contradicts the others?"

The AI reads through the wiki pages it built — pages you didn't write, organized by a structure you didn't design — and answers with citations pointing back to specific pages. You get synthesized insight from your own collected material, delivered on demand.

---

## What Happens After the First Month

Most second brain setups die in week three. This one doesn't, because there's nothing to maintain. The AI handles it.

After a month, you'll have a knowledge base that's genuinely useful — not because you spent hours organizing, but because you fed it sources and let the system do the work. You'll find yourself going to the wiki before Google. You'll ask questions you wouldn't have thought to ask. You'll find connections between topics you didn't realize were related.

After three months, it starts to feel indispensable. Your wiki knows more than you do about the connections between your sources. It's read everything more carefully than you ever could. It remembers the details you forgot. Asking it a question feels like consulting an expert who's studied your specific collection of material.

That's the compound effect. It's not about any single source or summary. It's about the network of understanding that grows denser with every addition. Every new source makes every existing page more valuable. The whole thing appreciates.

---

## The Skill File

You can grab it for free. No email, no signup, no strings.

Download the skill file, drop it into your AI agent's skills folder, type the command, and answer three questions. That's it. Your second brain is alive.

[Get the skill file →](https://www.mdshare.online/s/2eO1XN_280Iixz5z630oX)

---

## What to Build First

The hardest part of any knowledge system isn't the tool. It's deciding what to put in it.

Pick one domain. Not "everything I'm interested in" — that's too broad and you'll drown. Pick one specific area where you're actively learning or building something. AI agent architectures. Growth marketing. Rust programming. The history of the Roman Empire. Doesn't matter what. Just pick one.

Clip five sources. Run the skill. Feed the sources. Then add one new source per day.

In a week, you'll have a wiki with a dozen pages, all linked, all synthesized, all searchable. In a month, you'll have something that genuinely saves you time and surfaces insights you wouldn't have found otherwise.

The system rewards consistency, not intensity. One source per day beats fifty in a weekend. Let it compound.

---

A lot of people talk about building a second brain. Most never do because it's too much work to set up and too much work to maintain. This system removes both barriers. The AI does the heavy lifting. You just keep collecting interesting material — something you were going to do anyway.

If you build one, I'd love to see it. Tag me with what you're working on. And if you hit a wall, the skill file has troubleshooting built in — just ask the AI what went wrong and it'll help you fix it.
