# Paris je t'aime — équipe digitale & data

Nous sommes l'équipe digitale & data de **Paris je t'aime – Office du Tourisme et des Congrès de Paris**.
Nous construisons les outils qui rendent l'offre touristique parisienne plus facile à trouver, que ce soit pour les visiteurs, pour les professionnels ou pour les assistants IA.

🌐 [parisjetaime.com](https://parisjetaime.com) · 📅 [agenda.parisjetaime.com](https://agenda.parisjetaime.com)

---

## L'agenda des sorties à Paris, en accès libre

Chaque nuit, notre pipeline collecte les événements parisiens depuis plusieurs sources, supprime les doublons, les note, les réécrit et les traduit. Le résultat alimente notre agenda et est ouvert à tous :

| Service | Adresse | Pour qui |
|---|---|---|
| **API REST** | [`api.parisjetaime.com`](https://api.parisjetaime.com/docs) (documentation interactive sur `/docs`) | Sites, applications, ChatGPT Actions, Gemini Function Calling |
| **Serveur MCP** | `https://mcp.parisjetaime.com/mcp` | Claude et tout assistant compatible [Model Context Protocol](https://modelcontextprotocol.io) |

On peut y chercher des expositions, concerts, spectacles, festivals, événements sportifs, salons ou sorties de nuit, et filtrer par date, arrondissement ou gratuité. Les fiches sont disponibles en français et en anglais (`lang=en`).

**Essayer l'API**

```bash
curl "https://api.parisjetaime.com/events?category=expositions&free_only=true&limit=5"
```

**Ajouter le serveur MCP à Claude Code**

```bash
claude mcp add --transport http paris-je-t-aime https://mcp.parisjetaime.com/mcp
```

Dans Claude (web ou desktop) : *Paramètres → Connecteurs → Ajouter un connecteur personnalisé*, puis coller l'adresse ci-dessus.

> L'accès est gratuit et ne demande pas de clé. Merci de rester sous **30 requêtes par minute**.

---

## Nos autres chantiers

- **Accessibilité** : outils d'audit et de suivi de l'accessibilité des établissements partenaires.
- **Événementiel et congrès** : calculateur d'impact des événements (empreinte carbone, retombées économiques, héritage).
- **Données** : extraction, consolidation et mise à disposition des données touristiques.

Ces outils sont internes, leurs dépôts sont privés.

**Ce que nous utilisons** : Python · FastAPI · PostgreSQL / Supabase · React · Docker · MCP

---

<details>
<summary>🇬🇧 In English</summary>

We are the digital & data team of **Paris je t'aime, the Paris Convention and Visitors Bureau**.

Our events pipeline collects, deduplicates, scores, rewrites and translates Parisian events every night. The results are open to everyone, free of charge and without an API key:

- **REST API**: [`api.parisjetaime.com`](https://api.parisjetaime.com/docs), interactive docs at `/docs`
- **MCP server**: `https://mcp.parisjetaime.com/mcp`, for Claude and any MCP-compatible assistant

Add `lang=en` to get English listings. Please stay under 30 requests per minute.

</details>
