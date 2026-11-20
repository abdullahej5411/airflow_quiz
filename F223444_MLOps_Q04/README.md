# Airflow Quiz: Weekly Model Comparison DAG (F223444_MLOps_Q04)

Astro project (Astro Runtime 12.1.1) with one TaskFlow DAG.

- **DAG ID:** `weekly_model_comparison`
- **Schedule:** `@weekly`, start_date 2026-01-01, `catchup=False`
- **Start command:** `astro dev start`
- **Airflow UI:** http://localhost:8080 (login `admin` / `admin`)

## Structure
`preprocess_data` -> (`train_baseline`, `train_candidate`) -> `evaluate_models`

`train_baseline` and `train_candidate` run in parallel; `evaluate_models` runs only after both succeed.
