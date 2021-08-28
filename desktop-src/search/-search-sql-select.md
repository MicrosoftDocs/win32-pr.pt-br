---
description: 'Veja a seguir a sintaxe básica da instrução SELECT para uma consulta local:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instrução SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3655f279a149017da841f296ad29c18518bc96
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883434"
---
# <a name="select-statement"></a>Instrução SELECT

Veja a seguir a sintaxe básica da instrução SELECT para uma consulta local:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



Veja a seguir a parte da coluna da sintaxe da instrução SELECT:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Os especificadores de coluna devem ser colunas de nome de propriedade válidas, separadas por vírgulas. Nomes de coluna válidos são descrições de propriedade registradas ou são definidos pelo Esquema do Sistema de Propriedades do Shell. Você pode selecionar apenas as colunas marcadas como recuperáveis no Esquema do Sistema de Propriedades. Se você usar casos mistos para identificar propriedades que não são propriedades definidas pelo sistema, coloque o especificador de coluna entre aspas duplas. Os nomes de propriedade definidos pelo sistema incluem todas as propriedades que começam com "System" (por exemplo, System.Contact.FirstName) e não exigem aspas.

> [!Note]  
> Você também pode colocar nomes de propriedade definidos pelo sistema entre aspas duplas para maior leitura. Isso não afeta a compatibilidade.

 

Quando a consulta retorna um documento que não tem a coluna solicitada, o valor dessa coluna para o documento é **NULL.**

Você deve fornecer pelo menos um nome de coluna em uma instrução SELECT. Na consulta linguagem SQL (SQL), você tem permissão para usar o asterisco ( ) para especificar que todas as colunas em uma tabela devem \* ser retornadas. No entanto, nenhum conjunto definido e fixo de propriedades se aplica a todos os documentos. Por esse motivo, o SQL asterisco não é permitido no &lt; especificador de colunas &gt; da instrução SELECT.

## <a name="getting-the-top-n-results"></a>Obter os primeiros n resultados

Você pode especificar um número máximo de resultados a retornar usando a sintaxe TOP:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Tipos de dados de coluna de seleção

Às vezes, talvez seja necessário lançar dados de cadeia de caracteres extraídos de documentos como outro tipo de dados para que uma comparação apropriada possa ser feita. Para obter mais informações, consulte [Como lançar o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md).

## <a name="examples"></a>Exemplos

Os exemplos a seguir retornam o nome e a URL dos documentos correspondentes.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Como lançar o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



