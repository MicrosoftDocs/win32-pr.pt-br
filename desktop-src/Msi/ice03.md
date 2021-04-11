---
description: O ICE03 valida os tipos de dados e as chaves estrangeiras com base na \_ tabela de validação e nas tabelas de banco do dados no arquivo. msi.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017c13ee568a0efe4d88c28594fb568a7b4a0736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170235"
---
# <a name="ice03"></a>ICE03

O ICE03 valida os tipos de dados e as chaves estrangeiras com base na [ \_ tabela de validação](-validation-table.md) e nas tabelas de banco do dados no arquivo. msi.

## <a name="result"></a>Resultado

ICE03 posta as mensagens a seguir para os erros de validação.



| Mensagem de erro do ICE03                                                       | Descrição                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chave primária duplicada                                                     | As chaves primárias de uma nova linha duplicam as chaves primárias de uma linha existente. A coluna Nullable da [ \_ tabela de validação](-validation-table.md) mostra as chaves primárias no banco de dados.                                                                                              |
| Não é uma coluna anulável                                                     | Uma coluna de tabela que não é especificada como anulável na coluna anulável da [ \_ tabela de validação](-validation-table.md) contém uma entrada que é nula.                                                                                                                                |
| Não é uma chave estrangeira válida                                                   | Uma coluna que é uma chave estrangeira em uma segunda tabela contém uma entrada que não existe na chave primária da segunda tabela.                                                                                                                                                          |
| O valor excede MaxValue                                                    | O valor numérico de uma entrada em uma tabela de banco de dados excede o limite máximo especificado para esse campo na coluna MaxValue da [ \_ tabela de validação](-validation-table.md).                                                                                                           |
| Valor abaixo de MinValue                                                      | O valor numérico de uma entrada em uma tabela de banco de dados é menor que o limite mínimo especificado para esse campo na coluna MinValue da [ \_ tabela de validação](-validation-table.md).                                                                                                      |
| Valor não é um membro do conjunto                                             | O valor de uma entrada em uma tabela de banco de dados não é um membro do conjunto aceitável de valores especificado para esse campo na coluna de conjunto da [ \_ tabela de validação](-validation-table.md).                                                                                                  |
| Cadeia de caracteres de versão inválida                                                    | Consulte o tipo de dados [version](version.md) .                                                                                                                                                                                                                                                 |
| Todas as letras maiúsculas necessárias                                                   | Consulte o tipo de dados em [maiúsculas](uppercase.md) .                                                                                                                                                                                                                                             |
| Cadeia de caracteres GUID inválida                                                       | Consulte o tipo de dados [GUID](guid.md) .                                                                                                                                                                                                                                                       |
| Nome de arquivo/uso de curingas inválido                                      | O banco de dados contém um nome de arquivo inválido ou um curinga incorreto. Consulte o tipo de dados [WildCardFilename](wildcardfilename.md) .                                                                                                                                                          |
| Identificador inválido                                                        | Consulte o tipo de dados do [identificador](identifier.md) .                                                                                                                                                                                                                                           |
| ID de idioma inválida                                                       | O banco de dados contém um identificador de idioma numérico (LANGid) inválido. Consulte o tipo de dados [Language](language.md) . Consulte [constantes e cadeias de caracteres do identificador de linguagem](../intl/language-identifier-constants-and-strings.md). Por exemplo, 1033 para os EUA e 0 para idiomas neutros.<br/> |
| Nome de arquivo inválido                                                          | Consulte o tipo de dados [filename](filename.md) .                                                                                                                                                                                                                                               |
| Caminho completo inválido                                                         | Consulte os tipos de dados [Path](path.md), [AnyPath](anypath.md)e [Paths](paths.md) .                                                                                                                                                                                                      |
| Cadeia de caracteres condicional inadequada                                                    | O banco de dados contém uma cadeia de caracteres condicional inválida. Essa é uma cadeia de caracteres de texto que deve ser avaliada como verdadeira ou falsa de acordo com a [sintaxe da instrução condicional](conditional-statement-syntax.md). Consulte o tipo de dados [Condition](condition.md) .                                           |
| Cadeia de formato inválida                                                     | Consulte o tipo de dados [formatado](formatted.md) .                                                                                                                                                                                                                                             |
| Cadeia de caracteres de modelo inválida                                                   | Consulte o tipo de dados do [modelo](template.md) .                                                                                                                                                                                                                                               |
| Cadeia de caracteres DefaultDir inválida                                                 | Consulte o tipo de dados [DefaultDir](defaultdir.md) .                                                                                                                                                                                                                                           |
| Caminho de registro inválido                                                     | Consulte o tipo de dados [RegPath](regpath.md) .                                                                                                                                                                                                                                                 |
| Dados de Customize inválidos                                                     | Consulte o tipo de dados [Customize](customsource.md) .                                                                                                                                                                                                                                       |
| Cadeia de caracteres de propriedade inválida                                                   | Consulte o tipo de dados [Property](property.md) .                                                                                                                                                                                                                                               |
| Dados ausentes na \_ tabela de validação ou no banco de dados antigo                        | Há colunas no banco de dados que não estão listadas na coluna coluna da [ \_ tabela de validação](-validation-table.md). O banco de dados e a \_ tabela de validação não correspondem                                                                                                           |
| Sintaxe/nome de gabinete inválidos                                                   | Consulte o tipo de dados de [gabinete](cabinet.md) .                                                                                                                                                                                                                                                 |
| \_Tabela de validação: cadeia de caracteres de categoria inválida                               | Esse é um erro ao criar a \_ tabela de validação. A validação não reconhece a cadeia de caracteres de categoria usada para essa coluna específica na \_ tabela de validação. Consulte [tipos de dados de coluna](column-data-types.md) e especifique uma categoria válida.                                           |
| \_Tabela de validação: os dados na coluna keyTable estão incorretos                  | A coluna keyTable na \_ tabela de validação faz referência a uma tabela que não existe no banco de dados.                                                                                                                                                                                     |
| \_Tabela de validação: valor na coluna MaxValue < que na coluna MinValue | Esse é um erro ao criar a [ \_ tabela de validação](-validation-table.md). Min deve ser sempre menor ou igual ao máximo.                                                                                                                                                              |
| Destino de atalho inadequado                                                       | Consulte o tipo de dados de [atalho](shortcut.md) .                                                                                                                                                                                                                                               |
| Estouro de cadeia de caracteres (maior que o comprimento permitido na coluna)                 | O comprimento da cadeia de caracteres é maior que a largura da coluna especificada pela definição de coluna. Observe que o instalador não limita internamente a largura da coluna ao valor especificado. Consulte [formato de definição de coluna](column-definition-format.md).                                         |
| Erro indefinido                                                           | Erro desconhecido.                                                                                                                                                                                                                                                                            |
| A coluna não pode ser localizada                                                | As colunas de chave primária não podem ser localizadas.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 
