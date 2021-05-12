# `create-azure-search-indexer` GitHub Action

This repository contains an action for use with GitHub Actions, which creates a new Indexer within a specified Azure Cognitive Search instance.

## Usage

Create a new indexer using a local definition file:

```yaml
- name: Create indexer
  uses: heyitsmemark/create-azure-search-indexer@1.0.2
  with:
    azureSearchInstance: plop
    azureSearchAdminKey: ${{ secrets.AZURE_SEARCH_ADMIN_KEY }}
    indexerDefinitionFile: ./path/to/indexer.json
```

Create a new indexer using a remote definition file:

```yaml
- name: Create indexer 
  uses: heyitsmemark/create-azure-search-indexer@1.0.2
  with:
    azureSearchInstance: plop
    azureSearchAdminKey: ${{ secrets.AZURE_SEARCH_ADMIN_KEY }}
    indexerDefinitionUri: https://domain.com/path/to/indexer.json
```

## Samples

Sample workflows are available [here](.github/workflows/)