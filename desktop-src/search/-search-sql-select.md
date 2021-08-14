---
description: 'O seguinte mostra a sintaxe básica da instrução SELECT para uma consulta local:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instrução SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df8cc5f4b6bab673d20c981e44386d3fdbd651b5a2753d8c965ee55023a6562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227191"
---
# <a name="select-statement"></a>Instrução SELECT

O seguinte mostra a sintaxe básica da instrução SELECT para uma consulta local:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



O seguinte mostra a parte da coluna da sintaxe da instrução SELECT:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Os especificadores de coluna devem ser colunas de nome de propriedade válidas, separadas por vírgulas. Os nomes de coluna válidos são descrições de propriedade registradas ou são definidos pelo esquema do sistema de propriedades do Shell. Você pode selecionar somente as colunas marcadas como recuperáveis no esquema do sistema de propriedades. Se você usar maiúsculas e minúsculas para identificar propriedades que não são propriedades definidas pelo sistema, deverá colocar o especificador de coluna entre aspas duplas. Os nomes de propriedade definidos pelo sistema incluem todas as propriedades que começam com "System" (por exemplo, System. Contact. FirstName) e não exigem aspas.

> [!Note]  
> Você também pode colocar nomes de propriedade definidos pelo sistema entre aspas duplas para facilitar a leitura. Isso não afeta a compatibilidade.

 

Quando a consulta retorna um documento que não tem a coluna solicitada, o valor dessa coluna para o documento é **nulo**.

Você deve fornecer pelo menos um nome de coluna em uma instrução SELECT. na consulta linguagem SQL (SQL), você pode usar o asterisco ( \* ) para especificar que todas as colunas em uma tabela sejam retornadas. No entanto, nenhum conjunto definido e fixo de propriedades se aplica a todos os documentos. por esse motivo, o asterisco SQL não é permitido no <columns> especificador da instrução SELECT.

## <a name="getting-the-top-n-results"></a>Obtendo os n maiores resultados

Você pode especificar um número máximo de resultados a serem retornados usando a sintaxe superior:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Convertendo tipos de dados de coluna

Às vezes, talvez seja necessário converter dados de cadeia de caracteres extraídos de documentos como outro tipo de dados para que uma comparação apropriada possa ser feita. Para obter mais informações, consulte [convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md).

## <a name="examples"></a>Exemplos

Os exemplos a seguir retornam o nome e a URL dos documentos correspondentes.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



