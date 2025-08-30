# 🧠 TeamMind – AI-Powered Knowledge Management Platform

TeamMind is a collaborative platform designed to **help teams centralize knowledge, integrate productivity tools, and leverage AI for faster decision-making**.  
Built with **Next.js, Supabase, OpenAI, and Edge Functions**, it seamlessly connects with **Slack** and **Google Drive** to provide a unified knowledge hub.

---

## 🚀 Features
- 🔎 **Semantic Search** – Retrieve documents and messages using vector embeddings.  
- 🧠 **AI-Powered Assistant** – Context-aware Q&A across Slack and Google Drive.  
- 📂 **Knowledge Hub** – Centralized storage and organization of team data.  
- ⚡ **Edge Functions** – Fast, scalable, and secure API endpoints.  
- 🔗 **Integrations** – Works with Slack & Google Drive.  
- 🔒 **Secure Access** – Powered by Supabase authentication and policies.  

---

## 🛠️ Tech Stack
- **Frontend:** Next.js (React + Tailwind CSS)  
- **Backend:** Edge Functions (Next.js API Routes)  
- **Database:** Supabase (Postgres + Vector DB for embeddings)  
- **AI/ML:** OpenAI API (LLM + Embeddings)  
- **Integrations:** Slack API, Google Drive API  
- **Hosting:** Vercel (Frontend + API) and Supabase (DB + Auth)  

---

## 🔄 System Workflow

```mermaid
flowchart TD
    A[User Query] --> B[Frontend - Next.js]
    B --> C[API Routes - Edge Functions]
    C --> D[OpenAI API - LLM + Embeddings]
    C --> E[Supabase - Postgres + Vector DB]
    C --> F[Slack Integration]
    C --> G[Google Drive Integration]
    E --> C
    D --> C
    C --> B
    B --> H[Response to User]
graph TD
    subgraph Client
        FE[Frontend - Next.js]
    end
    
    subgraph Backend
        API[API Routes - Edge Functions]
        DB[(Supabase: Postgres + Vector DB)]
    end
    
    subgraph AI
        LLM[OpenAI API - LLM & Embeddings]
    end
    
    subgraph Integrations
        Slack[Slack API]
        GDrive[Google Drive API]
    end
    
    FE --> API
    API --> LLM
    API --> DB
    API --> Slack
    API --> GDrive
    DB --> API
    LLM --> API
    API --> FE
gantt
    title TeamMind Development Roadmap
    dateFormat  YYYY-MM-DD
    section Planning
    Requirements Gathering      :done,    a1, 2025-01-01, 2025-01-10
    Architecture Design         :done,    a2, 2025-01-11, 2025-01-20
    
    section Development
    Frontend Development        :active,  b1, 2025-01-21, 2025-02-10
    Backend Development         :         b2, 2025-01-25, 2025-02-15
    Database Setup & Supabase   :         b3, 2025-02-01, 2025-02-20
    
    section AI & Integrations
    OpenAI Integration          :         c1, 2025-02-10, 2025-02-25
    Slack + Google Drive APIs   :         c2, 2025-02-12, 2025-02-28
    
    section Testing & Deployment
    Internal Testing            :         d1, 2025-03-01, 2025-03-10
    Deployment (Vercel + Supabase) :     d2, 2025-03-11, 2025-03-15
    Final Release               :milestone, d3, 2025-03-15, 1d
git clone https://github.com/your-username/teammind.git
cd teammind
