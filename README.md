Drax — Site de présentation
===========================

Site Nuxt 3 de présentation pour Drax (l'assistant IA de Drix).

But: ce dépôt a été généré par des agents automatisés. Les contributions se font via issues/PRs.

Démarrage local
---------------

Prérequis: Node.js >=18, pnpm/npm, Git

Installation:

```bash
# installer deps
npm install
# lancer en dev
npm run dev
```

Workflow automatisé
-------------------

- Le projet est orchestré par le skill `launch-dev-team` (scripts/agent_orchestrator.py).
- Les agents (implementer, reviewer, errorwatch) traitent les issues étiquetées `ready`.
- Les agents créent des branches et ouvrent des PRs automatiquement (si autorisé). Les merges vers `main` nécessitent une approbation humaine.

Contribuer
----------

1. Crée une issue décrivant la page ou la fonctionnalité (label `ready` pour la prise en charge automatique).
2. L'implementer agent générera la page, ouvrira une PR et un reviewer automatisé exécutera des checks.
3. Un humain doit approuver la PR pour merger sur `main`.

Maintenance & autonomie
-----------------------

- Pour modifier le comportement des agents: consulte `skills/launch-dev-team/scripts/`.
- Pour exécuter l'orchestrator en mode simulation: `python3 skills/launch-dev-team/scripts/agent_orchestrator.py --dry-run`.
- Pour exécuter les implementers manuellement: `python3 skills/launch-dev-team/scripts/agent_worker_impl.py --issue <num> [--apply] --repo-path <path>`.

Contact
-------

Drix — @OxDrix (Telegram) — drix@example.com

Licence
-------

MIT
