---
description: Saiba mais sobre o argumento SUBQUERY no Shell Windows. Uma subconsistência é um arquivo de pesquisa salvo que você pode usar como um filtro para uma nova consulta.
title: Argumento SUBQUERY (o shell Windows)
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
# <a name="subquery-argument-the-windows-shell"></a>Argumento SUBQUERY (o shell Windows)

Uma subconsistência é um arquivo de pesquisa salvo ( .search-ms) que você pode usar como um \* filtro para uma nova consulta. Os resultados da subconsistência são usados como a origem da nova consulta. Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms. O uso `subquery` do argumento permite limitar as pesquisas de email a qualquer ou todas essas pesquisas salvas.

## <a name="example"></a>Exemplo


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informações de argumento



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operacional mínimo** | Windows Vista com Service Pack 1 (SP1) |



 

 

 



