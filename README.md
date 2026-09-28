# Spaces by Seedling
## Your Local AI Command Center

**One app. Every model. Complete control.**

---

You installed Ollama. You pulled a few models. You opened BobCLI. Everything worked fine — until you opened two apps at the same time and your computer froze.

Or maybe you are a developer and your users keep reporting crashes you cannot reproduce. Or you are running a team and everyone has different hardware and different experiences with the same tools.

The problem is not your models. The problem is that nothing is coordinating them.

**Spaces is the solution.**

Spaces is the central hub for every local AI app on your machine. It runs a silent background service called ArrP Protocol that monitors your GPU in real time, manages your model library intelligently, and coordinates every AI request from every app simultaneously — so nothing crashes, nothing conflicts, and you always know exactly what is happening.

Open Spaces and see your entire AI ecosystem at a glance. Close Spaces and everything keeps running exactly as it should.

---

## What You See When You Open Spaces

### System Health — Always at the Top

Three live gauges update every half second showing the real state of your hardware right now.

**VRAM Headroom** shows how much GPU memory is available. When it drops below 15% Spaces automatically starts managing requests more conservatively. Below 8% and queue enforcement kicks in to prevent crashes before they happen.

**Context Depth** shows how many active AI conversation threads your models are holding simultaneously. When this fills up Spaces routes new requests to models with smaller context requirements so nothing gets dropped.

**Compute Load** shows how hard your GPU is working right now. When it climbs above 85% Spaces switches to sequential processing to keep every active response flowing cleanly.

Below the gauges a full-width **Health Bar** shows your system state in plain language — STABLE, APPROACHING LIMIT, CRITICAL LOW VRAM, COMPUTE SATURATED — with a color that changes in real time. Green means you are clear. Amber means the system is managing load. Red means something needs attention and Spaces is already handling it.

---

### Your Model Library

Every model you have installed appears in the Model Registry. Spaces reads each model's actual capabilities directly from your Ollama installation — not guesses based on file names — so the context window, memory requirement, and quantization tier are always accurate.

**Enable and disable models** with one tap. Disabled models are excluded from all routing decisions immediately. Your preference persists across restarts.

**Pin a model** when you want Spaces to always use it regardless of what its intelligent selection would suggest. Useful when you need consistency for a specific workflow.

**Correct model information** when a model is showing wrong data. Tap any model to open its detail sheet and edit the context window size directly. Your correction is saved and used for every future routing decision.

**See live session stats** for each model. How many requests it has handled. How many tokens it has generated. Toggle between the current session and your full lifetime history.

Above the model list the **Performance Card** summarizes your session — total requests, total tokens generated, average response time, average tokens per second, routing mode breakdown showing parallel versus queued versus rejected, top models by usage, and a per-app breakdown showing which apps have been most active.

---

### Live Log Feed

Every event in your AI ecosystem streams into the log feed in real time. Routing decisions. State transitions. Threshold breaches. Stream completions with token counts and elapsed time.

Every entry is tappable. Tap any log entry to see the full detail — the exact VRAM headroom, context depth, and compute load at the precise moment that event fired. This is not approximate data. This is the exact hardware state that caused that decision.

---

### Suggestions and Alerts

**Suggestions** appear when Spaces detects conditions that might affect your experience. When memory is getting tight Spaces surfaces a plain-language recommendation for what to do. When compute is saturated Spaces explains what is happening and what will help. Suggestions stay visible until you dismiss them — nothing disappears before you have seen it.

**Alerts** capture every threshold breach with a full metrics snapshot. When your VRAM drops critically low or your context slots fill up the alert records the exact numbers at that moment. Tap any alert to see the complete picture. Dismiss it when you are done with it. Nothing auto-clears without your action.

---

### The Ecosystem Panel

The bottom of the suggestions column shows every app in the Seedling ecosystem. Installed apps show their version, their session request count, and a live activity indicator when they are currently making requests. Apps that are available but not installed show an Install Now button that handles installation silently — no terminal, no package manager commands. Apps coming soon are listed so you know what is on the way.

---

## The Background Service

Everything Spaces shows you is powered by the ArrP Protocol kernel — a Node.js service that starts automatically when your computer boots and runs silently until you shut down.

The kernel polls your GPU hardware 250 times per second. It maintains a six-state ledger of your system health. It scans your Ollama model library and reads each model's real capabilities. It accepts routing requests from any app that knows how to talk to `localhost:18204`. It logs every event to a permanent audit trail on your machine.

When Spaces is closed the kernel keeps running. Your apps keep working. The coordination never stops.

---

## Settings

Everything in Spaces can be configured from the settings panel.

**Model Sources** — Add as many model directories as you want. Your local Ollama installation is detected automatically at setup. Add network drives, external hard drives, company servers, or any folder on any path your machine can reach. Spaces scans all of them and adds every compatible model to your registry.

**Global Dispatch Policy** — Choose how Spaces assigns models to requests by default. Intelligent Tier picks the best model for current conditions. First Available picks whatever has capacity fastest. Manual Override always uses your pinned model.

**Per-App Dispatch Policy** — Override the global policy for any specific app. Give BobCLI one policy. Give BobCA another. Each app gets exactly the behavior you want.

**VRAM Thresholds** — Adjust the memory levels that trigger each system state. Move the Approaching Limit slider if you want more or less conservative memory management. The defaults are carefully chosen but every installation is different.

---

## What Is Coming

Spaces is the beginning of something larger.

**ArrP App Finder** — A built-in directory of every app that integrates with ArrP. Integration partners will be able to list their apps directly. Users will be able to discover, review, and install new ArrP-compatible tools without leaving Spaces.

**OTA Updates** — Spaces and ArrP will update themselves automatically in the background. No reinstalling. No manual update process. You always have the latest version.

**Cloud Inference Endpoints** — Developers will be able to list their own inference endpoints — free or paid — directly in the ArrP ecosystem. Users get access to cloud-grade models through the same routing layer they already use. The interface stays identical. The power scales.

**User Reviews and Community** — Users will be able to rate and review apps in the ecosystem. Early access programs. User showcases. Partnership opportunities between developers and the organizations that want to hire them or license their work.

**Cross-Platform Expansion** — macOS and Linux support is on the roadmap. The ArrP Protocol and the Spaces dashboard will expand beyond Windows to serve the full local AI developer community.

The infrastructure is built. The ecosystem is growing. What comes next is the community that builds on top of it.

---

## Getting Started

Download Spaces from our Releases and run the installer.

During setup you confirm where your AI models are stored and where your other Seedling apps are installed. Spaces handles the rest — the background service installs automatically, your model library is scanned, and your Dispatch Console is ready before the installer finishes.

Open Spaces. See your ecosystem. Start building.

---

*Spaces by Seedling — Built by Bob's Workshop*  
*Part of the Seedling ecosystem: Spaces · BobCLI · BobCA · Hansel · The Forge*
