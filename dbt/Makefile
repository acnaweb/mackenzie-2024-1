export PROJECT_DIR=test
export PROFILE_DIR=$(shell pwd)/profiles

# Local development
install:
	python -m venv venv; \
	. venv/bin/activate; \
	pip install --upgrade pip; \
	pip install -e .[interactive]; \

test:
	pytest

create_dbt:
	dbt init --profiles-dir $(PROFILE_DIR)

debug:
	dbt debug --profiles-dir $(PROFILE_DIR) --project-dir $(PROJECT_DIR)

run: 	
	dbt run --profiles-dir $(PROFILE_DIR) --project-dir $(PROJECT_DIR)

run_debug: 	
	dbt run --profiles-dir $(PROFILE_DIR) --project-dir $(PROJECT_DIR) --debug

docs: 	
	dbt docs generate --profiles-dir $(PROFILE_DIR) --project-dir $(PROJECT_DIR)
	dbt docs serve --profiles-dir $(PROFILE_DIR) --project-dir $(PROJECT_DIR)
