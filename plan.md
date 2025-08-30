**# 📚 Study Forge

Study Forge is your personal academic OS — a centralized platform to manage notes, track progress, reflect, and grow.

## 🧱 Architecture

### 🔥 studyforge-core (Main)
- Frontend: Next.js + Tailwind CSS
- Backend: Supabase (Auth, DB, Storage)
- Features: Logs, notes, quizzes, dashboard

### 🧩 Archived Paths
- MkDocs Material + Decap CMS (static site variant)
- Google Forms → Markdown export → GitHub sync

## 🧭 Roadmap

- [x] Repo structure created
- [ ] Build frontend scaffold (Next.js)
- [ ] Design DB schema on Supabase
- [ ] Implement notes and logging system
- [ ] Add analytics dashboard and markdown export

## 🚀 Deployment Targets
- Vercel (frontend)
- Supabase (auth + DB)
- GitHub Pages (static backups via MkDocs)

> Long-term goal: A powerful, student-first productivity platform.**# TeamMind: AI-Native Searchable Memory for Teams

## 1. Problem Statement

Teams use multiple platforms—Slack, Google Docs, Notion, GitHub, Drive—leading to scattered knowledge and wasted productivity. Critical information is hard to find, slowing down collaboration and decision-making.

## 2. Solution Overview

TeamMind unifies your team’s knowledge by integrating with common tools and providing a powerful, chat-based AI search. Ask any question in natural language, and get instant, context-rich answers—no more hunting across tabs.

## 3. Features

- Integrate multiple sources (Slack, Google Docs, more coming soon)
- AI-powered semantic search (not just keywords)
- Modern chat-based UI for asking questions
- Results with rich context: source, author, timestamp, link
- Secure authentication (Google, Slack OAuth)
- Scalable and privacy-respecting

## 4. System Architecture

### Frontend
- Next.js (React), Tailwind CSS
- Chat UI, Results display, OAuth integrations

### Backend
- Node.js/Express (API)
- Embedding generation (OpenAI/Cohere)
- Data importers for Slack & Google Docs

### Storage
- Vector DB (Pinecone/Weaviate/Milvus/FAISS): stores embeddings + metadata
- Postgres/Supabase: user info, source mapping

### Auth
- OAuth (Google, Slack), JWT

## 5. User Flow

1. User connects Slack & Google Docs.
2. System imports and chunks data.
3. AI embeddings generated and stored.
4. User asks a question in chat.
5. Relevant results shown with context.
6. User can filter, refine, or follow-up.

## 6. Tech Stack

| Layer        | Technology                |
|--------------|--------------------------|
| Frontend     | Next.js, Tailwind        |
| Backend      | Node.js/Express          |
| Embeddings   | OpenAI/Cohere API        |
| Vector Store | Pinecone/Weaviate/Milvus |
| Auth         | Google, Slack OAuth      |
| Storage      | Supabase/Postgres        |

## 7. Demo Walkthrough

- Connect accounts via OAuth.
- Import and process sample data.
- Ask questions in chat UI.
- Receive instant, context-rich answers.
- Follow up and filter results.

## 8. Future Roadmap

- More integrations: Notion, GitHub, Drive.
- Team features, analytics, summarization.
- Enterprise readiness: SSO, advanced security.

## 9. Why TeamMind?

- Boosts productivity by ending knowledge silos.
- AI-powered for smarter, faster answers.
- Extensible, secure, and ready for real-world teams.

---

**Contact:** [Your Name & Email]
