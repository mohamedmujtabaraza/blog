---
title: How I Set Up a Fresh Dev Environment in Under 5 Minutes
description:
permalink:
aliases:
tags:
draft:
date: 2026-01-01
---
<sup>[[Edit this page]](https://github.com/mohamedmujtabaraza/Blog/edit/main/content/Productivity/dev-env.md)</sup>

For the past few months, I've standardized my development setup using **VS Code's Dev Containers**<sup><span style="display: none;">[@Webpage-2MHIUP9U]</span><a href="#Webpage-2MHIUP9U">[1]</a></sup> combined with **mise**<sup><span style="display: none;">[@Webpage-45PG79FG]</span><a href="#Webpage-45PG79FG">[2]</a></sup>. This combo gives me reproducible environments across projects, whether it's ASP.NET, Node.js, or Python without polluting my local machine or dealing with version conflicts.

If you're tired of "it works on my machine" issues or onboarding headaches, this approach might click for you.

### Why Dev Containers + Mise?

Dev Containers isolate everything in Docker, so your editor runs "remotely" inside a container with all dependencies pre-configured. Mise handles tool versions (like Node 22, Python 3.12, etc). I switched to this workflow after struggling with mismatched versions in team projects. Now, everything just works.

### Prerequisites

- VS Code with the **Dev Containers** extension installed.
- Docker running on your machine.

### Step-by-Step Setup Guide

1. **Open a folder in VS Code**
2. **Open Command Palette (Ctrl+Shift+P)**\
	 \> "Dev Containers: Add Dev Container Configuration Files..."\
	 \> "Add configuration to workspace"\
	 \> "Debian"\
	 \> Select "Mise" as additional feature.<sup><span style="display: none;">[@Webpage-QQUVP7VP]</span><a href="#Webpage-QQUVP7VP">[3]</a></sup>
3. **Open Command Palette (Ctrl+Shift+P)**\
	\> "Dev Containers: Rebuild and Reopen in Container"\
	\> Wait around 2-3 minutes if this is your first time building the container.
	![Fresh Dev Environment](<../Attachments/devcontainer.png>)
4. **Configure [mise-en-place](<../Tools/mise-en-place.md>)**
	See my dedicated post linked above for activating various tools in your shell automatically.
	
5. **Verify**
	In the container terminal: `mise ls`, `node -v`, etc.


This keeps my workflows consistent and frustration-free. If you try it, let me know how it goes!
Have a favorite Dev Containers trick? Share in the comments.

---
### References

[1]\
“Developing inside a Container.” Accessed: Dec. 22, 2025. [Online]. Available: [https://code.visualstudio.com/docs/devcontainers/containers](https://code.visualstudio.com/docs/devcontainers/containers) ^Webpage-2MHIUP9U

[2]\
“Home | mise-en-place.” Accessed: Dec. 22, 2025. [Online]. Available: [https://mise.jdx.dev/](https://mise.jdx.dev/) ^Webpage-45PG79FG

[3]\
“features/src/mise at main · devcontainers-extra/features · GitHub.” Accessed: Dec. 22, 2025. [Online]. Available: [https://github.com/devcontainers-extra/features/tree/main/src/mise](https://github.com/devcontainers-extra/features/tree/main/src/mise) ^Webpage-QQUVP7VP

<sup>[Go to home](<../index.md>) &nbsp;&nbsp; [Jump to top](<./dev-env.md>)</sup>
