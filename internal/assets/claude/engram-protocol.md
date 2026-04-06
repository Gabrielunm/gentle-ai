## Engram Persistent Memory — Protocol (Gentleman Optimized)

You have access to Engram, a persistent memory system. This protocol is MANDATORY and ALWAYS ACTIVE.

### PROACTIVE SAVE TRIGGERS (Mandatory — No "Sure", No "I hope")

Call `mem_save` IMMEDIATELY after:
- Architecture or design decision made.
- Team convention or workflow change agreed upon.
- Tool or library choice made with tradeoffs.
- Bug fix completed (include root cause).
- Feature implemented with non-obvious approach.
- Notion/Jira/GitHub artifact created or updated with significant content.
- Configuration change or environment setup done.
- Non-obvious discovery about the codebase.
- Gotcha, edge case, or unexpected behavior found.
- Pattern established (naming, structure, convention).
- User preference or constraint learned.

### GENTLEMAN'S DREAM (Memory Consolidation)

To keep memory efficient and prevent "context rot", you MUST perform a "Dream" pass periodically or upon user request ("limpiá la memoria", "consolidá"):

#### Phase 1: Orient & Search
- Use `mem_search` to see what already exists before creating new topics.
- Read existing topic files to **improve/update** them rather than creating duplicates.
- Use `topic_key` religiously for evolving concepts (e.g., `arch/auth`, `api/conventions`).

#### Phase 2: Consolidate & Absolute Dates
- **Merge** new signals into existing topic files.
- **Convert** relative dates ("yesterday", "last week") to absolute dates (YYYY-MM-DD).
- **Prune** contradictions: If a new finding disproves an old memory, `mem_update` or delete the stale info at the source.

#### Phase 3: Concise Indexing
- Keep the main memory index concise (max 200 lines).
- Entries should be one-line hooks: `- [Title](topic_key) — brief summary`.
- Move detailed technical descriptions to specific topic files, NOT the index.

### FORMAT FOR `mem_save` / `mem_update`
- **title**: Verb + What (searchable).
- **type**: bugfix | decision | architecture | discovery | pattern | config | preference.
- **topic_key**: Stable, kebab-case (e.g., `ui/atomic-design`).
- **content**: 
  - **What**: One-line summary.
  - **Why**: Motivation/context.
  - **Where**: Affected paths.
  - **Learned**: Crucial gotchas (omit if none).
  - **Date**: YYYY-MM-DD.

### WHEN TO RECALL
1. User asks ("recordar", "qué hicimos").
2. Starting a task that sounds familiar.
3. User's first message references prior features/problems — call `mem_search` proactively.

### SESSION CLOSE (Mandatory)
Before saying "done" / "listo", call `mem_session_summary`:
- **Goal**: What we did.
- **Accomplished**: Key completions.
- **Next Steps**: For the next session.
- **Files**: Path — Purpose.

### AFTER COMPACTION

If you see a compaction message or "FIRST ACTION REQUIRED":
1. **IMMEDIATELY** call `mem_session_summary` with the compacted summary content — this persists what was done before compaction.
2. Call `mem_context` to recover additional context from previous sessions.
3. **Only THEN** continue working.

**Do not skip step 1.** Without it, everything done before compaction is lost from memory.
