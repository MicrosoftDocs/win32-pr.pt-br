---
description: saiba mais sobre o argumento de subconsulta no Shell de Windows. Uma subconsulta é um arquivo de pesquisa salvo que você pode usar como um filtro para uma nova consulta.
title: argumento de subconsulta (o Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fc478c9aff21b20566ffcd8d10580abaf8affa8eb36c39adb8c3c75486ca999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452862"
---
# <a name="subquery-argument-the-windows-shell"></a>argumento de subconsulta (o Shell de Windows)

Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta. Os resultados da subconsulta são usados como a origem para a nova consulta. Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: myDepartment. Search-MS, teamproject. Search-MS e corporatewide. Search-MS. O uso do `subquery` argumento permite que você limite as pesquisas de email a qualquer ou a todas essas pesquisas salvas.

## <a name="example"></a>Exemplo


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informações do argumento



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operacional mínimo** | Windows Vista com Service Pack 1 (SP1) |



 

 

 



