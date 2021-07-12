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
ms.openlocfilehash: c27ce11d4d2e6ac36792f3ce47c053e9646d9903
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581594"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="ae1d5-104">argumento de subconsulta (o Shell de Windows)</span><span class="sxs-lookup"><span data-stu-id="ae1d5-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="ae1d5-105">Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="ae1d5-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="ae1d5-106">Os resultados da subconsulta são usados como a origem para a nova consulta.</span><span class="sxs-lookup"><span data-stu-id="ae1d5-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="ae1d5-107">Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: myDepartment. Search-MS, teamproject. Search-MS e corporatewide. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="ae1d5-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="ae1d5-108">O uso do `subquery` argumento permite que você limite as pesquisas de email a qualquer ou a todas essas pesquisas salvas.</span><span class="sxs-lookup"><span data-stu-id="ae1d5-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="ae1d5-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ae1d5-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="ae1d5-110">Informações do argumento</span><span class="sxs-lookup"><span data-stu-id="ae1d5-110">Argument Information</span></span>



|                              | <span data-ttu-id="ae1d5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ae1d5-111">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="ae1d5-112">**Sistema operacional mínimo**</span><span class="sxs-lookup"><span data-stu-id="ae1d5-112">**Minimum Operating System**</span></span> | <span data-ttu-id="ae1d5-113">Windows Vista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ae1d5-113">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



