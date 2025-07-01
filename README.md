Brazil Finance Automation
=========================
Manda transações de bancos brasileiros (Nubank, Itaú, etc.) para o YNAB.

Prerequisites
-------------
You must go through [all the steps here](https://github.com/pluggyai/meu-pluggy?tab=readme-ov-file#connecting-your-bank-account-to-meupluggy) to create a MyPluggy account, a developer portal account, and link them together!

Use
---
### Running Locally
1. Fork this repo
1. Clone your fork to your machine
1. [Install the `uv` Python package manager](https://docs.astral.sh/uv/getting-started/installation/#pypi)
1. Setup the repo:
   ```
   make setup
   ```
   and fill in the created `.env` file, using the comments as guidance on where to get the values.
1. Sync transactions with:
   ```
   make run
   ```
1. Run tests with:
   ```
   make test
   ```

### Running Every Day
1. Fork this repo
1. Modify the `.github/workflows/sync-to-ynab.yml` file to pass in the appropriate environment variables based on the contents of your `.env` file
1. Update the repository's secrets to provide the values for the environment variables
1. Enable Github Actions on the repo
1. Test the action by clicking "Run"
