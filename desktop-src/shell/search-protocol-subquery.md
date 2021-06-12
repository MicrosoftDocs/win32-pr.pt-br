---
description: Saiba mais sobre o argumento de subconsulta no Shell do Windows. Uma subconsulta é um arquivo de pesquisa salvo que você pode usar como um filtro para uma nova consulta.
title: Argumento de subconsulta (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010659"
---
# <a name="subquery-argument-the-windows-shell"></a>Argumento de subconsulta (o Shell do Windows)

Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta. Os resultados da subconsulta são usados como a origem para a nova consulta. Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: myDepartment. Search-MS, teamproject. Search-MS e corporatewide. Search-MS. O uso do `subquery` argumento permite que você limite as pesquisas de email a qualquer ou a todas essas pesquisas salvas.

## <a name="example"></a>Exemplo


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informações do argumento



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operacional mínimo | Windows Vista com Service Pack 1 (SP1) |



 

 

 



