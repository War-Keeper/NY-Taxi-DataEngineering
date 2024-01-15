Git bash: cd ~/Documents/Projects/NY-Taxi-DataEngineering/01-docker-terraform


Create Postgres Container: 
docker run -it \
  -e POSTGRES_USER="root" \
  -e POSTGRES_PASSWORD="root" \
  -e POSTGRES_DB="ny_taxi" \
  -v c:/Users/Chintu/Documents/Projects/NY-Taxi-DataEngineering/Data/ny_taxi_postgres_data:/var/lib/postgresql/data \
  -p 5432:5432 \
  postgres:13

Install pgcli:
conda install -c conda-forge pgcli
pip install -U mycli

connect pgcli:
pgcli -h localhost -p 5432 -u root -d ny_taxi
