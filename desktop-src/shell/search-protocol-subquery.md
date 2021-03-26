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
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="4795a-103">Argumento de subconsulta (o Shell do Windows)</span><span class="sxs-lookup"><span data-stu-id="4795a-103">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="4795a-104">Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="4795a-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="4795a-105">Os resultados da subconsulta são usados como a origem para a nova consulta.</span><span class="sxs-lookup"><span data-stu-id="4795a-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="4795a-106">Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: myDepartment. Search-MS, teamproject. Search-MS e corporatewide. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="4795a-106">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="4795a-107">O uso do `subquery` argumento permite que você limite as pesquisas de email a qualquer ou a todas essas pesquisas salvas.</span><span class="sxs-lookup"><span data-stu-id="4795a-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="4795a-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4795a-108">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="4795a-109">Informações do argumento</span><span class="sxs-lookup"><span data-stu-id="4795a-109">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="4795a-110">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="4795a-110">Minimum Operating System</span></span> | <span data-ttu-id="4795a-111">Windows Vista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="4795a-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



