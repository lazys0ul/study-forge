# 📚 Team Mind
graph TD
    subgraph Initial Setup
        A[User connects Slack & Google Drive] --> B{Initial Data Import}
    end

    subgraph Data Ingestion Pipeline
        subgraph Real-Time Sync
            C(New Slack Message) --> D[Extract Content]
        end
        subgraph Periodic Sync
            E(Google Doc Updated) --> D
        end
        D --> F[Generate Embedding via OpenAI API]
        F --> G[Store in Supabase pgvector]
    end

    subgraph Search Workflow
        H[User Query] --> I[Next.js Frontend]
        I --> J[API Route]
        J --> K[Generate Query Embedding]
        K --> L[Hybrid Search (Supabase RPC)]
        L --> M[Fetch & Enhance Results]
        M --> N[Display to User]
    end

    B --> G
    G --> L
    
