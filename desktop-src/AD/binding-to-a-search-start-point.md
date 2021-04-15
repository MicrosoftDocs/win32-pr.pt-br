---
title: Associação ao ponto de início da pesquisa
description: O ponto de partida para uma pesquisa é um contêiner que contém diretamente ou indiretamente os objetos pesquisados.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, associação a um ponto de partida de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453477"
---
# <a name="binding-to-the-search-start-point"></a><span data-ttu-id="74d45-104">Associação ao ponto de início da pesquisa</span><span class="sxs-lookup"><span data-stu-id="74d45-104">Binding to the Search Start Point</span></span>

<span data-ttu-id="74d45-105">O ponto de partida para uma pesquisa é um contêiner que contém diretamente ou indiretamente os objetos pesquisados.</span><span class="sxs-lookup"><span data-stu-id="74d45-105">The start point for a search is a container that directly or indirectly contains the objects searched for.</span></span> <span data-ttu-id="74d45-106">A pesquisa não será executada em contêineres acima do ponto de início da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="74d45-106">The search will not be performed in containers above the search start point.</span></span> <span data-ttu-id="74d45-107">Por exemplo, considere a seguinte estrutura de diretório hipotética:</span><span class="sxs-lookup"><span data-stu-id="74d45-107">For example, take the following hypothetical directory structure:</span></span>

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

<span data-ttu-id="74d45-108">Se uma pesquisa for executada para todos os objetos e o ponto de partida de pesquisa for "contêiner 2", somente o "objeto 3" e o "objeto 4" serão recuperados.</span><span class="sxs-lookup"><span data-stu-id="74d45-108">If a search is performed for all objects and the search start point is "Container 2", only "Object 3" and "Object 4" would be retrieved.</span></span> <span data-ttu-id="74d45-109">Se a mesma pesquisa foi executada com o ponto de início de pesquisa em "contêiner 1", "objeto 1" e "objeto 2" seriam recuperados.</span><span class="sxs-lookup"><span data-stu-id="74d45-109">If the same search was performed with the search start point at "Container 1", "Object 1" and "Object 2" would be retrieved.</span></span>

<span data-ttu-id="74d45-110">Para associar ao ponto de início da pesquisa, associe ao ADsPath do contêiner que será o ponto de partida de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="74d45-110">To bind to the search start point, bind to the ADsPath of the container that will be the search start point.</span></span>

 

 




