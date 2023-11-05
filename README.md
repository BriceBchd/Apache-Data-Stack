# RL-deep-stats

## Getting Started

```bash
mkdir -p ./dags ./logs ./plugins ./config
echo -e "AIRFLOW_UID=$(id -u)" > .env
docker compose up airflow-init
docker compose up
```

## Clean Up

```bash
docker compose down --volumes --remove-orphans
```

## CLI Commands

```bash
docker compose run airflow-worker airflow info
docker compose run airflow-worker airflow list_dags
docker compose run airflow-worker airflow list_tasks <dag_id>
```

---

## References

- [Airflow](https://airflow.apache.org/docs/apache-airflow/stable/index.html)
- [Airflow Docker](https://airflow.apache.org/docs/apache-airflow/stable/start/docker.html)
