---
title: "AI coding agents need direction"
description: "AI coding assistants have transformed how we write software, but they need clear direction."
pubDate: 2025-08-20
readingTime: "5 min read"
---

AI coding assistants have transformed how we write software. GitHub Copilot, Cursor, and chat models can generate code faster than ever before. But after months of working with these tools daily, I've learned something important: AI is powerful, but it's not a replacement for good software architecture and clear direction.

Here are three recent examples that illustrate why you can't just let AI loose on your project and expect it to make the right decisions.

## Component Duplication

I was building a new blog and needed a blank state for when there are no posts yet—something to show on deployment before any content exists.

I asked my AI assistant to "add a blank state for when there are no posts." Instead of creating reusable header and footer components and then building a proper blank state component, the AI duplicated the entire header and footer HTML directly into the blank state template.

The result worked, but it was a maintainability problem. Any changes to the header or footer would now need to be made in multiple places. The AI had solved the immediate problem without understanding the broader architectural implications.

AI doesn't inherently understand component architecture or DRY principles unless you explicitly guide it toward those patterns.

## Security Bypass

While working on a React Native app that required Firebase authentication, I ran into login issues during development. The Firebase tokens weren't properly configured yet, so authentication was failing.

I mentioned to my AI assistant that the login wasn't working. Instead of helping me configure Firebase properly, it implemented a local bypass that completely circumvented the entire authentication system.

This wasn't just wrong—it was potentially dangerous. What if that bypass accidentally made it to production? What about maintaining consistent behavior between environments? The AI had taken the path of least resistance without considering security implications or proper development practices.

AI will often choose the quickest solution over the right solution, especially when it comes to security and architecture decisions.

## Migration Loop

I needed to upgrade a Remix application and its Node version because Vercel was dropping support for the current version. This seemed like a perfect task for AI—just follow the migration guides and update the dependencies.

The AI got itself stuck in a loop, trying different approaches and making changes that contradicted each other. It would update one dependency, then realize it broke something else, then try a different approach that undid the previous work.

I had to step in and be specific: "Follow the official Remix v2 migration guide step by step. Start with dependencies, then update the file structure, then handle the breaking changes." Only with this explicit roadmap did the AI successfully complete the migration.

For complex, multi-step processes, AI needs clear, sequential guidance. It doesn't intuitively understand project-wide migration strategies.

## The Bottom Line

AI has dramatically increased my productivity and made coding more efficient. I can prototype faster, handle tedious tasks more efficiently, and explore solutions I might not have considered. But it's not a silver bullet.

You still need to be a good software architect. You still need to understand your system's requirements, security implications, and long-term maintainability. You still need to provide clear direction and review every suggestion.

AI is a powerful assistant, but the emphasis is on assistant. The human is still the architect, the decision-maker, and the one responsible for the quality and integrity of the final product.
