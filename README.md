# Bonjour, je suis T-Rudy 👋

Je construis des **applications d'IA en Python** : des agents qui choisissent eux-mêmes leurs outils,
des chatbots qui répondent à partir de documents, et surtout des **évaluations chiffrées** pour
mesurer ce qui marche vraiment, trouver les bugs et prouver les améliorations. Basé à Paris.

---

## 🔎 [JobScout](https://github.com/T-R-Bama/JobScout) : agent IA de veille d'offres d'emploi

[![Démo](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://jobscout-trbama.streamlit.app)
[![Tests](https://github.com/T-R-Bama/JobScout/actions/workflows/tests.yml/badge.svg)](https://github.com/T-R-Bama/JobScout/actions/workflows/tests.yml)

Un agent qui **cherche des offres d'emploi, les résume et les compare à un CV**, avec un score
d'adéquation. La boucle d'agent (appel d'outils) est **codée à la main, sans framework**.

- **Évaluation sur 8 questions** : avec `gpt-oss-120b`, 100 % de réussite sur toutes les métriques
  (offre pertinente, lieu respecté, aucun lien inventé, CV lu à bon escient).
- **Un vrai bug trouvé par la mesure** : le filtre de lieu cachait 77 % des offres françaises
  (« Paris » n'était pas reconnu comme « France ») ; corrigé, 100 % des offres visibles.
- **Garde-fou contre les hallucinations** : tout lien que le modèle invente est retiré de la réponse.
- **Mémoire de conversation** (« compare la 2e offre à mon CV »), démo protégée pour un quota gratuit,
  **49 tests automatiques** lancés par GitHub Actions.

`Python` · `Groq` · `Ollama` · `function calling` · `Streamlit` · `pytest` · `GitHub Actions`

## 📚 [AskMyDocs](https://github.com/T-R-Bama/AskMyDocs) : chatbot RAG sur tes documents

[![Démo](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://chatbot-rag-trbama.streamlit.app)

Pose des questions à tes documents (PDF, Word, Markdown, pages web) et obtiens des **réponses sourcées**.

- **Évaluation sur 20 questions** : 100 % de réponses correctes avec `gpt-oss-120b`, refus d'inventer
  sur les questions hors sujet.
- **De la mesure à l'amélioration** : l'analyse des échecs a montré que le modèle d'embeddings
  tronquait les passages ; la **recherche hybride** sémantique + BM25 fait passer le bon passage
  en tête de **56 % à 78 %**.

`Python` · `RAG` · `ChromaDB` · `BM25` · `Groq` · `Ollama` · `Claude` · `Streamlit`

---

### Autres projets

- [**Atelier Tudor**](https://t-r-bama.github.io/refonte-artisan/) : site vitrine d'une menuiserie
  artisanale (HTML / CSS), en ligne sur GitHub Pages.
- [**gestion-inventaire**](https://github.com/T-R-Bama/gestion-inventaire) : gestion de stock en
  ligne de commande, en Python (ajout, recherche, alertes de stock).

### Ce que je sais faire

| Domaine | Outils |
|---|---|
| IA générative | Agents avec appel d'outils, RAG, prompts, LLM hébergés (Groq, Claude) et locaux (Ollama) |
| Qualité | Évaluations reproductibles, métriques déterministes et LLM juge, tests `pytest`, intégration continue |
| Applications | Python, Streamlit, ChromaDB, API REST, déploiement sur Streamlit Community Cloud |
| Web | HTML, CSS, GitHub Pages |
