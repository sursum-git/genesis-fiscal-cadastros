# Catálogos fiscais de referência

O pacote `genesis-cadastros-2026.11.16.1.zip` reúne três catálogos públicos. A data de referência é 16 de novembro de 2026.

| Arquivo | Chave de correspondência | Conteúdo |
| --- | --- | --- |
| `ncm.csv` | `ncm.br.codigo` | 10.516 códigos de oito dígitos da tabela vigente do Classif |
| `cnae.csv` | `cnae.br.codigo` | 1.332 subclasses CNAE 2.3 do IBGE |
| `cest.csv` | `cest.br.codigo` | 1.051 códigos dos anexos II a XXVI do Convênio ICMS 142/18, incluindo oito revogados |

- Os códigos devem ser tratados como texto para preservar zeros à esquerda. O CEST mantém a expressão NCM/SH tal como apresentada no anexo. Uma linha pode conter mais de um código ou uma posição da nomenclatura.
- Nas linhas CEST, as datas vazias indicam que não foi extraída uma data específica daquela redação. A coluna `observacao` identifica o anexo e, quando disponível, a nota de atualização. Os registros marcados como revogados não representam classificações vigentes.
- `fontes.json` identifica os documentos oficiais. `manifest.json` registra os modelos e os hashes dos arquivos dentro do ZIP.
- O formato é de referência para carga por código. O assistente **Importar Release de Perfis** usa outro leiaute. A carga no Odoo deve ocorrer em ordem NCM, CNAE e CEST para permitir a associação com o NCM e a classificação CNAE.

## Conferência dos catálogos relacionados

A base conferida tinha NF-e, CT-e e NFS-e, os nove tributos do escopo fiscal implantado e doze modalidades. Esses cadastros dependem dos módulos e do escopo de cálculo do Genesis.

A comparação com a planilha oficial da TIPI encontrou códigos e destaques EX ausentes e alíquotas divergentes na base. TIPI e EX TIPI aguardam conciliação antes de uma publicação como tabelas vigentes.
