---
description: Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento de subconsulta (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920766"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="e4f26-103">Argumento de subconsulta (pesquisa do Windows)</span><span class="sxs-lookup"><span data-stu-id="e4f26-103">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="e4f26-104">Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="e4f26-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="e4f26-105">Os resultados da subconsulta são usados como a origem para a nova consulta.</span><span class="sxs-lookup"><span data-stu-id="e4f26-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="e4f26-106">Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: myDepartment. Search-MS, teamproject. Search-MS e corporatewide. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="e4f26-106">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="e4f26-107">O uso do `subquery` argumento permite que você limite as pesquisas de email a qualquer ou a todas essas pesquisas salvas.</span><span class="sxs-lookup"><span data-stu-id="e4f26-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="e4f26-108">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e4f26-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e4f26-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e4f26-109">Example</span></span>](#example)
-   [<span data-ttu-id="e4f26-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4f26-110">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="e4f26-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e4f26-111">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="e4f26-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4f26-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f26-113">Introdução com argumentos de Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="e4f26-113">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="e4f26-114">Argumentos do identificador de localidade</span><span class="sxs-lookup"><span data-stu-id="e4f26-114">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="e4f26-115">Argumento de trilha</span><span class="sxs-lookup"><span data-stu-id="e4f26-115">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="e4f26-116">Argumento de sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4f26-116">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="e4f26-117">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="e4f26-117">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



