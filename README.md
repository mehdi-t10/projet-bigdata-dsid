# Projet Big Data — M1 MIAGE (UE DSID) — Université Paris-Saclay

**Auteur :** Mehdi MRABEUT · **Enseignant :** Guilherme ANTUNES

Chaîne d'ingestion **RAW → Bronze → Silver** :

| Flux | Source | Chemin |
|---|---|---|
| 1 | API TMDB (GET, authentification par token) | Airbyte → MinIO (RAW) → PostgreSQL `bronze` |
| 2 | CSV des cinémas d'Île-de-France (CNC) | Airbyte → MinIO (RAW) → PostgreSQL `bronze` |
| 3 | EspoCRM (MariaDB) | Airbyte → PostgreSQL `bronze` |
| — | Transformations SQL + contrôles qualité | `bronze` → `silver` (PostgreSQL) |

## Contenu du dépôt

- `MRABEUT_Mehdi_Rapport_BigData.pdf` : rapport complet (sources, contrat de données, flux, transformations, contrôles, reproductibilité, captures)
- `MRABEUT_Mehdi_Projet_BigData_DSID.zip` : rapport + dossier technique (README, compose.yaml, .env.example, connecteur Airbyte, scripts SQL Silver, contrôles, documentation, diagrammes UML)

## Relancer le projet

1. Télécharger et dézipper `MRABEUT_Mehdi_Projet_BigData_DSID.zip`.
2. Suivre le `README.md` du dossier `dossier_technique`.

> Le fichier `.env` (secrets) n'est pas fourni : copier `.env.example` en `.env` et renseigner ses propres mots de passe.
