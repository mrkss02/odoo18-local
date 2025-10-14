# Personal Odoo 18 development repo

## Setup

```bash
# 1. Clone Odoo source and add enterprise addons
git clone https://github.com/odoo/odoo.git --depth 1 --branch 18.0

# 2. Create config files
cp .env.example .env
cp conf/odoo.conf.example conf/odoo.conf

# 3. Start PostgreSQL
docker-compose up -d

# 4. Create Python virtual environment
python3 -m venv venv
source venv/bin/activate

# 5. Install dependencies
pip install -r odoo/requirements.txt

# 6. Run Odoo
python odoo/odoo-bin -c conf/odoo.conf
```

Clone addons into `custom-addons/`

Runs on http://localhost:8018