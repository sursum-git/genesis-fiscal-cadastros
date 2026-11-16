# Catálogos fiscais de referência

O pacote atual é `genesis-cadastros-2026.11.16.2.zip`. A data de referência é 16 de novembro de 2026.

| Arquivo | Chave de correspondência | Conteúdo |
| --- | --- | --- |
| `ncm.csv` | `ncm.br.codigo` | 10.516 códigos de oito dígitos da tabela vigente do Classif |
| `cnae.csv` | `cnae.br.codigo` | 1.332 subclasses CNAE 2.3 do IBGE |
| `cest.csv` | `cest.br.codigo` | 1.051 códigos dos anexos II a XXVI do Convênio ICMS 142/18, incluindo oito revogados |
| `tipi.csv` | `tipi.br.codigo` | 15.065 linhas TIPI da tabela oficial da Receita Federal |
| `ex-tipi.csv` | Código TIPI e código EX | 587 destaques da tabela oficial da Receita Federal |

- Os códigos devem ser tratados como texto para preservar zeros à esquerda. O CEST mantém a expressão NCM/SH apresentada no anexo. Uma linha pode conter mais de um código ou uma posição da nomenclatura.
- Nas linhas CEST, datas vazias indicam que a data específica da redação não foi extraída. A coluna `observacao` identifica o anexo e, quando disponível, a nota de atualização.
- As alíquotas da TIPI usam pontos percentuais e ponto decimal. O texto `NT` e as alíquotas vazias foram preservados. Nas linhas EX em que a planilha omite o código TIPI, o vínculo usa o código da linha anterior aplicável.
- `fontes.json` registra a edição oficial e os hashes de origem. `manifest.json` registra os modelos e hashes dos arquivos dentro do ZIP.
- O formato é de referência para carga por código. O assistente **Importar Release de Perfis** usa outro leiaute. Carregue NCM e TIPI antes de EX TIPI para permitir as associações.

A versão `2026.11.16.1` permanece disponível em seu ZIP original. A versão `2026.11.16.2` mantém os três catálogos daquela edição e acrescenta TIPI e EX TIPI.
