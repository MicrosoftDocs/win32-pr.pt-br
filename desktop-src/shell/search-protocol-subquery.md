---
description: Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta.
title: Argumento de subconsulta (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 43e4a5b904d5e769eb43acad05aa5d8ce37ebde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989072"
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



 

 

 



