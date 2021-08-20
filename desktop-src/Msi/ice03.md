---
description: ICE03 valida os tipos de dados e chaves estrangeiras com base na tabela Validação e nas tabelas de banco de \_ dados no arquivo .msi dados.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814bb8023b32c85e752201909f77bd851ec3545c907c03e1c2349a34117d4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946640"
---
# <a name="ice03"></a>ICE03

ICE03 valida os tipos de dados e chaves estrangeiras com base na tabela [ \_ Validação](-validation-table.md) e nas tabelas de banco de dados no arquivo .msi dados.

## <a name="result"></a>Resultado

ICE03 posta as seguintes mensagens para os erros de validação.



| Mensagem de erro ICE03                                                       | Descrição                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chave primária duplicada                                                     | As chaves primárias de uma nova linha duplicam as chaves primárias de uma linha existente. A coluna Anulada da tabela [ \_ Validação mostra](-validation-table.md) as chaves primárias no banco de dados.                                                                                              |
| Não é uma coluna que pode ser anulada                                                     | Uma coluna de tabela que não é especificada como anulada na coluna Anulada da tabela [ \_ Validação](-validation-table.md) contém uma entrada que é Null.                                                                                                                                |
| Não é uma chave estrangeira válida                                                   | Uma coluna que é uma chave estrangeira em uma segunda tabela contém uma entrada que não existe na chave primária da segunda tabela.                                                                                                                                                          |
| O valor excede MaxValue                                                    | O valor numérico de uma entrada em uma tabela de banco de dados excede o limite máximo especificado para esse campo na coluna MaxValue da tabela [ \_ Validação](-validation-table.md).                                                                                                           |
| Valor abaixo de MinValue                                                      | O valor numérico de uma entrada em uma tabela de banco de dados é menor que o limite mínimo especificado para esse campo na coluna MinValue da tabela [ \_ Validação](-validation-table.md).                                                                                                      |
| Valor que não é um membro do conjunto                                             | O valor de uma entrada em uma tabela de banco de dados não é um membro do conjunto aceitável de valores especificado para esse campo na coluna Definir da tabela [ \_ validação](-validation-table.md).                                                                                                  |
| Cadeia de caracteres de versão inválida                                                    | Consulte o [tipo de](version.md) dados Version.                                                                                                                                                                                                                                                 |
| Todos os maiúsculas e médios necessários                                                   | Consulte o [tipo de dados UpperCase.](uppercase.md)                                                                                                                                                                                                                                             |
| Cadeia de caracteres GUID inválida                                                       | Consulte o tipo de dados [GUID.](guid.md)                                                                                                                                                                                                                                                       |
| Nome de arquivo/uso inválido de curingas                                      | O banco de dados contém um nome de arquivo inválido ou um curinga incorreto. Consulte o [tipo de dados WildCardFilename.](wildcardfilename.md)                                                                                                                                                          |
| Identificador inválido                                                        | Consulte o [tipo de dados](identifier.md) Identificador.                                                                                                                                                                                                                                           |
| ID de idioma inválida                                                       | O banco de dados contém um LANGID (Identificador de Idioma Numérico) inválido. Consulte o [Tipo de dados](language.md) Language. Consulte [Constantes e cadeias de caracteres do identificador de idioma.](../intl/language-identifier-constants-and-strings.md) Por exemplo, 1033 para os EUA e 0 para neutralidade de idioma.<br/> |
| Nome de arquivo inválido                                                          | Consulte o [tipo de dados Filename.](filename.md)                                                                                                                                                                                                                                               |
| Caminho completo inválido                                                         | Consulte os tipos de dados [Path,](path.md) [AnyPath](anypath.md)e [Paths.](paths.md)                                                                                                                                                                                                      |
| Cadeia de caracteres condicional ruim                                                    | O banco de dados contém uma cadeia de caracteres condicional inválida. Essa é uma cadeia de caracteres de texto que deve ser avaliada como TRUE ou FALSE de acordo com a [sintaxe de instrução condicional](conditional-statement-syntax.md). Consulte o [Tipo de](condition.md) dados Condição.                                           |
| Cadeia de caracteres de formato inválido                                                     | Consulte o [tipo de dados](formatted.md) Formatado.                                                                                                                                                                                                                                             |
| Cadeia de caracteres de modelo inválida                                                   | Consulte o [Tipo de](template.md) dados modelo.                                                                                                                                                                                                                                               |
| Cadeia de caracteres DefaultDir inválida                                                 | Consulte o [tipo de dados DefaultDir.](defaultdir.md)                                                                                                                                                                                                                                           |
| Caminho do Registro inválido                                                     | Consulte o [tipo de dados RegPath.](regpath.md)                                                                                                                                                                                                                                                 |
| Dados customSource ruins                                                     | Consulte o [tipo de dados CustomSource.](customsource.md)                                                                                                                                                                                                                                       |
| Cadeia de caracteres de propriedade inválida                                                   | Consulte o [Tipo de](property.md) dados Property.                                                                                                                                                                                                                                               |
| Dados ausentes na \_ tabela validação ou banco de dados antigo                        | Há colunas no banco de dados que não estão listadas na coluna Coluna da tabela [ \_ Validação](-validation-table.md). O banco de dados e \_ a tabela validação não são corresponderem                                                                                                           |
| Sintaxe/nome de gabinete ruim                                                   | Consulte o tipo [de dados De](cabinet.md) gabinete.                                                                                                                                                                                                                                                 |
| \_Tabela de validação: cadeia de caracteres de categoria inválida                               | Esse é um erro ao ser autor da tabela \_ validação. A validação não reconhece a cadeia de caracteres de categoria usada para essa coluna específica na tabela \_ Validação. Consulte [Tipos de Dados de Coluna](column-data-types.md) e especifique uma categoria válida.                                           |
| \_Tabela de validação: os dados na coluna KeyTable estão incorretos                  | A coluna KeyTable na tabela \_ Validação faz referência a uma tabela que não existe no banco de dados.                                                                                                                                                                                     |
| \_Tabela de validação: Valor na coluna MaxValue < que na coluna MinValue | Esse é um erro ao ser autor da tabela [ \_ validação](-validation-table.md). Min sempre deve ser menor ou igual a Max.                                                                                                                                                              |
| Destino de atalho ruim                                                       | Consulte o [tipo de](shortcut.md) dados Atalho.                                                                                                                                                                                                                                               |
| Estouro de cadeia de caracteres (maior que o comprimento permitido na coluna)                 | O comprimento da cadeia de caracteres é maior que a largura da coluna especificada pela definição da coluna. Observe que o instalador não limita internamente a largura da coluna ao valor especificado. Consulte [Formato de definição de coluna](column-definition-format.md).                                         |
| Erro indefinido                                                           | Erro desconhecido.                                                                                                                                                                                                                                                                            |
| A coluna não pode ser localizada                                                | As colunas de chave primária não podem ser localizadas.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 
