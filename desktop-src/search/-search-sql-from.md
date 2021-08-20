---
description: Após a instrução SELECT, você usa a cláusula FROM para especificar onde pesquisar documentos correspondentes.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Cláusula FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6231244df2a2ec8753950ccb1a7d046c3510eff6582215d0aa3d71ebc127e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863392"
---
# <a name="from-clause"></a>Cláusula FROM

Após a instrução SELECT, você usa a cláusula FROM para especificar onde pesquisar documentos correspondentes. A seguir está a sintaxe da cláusula FROM para uma consulta local:


```
FROM [<ComputerName>.]SystemIndex
```



atualmente, Windows pesquisa dá suporte apenas a um catálogo, SystemIndex. Para consultar o catálogo local de um computador remoto, inclua o nome do computador antes do catálogo e um caminho UNC (Convenção de nomenclatura universal) no computador remoto na cláusula SCOPE ou DIRECTORY.

Especifique um escopo como uma restrição na cláusula WHERE, conforme descrito no tópico [predicados de escopo e diretório](-search-sql-folderdepth.md) .

## <a name="examples"></a>Exemplos


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



No segundo dos exemplos anteriores, a consulta tem como alvo um computador remoto chamado "zarascomputer". Observe que esse nome de computador aparece nas cláusulas de e de escopo. No terceiro exemplo, a consulta tem como alvo um nome de compartilhamento "Users" em um servidor chamado "Server" (no qual o caminho UNC seria \\ \\ usuários do servidor \\ ).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[visão geral da sintaxe de SQL de pesquisa](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Instrução SELECT](-search-sql-select.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

[Predicados de escopo e diretório](-search-sql-folderdepth.md)
</dt> </dl>

 

 



