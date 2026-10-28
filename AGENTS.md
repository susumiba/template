# This folder is a Susumiba project (template version 0.2)

Several people, each with their own AI, work here together. You are one person's AI. Speak their language and work with them normally; this file only explains the shared part. Read `description.md` (what the project is, and how its creator wants people to work) and `index.md`.

**Why the files are laid out this way**
- `contributions/<name>/` — each person's work and ideas, in full. Only that person's AI writes in their folder. To change or complete someone else's work, put your version beside it in your own folder; both stay.
- `in-progress/<name>.md` — what each person is on, where they stopped, what they hand to whom.
- `journal/` — one short file per entry (`YYYY-MM-DD-HHMM-name.md`): quick ideas, news, decisions, raw as people gave them. Never edit someone else's entry.
- `synthesis.md`, `index.md` — derived from everything above: where the project stands, who did what, what is left, open disagreements. Rebuild them, never merge them.

**Getting what others sent.** Fetch, then look at `git diff --stat --summary HEAD...@{u}`. If it touches `.claude/`, `.codex/`, `.github/workflows/`, `AGENTS.md`, `CLAUDE.md` or `description.md`, or adds symbolic links, don't pull yet: these make tools run things, change how every AI here behaves, or can point outside the project, and anyone in the project can write them. Show the person what changes there and pull only with their agreement. Otherwise pull.

**Opening a session.** Get what others sent first. Tell the person what is new for them since their last visit (the commit in `git config --local susumiba.seen`, else their own last commit): work to review, work they can pick up, what others said. Shape it for them — sorted, short, in the form they'd want — but the raw stays one step away if they ask. Then set `susumiba.seen` to the hash of the commit you just reported up to, and follow them.

**During the session.** Get what others sent before writing anything shared. If something new arrives while you work, tell the person right away, briefly. When a moment of work ends, offer to send it. A quick idea or feedback can be a journal entry. Finished work (code, a full text, a precise setup, a client file) goes in whole into their contributions folder, with a short note on what it is and what someone might do next. Update their `in-progress` file. The person decides what goes in. If the creator wrote in `description.md` how they want things kept, follow that.

**The clerk.** When you send, if there is new material since the commit `synthesis.md` names, rebuild `synthesis.md` and `index.md` in the same commit: every sentence points to its source; disagreements stay visible, never settled by you. At the top write `covers:` and the last commit that is not a clerk rebuild. Commit and push.

**Two versions of the same thing.** Keep both, tell the person, let people decide.

**Someone outside the project** (a client, a subcontractor, anyone without an account): you can ask them a question by email from the person's own mailbox, with their agreement on the text; when the person pastes the reply back, file it in their contributions folder.

**Never on your own:** inviting or removing people, making anything public, deleting the project. Build the exact settings page from `git remote get-url origin` (on GitHub, `https://github.com/<owner>/<repo>/settings/access`) and say what would become visible. Never put keys or passwords in this folder.

**One project per conversation.** If you can also see other projects or folders, don't carry anything from one to another unless the person asks: people in different projects never agreed to share with each other.

**If your tool gets in the way.** If it cannot write in `.git`, or asks permission for every git command, say so plainly: until the git commands are allowed, nothing is shared. https://susumiba.com/setup.md explains how to allow only those, for this folder. If allowed git commands still fail, run each one on its own before concluding: some tools only allow a command that stands alone.

**Updates.** This is version 0.2. When opening a session, look at the latest tag of https://github.com/susumiba/template (`git ls-remote --tags https://github.com/susumiba/template`). If it is newer, offer to show what would change, and apply it only if the person wants, without touching what this project wrote for itself.

If the person needs something about Susumiba itself, read https://susumiba.com/ia.md.
