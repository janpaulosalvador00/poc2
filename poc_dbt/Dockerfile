FROM quay.io/astronomer/astro-runtime:12.0.0

#Set enviroment variables
ENV AIRFLOW_HOME=/usr/local/airflow
ENV DBT_HOME=/usr/local/airflow/dbt_venv

#Install dbt-snowflake in a virtual enviroment
RUN python -m venv $DBT_HOME && \
    $DBT_HOME/bin/pip install --no-cache-dir dbt-snowflake

#Ensure virtual enviroment is activated for Airflow
ENV PATH="${DBT_HOME}/bin:${PATH}"