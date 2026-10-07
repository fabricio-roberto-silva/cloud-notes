# OCI CLI: comandos básicos

> Material de estudo. Use placeholders; nunca publique OCIDs, tenancy ou chaves reais.

## Configuração inicial
```bash
oci setup config      # gera ~/.oci/config e o par de chaves da API
oci iam region list   # testa a autenticação
```

## Consultas comuns
```bash
# Listar instâncias de um compartment
oci compute instance list --compartment-id <COMPARTMENT_OCID> --output table

# Listar redes virtuais (VCNs)
oci network vcn list --compartment-id <COMPARTMENT_OCID> --output table
```

## Dicas
- `--output table` deixa a saída legível; `--query` filtra campos (JMESPath).
- Use perfis no `~/.oci/config` para separar ambientes.
