---
description: Saiba mais sobre o argumento SUBQUERY Windows Search. Uma subconsistência é um arquivo de pesquisa salvo que você pode usar como um filtro para uma nova consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento SUBQUERY (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011029"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="fad4f-104">Argumento SUBQUERY (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="fad4f-104">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="fad4f-105">Uma subconsistência é um arquivo de pesquisa salvo ( .search-ms) que você pode usar como um \* filtro para uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="fad4f-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="fad4f-106">Os resultados da subconsistência são usados como a origem da nova consulta.</span><span class="sxs-lookup"><span data-stu-id="fad4f-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="fad4f-107">Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição por email: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="fad4f-107">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="fad4f-108">O uso `subquery` do argumento permite limitar as pesquisas de email a qualquer ou todas essas pesquisas salvas.</span><span class="sxs-lookup"><span data-stu-id="fad4f-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="fad4f-109">Este tópico é organizado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="fad4f-109">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="fad4f-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fad4f-110">Example</span></span>](#example)
-   [<span data-ttu-id="fad4f-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fad4f-111">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="fad4f-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fad4f-112">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="fad4f-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fad4f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fad4f-114">Ponto de Partida com Parameter-Value argumentos</span><span class="sxs-lookup"><span data-stu-id="fad4f-114">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="fad4f-115">Argumentos do identificador de localidade</span><span class="sxs-lookup"><span data-stu-id="fad4f-115">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="fad4f-116">Argumento DESaRELAÇÃO</span><span class="sxs-lookup"><span data-stu-id="fad4f-116">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="fad4f-117">Argumento SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fad4f-117">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="fad4f-118">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="fad4f-118">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



