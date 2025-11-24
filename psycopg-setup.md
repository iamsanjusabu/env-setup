# PostgreSQL Setup for Python (psycopg)

sudo -i -u postgres
psql
CREATE ROLE sanjusabu WITH LOGIN SUPERUSER PASSWORD 'mypassword';
\q
exit

sudo nvim /etc/postgresql/16/main/pg_hba.conf
# change ONLY these two lines:
# local   all             postgres            peer   ->   md5
# local   all             all                 peer   ->   md5

sudo systemctl restart postgresql

# Terminal test
sudo psql -U sanjusabu -d postgres

# Python test
import psycopg
with psycopg.connect(
    host="localhost",
    dbname="postgres",
    user="sanjusabu",
    password="mypassword"
) as conn:
    with conn.cursor() as cur:
        cur.execute("SELECT 1;")
        print(cur.fetchone())
