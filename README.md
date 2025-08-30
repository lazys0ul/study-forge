# 📚 Team Mind
import matplotlib.pyplot as plt
import matplotlib.patches as mpatches

# Create figure
fig, ax = plt.subplots(figsize=(12, 7))
ax.set_xlim(0, 12)
ax.set_ylim(0, 9)
ax.axis("off")

# Define components (x, y, width, height, label, color)
components = [
    (1, 6.5, 2.5, 1.2, "Frontend\n(Next.js)", "#bbdefb"),
    (5, 6.5, 2.5, 1.2, "API Routes\n(Edge Functions)", "#c8e6c9"),
    (9, 6.5, 2.5, 1.2, "OpenAI API\n(Embeddings + LLM)", "#ffe0b2"),
    (5, 3.8, 2.5, 1.2, "Supabase\n(Postgres + Vector DB)", "#fff9c4"),
    (1, 1.5, 2.5, 1.2, "Slack\nIntegration", "#f8bbd0"),
    (5, 1.5, 2.5, 1.2, "Google Drive/Docs\nIntegration", "#d1c4e9")
]

# Draw components
for x, y, w, h, label, color in components:
    rect = mpatches.FancyBboxPatch((x, y), w, h,
                                   boxstyle="round,pad=0.3,rounding_size=0.2",
                                   fc=color, ec="black", lw=1.5)
    ax.add_patch(rect)
    ax.text(x + w/2, y + h/2, label, ha="center", va="center", fontsize=10, weight="bold")

# Draw arrows
def draw_arrow(x1, y1, x2, y2, text=None):
    ax.annotate("", xy=(x2, y2), xytext=(x1, y1),
                arrowprops=dict(arrowstyle="->", lw=1.5, color="black"))
    if text:
        ax.text((x1+x2)/2, (y1+y2)/2 + 0.2, text, ha="center", va="bottom", fontsize=9, style="italic")

# Connections
draw_arrow(3.5, 7.1, 5, 7.1, "API Calls")
draw_arrow(7.5, 7.1, 9, 7.1, "Embedding / Query")
draw_arrow(6.25, 6.5, 6.25, 5, "Database Queries")
draw_arrow(2.25, 2.7, 6.25, 3.8, "Messages / Updates")
draw_arrow(6.25, 2.7, 6.25, 3.8, "Docs / Knowledge Base")
draw_arrow(6.25, 5, 6.25, 6.5, "Query Results")

# Title
ax.set_title("TeamMind – System Architecture", fontsize=16, weight="bold")

plt.savefig("system_architecture.png", dpi=300, bbox_inches="tight")
plt.show()

