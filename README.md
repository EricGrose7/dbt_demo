# Snowflake and dbt Workflow

This repository contains a Data Build Tool (dbt) project for building a data warehouse in Snowflake. The project contains models for staging, transforming, and aggregating data from various data sources.

**Getting Started**   <br>
To use this project, you will need to have dbt installed on your local machine. You will also need access to a Snowflake account.

To get started, clone this repository to your local machine:

```bash 
git clone https://github.com/EricGrose7/dbt_snowflake.git
```

You will also need to set up your Snowflake credentials in a profiles.yml file. A template file is provided in the repository:

```yml   
dbt_snowflake:
  target: dev
  outputs:
    dev:
      type: snowflake
      account: <your_account_name>
      user: <your_username>
      password: <your_password>
      role: <your_role>
      database: <your_database>
      schema: <your_schema>
      warehouse: <your_warehouse>
      threads: 4
```

**Project Structure**   <br>
The dbt_snowflake project is organized into four main directories:

- models: This directory contains the dbt models for staging, transforming, and aggregating data from various data sources.
- data: This directory contains the source data used in the dbt models.
- macros: This directory contains macros used in the dbt models.
- tests: This directory contains tests for the dbt models.

**Models**   <br>
The dbt models in this project are organized into several directories based on their purpose:

- staging: This directory contains models for loading raw data into Snowflake.
- transform: This directory contains models for transforming the data into a format suitable for analysis.
- aggregate: This directory contains models for aggregating the data for reporting purposes.

**Macros**   <br>
The macros in this project are used to simplify the creation of dbt models. The macros are organized into several directories based on their purpose:

- date: This directory contains macros for working with dates in the dbt models.
- snowflake: This directory contains macros for working with Snowflake-specific features in the dbt models.
- string: This directory contains macros for working with strings in the dbt models.

**Tests**   <br>
The tests in this project are used to ensure that the dbt models are functioning correctly. The tests are organized into several directories based on their purpose:

- data: This directory contains test data used in the dbt model tests.
- unit: This directory contains unit tests for individual dbt models.
- integration: This directory contains integration tests for the entire dbt project.

**Conclusion**   <br>
This dbt project provides a solid foundation for building a data warehouse in Snowflake. The project contains models for staging, transforming, and aggregating data from various data sources. The project is organized into several directories based on their purpose, making it easy to navigate and understand. The project also includes tests to ensure that the dbt models are functioning correctly.

### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [chat](https://community.getdbt.com/) on Slack for live discussions and support
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices
