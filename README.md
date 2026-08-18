# Neil Roberts

I build agentic AI tooling and ship it in production: MCP servers, custom agents, Claude Code skills, and eval harnesses. The work I care about is getting frontier models to do bounded, checkable work, and then packaging what I figure out so other people can run it too.

Right now I'm building Voygent, a platform for travel advisors that runs the whole agent loop inside a chat client. It's a Cloudflare Workers MCP server with interactive in-chat UI (MCP Apps), supplier adapters, and a test harness that migrates real trip data forward and then verifies every rendered surface by vision before I trust it. I keep a running write-up of the engineering at [demo.voygent.ai/blog](https://demo.voygent.ai/blog), where I post the dead ends and the calls I made as I hit them.

## What I work on

Mostly MCP in production: server design, how tools and routers are shaped, and building UI that runs inside the chat instead of off in a separate web app. A lot of agent orchestration too, including multi-agent workflows and honest session handoff across context limits. And I put more time into evals than most people expect, because I don't trust a tool change until I've measured whether the model still picks the right tools and finishes the task. Renaming one tool can quietly break that, and the only way to find out is to run it.

## Selected open work

| Repo | What it is |
|------|------------|
| [mcp-apps-interactive-ui](https://github.com/iamneilroberts/mcp-apps-interactive-ui) | Building interactive in-chat UI with MCP Apps: a runnable example plus a field guide to the shipping gotchas, distilled from Voygent's Folio Board. |
| [claude-skills](https://github.com/iamneilroberts/claude-skills) | The Claude Code skills, hooks, and agents I actually run day to day. The through-line is honest session and context management. |
| [mcp-tooluse-eval](https://github.com/iamneilroberts/mcp-tooluse-eval) | A cheap, bounded harness that checks whether a model picks the right tools and finishes a multi-step task against your MCP server. |
| [scaffold](https://github.com/iamneilroberts/scaffold) | Build niche AI tools that run inside the chatbot you already pay for, using MCP. |
| [lllm-eval](https://github.com/iamneilroberts/lllm-eval) | Benchmark local LLMs as coding agents against a deterministic in-memory repo. |
| [voygent-demo](https://github.com/iamneilroberts/voygent-demo) | Public interactive demo of Voygent with a record/replay honesty layer (featured trips replay, off-menu trips run live), plus my running engineering blog of deep dives at [demo.voygent.ai/blog](https://demo.voygent.ai/blog). |

Also here: [agent-deck](https://github.com/iamneilroberts/agent-deck) and [agent-glance](https://github.com/iamneilroberts/agent-glance) (phone-first control of local coding agents), [claude-grep](https://github.com/iamneilroberts/claude-grep) (search past Claude Code sessions), and [dba-box](https://github.com/iamneilroberts/dba-box) (an on-prem AI analyst for SQL Server), plus a couple of things I built for fun ([SQUAWK](https://github.com/iamneilroberts/SQUAWK), [LORAN](https://github.com/iamneilroberts/LORAN)).
