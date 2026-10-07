# Azure CLI: comandos básicos

> Material de estudo. Use placeholders; nunca publique IDs de subscription, tenant ou credenciais reais.

## Login e contexto
```bash
az login
az account show                                 # subscription ativa
az account set --subscription "<SUBSCRIPTION>"  # trocar de subscription
```

## Consultas comuns
```bash
az group list --output table
az vm list --resource-group <RG> --show-details --output table
```

## Controle de custo
```bash
# Desalocar uma VM (para a cobrança de computação)
az vm deallocate --resource-group <RG> --name <VM>
```

## Dicas
- `--output table` e `--query` ajudam na leitura.
- Parar a VM pelo sistema operacional **não** para a cobrança; é preciso desalocar.
