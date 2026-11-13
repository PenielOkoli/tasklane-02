# Tasklane — technical foundation

FlexiSAF deliverable 2: Next.js App Router, server/client boundaries, and TypeScript.

Live app: https://tasklane-foundation.vercel.app

This is Tasklane's typed frontend foundation. The board renders six sample tasks, with search, priority filtering, and local status movement. It uses Next.js App Router and TypeScript. The Vercel AI SDK and Groq adapter are installed at the server/model boundary for the next milestones; this milestone does not yet send model requests.

## Evidence

- [Architecture notes and security checklist](src/app/guide/page.tsx)
- [Shared task types](src/types/task.ts)
- [Server page](src/app/page.tsx)
- [Client board](src/components/board.tsx)
- [Module 2 implementation plan](docs/modules/02/plan.md)
- [Verification](docs/modules/02/verification.md)

## Run

Requires Node 22. Run `npm ci`, copy `.env.example` to `.env.local` only if preparing later server-side AI work, and run `npm run dev`. No secret is needed for this milestone because AI calls are not enabled. `npm run typecheck` and `npm run build` validate the application.

## Continuity

Submission 2 starts from the Tasklane product brief in [tasklane-01](https://github.com/PenielOkoli/tasklane-01) and lays the typed app foundation for later streaming chat, structured outputs, and tool calling. It has its own repository and Vercel project.
