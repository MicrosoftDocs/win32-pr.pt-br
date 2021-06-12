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
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="36339-104">Argumento de subconsulta (o Shell do Windows)</span><span class="sxs-lookup"><span data-stu-id="36339-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="36339-105">Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="36339-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="36339-106">Os resultados da subconsulta são usados como a origem para a nova consulta.</span><span class="sxs-lookup"><span data-stu-id="36339-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="36339-107">Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: myDepartment. Search-MS, teamproject. Search-MS e corporatewide. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="36339-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="36339-108">O uso do `subquery` argumento permite que você limite as pesquisas de email a qualquer ou a todas essas pesquisas salvas.</span><span class="sxs-lookup"><span data-stu-id="36339-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="36339-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="36339-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="36339-110">Informações do argumento</span><span class="sxs-lookup"><span data-stu-id="36339-110">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="36339-111">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="36339-111">Minimum Operating System</span></span> | <span data-ttu-id="36339-112">Windows Vista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36339-112">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



